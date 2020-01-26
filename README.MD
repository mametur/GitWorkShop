# GIT

Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency.

### BASIC GIT WORK FLOW 

* **git init** creates a new Git repository.This creates a new subdirectory named *.git* that contains all of your necessary repository files — a Git repository skeleton.
* **git status** inspects the contents of the working directory and staging area.
* **git add** adds files from the working directory to the staging area.
* **git diff** shows the difference between the working directory and the staging area.
* **git diff --staged** or **git diff --cached** compares your staged changes to your last commit.
* **git commit -m ''** permanently stores file changes from the staging area in the repository.
* **git commit -v** same the commend above(git commit -m)  you can see exactly what changes you’re committing more.  
* **git log** shows a list of all previous commits.
* **git log -p** You can also limit the number of log entries displayed, such as using -2 to show only the last two entries.(git log -p -2)


![minipic](picture/gitworkflow.png)

### First Exercise

1. Run **mkdir (repo name)**   &emsp;&emsp;  give repo name = famous
2. Run **cd famous**           &emsp;&emsp;     cd (change directory) 
3. Run **git init**            &emsp;&emsp;     to make git repo
4. Run  **touch people.txt**    &emsp;&emsp;    touch to make a file 
5. Run **ls** or **ls -a** **ls -l**    &emsp;&emsp;  see differences
6. Time to add some text to **people.txt** file [click here](mostknown.html) add just **Elon Musk's** info 
7. There are several ways to open file via terminal (nano filename,gedit filename etc..) Lets use run **gedit filename**
8. Run **git status** &emsp;&emsp; check to what happens you might see with red color file name 
9. Run **git add people.txt**  then run **git status** you might see (new file:   people.txt ) in green color 
10. Run **git commit -m 'add Elon Musk info and first commit'**
11. Add another text [click here](mostknown.html.php) add just **Jeff Bezos** info.
12. Run **git diff** see the difference between working directory and staging area then add file to staging area
13. After git add, run **git commit -m 'add Jeff Bezos info and second commit'**
14. Run **git log**  viewing the commit history,  extra and better command(**git log --oneline**).If your cursor gets stuck in “git log” mode in the terminal, press “**q**” on your keyboard to escape.
15. Run **history** command to show you all of the last commands that have been recently used.

* Well done FIRST exercise is done. Are you ready for next exercises?? :)))


### BACKTRACK  IN GIT

When working on a Git project, sometimes we make changes that we want to get rid of. We can absolutely do it with Git.

Before we dive into backtracking flow we need to know what HEAD is.In Git, the commit you are currently on is known as the **HEAD** commit. In other words HEAD is a reference to the last commit in the currently check-out branch.
To see HEAD commit run **git show HEAD**.


* **git checkout HEAD** or **git checkout** filename,  will restore the file in your working directory to look exactly as it did when you last made a commit. Be careful for this command.
* **git reset HEAD** filename, this command resets the file in the staging area to be the same as the **HEAD** commit. It does not discard file changes from the working directory.
* **git reset** commit_SHA, resets to a previous commit in your commit history.This command works by using the first 7 characters of the SHA of a previous commit( use **git log** to reach all commits).
* **git commit --amend** change the most recent commit message.
####  Second Exercise

1. Run **git show HEAD**.
2. Add text [click here](mostknown.html) add just **Mark Zuckerberg** info.
3. Run **git checkout HEAD people.txt** your working directory will be same as last commit.
4. Add text [click_here](mostknown.html) add just **Mark Zuckerberg** info than add to staging area(**git add poeple.txt**).
5. Run **git reset HEAD people.txt**, it will make unstage that file from the staging area but does not discard file changes from the working directory.
6. Run **git add people.txt** .
7. Run **git commit -m 'add Mark Zuckerberg's info'**.
8. Run **git log --oneline** to see whole commits history.
9.  **Now time to back previous commit you had made a mistake due to Mark Zuckerberg's info about Tim Cook (Lol:)) copy paste doesn't work every time)**.
10. Run **git reset  SHA-1 checksum**. 
11.  Run **git checkout HEAD people.txt**.
12. Run **git log** your last commit should shown as( **add Jeff Bezos info and second commit**).

* Well done Second exercise is done. You are learning so fast:)))

### BRANCHING
So far, We’ve worked in a one Git branch which is master. Branching means you diverge from the main line of development and continue to do work without messing with that main line.


![](picture/branch.png)

 The circles are commits, and together form the Git project’s commit history.
 New Branch is a different version of the Git project. It contains commits from Master but also has commits that Master does not have.


* **git branch** show branches and which branch you are on it.
* **git branch newBranchName** to create a new branch.

* **git checkout branchName** used to switch from one branch to another.
* **git merge branchName** Join two or more branches histories together (you will understand with exercises better).
* **git branch -d branchName** will delete the specified branch from your project.(- if you use 'D' instead of 'd' which force to delete branch)

#### Merge conflict
Be calm!! most developers are afraid of that part but once when you get it you will be able to solve it. To understanding merge conflict in good way do more exercises of course with me:))Basically Git doesn’t know which changes you want to keep.
