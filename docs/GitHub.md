## Git Hub
GitHub is a code hosting platform for version control and collaboration. It lets you and others work together on projects from anywhere.

We can Create the Global Repoistory in Github.It can be private ( not free of cost) or public Free of cost

### git push (Push files from local Repo to Remote Repo)

    #create a new repository on the command line 
    echo "# TestProj" >> README.md
    git init
    git add README.md
    git commit -m "first commit"   
    git remote add origin https://github.com/kmitsolution/TestProj.git
    git push -u origin main

### git fetch 
git fetch is the command that tells your local git to retrieve the latest meta-data info from the original (yet doesn't do any file transferring. It's more like just checking to see if there are any changes available).
it is mostly use with git merge command to pull the changes from remote Repoistory.

    git fetch
    git merge origin/master

### git pull
it pull the changes form remote repoistory to local repoistory. It is combination of git fetch and git merge command

     git pull origin master

### git clone
it clone the extact copy of the remote repoistory project to local system
    git clone https://github.com/kmitsolution/TestProj.git
     
