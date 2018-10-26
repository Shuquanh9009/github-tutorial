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
6. Then copy everything inside the first box,it will be under the title "Connect to your server using SSH" it will start off with "ssh-rsa"
7. Then go back to your github SSH key tab and paste it into the empty box  
8.  In your c9 terminal, type in ssh -T git@github.com
8. You should then see "Hi ! You've successfully authenticated, but GitHub does not provide shell access._" in your c9, after inputting "ssh -T git@github.com"  
- The good thing about using SSH key instead of HTTS is that you don't have to type in your username and password everytime you want to push your commits to your remote  (_This is only useful is your are working on your own computer and IDE, otherwise, using HTTS will be a bteer choice because you can protect your files from any unexpected changes made by someone else who's using the same computer_)
    


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
- When you see a red titled file, it means that you have made changed to it and din't add it to the staging area, which is a good time to use `git add .` or `git add --all`
- When you see a green titled file, it means that you have add it all of your file changes into the staging area and is ready to be commited into the repository

`git add .` - a command that adds your file to staging area from the working directory

`git add --all` - a command that adds all the files changes you made into the staging area, including the deleted ones.  

- This is useful when it comes to **renaming folders** because it will bring back all the files under the old folder into the new folder

`git commit -m `- a command to save your edits with a message you make to remember the edits you made  
- Your commit message should be meaningful/relates to the changes you had just made, so you know what you did when you look back at your work (_it should be in present tense_)

`git push` - a command to push your files up to your remote which is to Github.



---
## Rolling Back Changes
- So we all amde mistakes in our life, especially when you are not paying attention to your work. So here are some of the most common commands you could use if you happen to be one of those careless person who want to undo the mistakes they made in their file
- If the commands below can't help you to solve your problem, it is always good to ask the internet by searching on google (_99.99% of the time there's an answer sitting somewhere in the web waiting for you, is ok to google things, that's how we learn_)  

`git checkout -- filename`: Undo the changes in the working directory  
Use this commad when you want to discard the edit/changes you just made in your working directory

`git reset HEAD filename`: Unstage a specific file you had just added from staging area  

Use this command when you staged more more files than you wanted to be commit into the staging area

`git reset --soft HEAD~1`: Undo the commit you had just committed  

Use this command to undo the commit you had just made recently, it should be the very last commit you done

`git reset --hard HEAD~1`: Undo the commit you had just committed, and discard those changes in the file  

Use this command to undo the last commit you had just committed and it discard all the edits/changes you had made in that file that was undone

`git revert SHA` : Undo a push with the SHA or commit number you could find through using ` git log` 

Use this command to undo a push by going back into a commit version that was before you had pushed the commit that you want to undo at the moment

## Error Handling
- If you have accidentally initialize git (`git init`) under the wrong directory, you could simply uninitialize this by typing in this command `rm -rf .git`
    - The way you know if your directory/folder is initialized or not is by checking if there are (master) next to the folder name in the terminal
- If you want to delete a repositiory completely (local & remote):  
1- Go to your [Github account repositiory section](https://github.com/Shuquanh9009?tab=repositories)  
2- CLick on the repository name you want to delete completely  
3- Click on the gear setting icon inside of your repositiory, _located on the mid-top slightly to the right from the center_   
4- Scroll all the way down to the bottom, under **Danger Zone**, the very last option (Delete this repository), click on it and read the warnings  
5- Lastly you want to type in the whole repository's name in order to delete that repository

