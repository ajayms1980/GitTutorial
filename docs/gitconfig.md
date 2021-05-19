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

## Case Study

Ritika is a software developer and she works on  a project ( lets say MyWork) her laptop and manage her project's repistory on local system using git.She want to configure set up Author of the project with her name and email address so that when she commits the changes to the local repoistory then it records with her name and later she can push these changes to global repoistory.

## Solution

### Step 1 To Initialize git repository for MyProj project (Consider MyProj is a directory and all the files in this directory are project files).
            ```
           cd MyProject
            git init
            
            ```

### Step 2 Setup Author name and email on global level configuration
           - git config --global user.name ritika
           - git config --global user.name ritika@kmit.com

### Step 3 create a project file say myfile_1.txt under MyProj Folder
           - touch myfile_1.txt
           -            

