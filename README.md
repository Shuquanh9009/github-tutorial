# GitHub Tutorial

_by Shuquan Huang_

---
## Git vs. GitHub
- Git is a version-control system that keeps a snapshot of your code, in other words, it helps you to keep track of your coding progress. _(It doesn't require Github to run it)_ 
- Github, which stores your files into a cloud, allows you to share your work to the world, so others could see it and add on to it. _(It requires Git!)_


---
## Initial Setup
### Setting up a Github Account
1. [Go to Github and singup for an account](https://github.com/join?source=header)    
2. Chose a username of your preference (_If you are a HSTAT student, put in your HSTAT email but take out      @hstat.org_) and make sure is not taken by checking for a green check sign on the right.  
3. Then put in your email address. (_If you are a HSTAT student, use your HSTAT email_)  
4. Put in your personal password _(Make sure to have something is easy for you to remember)_  
5. Select the **unlimited public repositories for free plan**, unless you want to have the private repositories for $7/month.  
6. Last step will be tailoring your experience by check all boxes that applies to you.
#### After you have finished signing up your account:
1. Go to settings  
2. Click on SSH and GPG keys  
3. After you clicked on the SSH and GPG key tab, you will then click on the green **New SSH Key**
4. Then go to your cloud9 home page and click on the top right gear icon
5. Then click on the SSH key tab on the left side bar, or [click here](https://c9.io/account/ssh)
6. Then copy everything inside the first box, like below
7. Then go back to your github SSH key tab and paste it into the empty box 
8. You should then see "Hi ! You've successfully authenticated, but GitHub does not provide shell access._" in your c9, after inputting "ssh -T git@github.com"
    


---
## Repository Setup
1. Go to your [github account](https://github.com/)  
2. Click on the (+) symbol on the top right corner  
3. Click on **New Repository** 
4. Under the Repository Name box, type in the name you want for this repository  
5. Then you could give a description of your new repositiory that you are making _(is optional)_  
6. Then click on the green create repositiory on the bottom
7. Then you will be direct to a set-up page for your repositiory
8. Go to cloud9 `mkdir` a new directory, have the same **exact** name as your new repository you had just created in your GitHub account
9. Then `cd` into the directory you just made
10. inside that directory, type in `git init` to initlize the repository 
11. Then type in `touch README.md` which creates the readme file
12. Then type in `git add README.md` to add everyhting in this file to your repository
13. Then do `git commit -m "first repo"`
14. Add your git remote, copy the whole line of line in your github repository page and paste it in your cloud9  
15. Lastly type in `git push -u origin master` to push it into your github.


---
## Workflow & Commands
`git status`- a command to check the status of your files, whether if it was added, modified, deleted, commited and etc.  
- Is always useful to use `git status` after every changes you made, files you commited, because if you did something wrong, `git status` will inform you what went wrong and have type of undo commands you could type in depending on your situation

`git add .` - a command that adds your file to staging area   

`git add --all` - a command that adds all the files changes you made into the staging area, including the deleted ones.  

- This is useful when it comes to **renaming folders** because it will bring back all the files under the old folder into the new folder

`git commit -m `- a command to save your edits with a message you make to remeber the edits you made  

`git push` - a command to push your files up to your remote which is to like Github.



---
## Rolling Back Changes
`git checkout -- filename`: Undo the changes in the file  

`git reset HEAD filename`: Unstage the file you had just added from staging area  

`git reset --soft HEAD~1`: Undo the commit you had just committed  

`git reset --hard HEAD~1`: Undo the commit you had just committed, and discard those changes in the file

`git revert SHA` : Undo a push with the SHA or commit number you could find through using ` git log` 
