# 🛠️ chmod Examples

The `chmod` command in Linux is used to change file and directory permissions. Below are some common use cases.

## 📌 Changing File Permissions

### 1️⃣ Grant execute permission to the owner:
```sh
chmod u+x script.sh
```
- `u`: User (owner)
- `+x`: Adds execute permission

### 2️⃣ Remove write permission from the group:
```sh
chmod g-w document.txt
```
- `g`: Group
- `-w`: Removes write permission

### 3️⃣ Set exact permissions using numeric mode:
```sh
chmod 644 file.txt
```
- `6`: Owner (read + write)
- `4`: Group (read only)
- `4`: Others (read only)

## 📂 Changing Directory Permissions

### 4️⃣ Grant execute permission to everyone for a directory:
```sh
chmod a+x my_directory
```
- `a`: All users (Owner, Group, Others)
- `+x`: Adds execute permission

### 5️⃣ Make a directory accessible only to the owner:
```sh
chmod 700 private_folder
```
- `7`: Owner (read + write + execute)
- `0`: No permissions for Group and Others

For more details, use:
```sh
man chmod
