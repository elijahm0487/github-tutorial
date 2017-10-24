# GitHub Tutorial

_by Mr. Matos (The Elijah one)_

---
## Git vs. GitHub

**Git:** Git is all about snapshots. Git allows users to monitor their progress through the command line, where commands will be given. Think of git as a photo op where you can add, take snapshots of and remove people (in this case content) at will. 

**GitHub:** GitHub is entirely reliant on git. GitHub is the cloud-based storage platform which can store various forms of code. 



---
## Initial Setup
* To sign up for GitHub, first go to [the GitHub website](https://github.com/), then follow all the steps necessary to create a profile (if you are an HSTAT student use your HSTAT email). Once you've finished the sign-up process, check your inbox for a confirmation email. After that, you're ready to git to it! 
* Once you've successfully created a GitHub profile, you are prepared to create an SSH key
    1. Click on your profile icon and scroll to the settings tab. 

    2. On the left sidebar, you'll find a section called SSH and GPG. Choose to create a new SSH key called "cloud 9". 
    
    3. Go to cloud 9 (you should have created a cloud 9 account first). After creating the new SSH key, click on the gear icon in the top-right corner of your cloud 9. 
    
    4. On the SSH keys tab, there is a 2nd SSH key (it should begin with ssh-rsa). Copy that and then paste it into GitHub. 
    
    



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
    * Typing **`git remote add origin URL`** is going to establish the bridge between your local (c9) and remote (GitHub). 
    * Typing **`git push -u origin master`** ensures that your remote is your default push option. This will make sending code to GitHub a much smoother process as you'll be able to use the **`git push`** command on its own in the future. 
* MAJOR KEY: Remember to use **`git status`**  constantly! The git status command will let you know what's been modified (in red text), what's been committed (green text) and when there are no new commits to be made. 




---
## Workflow & Commands
##### From here on out, you're going to be using the above commands  in sequence as your GitHub process. Anytime you make changes to a file within a repository, you'll want to use the commands. 
1. `Git add` - Adds at least one file with changes to the staging area, preparing that file for a commit. 
2. `git commit -m` Takes the snapshot and attaches a commit message as a description. Every commit message should be in present tense. 
3. `git push` - Sends your changes with the commit to your remote repository (GitHub). 
4. `git status` - Should constantly be used, letting you track modifications, commits and what's ready to be pushed. 


---
## Rolling Back Changes
##### At times, working in git can be frustrating. Coders oftentimes want to revert to previous versions of our files. There are a few places users can rollback their changes from. 
*  If a user's edits are very new and have not been added yet, they should use **`git checkout --`** and the name of their file to go back to the last version of the file. 
*  If a user has added a file to the staging area and wants to remove it, they should type **`git reset HEAD`** alongside the _name of their file_ to undo the add. 
*  Undoing commits has a bit more variation as opposed to other ways of undoing in git: 
    *  To revert back to the previous commit, users will want to use **`git reset --hard HEAD~1`**. This command will completely erase or nuke the current commit from the pus or commit stage, reverting the repository back to the previous commit.
    *  If you want to retain the version of your file that you committed so you can make some changes, you'll want to use **`git reset HEAD~1`**. Leaving the `hard` portion of the command off will revert back to the previous commit for editing purposes. 
    *  **`git reset --soft HEAD~1`** will allow users to retain their changes up to the adding stage. The previous two commands will bring users back to the editing stage, but this one will bring them to the point between adding and committing. 
    *  At times, users want to change or revert their commits. To do so, you'll need to use **`git revert`** along with the _commit code_ of the commit you want to revert to. Sounds difficult trying to find commit codes huh? Nope! Just use **`git log`**! Git log will give you the rundown of all the commits you've done with their corresponding commit codes. So to revert to a previous commit, type **`git revert`** with your preferred commit code. 




