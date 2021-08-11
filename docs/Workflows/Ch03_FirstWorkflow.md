## Steps to Create the First Workflow
### Prerequisite
<ul>
 <li> You Should have Github Account so that you can create atleast a public repository </li>
 <li> Optionally You can have <a href="https://code.visualstudio.com/downlo ad"> Visual Studio Code </a> installed with YAML Extension (It's not mandatory but in my example I am using VSCode for Yaml Scripting) </li>
 <li> You Should have git software installed on your local system ( it is required because you need to perform the actions whenever push or pull happens to GitHub Repo) </li>
</ul>

## Follow below steps to create your first workflow
<ul>
  <li> Goto <a href="https://github.com"> GitHub </a> & Sign in with your GitHub Account</li>
  <li> Create a New Public Repoistory Called GitHubAction <b>( You can use any name)</b> with default Options Selction</li>  
  <li> Go back to your local system and Create a Folder Called MyProject <b>( You can use any name but in further steps I will use name MyProject)</b></li>
  <li> Navigate to your Folder MyProject and initialize git repo usint <i>git init</i> command ( it totally depends upon you how you initalize local Repository using Terminal or command prompt or visual studio code or git bash) </li>
  <li> Create folder .github/workflows <b>(It should be same name)</b> under MyProject folder ( means under MyProject first you need to create .github folder and then under .github folder you need to create workflows folder).</li>
  <li> Crate a Yaml file action.yaml <b>( You can use any name but the extension should be either .yaml or .yml)</b> with following code. <br /> </li>
    
    
    name: First Workflow

    on: [push]
    jobs:
      test:
        runs-on: ubuntu-latest
        steps:
         - name: simple echo command
           run: echo "Welcome To GitHub Action"
    
    
  <li> Commit the code in local Git Repository (use git add and git commit command) </li>
  <li> Add GitHubAction remote repo to MyProject local repo. (git remote add origin << Git Repo url >>) </li>
  <li> Push the code to GitHub by using below command <br />
    
     git push origin master
    
  </li>
  <li> Go To Github Repository GitHubAction and Click on Action Tab and you can see the WorkFlow get created. </li>
</ul>  
