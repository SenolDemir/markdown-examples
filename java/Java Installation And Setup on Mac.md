
# Java Installation And Setup on Mac

##	Java Setup on Mac

Step 1 <br>
Download the latest stable version of JDK from Oracle website:
You should select 'DGM' file
If your Mac is M1, M2 or later ones you should select 'ARM64 Installer'

Step 2 <br>
Find donloaded file and click on it
Click continue to install
When you finish you can move to downloaded file into bin


Step 3: Set JAVA_HOME <br>
Find the location where Java intalled in your machine
For it open the terminal and type:
```bash
/usr/libexec/java_home -V
```			
the to list directory file:
```bash
ls -al
```
You have to see a file named .zshrc
If you don't see it, create one by typing
```bash 
touch .zshrc
```
then open it:
```bash 
open .zshrc
```
it will be opned by your text editor program.
It will be blank copy and paste the following (You have to change the version number with the number of your downloaded one)
			
```bash			
export JAVA_HOME=$(/usr/libexec/java_home -v 21.0.1)
export PATH=$JAVA_HOME/bin:$PATH
```
save it and close
in terminal type:
```bash 
source .zshrc
```
after this close your terminal
then re-open terminal and to check setting java home is okey or not type
```bash 
echo $JAVA_HOME
```
You have to see the location of it. If you see setting is okey.


	



First Java Program

Create first java program
on terminal any location on your machine to create a java project
then create a folder -> mkdir firstJavaProject
go to this folder
create a java file -> Hello.java
then copy paste basic java codes and save
you have to compile it first -> javac Hello.java
to run compiled file -> java Hello


