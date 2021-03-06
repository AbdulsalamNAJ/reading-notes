![git](https://user-images.githubusercontent.com/83532131/116826049-c1d1d680-ab9a-11eb-89aa-e64ca7c1d412.png)

# What is Git and how to use it?
Git is a sofware used for version control system. Git tracks the changes you make to files, so you have a record of what has been done, and you can revert to specific versions should you ever need to. Git also makes collaboration easier, allowing changes by multiple people to all be merged into one.

## Why a Version Control System like Git is needed?
A version control system allows developers to revert and go back to an older version of the code.
Real life projects generally have multiple developers working in parallel. So a version control system like Git is needed to ensure there are no code conflicts between the developers

## Download git

You can install Git for Linux, Mac and windows:
https://git-scm.com/book/en/v2/Getting-Started-Installing-Git

## Create your local Git repository

In your computer, create a folder for your project such as git-demo.

Go into your project folder and add a local Git repository to the project using these commands:

`cd git-demo  
git init`

## Staging and Committing the code

Committing is the process in which the code is added to the local repository. Before committing the code, it has to be in the staging area. The staging area is  to keep track of all the files which are to be committed.

Any file which is not added to the staging area will not be committed. This gives the developer control over which files need to be committed.

## Staging
![image](https://i.stack.imgur.com/zLTpo.png)

Use the following command for staging the file:

`git add demo.txt`

In case you want to add multiple files you can use:

`git add file1 file2 file3`

If you want to add all the files inside your project folder to the staging area, use the following command:

`git add .`

Use this carefully since it adds all the files and folders in your project to the staging area.

## Committing

Use the following command to commit the file:

`git commit -m "Initial Commit"`

Now modify the demo.txt file and add the following snippet:

Initial Content Adding more Content

## Status

Use git status to find out information regarding what files are modified and what files are there in the staging area ??? it shows other information, which we can ignore for now.

Use the following command to see the status:

`git status`

The status shows that demo.txt is modified and is not yet in the staging area.

Now let us add demo.txt to the staging area and commit it using the following commands:

`git add demo.txt git commit -m "demo.txt file is modified"`

## Log

Use git log to print out all the commits which have been done up until now.

The command used for this is:
`git log`

The log shows the author of each commit, the date of the commit, and the commit message.

## Branches

![image](https://www.nobledesktop.com/image/gitresources/git-branches-merge.png)

Until now we have not created any branch in Git. By default, Git go into the master branch.

## What is a branch?

A branch is nothing but a pointer to the latest commit in the Git repository. So currently our master branch is a pointer to the second commit ???demo.txt file is modified???.

## Why are multiple branches needed?

Multiple branches are needed to support multiple parallel developments. Refer the image below to see how branches work.

Commit 1 and commit 2 were done in the master branch. After commit 2 a new Branch called as ???Test??? is created, and commit 3 and commit 4 are added to the test branch.

Different commit 3 and commit 4 are added to the master branch. Here we can see that after Commit 2, two parallel developments are being done in 2 separate branches.

The Test Branch and the Master Branch have diverged here and have different code ??? the code from Test Branch can be merged with the Master branch using git merge. This will be covered later.

## Create a New Branch in Local

Create a new branch called test using the following command:

`git branch test`

This command creates the test branch.

We are still in the context of the master branch. In order to switch to the test branch. use the following command:

`git checkout test`

Now we are in the test branch.

You can list out all the branches in local using the following command:

`git branch`

Do Some Commits in the New Branch

Modify demo.txt by adding the following snippet:

Initial Content Adding more Content Adding some Content from test Branch

Now stage and commit using the following commands:

`git add demo.txt git commit -m "Test Branch Commit"`

This commit was done in the Test Branch, and now Test Branch is ahead of Master Branch by 1 commit ??? as the test branch also includes the 2 commits from the master branch.

You can verify the commit history in Test Branch using:

`git log`

## Merging

![image](https://cdn-images-1.medium.com/max/868/1*g48HJkKNsZwNlWEM6Z82ig.jpeg)

Currently, Test Branch is ahead of the Master by 1 commit. Let???s say that now we want all the code in the Test Branch to be brought back to the Master Branch. This is where git merge is very useful.

In order to merge the code from the test branch into the master branch, follow these steps:

First go back to the master branch:

`git checkout master`

Then run the merge command:

`git merge test`

After running these 2 commands, the merge should be successful. In this example, there are no conflicts.

But in real projects, there will be conflicts when a merge is being done. Resolving the conflict is something which comes with experience, so as you work more with Git you will be able to get the hang of resolving conflicts.

Run git log now and you will notice that the master also has 3 commits.
The Remote Git Repository

Until now, we have been working only in the local repository. Each developer will work in their local repository but eventually, they will push the code into a remote repository. Once the code is in the remote repository, other developers can see and modify that code.
