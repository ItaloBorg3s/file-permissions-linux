# 📌 File Permissions in Linux

## 📟 Project Description

In this project, I explored and modified file and directory permissions in a Linux system to ensure better security. The goal was to check and adjust the permissions of the files and directories within the `/home/researcher2/projects` directory, following security best practices.

---

## 🔍 Check File and Directory Details

First, I navigated to the `projects` directory using the `cd` command and listed the content using `ls -la` to check the permissions and details of the files and directories. This command shows information about permissions, owner, group, and other file details.

- **Command used:** `ls -la`
- **Explanation:** `ls` lists the files in the directory and `-la` provides detailed information, including hidden files.

<p align="center">
  <img src="https://github.com/user-attachments/assets/c6d9cb6f-6f6b-4bda-9880-734136bafe59" width="500" style="margin-right: 500px;"/>
  <img src="https://github.com/user-attachments/assets/a3f4af1a-8f04-4054-9466-3cc65dee0207" width="500" style="margin-left: 20px;"/>
</p>

---

## 💾 Describe the Permissions String

The permissions string in Linux consists of 10 characters that represent the permissions for files and directories:

1. The first character indicates the file type (`d` for directory, `-` for regular file).
2. The next three characters represent the owner's (User) permissions.
3. The next three represent the group's (Group) permissions.
4. The last three represent the permissions for "Other."

Example output:
```
-rw-r--r-- 1 researcher2 researcher2 1234 Feb 21 12:00 project_k.txt
```
In this case:
- The file `project_k.txt` is a regular file.
- The owner has read and write permissions (`rw-`).
- The group and "Other" have read-only permissions (`r--`).

---

## 🔒 Change File Permissions

I checked and changed the permissions of the `project_k.txt` file to remove the write permission for "Other" using the command:

- **Command used:** `chmod o-w project_k.txt`
- **Explanation:** This command removes the write permission for "Other," ensuring that only the owner and group can modify the file.

![print 3](https://github.com/user-attachments/assets/7e5b5439-c85d-45a2-a25f-a9afc6d33f0a)

---

## 🔓 Change File Permissions on a Hidden File

The hidden file `.project_x.txt` should not allow write access for any user. To achieve this, I removed the write permissions for both the user and the group:

- **Command used:** `chmod u-w,g-w,g+r .project_x.txt`
- **Explanation:** This command removes the write permission for the user (`u-w`) and the group (`g-w`), leaving read-only access for both.

An alternative simplified command to achieve the same result would be:
- **Alternative command:** `chmod u=r,g=r .project_x.txt`

![print 4](https://github.com/user-attachments/assets/1ce551c2-67a8-4c73-a8bd-ca99f0176994)

---

## 🛡️ Change Directory Permissions

The `drafts` directory should only be accessible by the owner, so I removed the group permissions to access the directory.

- **Command used:** `chmod g-x drafts`
- **Explanation:** This command removes the execute permission for the group on the `drafts` directory, preventing group users from accessing its content.

![print 6](https://github.com/user-attachments/assets/6352fbc3-b776-4ad0-a90d-85cf06a514da)

---

## 📊 Summary

In this project, I examined the permissions of various files and directories within the `projects` directory, adjusting them as necessary to improve system security. Actions included removing inappropriate write and read permissions and restricting access to critical directories to the owner only.

---
