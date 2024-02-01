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

# Working with branches
### Making my first branch
For example, if we wanna create a branch named **PRODUCTION**, we would use the syntax `git checkout -b PRODUCTION`. Where PRODUCTION, is the branch name.
The flag `-b` helps you switch to the new branch at once.

![Alt text](<Images/Screenshot 2024-01-31 154342.png>)

### Listing my branches
Use the commsnd `git branch` to list all branches

![Alt text](<Images/Screenshot 2024-01-31 154909.png>)

### Change into an Old Branch
Right now, we are in the Production branch, let us switch back to the master branch. `git checkout maaster`

![Alt text](<Images/Screenshot 2024-01-31 155139.png>)

### Merging a Branch into another Branch
In order for us to merge the production branch to the master branch, we have to first switch to the master branch which we are in already, and run the command `git merge production`

### Deleting a git branch
To delete a branch, we run the command `git branch -d production` where production is the branch name.

![Alt text](<Images/Screenshot 2024-01-31 155552.png>)

# Collaboration and Remote Repositories
### Creating a Github account
The first step to colaborate and create remote repositories, is to create a Github account. It can be done by navigating to https://github.com/ and click signup.

### Creating a repository
For the puporse of this, i created a repository name `Tonye`, made it public and ticked the checkbox to add a README.md file.

![Alt text](<Images/Screenshot 2024-01-31 160919.png>)

### Pushing your Local git Repository to your Remote github Repository
After making commits, the next step would be to push this commits to a remote repository. To do this, we have to first link our remote repo to our local repo. We will do this using ssh. We will copy the link and run the following command: `git remote add origin git@github.com:Vqshaw/Tonye.git`.

![Alt text](<Images/Screenshot 2024-01-31 161339.png>)

Now we can commit our changes using the command `git push origin master` where master is our branch name. 

When done, you will get a prompt to add your username and password, but unfortunately, Git has disabled that feature and you would have to link your remote and local repo using an ssh key. Here are the steps below:

- Open your command link interface, and run the command ssh-keygen -t ed25519 -C "your_email@example.com", where **your_email@example.com** is your Github email address.

- You will be prompted to provide a file name for your SSHkey. You can do that or use the default. click enter.

- You will be prompted to provide a password, you can do that or also choose to ignore.

- Download the SSHkey to your local computer. I am using MobaXterm, so I downloaded it to my desktop.

![Alt text](<Images/Screenshot 2024-01-31 163522.png>)

In order to add this SSHkey to our Github account, we have to do the following:

- In the upper-right corner of any page, click your profile photo, then click Settings.
- In the "Access" section of the sidebar, click  SSH and GPG keys.
- Click New SSH key or Add SSH key.
- In the "Title" field, add a descriptive label for the new key. 
- Select the type of key, either authentication or signing.
- In the "Key" field, paste your public key.
- Click Add SSH key.
- If prompted, confirm access to your account on GitHub. For more information, see "Sudo mode."

![Alt text](<Images/Screenshot 2024-02-01 150313.png>)

After that, you add your sshkey to your ssh agent. to do that, i ran this command `ssh-add <file path>` where file path is the path where your key is.

![Alt text](<Images/Screenshot 2024-02-01 150511.png>)

Now, you can run the `git remote set-url <ssh_link` command and it will be a success. so, anytime you run the `git push origin master` command.

![Alt text](<Images/Screenshot 2024-02-01 150702.png>)

## Markdown Syntax

### 1. Headings
- #heading 1
- ##heading 2
- ###heading 3

### 2. Emphasis: asterisks or underscore 
- *italic * or _ italic _
- ** bold** or __ bold__

### 3. Lists: ordered and unorderd list
- unrdered list example:

  - -Item 1
  - -Item 2
  - -Item 3

- ordered list example:

  1. Item 1
  2. Item 2
  3. Item 3

### 4. Links
  [visit google.com] (https://google.com)

### 5. Images
  ![alt text](image link)

### 6. Code: To display code or code snippets, use backticks (`) to enclose the code.
![Alt text](<Images/Screenshot 2024-02-01 153323.png>)

