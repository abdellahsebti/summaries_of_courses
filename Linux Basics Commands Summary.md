
## **File System Navigation**
- **`pwd`** : Print Working Directory — shows the full path of your current location in the file system.  
  ```bash
  pwd
  # Output: /home/user/Documents
  ```

- **`cd`** : Change Directory — moves you from your current directory to another.  
  ```bash
  cd /etc
  ```

- **`ls`** : List — shows files and directories in the current directory (or specified path).  
  ```bash
  ls -l
  ```

- **`tree`** : Displays directory structure in a tree-like format. *(Might require installation)*  
  ```bash
  tree /var
  ```

---

## **File and Directory Management**
- **`touch`** : Create an empty file or update file timestamp.  
  ```bash
  touch notes.txt
  ```

- **`mkdir`** : Make Directory — creates a new folder.  
  ```bash
  mkdir projects
  ```

- **`rm`** : Remove — deletes files or directories (`-r` for recursive).  
  ```bash
  rm file.txt
  rm -r old_folder
  ```

- **`cp`** : Copy — duplicates files or directories (`-r` for recursive).  
  ```bash
  cp file.txt backup.txt
  cp -r folder1 folder2
  ```

- **`mv`** : Move or rename files and directories.  
  ```bash
  mv file.txt /home/user/Documents
  mv oldname.txt newname.txt
  ```

---

## **Viewing & Editing Files**
- **`cat`** : Concatenate — shows file content.  
  ```bash
  cat notes.txt
  ```

- **`less`** : View large files page by page.  
  ```bash
  less bigfile.txt
  ```

- **`nano`** : Command-line text editor.  
  ```bash
  nano notes.txt
  ```

---

## **Searching & Finding**
- **`find`** : Search for files and directories.  
  ```bash
  find /home -name "*.txt"
  ```

- **`grep`** : Search text patterns inside files.  
  ```bash
  grep "error" logfile.txt
  ```

---

## **Permissions**
- **`chmod`** : Change file permissions.  
  ```bash
  chmod 755 script.sh
  ```

- **`chown`** : Change file owner and group.  
  ```bash
  chown user:group file.txt
  ```

---

## **Process Management**
- **`ps`** : Process Status — lists running processes.  
  ```bash
  ps aux
  ```

- **`top`** : Interactive process viewer (shows CPU/memory usage).  
  ```bash
  top
  ```

- **`htop`** : Improved interactive process viewer *(may require installation)*.  
  ```bash
  htop
  ```

- **`kill`** : Send a signal to a process (usually to stop it).  
  ```bash
  kill 1234
  ```

- **`killall`** : Kill processes by name.  
  ```bash
  killall firefox
  ```

- **`bg`** : Resume a process in the background.  
  ```bash
  bg %1
  ```

- **`fg`** : Bring a background process to the foreground.  
  ```bash
  fg %1
  ```
