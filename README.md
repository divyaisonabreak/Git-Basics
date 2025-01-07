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

We need clone command to copy the remote repo. into our local (laptop)

