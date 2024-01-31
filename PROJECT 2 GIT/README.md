# Initializing a Repository and Making Commits
## Initializing my first commit
Before initializing a git repo you have to install git on your computer.

Git is available for Windows, Linux, and Mac users. So, goto https://git-scm.com/downloads and download the one for your operating system.

To initialize a git repo follow these steps:
- Open a terminal on your computer, eg git bash, powershell, command prompt.

- On your terminal create your working folder or directory eg Tonye folder using the `mkdir Tonye` command.

- Change or move into your working directory/folder.

- While you are inside the folder, run `git init` command

![Alt text](<Images/Screenshot 2024-01-31 152136.png>)




## Making my first Commit
- Inside your working directory create a file tonye.txt 

- You can use this command `touch tonye.txt` but in my case I will be using this `echo "I am a very big fan of Darey.io" > tonye.txt`

- Add your changes to git staging area using this command git add .

- To commit your changes to git, run the command git commit -m "initial commit"
- I was prompted to set my Identity, so I used this command syntax `git config --global user.name "your name"` and `git config --global user.email "your email"`, and then I ran the commit command again and it was successful.

![Alt text](<Images/Screenshot 2024-01-31 153534.png>)

The -m flag is used to provide a commit message. The commit message is a nice way to provide context about the commit. When writing a commit message, make it descriptive as possible. Let it explain why the commit was made.