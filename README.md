# GitHub Tutorial

by Mr. Matos (The Travis one)

---
## Git vs. GitHub
*Git* is a version control system, meaning that its a system that helps track the changes that you make to the files you have. It takes "snap-shots" of your code known as commits, which are saves of the changes you made. Git-hub is where you can post the files and changes of the code you saved. It makes the code "open sourced" which makes it freely available to anyone to access. *Git-hub*, being on the cloud, also makes it easier to code collaboratively with others. It visually tracks the changes that were made to the shared code in different commits (showing what was added in green and what was deleted in red). In summary, Git helps you save and track changes made to your code while Git-hub helps you save those changes on the cloud. Remember, Git can work without Git-hub, but Git-hub does need Git.



---
## Initial Setup
1. Well the first step to get git up and running (get git, thats funny) first we got to get on the [Git-Hub](https://github.com/) website
2. If you have an account on github already go and sign in, otherwise go ahead and make a Github acoount. Just click 'sign up', make your own username and password, choose free account, hit 'finish sign up' and bam, new github account. 
3. Now its a matter of getting your account linked with cloud9. SO, on the top-right of cloud 9 click on the gear icon and then the SSH keys tab where you will highlight and copy the 2nd SSH key which starts with ssh-rsa
4. Then on github, at the top right, click on the profile icon and go to settings
 on the left sidebar click on SSH and GPG and go to 'New SSH key'. Afterwards, you will then paste the ssh key from cloud9 into where it says "Key" and name the title whatever you want (preferably cloud 9)
`ssh -T git@github.com`
 And then BAM your done here



---
## Repository Setup
Its pretty simple to get one set up once you do it a couple times but heres the basic review 
1. first you wanna a make sure that you actually have a commit to push, remember *you can't push unless you have a new commit that you have not pushed*
2. then once you have a commit to push, go back to github and the top-right click the + button and hit New repository and input a name for it. Then hit "create repository"
3. You should see on your screen several snippits of text to copy, however, make sure that you click on ssh before copying anything. 
4. then copy where it says ```git remote add origin git@github.com:(your username)/(the name you created .git 
git push -u origin master``` and paste it to the command line while in the directory of your choosing.

Some helpful comands that can use through out git.  
`git init`- Initializes a repository into the current directory  
`rm -rf .git` Removes git from specified directory  
`remote` - creates a link between a external and internal repository  
`url` - the location of the remote repo. Could be HTTPS or SSH   
`Origin `- This is which remote we are pushing to   
`Master` - the “main” branch of our project  
`git remote -v`  
shows the remote of the repository (where the bridge is, where its sending the changes to)




---
## Workflow & Commands

`git add file` Adds the changes from file to the staging area, preparing it to be saved 
`git add .` adds all the new changes that were added inside the current directory into the staging area (not including changes of deleted stuff)
`git add --all` Adds all changes, including the stuff that were deleted to the staging area (prepares all changes to be saved )

`git commit -m "message"`  
Commits changes, or saves the changes. It must contain a message acting as a reminder or summary of changes.


`remote` - creates a link between a external and internal repository  

`origin` - this is the “nickname” for the remote repo name it whatever you want, “origin” is the standard.  

`Push` - we are sending our commits from our local repo to ur remote repo  
`- u -` means “upstream” This tells git to remember which remote repo & branch to push our changes to when we type git push in the future.  
`git push`
Pushes files into repository  
`git diff`
Reveals changes made 
`git log`  View changes
`q (while in git log)`
Backs out of git log  
`git checkout -- file`
Removes changes of the file/ reverts to an older version.  
`git reset HEAD file`
Resets the file to before you added it/unstages it.
`git remote -v`  
shows the remote of the repository (where the bridge is, where its sending the changes to)





---
## Rolling Back Changes
Rolling back changes depends on where you want to roll back to. But here are a couple of examples. 
* Made a edit that you didn't want to make? try `git checkout -- file` 
* Accidently added something to the staging area and want to go back and edit? type `git reset HEAD file`
