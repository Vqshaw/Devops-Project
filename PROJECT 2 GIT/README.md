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
For the puporse of this, i created a repository name `Tonye`, made it public and ticked the chickbox to add a README.md file.

![Alt text](<Images/Screenshot 2024-01-31 160919.png>)

### Pushing your Local git Repository to your Remote github Repository
After making commits, the next step would be to push this commits to a remote repository. To do this, we have to first link our remote repo to our local repo. We will do this using HTTPS. We will copy the link and run the following command: `git remote add origin https://github.com/Vqshaw/Tonye.git`.

![Alt text](<Images/Screenshot 2024-01-31 161339.png>)

Now we can commit our changes using the command `git push origin master` where master is our branch name. 

When done, you will get a prompt to add your username and password, but unfortunately, Git has disabled that feature and you would have to link your remote and local repo using an ssh key. Here are the steps below:

