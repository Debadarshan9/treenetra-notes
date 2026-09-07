# Date: 31-August-2026

### **What is Operating System ?**

&rarr; It is a software that manage the computer's hardware and provides a platform for applications to run.

&rarr; EX: Windows, Linux, Unix, Android

### **What is Hardware ?**

&rarr; It means the physical parts of a compputer that we can see and touch.

&rarr; CPU, Mouse, Keyboard

### **What is server ?**

It is a computer or system that provides a service or resource to other computers for clients.

### **Hardware or Physical Server**

It is a physical computer designed for use to run server workloads.

### **Software Server**

Is is a program that provides a particular service to client.

### **Virtual Machine (VM)**

It is a software created computer that runs on a physical computer or server.

### **UNIX**

&rarr; It is a family of OS designed for multi user and multitasking computing.

&rarr; It was developed at Bell Labs around 1969.

### **Characteristices of UNIX**

&rarr; Multi use

&rarr; Multitasking

&rarr; Shell

&rarr; Powerful command line tools

### **LINUX**

&rarr; It is an open source unix like os echo system built around the linux kernel

&rarr; It was developed by Linux Torvalds in 1991

&rarr; It was inspired by unix but linux is not the original unix and its kernel is not copied from unix.

### **Windows**

&rarr; It is a GUI version.

&rarr; It is `Microsoft` OS family.

&rarr; Windows traditionally emphasize a graphical desktop of experience but it also provieds powerfull command line environment such as `powershell` and `command prompt`.

&rarr; We use `WSL (Windows Search System for Linux)` in windows that allows us to run a linux environment directly on windows without creating a separate VM.

### **Shell**

&rarr; It is a program that asts as an interface between the user and OS.

&rarr; It accepts commands from the user, interprets them and asks OS to perform the requested operation.

**1. sh (Bourne Shell)**

It is associated with bourne shell, one of the important historical unix shell.

**2. bash (Bourne Again Shell)**

It is the most commonly used shell on linux system.

**3. csh (C Shell)**

**4. ksh (Korn Shell)**

**5. zsh (Z Shell)**

# Date: 1-Sept-2026

### **Process Commands**

**`ps`** &rarr; Display current running process

**`top`** &rarr; shows running processes and system resource usage in real time

**`kill`** &rarr; Sends a signal to a process, commonly to stop it

### **System Commands**

**`whoami`** &rarr; It displays the current loged in username

**`hostname`** &rarr; It displays the system or computer name

**`uname`** &rarr; It displays the system or kernel information

**`uptime`** &rarr; It shows how long the system has been running and load information

**`free or free -h`** &rarr; It shows RAM and swap memory usage

**`df -h`** &rarr; It display available and used disk space

**`lsblk`** &rarr; It shows the information about block storage devices

**`lscpu`** &rarr; It shows CPU information

**`pwd (Present Working Drectory)`** &rarr; It shows the current directory

**`mkdir(Make Directory)`** &rarr; It creates a new directory or folder

```unix
mkdir foldername
```

**`ls(List)`** &rarr; It show all the folders inside the current directory

**`cd(Change Directory)`** &rarr; It moves from one directory to another

**`cd ..`** &rarr; Move one level of from parent level

**`touch`** &rarr; It creates a new empty file

```unix
touch filename
```

**`mv`** &rarr; It moves a file or directory and it can also rename the file

```unix
mv sourcename targetname

mv currentFileName NewFileName

sourcename: What you want to move
targetname: where you want to move
```

**`cp`** &rarr; It copies a file from one directory to another location

```unix
cp filename
```

**`cat`** &rarr; It displays the content of a file

```unix
cat fileName
```

**`rm`** &rarr; It removes or deletes a file or folder

```unix
rm fileName --for fileName
rm -r folder --for folder
```

**_NOTE: rm doesn't move the file to the recicle bin_**

### **What is a text editor?**

It is a program used to perform CRUD operations.

### **Types of editor**

vi, sed, nano

#### **VI Editor**

It is a command line text editor used to create and modify files

```
vi fileName
```

**`i`** &rarr; Used for inserting data

**`esc key`** &rarr; used to return to the normal mode

**`:w`** &rarr; for save

**`:q`** &rarr; for quite

**`:wq`** &rarr; for save and quite

**`:q!`** &rarr; for quite without saving

# Date: 2-Sept-2026

**`ls -a`** &rarr; It shows normal and hidden files

**`touch -a`** &rarr; It creates hidden file

`cat`, `less`, `more`

**`head`** &rarr; It shows first 10 lines of a file

```unix
head file_name
head -4 file_name # If we want specific lines from first
```

**`tail`** &rarr; It shows last 10 lines of a file

```unix
tail file_name
tail -4 file_name # If we want specific lines from last
```

**`sudo command`** &rarr; Run a command with admin

**`sudo apt update`** &rarr; Update package information

**`sudo apt upgrade`** &rarr; It update installed package

**`sudo apt install (packagename)`** &rarr; Install a package

**`sudo -i`** &rarr; Open a root shell

**`sudo apt search (packagename)`** &rarr; Search for a package

**`sudo apt list --installed`** &rarr; List installed package

**`sudo apt list --upgradable`** &rarr; Show packge that can b upgradable

| drwxr-xr-x                | 2          | debadarshan9 | debadarshan9 | 4096               | Sep 1 17:22   | folder1             |
| ------------------------- | ---------- | ------------ | ------------ | ------------------ | ------------- | ------------------- |
| File type and permissions | Hard links | users        | group        | file size in bytes | Date and time | File or folder name |

**drwxr-xr-x**

**-rw-r--r--**

`d` &rarr; directory

`-` &rarr; file

| owner (first 3) | group (second 3) | others (last 3) |
| --------------- | ---------------- | --------------- |
| rwx             | r-x              | r-x             |
| rw-             | r--              | r--             |

### **Permission Values**

| Number | Permission | Meaning                |
| ------ | ---------- | ---------------------- |
| 0      | ---        | No permission          |
| 1      | --x        | Execute only           |
| 2      | -w-        | Write only             |
| 3      | -wx        | Write + Execute        |
| 4      | r--        | Read only              |
| 5      | r-x        | Read + Execute         |
| 6      | rw-        | Read + Write           |
| 7      | rwx        | Read + Write + Execute |

**`chmod`** &rarr; It is used to change the permission of file or directory

```
chmod permision filename
chmod 432 file1.txt
```

**`chown`** &rarr; It is used to change the ower of a file or directory

```
sudo chown owner file
sudo chwon deba file1.txt
```

**`sudo su`** &rarr; Normal to root user

**`sudo adduser username`** &rarr; For adding new user

**`exit`** &rarr; Root to normal user

# Date: 3-Sept-2026

**`find`** &rarr; It is used to search for files and directories based on different conditions such as type, name, extension, size and midification time.

```unix
find [location][condition]
```

**`find .`** &rarr; Assume searching current directory

**`find /`** &rarr; Searching from root

### **Find by Type**

**`find . -type f`** &rarr; It will find all regular files

**`find . -type d`** &rarr; It will find all directories

### **Find by Name**

**`find . -name "treenetra"`** &rarr; It finds exact file name

**`find . -iname "treenetra"`** &rarr; It will find the file with same name

**_Note: `-i` is used for `case insensitive`_**

### **Find by extension**

**`find . -type f -name "*.py"`** &rarr; It will find all given extension files

**_Note: `*` is used for `all files`_**

### **Find by size**

**`find . -type f -size +10M`** &rarr; I will find the files with larger than the given size

**`find . -type f -size -10M`** &rarr; I will find the files with smaller than the given size

**`find . -type d -size +10M`** &rarr; I will find the folder with larger than the given size

**`find . -type d -size -10M`** &rarr; I will find the folder with smaller than the given size

### **Find by Modification Time**

**`find . -type f -mtime +1`** &rarr; I will find the file which is modified after 1 days.

**`find . -type f -mtime -1`** &rarr; I will find the file which is modified before 1 days.

**`grep`** &rarr; It is used to search for a speacific text or pattern inside files and display the lines that contained it.

```
grep "text" filename

grep "error" at26 #It will show exactly error

grep -i "error" at26 #It will show the word error with case insensitive (error, ERROR)

grep -n -i "error" at26 #It will show all the words along with its line no.

grep -v -i "error" at26 #It will show all words except the given word

grep -c -i "error" at26 #It will count all matching words in the given file
```

**`pipeline (|)`** &rarr; It is used to send the output of one command as the input to another command.

```
commnd1 | command2

ls | grep -i ".py" #It will show all the files with .py ext. inside the current directory
```

# Date: 7-Sept-2026

### **`sed` Editor**

&rarr; It is known as stream editor.

&rarr; It is a linux command used to read text from a file or a input, search for patterns and perform operations such as replacing, deleting or displaying lines.

**`delete line`** &rarr; Delete a specific line from the output

```unnix
sed "2d" file1 #For a specific line

sed "2,4d" file1 #For a range of lines

sed "2,4d" -i file1 #For permanent delete from a file (-i is used for permanent save)
```

**`replace text`** &rarr; Replace one text with another using the substitute command `s`.

```unix
sed "s/old_word/new_word/" file1 #It will replace all old_word with new_word
```

**`display line`** &rarr; We use `-n` with `p` when we want to display only specific lines.

```unix
sed -n "3p" file1 #It will show only 3rd line

sed -n "2,4p" file1 #It will show range of lines
```

**`find pattern`** &rarr; Search for a specific word

```unix
sed -n "/patttern/p" file1
```

**`insert line`** &rarr; `i` is used to insert a new line before a specific line.

```unix
sed -i "2i\Helo" #Insert a new line before a specific line

sed -i "3a\Welcome" #Insert a new line after a specific line
```
