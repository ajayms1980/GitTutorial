# Git Branch 
Branching means you diverge from the main line of development and continue to do work without messing with that main line.

 <img src="https://github.com/kmitsolution/GitTutorial/blob/gh-pages/Images/gitbranch.PNG" width="500" height="200" /> <br />
 
## Commands

### List all the branch

     git branch

### Create a branch 

     git branch <<branch name>>
     git branch dev

### Switch to a branch

     git checkout <<branch name>>
     git checkout dev

### Find the current branch (The current branch should have * infront of current branch 
     git branch

    * dev
      master
### Delete a branch

     git checkout master
     git branch -D dev

     
## Git Merge

Git Merge command is used to integrate the changes of different branches into a single branch (mostly used for master branch).For example if we create a branch say dev branch from master branch (now dev branch will have a complete copy of all commited files of master branch) and in dev branch( git checkout dev command to swtich to dev branch) if we  add some new files or modify existing files then at last we need to merge these files to master branch because in most of the cases master branch is considered as the branch which has latest project code.

### Example

In below diagram there are 3 branches(master,Feature1 and Feature2) , after creation Feature1 branch, it has 2 commits(green color circles) and Feature2 branch also has 2 commits( blue color circles) and these changes are getting merge into master branch at merge commit, now master branch includes the commits of feature1 and feature2 branch ( you can check it with git log command)

<img src="https://github.com/kmitsolution/GitTutorial/blob/gh-pages/Images/merge.PNG" width="500" height="200" /> <br />

### command 

    git merge <branch_name>
    git merge dev
 
