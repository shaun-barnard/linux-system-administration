## [Filesystem](https://github.com/shaun-barnard/linux-system-administration/blob/main/arch-linux/filesystem.md)

In Arch Linux, a filesystem is a method used to control how data is stored, organized, managed,and retrieved on storage devices. The filesystem also provides a way to identify, access, and modify the stored information. Arch Linux supports various filesystem types, each with its own advantages, disadvantages, and unique characteristics.

Arch Linux follows the **Filesystem Hierarchy Standard (FHS)** for operating systems using the **systemd** service manager. This standard defines the directory structure and organization for the operating system, ensuring consistency and compatibility across different systems.

The filesystem in Arch Linux is typically created on a **partition**, inside **logical containers** such as **LVM**, **RAID**, and **dm-crypt**, or on a regular file. After creating a new filesystem, it can be mounted to make it accessible for use.