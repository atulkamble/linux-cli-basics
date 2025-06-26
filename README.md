# 📖 Linux Files, Folders, and Command Line Essentials

## 📌 Command Line Syntax

In Linux, the **Command Line Interface (CLI)** is a text-based interface for interacting with the system. Commands generally follow this syntax:

```bash
command [options] [arguments]
```

* **command** → the program you want to run
* **options** → optional flags to modify the command behavior (usually start with `-` or `--`)
* **arguments** → the target files, directories, or other data

**Example:**

```bash
ls -l /home
```

* `ls` → command to list directory contents
* `-l` → option for long listing format
* `/home` → argument (target directory)

---

## 📂 Linux File System Hierarchy (FHS)

The Linux file system follows a **tree-like hierarchy**, starting at the root `/`. Important directories:

| Directory         | Purpose                                     |
| :---------------- | :------------------------------------------ |
| `/`               | Root of the file system                     |
| `/bin`            | Essential user binaries (e.g. `ls`, `cp`)   |
| `/sbin`           | System binaries (admin commands)            |
| `/etc`            | System configuration files                  |
| `/home`           | User home directories                       |
| `/var`            | Variable files (logs, spools)               |
| `/tmp`            | Temporary files                             |
| `/usr`            | User-installed software and libraries       |
| `/opt`            | Optional, third-party software              |
| `/root`           | Home directory of root user                 |
| `/dev`            | Device files                                |
| `/proc`           | Kernel and process information (virtual FS) |
| `/mnt` & `/media` | Mount points for external devices           |

---

## 📍 Directory Navigation Commands

| Command        | Description                  |
| :------------- | :--------------------------- |
| `pwd`          | Print current directory      |
| `ls`           | List contents of a directory |
| `cd <dir>`     | Change directory             |
| `cd ..`        | Move up one directory        |
| `cd ~` or `cd` | Go to the home directory     |
| `cd -`         | Switch to previous directory |

**Examples:**

```bash
cd /var/log
pwd
ls -l
```

---

## 📦 Managing Files and Directories

### 📄 File Management

| Command               | Description                        |
| :-------------------- | :--------------------------------- |
| `touch file`          | Create an empty file               |
| `cp source dest`      | Copy files                         |
| `mv source dest`      | Move or rename files               |
| `rm file`             | Delete a file                      |
| `cat file`            | View file contents                 |
| `nano file`           | Edit file using `nano` editor      |
| `echo "text" > file`  | Write text into a file (overwrite) |
| `echo "text" >> file` | Append text to a file              |

### 📂 Directory Management

| Command                 | Description                         |
| :---------------------- | :---------------------------------- |
| `mkdir dir`             | Create a new directory              |
| `mkdir -p /path/to/dir` | Create parent directories as needed |
| `rmdir dir`             | Remove empty directory              |
| `rm -r dir`             | Remove directory and its contents   |
| `cp -r src dest`        | Copy a directory recursively        |
| `mv dir newname`        | Rename or move a directory          |

**Examples:**

```bash
mkdir /home/atul/new_project
cd /home/atul/new_project
touch readme.txt
echo "Project Initialized" > readme.txt
cat readme.txt
rm readme.txt
```

---

## ✅ Bonus: Common File Handling Tips

* Use `ls -a` to show hidden files (those starting with `.`)
* Use `rm -i` for interactive deletion (asks before removing)
* Use `cp -v` for verbose copy (shows progress)
* Combine commands with `&&` or `;`

**Example:**

```bash
mkdir test && cd test && touch file1 file2
```

---

## 📚 Summary

The Linux CLI is powerful for managing the file system efficiently. Mastering basic file and directory operations is foundational for any Linux administrator, DevOps engineer, or cloud architect.

---
