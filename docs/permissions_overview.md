# 🔐 Permissions Overview

Linux file permissions determine who can read, write, or execute a file or directory. Understanding these permissions is crucial for managing system security.

## 📜 Permission Structure
A typical Linux file permission string looks like this:
```
-rwxr-xr-- 1 user group 1234 Feb 21 12:00 file.txt
```
Breaking it down:
- `-` (first character): File type (`d` for directory, `-` for regular file)
- `rwx` (positions 2-4): Owner (User) permissions (Read, Write, Execute)
- `r-x` (positions 5-7): Group permissions (Read, Execute)
- `r--` (positions 8-10): Others' permissions (Read-only)

## 🔍 Checking Permissions
To view file permissions, use:
```sh
ls -la
```
This command lists files with detailed information, including permissions.

## 🏗️ Modifying Permissions
To change file permissions, use:
```sh
chmod [permissions] [file]
```
Example:
```sh
chmod u+w file.txt  # Add write permission for the owner
chmod g-r file.txt  # Remove read permission for the group
chmod o+x file.txt  # Add execute permission for others
```

For more details, refer to `chmod` documentation using:
```sh
man chmod
