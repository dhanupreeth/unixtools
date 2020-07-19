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

