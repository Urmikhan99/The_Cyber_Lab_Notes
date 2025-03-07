# Essential Linux Commands

## 1. **File and Directory Operations**:
- **`ls`**: Lists all files and directories in the present working directory.
- **`ls -R`**: Lists files in sub-directories as well.
- **`ls -a`**: Shows hidden files.
- **`ls -al`**: Lists files and directories with detailed information like permissions, size, owner, etc.
- **`cd directoryname`**: Changes the directory.
- **`cd ..`**: Moves one level up.
- **`pwd`**: Displays the present working directory.
- **`cat > filename`**: Creates a new file.
- **`cat filename`**: Displays the file content.
- **`cat file1 file2 > file3`**: Joins two files (file1 and file2) and stores the output in a new file (file3).
- **`touch filename`**: Creates or modifies a file.
- **`rm filename`**: Deletes a file.
- **`cp source destination`**: Copies files from the source path to the destination path.
- **`mv source destination`**: Moves files from the source path to the destination path.
- **`find / -name filename`**: Finds a file or a directory by its name starting from root.
- **`file filename`**: Determines the file type.
- **`less filename`**: Views the file content page by page.
- **`head filename`**: Views the first ten lines of a file.
- **`tail filename`**: Views the last ten lines of a file.
- **`lsof`**: Shows which files are opened by which process.
- **`du -h --max-depth=1`**: Shows the size of each directory. Use `--max-depth=1` to limit the output to the current directory and its immediate children.
- **`fdisk`**: Disk partition manipulation command.


## 2. **Directory Operations**:
- **`mkdir directoryname`**: Creates a new directory in the present working directory.
- **`rmdir directoryname`**: Deletes a directory.
- **`cp -r source destination`**: Copies directories recursively.
- **`mv olddir newdir`**: Renames directories.
- **`find / -type d -name directoryname`**: Finds a directory starting from root.

## 3. **Process Operations**:
- **`ps`**: Displays your currently active processes.
- **`top`**: Displays all running processes.
- **`kill pid`**: Kills the process with given pid.
- **`pkill name`**: Kills the process with the given name.
- **`bg`**: Resumes suspended jobs without bringing them to foreground.
- **`fg`**: Brings the most recent job to foreground.
- **`fg n`**: Brings job n to the foreground.
- **`renice +n [pid]`**: Change the priority of a running process.
- **`&>filename`**: Redirects both stdout and stderr to the file filename.
- **`1>filename`**: Redirect stdout to file filename.
- **`2>filename`**: Redirect stderr to file filename.

## 4. **File Permissions**:
- **`chmod octal filename`**: Change the permissions of file to octal, which can be between 0 (no permissions) to 7 (full permissions).
- **`chown ownername filename`**: Change file owner.
- **`chgrp groupname filename`**: Change group owner.


## 5. **Networking**:
- **`ping host`**: Ping a host and outputs results.
- **`whois domain`**: Get whois information for domain.
- **`dig domain`**: Get DNS information for domain.
- **`netstat -pnltu`**: Display various network-related information such as network connections, routing tables, interface statistics, etc.
- **`ifconfig`**: Displays IP addresses of all network interfaces.
- **`ssh user@host`**: Remote login into the host as user.
- **`scp`**: Transfers files between hosts over ssh.
- **`wget url`**: Download files from the web.
- **`curl url`**: Sends a request to a URL and returns the response.
- **`traceroute domain`**: Prints the route that a packet takes to reach the domain.
- **`mtr domain`**: mtr combines the functionality of the traceroute and ping programs in a single network diagnostic tool.
- **`ss`**: A more modern alternative to netstat to investigate sockets.
- **`nmap`**: Network exploration tool and security scanner.

## 6. **Archives and Compression**:
- **`tar cf file.tar files`**: Create a tar named file.tar containing files.
- **`tar xf file.tar`**: Extract the files from file.tar.
- **`gzip file`**: Compresses file and renames it to file.gz.
- **`gzip -d file.gz`**: Decompresses file.gz back to file.
- **`zip -r file.zip files`**: Create a zip archive named file.zip.
- **`unzip file.zip`**: Extract the contents of a zip file.

## 7. **Text Processing**:
- **`grep pattern files`**: Search for pattern in files.
- **`grep -r pattern dir`**: Search recursively for pattern in dir.
- **`command | grep pattern`**: Pipe the output of command to grep for searching.
- **`echo 'text'`**: Prints text.
- **`sed 's/string1/string2/g' filename`**: Replaces string1 with string2 in filename.
- **`diff file1 file2`**: Compares two files and shows the differences.
- **`wc filename`**: Count lines, words, and characters in a file.
- **`awk`**: A versatile programming language for working on files.
- **`sed -i 's/string1/string2/g' filename`**: Replace string1 with string2 in filename. The -i option edits the file in-place.
- **`cut -d':' -f1 /etc/passwd`**: Cut out the first field of each line in `/etc/passwd`, using colon as a field delimiter.

## 8. **Disk Usage**:
- **`df`**: Shows disk usage.
- **`du`**: Shows directory space usage.
- **`free`**: Show memory and swap usage.
- **`whereis app`**: Show possible locations of app.

## 9. **System Info**:
- **`date`**: Show the current date and time.
- **`cal`**: Show this month's calendar.
- **`uptime`**: Show current uptime.
- **`w`**: Display who is online.
- **`whoami`**: Who you are logged in as.
- **`uname -a`**: Show kernel information.
- **`df -h`**: Disk usage in human-readable format.
- **`du -sh`**: Disk usage of current directory in human-readable format.
- **`free -m`**: Show free and used memory in MB.



## 10. **Package Installations**:
- **`sudo apt-get update`**: Updates package lists for upgrades.
- **`sudo apt-get upgrade`**: Upgrades all upgradable packages.
- **`sudo apt-get install pkgname`**: Install pkgname.
- **`sudo apt-get remove pkgname`**: Removes pkgname.

## 11. **Others (Mostly Used in Scripts)**:
- **`command1 ; command2`**: Run command1 and then command2.
- **`command1 && command2`**: Run command2 if command1 is successful.
- **`command1 || command2`**: Run command2 if command1 is not successful.
- **`command &`**: Run command in background.

## 12. **Version Control (Git commands)**:
- **`git init`**: Initialize a local git repository.
- **`git clone url`**: Create a local copy of a remote repository.
- **`git add filename`**: Add a file to the staging area.
- **`git commit -m "Commit message"`**: Commit changes with a message.
- **`git status`**: Check the status of the working directory.
- **`git pull`**: Pull the latest changes from the remote repository.
- **`git push`**: Push changes to the remote repository.
- **`git branch`**: List all local branches.
- **`git branch branchname`**: Create a new branch.
- **`git checkout branchname`**: Switch to a branch.
- **`git merge branchname`**: Merge a branch into the active branch.
- **`git stash`**: Stash changes in a dirty working directory.
- **`git stash apply`**: Apply changes from a stash.
- **`git log`**: View commit history.
- **`git reset`**: Reset your HEAD pointer to a previous commit.
- **`git rm filename`**: Remove a file from version control.
- **`git diff`**: View changes not staged for commit.

---

