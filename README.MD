# GIT
Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency.

### BASIC GIT WORK FLOW

* **git init** creates a new Git repository
* **git status** inspects the contents of the working directory and staging area
* **git add** adds files from the working directory to the staging area
* **git diff** shows the difference between the working directory and the staging area
* **git commit** permanently stores file changes from the staging area in the repository
* **git log** shows a list of all previous commits


![minipic](picture/gitworkflow.png)

###  First Exercise

1. Run **mkdir (repo name)**   &emsp;&emsp;  give repo name = famous
2. Run **cd famous**           &emsp;&emsp;     cd (change directory) 
3. Run **git init**            &emsp;&emsp;     to make git repo
4. Run  **touch people.txt**    &emsp;&emsp;    touch to make a file 
5. Run **ls** or **ls -a** **ls -l**    &emsp;&emsp;  see differences
6. Time to add some text to **people.txt** file [click here](mostknown.html) add just **ELON MUSK's** info 
7. There are several ways to open file via terminal (nano filename,gedit filename etc..) Lets use run **gedit filename**
8. Run **git status** &emsp;&emsp; check to what happens you might see with red color file name 
9. Run **git add people.txt**  then run **git status** you might see (new file:   people.txt ) in green color 
10. Run **git commit -m 'add Elon Musk info and first commit'**
11. Add another text [click here](mostknown.html.php) add just **Jeff Bezos** info.
12. Run **git diff** see the difference between working directory and staging area then add file to staging area
12. After git add, run **git commit -m 'add Jeff Bezos info and second commit'**
13. Run **git log**  viewing the commit history,  extra and better command(**git log --oneline**).If your cursor gets stuck in “git log” mode in the terminal, press “**q**” on your keyboard to escape.
14. Run **history** command to show you all of the last commands that have been recently used.
* Well done FIRST exercise is done. Are you ready for next exercises?? :)))


### BACKTRACK  IN GIT

When working on a Git project, sometimes we make changes that we want to get rid of. We can absolutely do it with Git.

Before we dive into backtracking flow we need to know what HEAD is.In Git, the commit you are currently on is known as the **HEAD** commit. In other words HEAD is a reference to the last commit in the currently check-out branch.
To see HEAD commit run **git show HEAD**.


* **git checkout HEAD** filename,  will restore the file in your working directory to look exactly as it did when you last made a commit.
* **git reset HEAD** filename, this command resets the file in the staging area to be the same as the **HEAD** commit. It does not discard file changes from the working directory.
* **git reset** commit_SHA, resets to a previous commit in your commit history.This command works by using the first 7 characters of the SHA of a previous commit( use **git log** to reach all commits).