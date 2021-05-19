# Git Configuration 
Git configuration is the convient way to setup global or local configuration for git project.
## Global configuration <br />
Global configuration file is common for all git project which resides on same local system.If there is no configration defined on local level then global configuration is refered for git project settings.A file .gitconfig get created under user folder. 

#### Example :- To Create a user name and email in global configuration file.
- git config --global user.name kmit
- git config --local user.email kmitsolutionservices@gmail.com

With above command a new section will be created in .gitconfig file

[user]

  name = kmit

  email = kmitsolutionservices@gmail.com

## Case Study 1 -For Global Configuration

Ritika is a software developer and she works on  a project ( lets say MyProj) her laptop and manage her project's repistory  using git.She wants to  set up Author of the project with her name and email address so that when she commits the changes to the local repoistory then it records with her name and later she can push these changes to global repoistory.

### Solution

#### Step 1 To Initialize git repository for MyProj project (Consider MyProj is a directory and all the files in this directory are project files).
            
           cd MyProj
           git init


#### Step 2 Setup Author name and email on global level configuration(Check .gitconfig file for your reference after running below commands)
           git config --global user.name ritika
           git config --global user.name ritika@kmit.com

#### Step 3 create a project file say myfile_1.txt under MyProj Folder
           touch myfile_1.txt
           
#### Step 4 Check the git status of the file ( it should be untracked file)
           git status
           
 #### Step 5 Commit the changes to local git repository.
           git add myfile_1.txt
           git commit
           
 #### Step 6 Check log history of git and it should show the Author as "kmit" and email as "kmitsolutionservices@gmail.com"
           git log

## Case Study 2 - For Local Configuration 

Now Ritika has to do the development on developement server where multiple developers works on their projects.In this case Ritika does not want to use git Global configuration instead of that she wants to set the author name and email address in local configuration file of project so that if she push the changes to GitHub Repoistory then it should be recorded with her name.

### Solution

#### Step 1 To Initialize git repository for LocalConfigProj project (Consider LocalConfigProj is a directory and all the files in this directory are project files).
            
           cd LocalConfigProj
           git init
           
#### Step 2 Setup Author name and email on local level configuration(Check .git/config file for your reference after running below command)
           git config --local user.name dev_ritika
           git config --global user.name dev_ritika@kmit.com

#### Step 3 create a project file say myfile_1.txt under LocalConfigProj Folder
           touch myfile_1.txt
           
#### Step 4 Check the git status of the file ( it should be untracked file)
           git status
           
 #### Step 5 Commit the changes to local git repository.
           git add myfile_1.txt
           git commit
           
 #### Step 6 Check log history of git and it should show the Author as "dev_ritika" and email as "dev_ritika@kmit.com"
           git log
