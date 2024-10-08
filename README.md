# mnt - Mount and Unmount Drives

`mnt` is a simple Bash script that allows you to easily mount and unmount drives on your Linux system. It detects available drives, prompts for user input, and handles the mounting/unmounting process.

## Features

- Lists available drives.
- Supports mounting and unmounting specified devices.
- Automatically creates a mount point based on the device label.
- Configurable options for FAT32 file systems.

## Installation

1. **Download the Script:**
   Clone this repository or download the `mnt` script file.

   ```bash
   git clone https://github.com/TaluKara/mnt.git
   cd mnt
   ```

2. **Copy the Script:**
   You can place the script in `/usr/local/bin` for easy access:

   ```bash
   sudo cp mnt /usr/local/bin/
   sudo chmod +x /usr/local/bin/mnt
   ```

   By placing the script in `/usr/local/bin`, you can run it from anywhere in the terminal without specifying the path.

## Usage

To run the script, simply use the following command:

```bash
mnt
```

You will be prompted to enter an action (either `add` to mount a drive or `remove` to unmount it) and the device name (e.g., `sdb1`).

### Example

1. **Mounting a Drive:**
   ```bash
   $ sudo mnt
   Available drives:
   ...
   Enter action (add/remove): add
   Enter device name (e.g., sdb1): sdb1
   ```

2. **Unmounting a Drive:**
   ```bash
   $ sudo mnt
   Available drives:
   ...
   Enter action (add/remove): remove
   Enter device name (e.g., sdb1): sdb1
   ```

## Notes

- Ensure you have the necessary permissions to mount and unmount drives (you may need to run the script with `sudo`).
- The script automatically removes empty mount points when a drive is unmounted.
- Customize the mount options as needed in the script.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
