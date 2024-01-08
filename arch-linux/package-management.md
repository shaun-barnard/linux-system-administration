<p align="center">
    <a href="#arch-linux-filesystem" style="font-size: 24px;">Overview</a> |
     <a href="#types" style="font-size: 24px;">AUR</a> |
    <a href="#arch-linux-filesystem-structure" style="font-size: 24px;">Pacman</a> |
    <a href="#commands" style="font-size: 24px;">Yay</a>
</p>

### Arch Linux Package Management

Package management in Linux refers to the process of installing, updating, configuring, and removing software packages on a Linux system. It involves the use of package management utilities to handle these tasks efficiently. In the context of Arch Linux, the primary package management utilities are **pacman** and AUR helpers such as **yay**.

#### Arch User Repository (AUR)

The Arch User Repository (AUR) is a **community-driven** repository for Arch Linux users. It contains package build scripts (PKGBUILDs) that allow users to create custom-built packages, which are **NOT available in the official repositories**. These **PKGBUILDs** automate the process of retrieving the source code, compiling it, and packaging it into a single, installable package using the **makepkg** script.

#### Pacman

In Arch Linux, **pacman** is the default **package manager** for Arch Linux and its derivatives. It is a simple and fast package manager that allows for continuously upgrading the entire system with one command. Pacman combines a simple **binary package format** with an easy-to-use build system, making it possible to easily manage packages, whether they are from the **official repositories** or the user's own builds. It keeps the system up-to-date by **synchronizing package lists** with the master server, and it also handles **dependencies** and can download packages from a remote server.

| Command | Description | Example |
| ------- | ----------- | ------- |
| `pacman {-S --sync} [options]` | Synchronize the package databases and install or upgrade packages | `pacman -S package_name` |

**Options:**

| Option | Description | Example |
| ------ | ----------- | ------- |
| `-b, --dbpath <path>` | Set an alternate database location | `pacman -S --dbpath /path/to/db package_name` |
| `-c, --clean` | Remove old packages from the cache directory | `pacman -Sc` |
| `-d, --nodeps` | Skip dependency version checks | `pacman -S package_name --nodeps` |
| `-g, --groups` | View all members of a package group | `pacman -Sg group_name` |
| `-i, --info` | View package information | `pacman -Si package_name` |
| `-l, --list <repo>` | View a list of packages in a repository | `pacman -Sl core` |
| `-p, --print` | Print the targets instead of performing the operation | `pacman -Sp package_name` |
| `-q, --quiet` | Show less information for query and search | `pacman -Qq package_name` |
| `-r, --root <path>` | Set an alternate installation root | `pacman -S package_name --root /mnt` |
| `-s, --search <regex>` | Search remote repositories for matching strings | `pacman -Ss keyword` |
| `-u, --sysupgrade` | Upgrade installed packages | `pacman -Syu` |
| `-v, --verbose` | Be verbose | `pacman -Sv package_name` |
| `-w, --downloadonly` | Download packages but do not install/upgrade anything | `pacman -Sw package_name` |
| `-y, --refresh` | Download fresh package databases from the server | `pacman -Sy` |

#### Yay (Yet Another Yaourt)

AUR helpers, such as **yay**, are used to simplify the process of interacting with the AUR. They automate the retrieval and building of packages from the AUR, as well as **handling dependencies** and updates. Users can **search**, **install**, and **manage** AUR packages using these helpers, which streamline the process of working with the AUR.

*Note: All packages available in Pacman are also available in Yay, as Yay simply wraps Pacman and provides additional AUR functionality*

| Command | Description | Example |
| ------- | ----------- | ------- |
| `yay` | Perform system upgrade (`yay -Syu` if no operation is specified) | `yay` |
| `yay <operation> [... ]` | Perform a specific operation | `yay -S package1 package2` |
| `yay <package(s)>` | Perform an operation on the specified package(s) | `yay -S package1` |

**Operations:**

| Command | Description | Example |
| ------- | ----------- | ------- |
| `yay {-h --help}` | Display help information | `yay -h` |
| `yay {-V --version}` | Display version of yay | `yay -V` |
| `yay {-D --database} <options> <package(s)>` | Query the package database | `yay -D <package>` |
| `yay {-F --files} [options] [package(s)]` | Query the files database | `yay -F <file>` |
| `yay {-Q --query} [options] [package(s)]` | Query the package database | `yay -Q <package>` |
| `yay {-R --remove} [options] <package(s)>` | Remove a package | `yay -R <package>` |
| `yay {-S --sync} [options] [package(s)]` | Install or upgrade a package | `yay -S <package>` |
| `yay {-T --deptest} [options] [package(s)]` | Check dependencies | `yay -T <package>` |
| `yay {-U --upgrade} [options] <file(s)>` | Upgrade or add a package to the system | `yay -U <package>` |

**New Operations:**

| Command | Description | Example |
| ------- | ----------- | ------- |
| `yay {-B --build} [options] [dir]` | Build a package from a build directory | `yay -B /path/to/PKGBUILD` |
| `yay {-G --getpkgbuild} [options] [package(s)]` | Download PKGBUILD from ABS or AUR | `yay -G package` |
| `yay {-P --show} [options]` | Show specific options | `yay -P` |
| `yay {-W --web} [options] [package(s)]` | Open the package URL in a web browser | `yay -W package` |
| `yay {-Y --yay} [options] [package(s)]` | Perform an operation using yay | `yay -Y package` |
