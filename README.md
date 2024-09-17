# Folder Backup Script

This script is designed to automatically copy a folder from a source directory to a destination directory every day at a specified time. The copied folder is named with the current date.

## Features

- Automatically copies a folder from the source directory to the destination directory.
- Names the copied folder with the current date.
- Schedules the copy operation to run daily at a specified time.

## Requirements

- Python 3.x
- `os` module (standard library)
- `shutil` module (standard library)
- `datetime` module (standard library)
- `schedule` module (`pip install schedule`)

## Usage

1. **Clone the repository** (if applicable) or download the script file.

2. **Install the required module**:
   ```bash
   pip install schedule
   ```

3. **Edit the script**:
   - Replace `"Enter your source folder path"` with the path to the source directory.
   - Replace `"Enter your destination folder path"` with the path to the destination directory.

4. **Run the script**:
   ```bash
   python script_name.py
   ```

## How It Works

1. The script defines the source and destination directories.
2. The `copy_folder_to_directory` function copies the folder from the source directory to a new folder in the destination directory named with the current date.
3. The script schedules the `copy_folder_to_directory` function to run every day at 18:55.
4. The script enters an infinite loop, checking every minute if the scheduled task should run.

## Notes

- Ensure that the destination directory does not already contain a folder with the same name as the current date, as this will cause a `FileExistsError`.
- Adjust the scheduled time as needed by modifying the `schedule.every().day.at("18:55")` line.
