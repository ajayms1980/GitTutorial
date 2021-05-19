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

Ritika is a software developer and she works on her laptop and manage her project's repistory on local system using git.She want to configure set up Author of the project with her name and email as her email address. When she commits the changes to the local repoistory then it records with her name.


