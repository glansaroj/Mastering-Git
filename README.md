# Mastering Git


## ⬛ Git/ Github Intro:
 Git is a version control system used for tracking changes in source code during software development. It helps multiple developers work on a project simultaneously without conflicts, allowing them to collaborate efficiently.


GitHub is a web-based platform built around Git, providing hosting for software development and version control using Git. It enhances Git's capabilities by adding a user-friendly interface and collaborative features for teams.
 
 Key points
- Git is a version control system.
- Git helps you keep track of code changes.
- Git is used to collaborate on code.
- Git and GitHub are different things.


<br>

___________________________________________________________________________________

<br>


## ⬛ Features of Git :
- When a file is changed, added or deleted, it is considered
  modified
- You select the modified files you want to Stage
- The Staged files are Committed, which prompts Git to store a
   permanent snapshot of the files
- Git allows you to see the full history of every commit.
- You can revert back to any previous commit.
- Git does not store a separate copy of every file in every
  commit, but keeps track of changes made in each commit!

<br>

___________________________________________________________________________________

<br>

## ⬛ Configuring  Git :
Configuring Git for the first time involves a few initial setup steps. 
Here's a step-by-step guide to help you get started:


> (1) Install Git: First, you need to install Git on your system.

> (2) Configure your identity: Open a terminal or command prompt and configure 
    your Git username and email.

Use the following commands, replacing "Your Name" and "Your Email".



``` 
git config --global user.name "Your Name"
```

```
git config --global user.email "youremail@example.com"
```

<br>

___________________________________________________________________________________

<br>



## ⬛  General Git Features:

### ✅ Initializing Git 
git init command is the first step in creating a new Git repository from scratch. When you run git init in a directory, it initializes a new Git repository, enabling version control for the files within that directory.
Git creates a hidden folder to keep track of changes.

```

git init

```

### ✅ Staging files/Adding files to Git repo: 
Staged files are files that are ready to be committed to the repository you are working on.
When you first add files to an empty repository, they are all untracked. 
To get Git to track them, you need to stage them, or add them to the staging environment.

```

git add <file1> <file2> ... # Add specific files
git add .                   # Add all files in the directory

```


### ✅ Making a Commit:
Adding commits keep track of our progress and changes as we work.
When we commit, we should always include a message.

```

git commit -m “<Enter your message here>”

```


### ✅ Git Commit without Stage 
Sometimes, when you make small changes, using the staging environment seems like a waste of time. 
It is possible to commit changes directly, skipping the staging environment.

```

git commit -a -m “<Enter your message here>”

```

### ✅  Status of files and log:
**git log** command in Git is used to display the commit history in a repository. When executed, it shows a list of commits in reverse chronological order, displaying information about each commit such as the commit hash, author, date, and commit message.

Git log

```

git log

```

**git status** is a command used in Git to check the current status of your repository. When you run git status, Git provides information about the state of files and branches within your working directory.

```

git status

git status --short  (File status in a more compact way)

```

### ✅ Git Help:
If you are having trouble remembering commands or options for commands, 
you can use Git help.


To See all the available options for the specific command:

```

git <command> -help

```

To See all possible commands -

```

git help --all

```

*Note: If you find yourself stuck in the list view 
      SHIFT + G ---> to jump the end of the list. 
      q  ---> to exit the view.*

<br>

___________________________________________________________________________________

<br>


## ⬛ Working with Github:
To get stated, Create a GitHub account to create your remote repositories. 
Now, create a new repo where we will be uploading our files from the local repo.

**Local repository** (repo.)  ---> the repo. which is on our system

**remote repo**  ---> the one which is on another remote system/server, for eg. - GitHub, GitLab, Bitbucket, etc.


 
### ✅ Push local repo to GitHub:

> Copy the URL or the link of the repo that we just created. 
Paste the copied URL in the below git command.

```

git remote add origin <paste copied URL here>

```

> Pushing our master branch to the origin URL (remote repo)
and set it as the default remote branch.

```

git push --set-upstream origin master

```

(Go back into GitHub and see that the repository has been updated.)


> **Pushing local repo to GitHub after doing the above process at least once
First, commit all the changes. Then push all the changes to our remote origin**

```

git push origin

```


