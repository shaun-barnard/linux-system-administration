[![Discord](https://img.shields.io/discord/1193946747878260767?color=blue&label=Discord&logo=discord&logoColor=white)](https://discord.gg/KmAkuNyr)

#### Linux System Administration

### [Arch Linux](https://archlinux.org/)

### Package Management
- **Pacman Commands:**
  - `pacman -Syu`: Synchronize the package databases and update the system.
  - `pacman -S package_name`: Install a package.
  - `pacman -R package_name`: Remove a package.
- **Yay Commands:**
  - `yay -Syu`: Synchronize the AUR package databases and update the system.
  - `yay -S package_name`: Install an AUR package.
  - `yay -R package_name`: Remove an AUR package.
- **Managing Repositories:**
  - Edit /etc/pacman.conf to manage official repositories.
  - Edit /etc/pacman.d/mirrorlist to manage mirrors.
- **Querying Package Information:**
  - `pacman -Q package_name`: Query installed package information.
  - `pacman -Ss keyword`: Search for a package in the repositories.

### System Configuration
- **User and Group Management:**
  - `useradd`: Add a user.
  - `usermod`: Modify a user.
  - `userdel`: Delete a user.
  - `groupadd`: Add a group.
  - `groupmod`: Modify a group.
  - `groupdel`: Delete a group.
- **Network Configuration:**
  - `ip addr show`: Show network interfaces and IP addresses.
  - `ip link set dev interface_name up/down`: Enable/disable a network interface.
- **Firewall Setup:**
  - Use iptables or nftables for firewall configuration.

### File System and Storage
- **File System Management:**
  - `lsblk`: List block devices.
  - `mkfs`: Make a file system.
  - `mount` / `umount`: Mount and unmount file systems.
- **Disk Partitioning:**
  - Use fdisk, parted, or gdisk for disk partitioning.

### Service Management
- **Systemd Commands:**
  - `systemctl start service_name`: Start a service.
  - `systemctl stop service_name`: Stop a service.
  - `systemctl enable service_name`: Enable a service to start on boot.

### Security
- **User Privilege Management:**
  - Use sudo for granting administrative privileges.
- **System Hardening:**
  - Follow security best practices, such as limiting user privileges and keeping the system updated.

### Networking
- **Network Configuration:**
  - Use ip and netctl for network configuration.
- **Troubleshooting:**
  - Use ping, traceroute, and ip for network troubleshooting.

### General Recommendations
- The Arch Linux community provides general recommendations and best practices for system administration, maintenance, and troubleshooting. These resources are valuable for improving the overall Arch Linux system.

