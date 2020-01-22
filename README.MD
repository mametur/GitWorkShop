# GIT
Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency.

### BASIC GIT WORK FLOW

* **git init** creates a new Git repository
* **git status** inspects the contents of the working directory and staging area
* **git add** adds files from the working directory to the staging area
* **git diff** shows the difference between the working directory and the staging area
* **git commit** permanently stores file changes from the staging area in the repository
* **git log** shows a list of all previous commits


(![minipic](picture/gitworkflow.png)

###  First Exercise

1. Run **mkdir (repo name)**   &emsp;&emsp;  give repo name = famous
2. Run **cd famous**           &emsp;&emsp;     cd (change directory) 
3. Run **git init**            &emsp;&emsp;     to make git repo
4. Run  **touch people.txt**    &emsp;&emsp;    touch to make a file 
5. Run **ls** or **ls -a** **ls -l**    &emsp;&emsp;  see differences
6. Time to add some text to **people.txt** file [click here](mustknown.html) add just **ELON MUSK's** info 
7. There are several ways to open file via terminal (nano filename,gedit filename etc..) Lets use run **gedit filename**
8. Run **git status** &emsp;&emsp; check to what happens you might see with red color file name 
9. Run **git add people.txt**  then run **git status** you might see (new file:   people.txt ) in green color 
10. Run **git commit -m 'add Elon Musk info and first commit'**
11. Add another text [click here](mustknown.html.php) add just **Jeff Bezos** info.
12. Run **git diff** see the difference between working directory and staging area then add file to staging area
12. After git add, run **git commit -m 'add Jeff Bezos info and second commit'
13. Run **git log**  viewing the commit history,  extra and better command(**git log --oneline**)
14. Run **history** command to show you all of the last commands that have been recently used.
* Well done FIRST exercise is done. Are you ready for next exercises?? :)))