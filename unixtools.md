# Unix Tools

## Bash Commands
```bash
uname -a                # Get the Kernel Version
lsb_release -a          # Release or Distibution info
cat /etc/SuSE-release   # Suse Linux Version Check
cat /etc/debian_version # Debian Version check
```
## Basic Commands to know the Server status
```bash 
uptime                  # it will shows how long the system has been running
hostname                # System Host Name
hostname -i             # To Display to the ip address of the Host, Linux based distribution
man hier                # File system hierarchy Description
last reboot             # to know the system reboot history
```
## Hardware informations
### Kernel Detected HW
``` bash
dmesg                   # Detect Hardware and Boot messages
lsdev                   # Info about the installed Hardware like PCI Card
dd if=/dev/mem bs=1k skip=768 count=256 2>/dev/null | strings -n 8  # Read BIOS
```
### Linux
```bash 
cat /proc/cpuinfo                # CPU Model 
cat /proc/meminfo                # Hardware Memory
grep MemTotal /proc/meminfo      # Physical Memory
watch -n1 'cat /proc/interrupts' # watch changecable interrupts 
free -m                          # To know the used & free memory ( -m for MB)
cat /proc/devices                # Configured devices
lspci -tv                        # PCI Device info
lsusb -tv                        # USB Device info
lshal                            # List all devices with properties
dmidecode                        # DMI/SMBIOS: hw info from the BIOS
```
### Free BSD
``` bash
sysctl hw.model                 # CPU Model
sysctl hw                       # More information about hardware
sysctl hw.ncpu                  # No. of active CPU's Installed
sysctl vm                       # Memory Usage
sysctl hw.realmem               # Hardware Memory (Physical)
sysctl -a | grep mem            # Kernel memory settings and info
sysctl dev                      # Configured devices
pciconf -l -cv                  # PCI Device info
usbdevs -v                      # USB Device info
atacontrol list                 # ATA Device info
camcontrol devlist -v           # SCSI Device info 
```
### Load, Statistics and Messages
Folowing Commands are useful to find out what is going on the system realtime. 
``` bash
top                             # display & update the top CPU processes             
mpstat 1                        # display processors related statistics
vmstat 2                        # virtual memory statistics
iostat 2                        # I/O statistics - 2sec intervals
systat -vmstat 1                # system statistics - 1sec intervals
systat -tcp 1                   # tcp connections (try also -ip)
systat -netstat 1               # active network connections - BSD
systat -ifstat 1                # network traffic through active interfaces - BSD
systat -iostat 1                # CPU and Disk throughput - BSD
ipcs -a                         # info on system V interprocess 
tail -n 500 /var/log/messages   # Last 500 Kernel/syslog messages
tail /var/log/warn              # System Warnings messages see syslog.conf
```
