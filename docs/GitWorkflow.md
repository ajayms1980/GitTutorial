## Git -Saving Changes

The commands: git init git add, git status, and git commit are all used in combination to save a snapshot of a Git project's current state.

#### .gitignore
This file contains the files which you donot want to track in the git repository. It can have file name or we can use the wild characters (*.log)

### commands

git add git commit git diff git stash .gitignore

#### git init
This command is used to initialize a directory with git repoistory
   git init

#### git status
This command is used to check the status of local git repoistory.Untracked files by default shows as in RED color , Stage files in GREEN Color. If the all the files of git repoistory are commited then it is show Nothing to commit message

   git status

#### git add
The git add command adds a change in the working directory to the staging area. It tells Git that you want to include updates to a particular file in the next commit. However, git add doesn't really affect the repository in any significant way—changes are not actually recorded until you run git commit.

Instead of committing all of the changes you've made since the last commit, the stage lets you group related changes into highly focused snapshots before actually committing it to the project history. This means you can make all sorts of edits to unrelated files, then go back and split them up into logical commits by adding related changes to the <b><u>stage</u></b> and commit them piece-by-piece. 

     git add <<file name>>
     # To add all the changes to stage area
     git add .       
     # To change the file status stage to untrack
     git rm --cached <file>..." to unstage
     or
     git reset <<filename>>
#### git commit
This git command is used to commit the changes into git repositry ( It commits the changes of all the stage area files ). -m option is mandatory to use with commit to set a message for each commit

    git commit -m "some message "

#### git log
This command is used to check the history of all the commits for a particular local git repository.
   
     git log
     git log --oneline

#### git diff
This command is used to find the difference between 2 commits of a git repository.

    git diff <<commit 1>> <<commit 2>>

#### git reset
This command is used to reset the git commits. for example if we have 2 commits and HEAD is at 2nd commit and we want to undo the last commit( we can only remove the recent continuous commit not a specific commit)

    git reset HEAD~1
    # mixed (default mode) is used to reset the index and the commited files will be in untracked stage (Working area)
    git reset --mixed HEAD~1
    # soft mode is used to reset the files in Stage area
    git reset --soft HEAD~1
    # hard mode (DANGER COMMAND) is used to remove the changes from untracked area)
    git reset --hard HEAD~1
    
#### git revert
 This command is used to revert the changes of a commit ( any commit id not neccesarily recent one) and it will not tempered the history.
 
     git revert <<commit id>>

#### git stash
Stashing takes the dirty state of your working directory — that is, your modified tracked files and staged changes — and saves it on a stack of unfinished changes that you can reapply at any time (even on a different branch)
  
     # modify the file (Not commited)
          git stash save "some message"
     #list all the stash changes
         git stash list
     #revert the change in git repo
         git stash apply  stash@{0}
     # revert and remove it from git list
         git stash pop
     #drop the stash changes 
          git stash drop  stash@{0}
     #drop all stash changes
          git stash clear
     
