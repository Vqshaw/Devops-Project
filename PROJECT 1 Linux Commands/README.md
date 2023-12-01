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

