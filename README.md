# Linux Scripts

This repository contains a collection of useful shell scripts for automating various tasks on Linux systems.

## Scripts

- **`incremental_backup.sh`**: Performs an incremental backup of specified directories.
- **`differential_backup.sh`**: Performs a differential backup of specified directories.
- **`update_system.sh`**: Updates and upgrades system packages.
- **`check_memory_usage.sh`**: Displays current memory usage statistics.

## Usage

Clone the repository:
```bash
git clone https://github.com/yourusername/linux-scripts.git
```
##Navigate to the script directory:
```bash
cd linux-scripts
```
##Make the scripts executable:
```bash
chmod +x *.sh
```
##Run a script:
```bash
./script_name.sh
```
###Script Details
```bash
incremental_backup.sh
```
This script performs an incremental backup, which only copies files that have changed since the last backup. It uses rsync with the --link-dest option to create hard links for unchanged files, saving space.
```bash
differential_backup.sh
```
This script performs a differential backup, which copies all files that have changed since the last full backup. It uses rsync with the --compare-dest option to compare files with the latest full backup.
```bash
update_system.sh
```
This script updates the package lists and upgrades all installed packages on the system. It's designed for Debian-based systems using apt.
```bash
check_memory_usage.sh
```
This script displays current memory usage statistics, including total memory, used memory, and usage percentage.

##Customization
Before using the backup scripts, make sure to set the SOURCE_DIR and BACKUP_DIR variables in both incremental_backup.sh and differential_backup.sh to match your desired source and destination directories.

##Contributing
Contributions are welcome! If you have a useful script to add or improvements to existing ones, please feel free to submit a pull request, I would love to collaborate.

##License
This project is licensed under the MIT License - see the LICENSE file for details.
