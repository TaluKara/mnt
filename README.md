# mnt

**A Bash Script for Managing Disk Partitions**

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Key Controls](#key-controls)
- [Requirements](#requirements)
- [Contributing](#contributing)
- [License](#license)

## Introduction

`mnt` is a user-friendly Bash script designed to simplify the management of disk partitions on Linux systems. Whether you need to mount or unmount partitions, `mnt` provides an intuitive interface to handle these tasks efficiently without the need for complex command-line operations.

## Features

- **Easy Navigation:** Browse through available partitions using arrow keys.
- **Mount & Unmount:** Quickly mount or unmount selected partitions with simple key presses.
- **Automatic Mount Point Management:** Automatically creates and removes mount points as needed.
- **Supports Multiple Filesystems:** Optimized options for various filesystem types, including `vfat`.
- **Dynamic Updates:** Reflects real-time changes in partition statuses after mount/unmount operations.

## Installation

### Step 1: Download the Script

Clone this repository or download the `mnt` script file.

```bash
git clone https://github.com/TaluKara/mnt.git
cd mnt
```

### Step 2: Copy the Script

You can place the script in `/usr/local/bin` for easy access:

```bash
sudo cp mnt /usr/local/bin/
sudo chmod +x /usr/local/bin/mnt
```

By placing the script in `/usr/local/bin`, you can run it from anywhere in the terminal without specifying the path.

## Usage

Simply run the `mnt` command in your terminal:

```bash
mnt
```

Ensure you have the necessary sudo privileges, as the script requires them to manage mount points.

## Key Controls

- **Up Arrow (`↑`):** Navigate to the previous partition.
- **Down Arrow (`↓`):** Navigate to the next partition.
- **`e` or `E`:** Mount the selected partition.
- **`r` or `R`:** Unmount the selected partition.
- **`d` or `D`:** Copies the mountpoint in to the system clipboard.
- **`q` or `Q`:** Quit the script.


### Example Interface

```
------------------------------------------------------------------------------------------
NAME       LABEL                SIZE       TYPE       MOUNTPOINT         
------------------------------------------------------------------------------------------
  sda1      System               100G      part      /mnt/system        
> sda2      Data                 500G      part      -
  sdb1      Backup               250G      part      /mnt/backup        
------------------------------------------------------------------------------------------
Press 'e' to mount, 'r' to unmount, 'd' to copy, 'q' to quit.
```

In this example, the currently selected partition is highlighted with a `>` symbol. Use the arrow keys to change the selection and press the corresponding key to perform actions.

## Requirements

- **Operating System:** Linux
- **Shell:** Bash
- **Permissions:** Sudo privileges are required to execute mount and unmount operations.
- **Dependencies:** Utilizes standard Linux utilities like `lsblk`, `blkid`, `mount`, `umount` and `xclip` or `xsel` or `wl-copy`.

## Contributing

Contributions are welcome! If you have suggestions, bug reports, or want to contribute code, please open an issue or submit a pull request on [GitHub](https://github.com/TaluKara/mnt).

## License

This project is licensed under the [GPL License](LICENSE).

---

**Disclaimer:** Use this script at your own risk. Ensure you understand the implications of mounting and unmounting partitions to prevent data loss.
