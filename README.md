# Git-Basics
Notes from which I learnt Git-Github

## Git - Version control System (Software)
Example: Bank account has statements which keep the track of all the transactions similarly the Git is a software that works as a history tracker for a project.

Why Git? - 1. Popular for tracking the history and colaboration
2. Open Source
3. Fast and Scalable

## Github - website that allows developers to store and manage their code using Git.
It is a platform for Git.

On Github there are reposetories in which we can upload our project's code.

There is a two step process when you make any changes in the Repository:
1. add (stage the changed files)
2. commit (entry in the statement - similar to taking a screenshot to keep the track of changes)

## First thing after downloadng the Git and Gitbash -
is confirguring git - it means that when we make any changes using Git what account it should reflect on Github.

Open gitbash check if it shows "~" which means that we are in our root directory and enter the following commands:
1. git config --global user.name "Username"
2. git config --global user.email "email address"
3. git config --list

There is an interesing key words "global" and "local" if you have only one git account and you are using to make all the changes use global for configuration otherwise use local which means that you are making changes to particular repo. or project using different account.

## Now let's learn about clone and statu:

There are two keywords to understand first:
1. Local: our laptop of PC
2. Remote: github

We need clone command to copy the remote repo. into our local (laptop):

git clone (URL - from the code section on Github)

Status command - shows the status of the file

git status (status of the file or files which we are working)

There are four type of status:
1. untracked - new file that git doesn't yet track (git does not know anything about this file)
2. modified - changed in the local and not added yet
3. staged - file is already to be commited (added files using add command but not commited yet)
4. unmodified - obviously unchaged

Now let's learn about Add and Commit

1. add - adds new or changed file in your working directory (local folder on your PC) to the git stating area.
   git add "file name" or git add .

2. commit - it is a record (screenshot) of the change (entry in the statement)
   git commit -m "message"

Important - When you commit something without any errors the message (your branch is ahead of 'origin/main' by 1 commit - It means that your laptop has modification to the files that has not been reflected on the github.

To do so we need to use the push command.

push - upload local repo. content to the remote repo.
  git push origin main

there is two keywords to understand here:
1. origin - you can understand it as a remote repo.
2. main - is the branch in the of the origin repo.

So far we have learned about working on the ongoing project (github already have folders (repo.) and branches we can clone them and work on it and push the modified version) - we will usually follow this process when working on the assignments as we have some code already written for us and we will add methods to it.

Now what if you are working on project on your computer and then decided to collaborate with the team by uploading the project on github. This is important to learn as mainly all the small level projects starts on local platform and then extended.

To do so we must learn about the inti command:

init - used to create a new git repo.

  git init
  git remote add origin "link" (to do this step first go to the github and create new repo name it the same as your folder in your laptop and then get the link from there and name the repo. origin - you can name something else but we usually use git push origin main so we will name the repo. origin)
  git remote -v (to verify remote) - if the push command gives you an error check you remote (name is origin or if something else try to push on that name or change the name by following step 2)
  git branch (to check the branch) - usually you will get confued in this step while submitting your assignment as there are two names main and master and we use the main in the push command so check the branch name using this command and change the name if needed)
  git branch -m main (to rename branch)
  git push origin main
  git push -u origin main (we can use -u if we do not want to type push origin main everytime if we are pushing all the content in the origin main but if this command does not work check your repo. and banch name)

About Branches - suppose we are working on a web development project and we have 3 teams team 1 working on the buttons, team 2 working on the nevigation and team 3 working on the content so they create branches from the project at certain point and start working on the tasks they are assigned without waiting for other teams to complete their task. For example, while working on the content team 3 does not need to wait for team 2 to complete the code for neviaration bar by creating a separate branch. 
  
Branch commands
  git branch (to check how many branches are there)
  git branch -M main (to rename branch)
  git checkout "branch name" (to nevigate)
  git checkout -b "branch name" (to create new branch)
  git branch -d "branch name" (to delete the branch)

If you see "compare and pull request" message on github - you have more than one branch

In that case you have an option to merge the branches - it means our team 1,2 and 3 have completed their task and we want to merge the branches to get all the code and contect togather.

There are two ways to merge the branches:
1. Through git
  git diff "branch name" - you should know which branch you are in and with which branch you want to compare the dfferences on your current branch.
  git merge "branch name" (to merge two branches) - there is a question might arise - what if both the files have different code in the same line which one git will override?


2. Using github
   in this case we create a pull request.
   pull request - it lets you tell others about the changes you have pushed to a branch in a repo. on github.

It is useful when there are so many merge happening between branches - in this case senior or project/product manager review your pull request (if there is no conflic into your pull reuqest - which means that you have not editied content in the same line and git has confusion deciding which one to override) and see what changes are you making and add comments if any modifications needed and then merge the pull reuqest so the code in your branch will be added to the main branch.

Now let's see the case when we have the merge conflict:

merge conflict is an event that takes place when git is unable to autometically resolve differences in code between two commits.

we follow the same process if we doing it through the git we can check the differences using git diff command and decide which change we want to keep. If we are doing it on the github then we can see the differences in the pull request and decide which one to approve.

## Now let's learn about undoing changes:

Case 1: staged changes - changes which are added but not commited 
  git reset "file name"
  git reset (for all files)

Case 2: commited changes - for one commit
  git reset HEAD~1

Case 3: commited changes - for many commits
  git reset "commit hash" - gonna take us to the commit with the hash code on github
  git reset --hard "commit hash" - it will change the code according to the commit has provided (code that we had before we had that particular commit)
  git log (to check all the commits and get the hash code for commit and type q to quit)



