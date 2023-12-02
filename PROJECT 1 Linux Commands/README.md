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
![mkdir](<Screenshot 2023-12-01 192217.png>)

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
![cd](<Screenshot 2023-12-01 193443.png>)

### 4. `touch` command:
This command is used to create a new empty file
```
ls
```
![ls](<Screenshot 2023-12-01 193849.png>)

### 5. `pwd` command:
This command is used to find the path of your present working directory
```
pwd
```
![pwd](<Screenshot 2023-12-01 194152.png>)

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
![cat](<Screenshot 2023-12-01 200601.png>)

### 7. `cp` command:
This command is used to copy files or directories and their contents.


To copy a file to a new directory, use the following command as seen below:
```
cp file_name.txt /home/bagshaw/Downloads
```
![cp](<Screenshot 2023-12-01 203718.png>)


To copy the content of a file to a new file, enter `cp` followed by the source file and the destination file
```
cp newfile1.txt newfile.txt
```
![cp](<Screenshot 2023-12-01 204639.png>)

To copy an entire directory, do the following:
```
cp -r /home/username/directory /home/username/directory
i.e
cp -r /home/bagshaw/Downloads /home/bagshaw/Documents
```
![cp](<Screenshot 2023-12-02 110038.png>)

### 8. `mv` command:
The primary use of the `mv` command is to move or rename file or directories. Additionally, it doesnt produce an output on execution.

To execute this command, simply type `mv` followed by the file name as well as the destination directory. Here is an example below:

```
mv newfile.txt /home/bagshaw/Music
```
![mv](<Screenshot 2023-12-02 111008.png>)

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

