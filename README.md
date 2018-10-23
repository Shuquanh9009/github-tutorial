# GitHub Tutorial

_by Shuquan Huang_

---
## Git vs. GitHub
- Git is a version-control system that keeps a snapshot of your code, in other word, it helps you to keep track of your coding progress. _(It doesn't require Github to run it)_ 
-  Github, which stores your files into a cloud, where you could share your work to the world, so others could see it and add on it. _(It requires Git!)_


---
## Initial Setup
### Setting up a Github Account
1. [Go to Github and singup for an account](https://github.com/join?source=header)    
2. Chose a username of your preference (_If you are a HSTAT student, put in your HSTAT email but take out      @hstat.org_) and make sure is not taken by checking for a green check sign on the right.  
3. Then put in your email address. (_If you are a HSTAT student, use your HSTAT email_)  
4. Put in your personal password _(Make sure to have something is easy for you to remember)_  
5. Select the **unlimited public repositories for free plan**, unless you want to have the private repositories for $7/month.  
6. Last step will be tayloring your experience by check all boxes that applies to you.
#### After you have finished signing up your account:
1. Go to setting  
2. Click on SSH and GPG keys  
3. Afer you clicked on the SSH and GPG key tab, you will then click on the green **New SSH Key**
4. Then go to your cloud9 home page and click on the top right gear icon
5. Then click on the SSH key tab on the left side bar, or [click here](https://c9.io/account/ssh)
6. Then copy everything inside the first box, like below
7. Then go back to your github SSH key tab and paste it into the empty box 
    


---
## Repository Setup
1. Go to your [github account](https://github.com/)  
2. Click on the (+) symbol on the top right corner  
3. Click on **New Repository** 
4. Under the Repository Name box, type in the name you want for this repository  
5. Then you could give a description of your new repositiory that you are making _(is optional)_  
6. Then click on the green create repositiory on the bottom
7. Then you will be direct to a set-up page for your repositiory
8. 


---
## Workflow & Commands
`git status`- a command to check the status of your files, whether if it was added, modified, deleted, commited and etc.  
`git add .`


---
## Rolling Back Changes
`git checkout -- filename`: Undo the changes in the file  
`git reset HEAD filename`: Unstage the file you had just added from staging area  
`git reset --soft HEAD~1`: Undo the commit you had just commited  
`git revert SHA` : 