### ✅ Pull local repo from GitHub:
Git pull is used to pull all changes from a remote repository into the branch we are working on. 
It is a combination of fetch and merge. Use it to update your local Git.

```

 git pull origin

```

### ✅ Pull branch from GitHub
irst, check which branches we have and where are we working at the moment by ‘git branch’ command. 
Since we do not have the new branch on out local Git which is to be pulled from the Github. 
So, to see all local and remote branches, use -

```

git branch -a

```


### ✅  Push branch to GitHub
> First, create a new local branch which we will be pushing to Github. 
Enter the command as,

```

git checkout -b <branch name>

```

> Then, Commit all the uncommitted changes for all the files in this branch using

```

git commit -a -m “<Message>”

```

> **Now, push this branch from our local repo to GitHub using**


```

git push origin <branch name>

```


### ✅ Git clone from GitHub
We can clone a forked repo from Github on our local repo. A clone is a full copy of a repository, 
including all logging and versions of files. 
Move back to the original repository, and click the green "Code" button to get the URL to clone. 
Copy the URL.

Now, enter the following command to clone the
copied repo onto your local machine -


```

git clone <copied URL>

```


> **To specify a specific folder to clone to**
add the name of the folder after the repository URL, like this -

```

git clone <copied URL> <folder name>

```


<br>

___________________________________________________________________________________

<br>


## ⬛ Git Branching: {#branch}
Branch is a new/separate version of the main repository. Branches allow you to work on different parts of a project without
    impacting the main branch. 
 When the work is complete, a branch can be merged with the main project.
We can even switch between branches and work on different projects 
    without them interfering with each other.



### ✅ Making a new Git Branch:

```

git branch <name of branch>

```


### ✅ Checking all available Branches:

```

git branch

```



### ✅ Switching to other Branches:

```

git checkout <branch name>

```


### ✅ Making a new branch and directly switching to it:

```

git checkout -b <branch name>

```


### ✅ Deleting a Branch :

```

git branch -d <branch name>

```


### ✅ Merging two Branches:
It’s preferred to change/switch to the master branch before any branch needs to be merged with it.


```

git merge <branch name>

```


***(This will merge the specified branch with our master branch)***


<br>

___________________________________________________________________________________

<br> 

## ⬛ Git Undo :
"Git undo" generally refers to reverting or correcting changes in Git. Here are some common scenarios and the corresponding commands to undo or correct changes in Git:

### ✅ Git Revert :
‘revert’ is the command we use when we want to take a previous commit 
and add it as a new commit, keeping the log intact. 
First thing, we need to find the point we want to return to. 
To do that, we need to go through the log. To avoid the very long log list, 
use the --oneline option which gives just one line per commit showing –

>  (i) The first seven characters of the commit hash

> (ii) The commit message



### ✅ Git Revert HEAD :
We revert the latest commit using ‘git revert HEAD’ (revert the latest
change and then commit). By adding the option --no-edit, we can skip the
commit message editor (getting the default revert message).

```

git revert HEAD --no-edit

```


### ✅ Git Reset :-
‘reset’ is the command we use when we want to move the repository
back to a previous commit, discarding any changes made after that commit.
First, get the seven characters of the commit hash from the log for the
commit that you want to go back for. Then we reset our repository back to
that specific commit using ‘git reset commithash’ (commithash being the first
7 characters of the commit hash we found in the log).


```

git reset <commithash>


```


### ✅ Git Undo Reset
Even though the commits are no longer showing up in the log, it is not
removed from Git. If we know the commit hash, we can reset to it using:

```

git reset <commithash>

```


### ✅ Git Amend :
- commit --amend is used to modify the most recent commit. 
- It combines changes in the staging environment with the latest commit, and creates a
    new commit. 
- This new commit replaces the latest commit entirely.
- One of the simplest things you can do with --amend is to change a commit message



```

 git commit --amend -m “<New Commit Message >

```

***(Using this, the previous commit is replaced with our amended one.)***





#### Git Amend Files :
Adding files with --amend works the same way as above. 
Just add them to the staging environment before committing.


<br>

___________________________________________________________________________________

<br> 

#### This is the end of a section, You can fork this repo if you find it helpful 
Thank you 🙏

Saroj

