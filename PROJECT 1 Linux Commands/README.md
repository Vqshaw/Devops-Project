#  INTRODUCTION TO LINUX AND BASIC COMMANDS
Linux is a family of **open-source Unix** operating system based on the Linux Kernel. They include Fedora, Ubuntu, Open SUSE, red HAT, and Dabian. It is required that when using Linux operating systems, you use a shell (a shell is a program that gives you access to the operating system's services.)

Tasks that require multiple steps on the GUI (Graphical User Interface) can be done in a matter of seconds by entering commands into the CLI (Command-line Interface). That is why it is recommended to use the CLI because it is faster, quicker, and it offers more control.


##  What is a Linux Command?
A Linux command is utility or program that on the CLI. What is this CLI? it is a console that interacts with the system using texts and processes. 

By pressing Enter at the end of every line, Linux commands are executed on the terminal. You can run commands to perform various tasks, such as: file manipulation, user management to package installation. 

A typical command syntax looks like this:

```
CommandName [option(s)] [parameter(s)]
```

Above are the 3 most common part of a command line, **CommandName** is the rule that you wanna perform. **Option/flag** modifies a command's operation. To invoke it, use hypens *(-)* or double hypens *(--)*. A command might contain an *option* or *parameter*, but in some cases, a command can run without it.

## File Manipulation
### 1. `ls` command:
This command list files and folders/directories within a system. Running it without a flag shows the contents in the present working directory as seen below.

```
ls
ls -l
```

![ls pictorial example](<Images/Screenshot 2023-11-11 001502.png>)


### 2. `mkdir` command:
This command is used to create a one or more directories at once and set permissions for each of them. The user executing this command must have the previlege to create a new folder in the parent directory or they might get a permissin denied error.

Here is the syntax below:

```
mkdir [option] directory_name
```
![mkdir](<Images/Screenshot 2023-12-01 192217.png>)

### 3. `cd` command:
This command is used to navigate through files and directories. Running this command without an option will take you to the home drirectory.

To navigate into anothe directory, use this command `cd directory_name` as shown below

```
cd Devops_project
```
To go one directory backwards, use the below command
```
cd ..
```
To go to the home directory, use the below command
```
cd
```
![cd](<Images/Screenshot 2023-12-01 193443.png>)

### 4. `touch` command:
This command is used to create a new empty file
```
ls
```
![ls](<Images/Screenshot 2023-12-01 193849.png>)

### 5. `pwd` command:
This command is used to find the path of your present working directory
```
pwd
```
![pwd](<Images/Screenshot 2023-12-01 194152.png>)

### 6. `cat` command:
Concatenate, or `cat` combines and writes file to the standard output. There are various ways to use the cat command and they are listed below.

To display the content of a file, run this command:

```
cat file_name.txt
```
To merge the content of two files and store the output in a new file, run the following command:
```
cat file_name1.txt file_mame2.txt > file_name3.txt
```
To dispaly content in reverse order, run this command:
```
tac file_name.txt
```
![cat](<Images/Screenshot 2023-12-01 200601.png>)

### 7. `cp` command:
This command is used to copy files or directories and their contents.


To copy a file to a new directory, use the following command as seen below:
```
cp file_name.txt /home/bagshaw/Downloads
```
![cp](<Images/Screenshot 2023-12-01 203718.png>)


To copy the content of a file to a new file, enter `cp` followed by the source file and the destination file
```
cp newfile1.txt newfile.txt
```
![cp](<Images/Screenshot 2023-12-01 204639.png>)

To copy an entire directory, do the following:
```
cp -r /home/username/directory /home/username/directory
i.e
cp -r /home/bagshaw/Downloads /home/bagshaw/Documents
```
![cp](<Images/Screenshot 2023-12-02 110038.png>)

### 8. `mv` command:
The primary use of the `mv` command is to move or rename file or directories. Additionally, it doesnt produce an output on execution.

To execute this command, simply type `mv` followed by the file name as well as the destination directory. Here is an example below:

```
mv newfile.txt /home/bagshaw/Music
```
![mv](<Images/Screenshot 2023-12-02 111008.png>)

Also, the `mv` command can be used to rename file or directories as seen below:
```
mv newfile1.txt newfile1.sh
```
![mv](<Images/Screenshot 2023-12-02 111339.png>)


### 9. `rmdir` command:
To permanently delete a directory, use the `rmdir` command. In order for a user to run this command, that user has to have sudo privileges in the parent directory. Example below:
```
rmdir Devops_project/junk_files
```
![rmdir](<Images/Screenshot 2023-12-02 112119.png>)

### 10. `rm` command:
The command deletes files within a directory. The user performing this has to have write permission. Once a file has been deleted, it cannot be undone.

```
rm Downloads
```
![rm](<Images/Screenshot 2023-12-02 112556.png>)

To remove multiple files, you can run this command:
```
rm filename1.txt filename2.txt filename3.txt
```
Here are other optons you can add:
- -f removes a file without confirmation
- -i prompts system confirmation before removing a file
- -r deletes file and directories recursively



### 11. `locate` command:
This command is used to find a file the the database system. 
Adding the -i argument, will turn off case sensitivity so that you can search for a file even if you do not remeber its exact name.
```
locate -i Downloads
```


![locate](<Images/Screenshot 2023-12-02 114113.png>)

If you need to look for contents that have two or more words, you can add an asterisk(*).

```
locate -i school*note
```
This command will search for files that contain the words school and note, whether they are uppercase or lowercase.

### 12. `find` command:
THis command is used to search for files within a specific directory and perform subsequent operations. The general syntax is stated below:

```
find [option] [path] [expression]
```

If you want to look for a file name *newfile1.txt* within the home directory and its subfolders, here is the code below:
```
find /home newfile1.sh
```
![find](<Images/Screenshot 2023-12-02 115156.png>)

### 13. `grep` command: 
Also known as **global regular expression print**, this command lets you find a word by searching through a text in a specific file.

Once the `grep` command finds a match, it will print out all line that contain the specific pattern. THis command is very helpful when filtering through large log files.

If I wanna search for the word 'rivers' in the file newfile1.sh, here is the command line.

```
grep Rivers newfile1.sh
```
![grep](<Images/Screenshot 2023-12-02 121147.png>)\

### 14. `df` command:
This command is used to report the system's disk space usage, shown in percentage and kilobyte (KB). Here is the general syntax:

```
df [option] [file]
```
- To see the current directory's disk system space in a human readable format. use `df -h`
- To display information on the file system usage in MBs, use `df -m`
- To display information on the file system usage in Kb, use `df -k`
- To show file system type in a new column, use `df -T`

![Alt text](<Images/Screenshot 2023-12-02 122241.png>)

### 15. `du` command:
This command can be used to check how much space a file or directory takes up. You can also run this command to identify which part of the system uses the storage excessively. For example:

```
du /home/bagsahw/Devops_project
```

alternatively,
- use `du -s` to know the total size of a specific folder
- use `du -m` to know the file and folder information in MBs
- use `du -k` to know the file and folder information in kb
- USE `DU -H` Tto know the last modification date of the dispalyed files and folders

![du](<Images/Screenshot 2023-12-02 123754.png>)

### 16. `head` command:
This commands lets you view the first ten lines of a text.Adding an option lets you change the number of lines shown. THe hed command is also used output piped data to the CLI. For example:

```
head [option] [file]

head readme.txt
```
![head](<Images/Screenshot 2023-12-02 125252.png>)

- `-n` or `-lines` prints the first customized number of lines.
- `-c` or `-bytes` prints the first customized number of bytes of each file.
- `-q` or `-quiet` will not print headers specifying the file name.

### 17. `tail` command:
This command reads the last ten lines of a text, and it is also used to check if a file has new data or to check for error messages.

```
tail [option] [file]

tail readme.txt
```
![tail](<Images/Screenshot 2023-12-02 130120.png>)

### 18. `diff` command:
Short for difference, this command compares two contents of a file line by line. After analyzing them, it will display the part that do not match.

The general syntax:
```
diff [option] file1 file2
```
![diff](<Images/Screenshot 2023-12-02 133807.png>)

Other options you can use:
- `-c` displayes the difference between two files in a context form.
- `-u` displays the output without redundant information.
- `-i` makes the diff command case insensitive.

### 19. `tar` command:
This command archives multiple files into a TAR file - a common LInux format similar to a ZIP, with optional compression.

Basic syntax:
```
tar [option] [archive_file] [file or directory to be archived]
```
For example, if I wanna archive files in a directory, here is the syntax code for that:
```
tar -cvf newfile1.tar /home/bagshaw/Devops_project
```
![tar](<Images/Screenshot 2023-12-02 135221.png>)

Use:
- -x to extract a file
- -t to list the contents of a file
- -u archives and add to an existing archive file

### 20. `sudo` commands:
Short for *superuser do*, this command lets you perform tasks that require administrative or root permissions.
When using `sudo`, the system prompts users to authenticate themselves with their password. Then the system will log a timestamp as a tracker. By default, every root user can run `sudo` cpmmand for 15 minutes/session.

If you try to run the `sudo` command without authenticating yourself, the system will log the activity as a security event.

Basic syntax:
```
sudo (xcommand e.g apt upgrade)

sudo apt upgrade
```

![sudo](<Images/Screenshot 2023-12-02 140513.png>)

## File Permissions and Ownership
### 21. `chmod`command:
This is a command that lets you modify a directorie's read, write, and execute permissions. In Linux, each file is associated with three user classes - owner, group member, and others.

Below is the basic syntax:
```
chmod [option] [permission] [file_name]
```
For example, the owner is currently the only one with full permissions to change note.txt. To allow group members and others to read, write, and execute the file, change it to the -rwxrwxrwx permission type, whose numeric value is 777:
```
chmod 777 tonye.yml
```
![chmod](<Images/Screenshot 2024-01-21 121128.png>)

This command supports many options, including:

-c or –changes displays information when a change is made. -f or –silent suppresses the error messages. -v or –verbose displays a diagnostic for each processed file.

### 22. `chown` command:
The chown command lets you change the ownership of a file, directory, or symbolic link to a specified username.

Here’s the basic format:
```
chown [option] owner[:group] file(s)
```
For example, you want to make tonye the owner of tonye.yml:
```
chown linuxuser2 filename.txt
```
![chown](<Images/Screenshot 2024-01-21 121738.png>)

### 23. `jobs` command:
A job is a process that the shell starts. The jobs command will display all the running processes along with their statuses. Remember that this command is only available in csh, bash, tcsh, and ksh shells.

This is the basic syntax:
```
jobs [options] jobID
```
To check the status of jobs in the current shell, simply enter jobs to the CLI.

Here are some options you can use:

-l lists process IDs along with their information. -n lists jobs whose statuses have changed since the last notification. -p lists process IDs only.

### 24. `kill` command:
Use the kill command to terminate an unresponsive program manually. It will signal misbehaving applications and instruct them to close their processes.

To kill a program, you must know its process identification number (PID). If you don’t know the PID, run the following command:
```
ps ux
```
There are 64 signals that you can use, but these two are among the most commonly used:

SIGTERM requests a program to stop running and gives it some time to save all of its progress. The system will use this by default if you don’t specify the signal when entering the kill command. SIGKILL forces programs to stop, and you will lose unsaved progress. For example, the program’s PID is 1552, and you want to force it to stop:

```
kill SIGKILL 1552
```
![Alt text](<Images/Screenshot 2024-01-21 122635.png>)

### 25. `ping` command:
The ping command is one of the most used basic Linux commands for checking whether a network or a server is reachable. In addition, it is used to troubleshoot various connectivity issues.

Here’s the general format:

Here is the syntax code
```
ping [option] [hostname_or_IP_address]
```
For example, you want to know whether you can connect to Google and measure its response time:
```
ping google.com
```

### 26. `wget` command:
The Linux command line lets you download files from the internet using the wget command. It works in the background without hindering other running processes.

The wget command retrieves files using HTTP, HTTPS, and FTP protocols. It can perform recursive downloads, which transfer website parts by following directory structures and links, creating local versions of the web pages.

To use it, enter the following command:

```
wget [option] [url]
```
For example, enter the following command to download the latest version of WordPress:
```
wget https://wordpress.org/latest.zip
```
![wget](<Images/Screenshot 2024-01-21 124459.png>)

### 27.    `uname` command:
The uname or unix name command will print detailed information about your Linux system and hardware. This includes the machine name, operating system, and kernel. To run this command, simply enter uname into your CLI.

Here’s the basic syntax:

```
uname [option]
```
These are the acceptable options to use:

-a prints all the system information. -s prints the kernel name. -n prints the system’s node hostname.

![uname](<Images/Screenshot 2024-01-21 125055.png>)

### 28. `top` command:
The top command in Linux Terminal will display all the running processes and a dynamic real-time view of the current system. It sums up the resource utilization, from CPU to memory usage.

The top command can also help you identify and terminate a process that may use too many system resources.

To run the command, simply enter top into the CLI.

```
top
```

![Alt text](<Images/Screenshot 2024-01-21 125313.png>)

### 29. `history` command:
With history, the system will list up to 500 previously executed commands, allowing you to reuse them without re-entering. Keep in mind that only users with sudo privileges can execute this command. How this utility runs also depends on which Linux shell you use.

To run it, enter the command below:
```
history [option]
```
This command supports many options, such as:

-c clears the complete history list. -d offset deletes the history entry at the OFFSET position. -a appends history lines.

![history](<Images/Screenshot 2024-01-21 125628.png>)

### 30. `man` command:
The man command provides a user manual of any commands or utilities you can run in Terminal, including the name, description, and options.

It consists of nine sections:

Executable programs or shell commands System calls Library calls Games Special files File formats and conventions System administration commands Kernel routines Miscellaneous To display the complete manual, enter:

```
man [command_name]
```
For example, you want to access the manual for the ls command:

```
man ls
```
Enter this command if you want to specify the displayed section:

```
man [option] [section_number] [command_name]
```
For instance, you want to see section 2 of the ls command manual:

```
man 2 ls
```

### 31. `echo` command:
The echo command is a built-in utility that displays a line of text or string using the standard output. Here’s the basic syntax:

```
echo [option] [string]
```
This command supports many options, such as:

- `-n` displays the output without the trailing newline. 
- `-e` enables the interpretation of the following backslash escapes: \a plays sound alert. \b removes spaces in between a text. \c produces no further output. 
- `-E` displays the default option and disables the interpretation of backslash escapes.

### 32. ``zip, unzip` commands:
Use the zip command to compress your files into a ZIP file, a universal format commonly used on Linux. It can automatically choose the best compression ratio.

The zip command is also useful for archiving files and directories and reducing disk usage.

To use it, enter the following syntax:

```
zip [options] zipfile file1 file2….
```
For example, you have a file named tonye.yml that you want to compress into archive.zip in the current directory:

```
zip tonye.zip tonye.yml
```
On the other hand, the unzip command extracts the zipped files from an archive. Here’s the general format:

```
unzip [option] file_name.zip
```
So, to unzip a file called archive.zip in the current directory, enter:

```
unzip tonye.zip
```

![zip](<Images/Screenshot 2024-01-21 131029.png>)


### 33. `hostname` command:
Run the hostname command to know the system’s hostname. You can execute it with or without an option. Here’s the general syntax:

```
hostname [option]
```
There are many optional flags to use, including:

-a or –alias displays the hostname’s alias. -A or –all-fqdns displays the machine’s Fully Qualified Domain Name (FQDN). -i or –ip-address displays the machine’s IP address. For example, enter the following command to know your computer’s IP address:

```
hostname -i
```
![hostname](<Images/Screenshot 2024-01-21 131756.png>)

### 34. `useradd`, `userdel` commands:
Linux is a multi-user system, meaning more than one person can use it simultaneously. useradd is used to create a new account, while the passwd command allows you to add a password. Only those with root privileges or sudo can run the useradd command.

When you use the useradd command, it performs some major changes:

Edits the /etc/passwd, /etc/shadow, /etc/group, and /etc/gshadow files for the newly created accounts. Creates and populates a home directory for the user. Sets file permissions and ownerships to the home directory. Here’s the basic syntax:

```
useradd [option] username
```
To set the password:

```
passwd the_password_combination
```
For example, to add a new person named John, enter the following command simultaneously:

```
useradd John

passwd 123456789
```
To delete a user account, use the userdel command:

```
userdel username
```

### 35. `apt-get` command:
apt-get is a command line tool for handling Advanced Package Tool (APT) libraries in Linux. It lets you retrieve information and bundles from authenticated sources to manage, update, remove, and install software and its dependencies.

Running the apt-get command requires you to use sudo or root privileges.

Here’s the main syntax:

```
apt-get [options] (command)
```
These are the most common commands you can add to apt-get:

- `update` synchronizes the package files from their sources. 
- `upgrade` installs the latest version of all installed packages. 
- `check` updates the package cache and checks broken dependencies.

![aptget](<Images/Screenshot 2024-01-21 132707.png>)

### 36. `nano`, `vi`, `jed` commands:
Linux allows users to edit and manage files via a text editor, such as nano, vi, or jed. nano and vi come with the operating system, while jed has to be installed.

The `nano` command denotes keywords and can work with most languages. To use it, enter the following command:

```
nano [filename]
```
`vi` uses two operating modes to work – insert and command. insert is used to edit and create a text file. On the other hand, the command performs operations, such as saving, opening, copying, and pasting a file.

To use vi on a file, enter:

```
vi [filename]
```
`jed` has a drop-down menu interface that allows users to perform actions without entering keyboard combinations or commands. Like vi, it has modes to load modules or plugins to write specific texts.

To open the program, simply enter jed to the command line.

### 37. `alias`, `unalias` commands:
alias allows you to create a shortcut with the same functionality as a command, file name, or text. When executed, it instructs the shell to replace one string with another.

To use the alias command, enter this syntax:

```
alias Name=String
```
For example, you want to make k the alias for the kill command:

```
alias k=’kill’
```
On the other hand, the unalias command deletes an existing alias.

Here’s what the general syntax looks like:

```
unalias [alias_name]
```

### 38. `su` command:
The switch user or su command allows you to run a program as a different user. It changes the administrative account in the current log-in session. This command is especially beneficial for accessing the system through SSH or using the GUI display manager when the root user is unavailable.

Here’s the general syntax of the command:

```
su [options] [username [argument]]
```
When executed without any option or argument, the su command runs through root privileges. It will prompt you to authenticate and use the sudo privileges temporarily.

Here are some acceptable options to use:

-p or –preserve-environment keeps the same shell environment, consisting HOME, SHELL, USER, and LOGNAME. -s or –shell lets you specify a different shell environment to run. -l or –login runs a login script to switch to a different username. Executing it requires you to enter the user’s password.

### 39. `htop` command:
The htop command is an interactive program that monitors system resources and server processes in real time. It is available on most Linux distributions, and you can install it using the default package manager.

Compared to the top command, htop has many improvements and additional features, such as mouse operation and visual indicators.

To use it, run the following command:

```
htop [options]
```
You can also add options, such as:

-d or –delay shows the delay between updates in tenths of seconds. -C or –no-color enables the monochrome mode. -h or –help displays the help message and exit.

### 40. `ps` command:
The process status or ps command produces a snapshot of all running processes in your system. The static results are taken from the virtual files in the /proc file system.

Executing the ps command without an option or argument will list the running processes in the shell along with:

The unique process ID (PID) The type of the terminal (TTY) The running time (TIME) The command that launches the process (CMD)

Here are some acceptable options you can use:

-T displays all processes associated with the current shell session. -u username lists processes associated with a specific user. -A or -e shows all the running processes.

![ps](<Images/Screenshot 2024-01-21 134616.png>)