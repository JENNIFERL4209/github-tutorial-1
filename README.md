# GitHub Tutorial

_By : Johnson Wu_

---
## Git vs. GitHub
* #### Git
    * version control
    * keep "snapshots" of codes
    * does not require github
* #### Github
    * store code in the cloud or online
    * visually track changes
    * requires git  

---
## Initial Setup
1. _Create Github Account_
    1. Go to [Github](www.github.com)
    2. Click on _"Sign Up"_ on top right
    3. Complete all steps in creating your account
    4. After you've successfully created your Github account, explore Github and get familiar with it
2. Create a SSH key between your Github and c9
    1. In Github, click on your profile icon on the top right
    2. Click on _"Settings"_
    3. On the leftside bar click on _"SSH and GPG keys"_
    4. Click on _"New SSH key"_
    5. For the title put _"cloud9"_
    6. Open a new tab and go to your [c9](https://c9.io/) account
    7. After you've logged on to your c9 account click on the gear icon on the top right
    8. Click on _"SSH Keys"_ then copy the **second SSH key** to your Github and press _"Add SSH key"_
    9. Finally go back to your cloud9 and open your "github-learning" IDE then type in `ssh -T git@github.com`. You should see `Hi <your username>! You've successfully authenticated, but GitHub does not provide shell access._`. If not, you must have done something wrong or there might be an error so please ask for **help**.

---
## Repository Setup
Now that you've created a github account and SSH key let's create your first repository!
1. Make a new directory called `first-repo` by typing `mkdir <name>`
2. `cd` into `first-repo`
3. Initialize git in `first-repo` by typing in `git init`
4. Create `README.md` file by typing `touch <filename>`
5. Open `README.md` file and type in anything you like
6. Save the file then add the file to the staging area using `git add <filename>`
7. Commit your file using `git commit -m "<insert message>"`
8. Open a new tab and go to your Github account 
9. Once you've logged into Github account click on the + icon the top right then click on "New repository". _**If it ask to verify your email, verify it**_.
10. For the repository name type in "first-repo" (_**remember the repository name on your github must match your repository name on c9**_) then click on "Create repository"
11. Now you should be somewhere that says "Quick setup - if you've this kind of thing before" _**make sure you have SSH selected**_
12. Copy and paste the line of code that says `git add remote origin URL` to your c9 first then copy and paste the line of code that says `git push -u origin master` to your c9
13. To check your remote in your c9 use `git remote -v`
14. To delete the remote use `git remote rm origin`

---
## Workflow & Commands
Now that you've created your Github account and created your first repository, here are some tips when working with github.
1. always use `git status` to check the status of your work because ... 
2. everytime you've made edits to your work add it to the staging area using `git add filname` then commit it using `git commit -m "message"` then `git push` it to your remote in github.  
_why do you have to git push_
---
## Rolling Back Changes
If you've accidentally edited your work, add a file, commit a file, or push your work here's how you undo them:
* To undo an edit use `git checkout -- filename`. This will change your work back to your previous commit
* To undo an add use `git reset HEAD filename`
* To undo a commit use `git reset --soft HEAD~1`
* To undo a commit use `git revert` _difference?_
* To undo a commit and an add use `git reset HEAD~1` _why do we need this and what is the purpose?_
* To undo an edit, an add, and a commit use `git reset --hard HEAD~1`
























