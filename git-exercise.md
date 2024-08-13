

Open a new branch called practice2 

Add a new file . Feature2.java
commit your change 
add 3 lines and commit each lines separately 
	so we can have some history 
	compare the branches 

--TODO (NEW)
DO NOT MERGE YET 
	we will do rebase this time to see the difference 



--- 
create branch practice4 

Add new java file Practice4.java  as 1st commit 

add 3 more commits by adding few lines 	
	to existing Feature3.java :


eventually , only cherry-pick last commit into master 


## Using git with command line

* `terminal` on mac  
* `gitbash` on windows 

### Steps : 
1. natigate to the desktop 
	cd ~/Desktop

2. make a folder in desktop 
	mkdir myrepo

3. check if the folder is created by using ls command.

to list everything under current (desktop) folder 
	
	ls  

4. go inside the myrepo folder by 
```
  cd myrepo
```
5. check if you are actually at my repo by 
```
  pwd 
```
6. This is where git start 
	
create a repository under this folder myrepo: 
```
	git init 
```
7.  add new file by and add some content by using below command 
```
	echo "Hello world" >> file1.txt
```
8. check the status of our repo 
```
	git status 
```
output will be as below
```
	On branch master

	No commits yet

	Untracked files:
	  (use "git add <file>..." to include in what will be committed)
		file1.txt

	nothing added to commit but untracked files present (use "git add" to track)
```


9. add the change into staging area 
```
	git add file1.txt 
```
then check if its staged 
```	
  git status  
```
10. commit the staged file 
```
	git commit -m "initial commit"
```

11. add two more files ,stage them and commit them using same steps above

12. create a GitHub Repo 
 from GitHub website in your account

13. observe the instruction 
	1. creating local repo from scractch and connect 
	2. set up remote repo for your local repo

 please run this command first 
 you copied from GitHub 

setting up remote 
```
git remote add origin https://github.com/eu3-user/my-repo.git
```
 creating link between local master to remote master
``` 	
  git push -u origin master 
```
 it might ask you to enter username password 
 please enter correct username and password

