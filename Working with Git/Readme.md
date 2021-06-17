#### Push all local workspace to Git ####

Step 1 - Create a new Repository on Github.

Step 2 - Add the Git Repository to VSC by running command below in VSC Terminal
    git remote add origin https://github.com/andy-pham-aussiecloudguru/myCloudFormation.git
    // to check if the origin has been added to VSC, run command: git remote
    // It will show the origin as output.

Step 3 - Push the local master into the Origin
    git push -u origin master

#### Timeline ####
From VSC Terminal, run: git log
Open Timeline tab

#### Pull Change from Git ####
Goto "Source Control" -> Select ... -> Pull

#### Clone Git Repository to VSC by using Git Clone GUI of VSC ####    
Step 1: Open blank VSC (Close all existing workspace)

Step2: Goto "Resource Control" -> Clone Repository -> Enter Clone URL from GitHub

#### Git Branches ####
Step1: Create new branch from VSC

Step2: Make changes in the local files and save

Step3: 