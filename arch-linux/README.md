## [Filesystem](https://github.com/shaun-barnard/linux-system-administration/blob/main/arch-linux/filesystem.md)

In Arch Linux, a **filesystem** is a method used to control how data is stored, organized, managed,and retrieved on storage devices. The filesystem also provides a way to **identify**, **access**, and **modify** the stored **information**. Arch Linux supports various filesystem types, each with its own advantages, disadvantages, and unique characteristics.

| Filesystem | Description |
| --- | --- |
| Btrfs | Btrfs is a Linux native filesystem that offers features such as subvolumes, snapshots, and integrated RAID support. It is considered stable and is known for its flexibility and reliability. |
| Ext4 | Ext4 is a widely used and well-established filesystem in the Linux community. It is known for its stability, performance, and compatibility with older Ext2 and Ext3 filesystems. |
| F2FS | F2FS (Flash-Friendly File System) is designed for NAND-based flash storage devices. It is optimized for use in solid-state drives (SSDs) and offers features tailored for flash memory. |
| ZFS | While not a native Linux filesystem, ZFS is known for its advanced features such as data integrity, snapshots, and built-in RAID support. It requires a significant amount of ECC RAM to run effectively. |

Arch Linux follows the **Filesystem Hierarchy Standard (FHS)** for operating systems using the **systemd** service manager. This standard defines the directory structure and organization for the operating system, ensuring consistency and compatibility across different systems.

The filesystem in Arch Linux is typically created on a **partition**, inside **logical containers** such as **LVM**, **RAID**, and **dm-crypt**, or on a regular file. After creating a new filesystem, it can be mounted to make it accessible for use.