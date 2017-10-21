# GitHub Tutorial

_by Mr. Matos (The Elijah one)_

---
## Git vs. GitHub

**Git:** Git is all about snapshots. Git allows users to monitor their progress through the command line, where commands will be given. Think of git as a photo op where you can add, take snapshots of and remove people (in this case content) at will. 

**Github:** Github is entirely reliant on git. Github is the cloud-based storage platform which can store various forms of code. 



---
## Initial Setup
* To sign up for github, first go to [the github website](https://github.com/), then follow all the steps necessary to create a profile (if you are an HSTAT student use your HSTAT email). Once you've finished the sign up process check your inbox for a confirmation email. After that, you're ready to git to it! 
* Once you've successfully created a github profile, you are ready to create an SSH key
    1. Click on your profile icon and scroll to the settings tab. 

    2. On the left sidebar, you'll find a section called SSH and GPG. Choose to create a new SSH key called "cloud 9". 
    
    3. Go to cloud 9 (you should have created a cloud 9 account first). After creating the new SSH key, click on the gear icon in the top-right corner of your cloud 9. 
    
    4. On the SSH keys tab, there is a 2nd SSH key (it should begin with ssh-rsa). Copy that and then paste it into github. 
    
    



---
## Repository Setup
* Now that the preliminary stuff is out of the way, you're ready to start working in the command line. Start by creating a repo (**`mkdir`** and _whatever you want to name the repo_). 
* Change directories (**`cd`**) into the repo and type **`git init`**. DO NOT  GIT INIT IN YOUR WORKSPACE (but if you do, there's a fix). 
* Create a file using **`touch`** alongside your name for the file (for example, touch _apples_ will create a file called _apples_). 
* Now, you're ready to git add. Typing git add adds at least one file to the staging area from the working directory, preparing it for a commit. You can do this a few ways:
    * You can git type **`git add`** and _include the name_ of the specific file that you want to add. 
    * You can type **`git add .`** to add all files within the working directory that have changes to the staging area. 
    * You can type **`git add --all`** to add all files in the working directory, even if they have been deleted to the staging area. 
* Next up is git commit. Git commit is the stage in which the snapshot function of git is activated. To git commit successfully, you'll need to type **`git commit -m`** along with a _commit message_ wrapped in quotes. 
* Finally, you're ready to push to your remote repository. There are two important steps to this:
    * Typing **`git remote add origin URL`** is going to establish the bridge between your local (c9) and remote (github). 
    * Typing **`git push -u origin master`** ensures that your remote is your default push option. This will make sending code to github a much smoother process as you'll be able to use the **`git push`** command on its own in the future. 
* MAJOR KEY: Remember to use **`git status`**  constantly! The git status command will let you know what's been modified (in red text), what's been committed (green text) and when there are no new commits to be made. 




---
## Workflow & Commands



---
## Rolling Back Changes