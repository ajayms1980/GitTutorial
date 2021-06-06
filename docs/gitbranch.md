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
    
## Git Rebase 
In Git, the rebase command integrates changes from one branch into another. It is an alternative to the better known "merge" command. Most visibly, rebase differs from merge by rewriting the commit history in order to produce a straight, linear succession of commits.

   
       git init # initialize the repoistory
       # create a file m1 and m2 in master branch and commit it
       touch m1 
       git add m1
       git commit -m "m1 is added"
       touch m2
       git add m2
       git commit -m "m2 is added"
       # Create another branch(feature) from master branch and add a new file f1
       git branch feature
       git checkout feature
       touch f1
       git add f1
       git commit -m "f1 is added"
       git log --oneline
       # create a new commit m3 in master branch a
       git checkout master
       touch m3
       git add m3
       git commit -m "m3 is added"
       git log --oneline
       # merge the changes into feature branch using rebase command and check the log entries - master commit graph is seprate from feature commit graph
       git checkout feature
       git rebase master
       git log --oneline

## Git Merge Conflict
Conflicts generally arise when two people have changed the same lines in a file, or if one developer deleted a file while another developer was modifying it. In these cases, Git cannot automatically determine what is correct. Conflicts only affect the developer conducting the merge, the rest of the team is unaware of the conflict. Git will mark the file as being conflicted and halt the merging process. It is then the developers' responsibility to resolve the conflict.
     
    # initialize the local git repo and create a file in master branch
    git init
    touch main.py
    git add main.py
    git commit -m "main branch created the file"
    # Create 2 branches with master and modify same file(main.py) and try to merge in master branch it will raise the merge conflict
    git branch feature1
    git branch feature2
    git checkout feature1
    echo " line is added by feature1 branch" >> main.py
    cat main.py
    git add main.py
    git commit -m " feature1 has modified main.py file"
    git checkout feature2
    echo "line is added by feature2 branch" >> main.py
    cat main.py
    git add main.py
    git commit -m "feature2 has modified main.py file"
    git checkout master
    git merge feature1
    git merge feature2 # Here merge conflict will occur
    git mergetool  # use this to solve the merge conflict

<img src="https://github.com/kmitsolution/GitTutorial/blob/gh-pages/Images/mergeConflict.PNG" width="500" height="300" />  


