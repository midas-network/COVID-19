# Contributing to the MIDAS 2019 Wuhan coronavirus repo 
  
## GitHub
### Create GitHub account & fork midasnetwork/Wuhan-Cov  
1. Create a GitHub account and log in through: https://github.com
2. Go to CDC Zika Repo: https://github.com/midasnetwork/Wuhan-Cov 
3. On the upper right corner, click on **Fork**.  
   **You have now forked the MIDAS 2019 Wuhan coronavirus repo into your github account.**  
  
  ***
  
### Contributing to the nCoV Project from GitHub  
1. Creating New Files in YOUR Fork  
     + To create a sub-directory within the repo, you must Create a New File and add the sub-directory name before the file name:  
     + i.e. /SUB-DIR/FILE-NAME.ext, OR
2. Uploading Files to YOUR Fork.  
     + upload local files to your created sub-directory by clicking the "Upload Files" button.  
     + uploaded files can be edited within github by clicking on each file and the edit button.
3. Then "Commit" all changes to your fork.
4. To merge changes into the original repo, a *Pull Request* must be initiated by you from your fork.  
     + This request will be reviewed and merged by owner.  
     + Note: All changes must be made from YOUR repo fork.  
     + Click on the green **Pull Request** button.  
     + Owners of the cdc zika repo will verify and merge your changes to the original repo
  
  ***     
       
## Git  
### Configure Git locally (using Windows)  
  Git must be installed on your computer.  
  You must have a GitHub account active and the forked zika repo in your account.  
  
1. Open Git Bash  
2. Change directory to where you will clone your repo to configure Git:  
3. Configure as follows (*YOUR_USERNAME* and *YOUR_EMAIL* must match those on your GitHub account):  
     + `git config --global user.name "YOUR_USERNAME"`  
     + `git config --global user.email "YOUR_EMAIL"`  
     + `git config --global credential.helper wincred` <--for https credentials  
4. Clone your fork locally:  
     + `git clone https://github.com/YOUR_USERNAME/zika.git` <-- you are cloning *your* fork.  
     + Within your current directory, a new directory will be created locally. This is your cloned fork.  
  
  ***
  
### Contributing to the nCoV Project from Git  
  New information can be added to your *local repo* and then uploaded to *your* github fork as follows:  
  **Please, update and sync your local clone to the upstream before pushing any changes (see below).**   
  
1. Open Git Bash
2. Change current working directory to local repo.
3. Once you have finished editing your files, save them in your local repo.
4. Before staging, verify which files are ready to be staged:  
     + `git status`
5. Choose files to stage:  
     + `git add file1 file 2` <-- this will add file 1 and file 2 to your local repo.
6. Commit the staged files in your local repo:  
     + `git commit -m "adding file 1 anf file 2"` <- make the message short  
     + This will prepare the staged files to be pushed into your local repo.
7. Check to see what you are commiting:  
     + `git status`  
     + If you want to remove the commit: `git reset --soft HEAD~1`  
     + If you want to unstage files & start again: `git reset`
8. Otherwise, push the commited files to your github fork:  
     + `git push`  
     + Your GitHub fork should now have the commited files.
9. You can now issue a *Pull Request* from your GitHub fork.
  
  ***
  
### Updating your local clone and GitHub fork: Syncing
  To update your clone, you must sync your fork by fetching the updated MIDAS repo to update your local clone and then pushing the updated clone to your GitHub fork:  
  
1. Open Git Bash
2. Change directory to your local fork:  
     + `git remote -v` <--your URL for will show as "original"  
     + `git remote add upstream https://github.com/midas-network/Wuhan-CoV.git` <--the original repo will show as "upstream"  
3. Fetch updated original repo from upstream. This will fetch all updated info from original repo:  
     + `git fetch upstream`  
4. Pull updated repo version to local fork. This will update your LOCAL fork:  
     + `git pull upstream master`  
5. Upload updated repo to your github repo. This will update your GITHUB fork from your local fork:  
     + `git push`  
     + Github will ask for your credentials to log in  
     + You can update your local and github fork weekly or as needed  
  
  ***
  
 *Instructions adapted from Michael Johansson's zika repository:* [![DOI](https://zenodo.org/badge/51947303.svg)](https://zenodo.org/badge/latestdoi/51947303) 
