# Jenkins


# Jenkins Installation and Setup in Local Machines

## on Mac

#### with homebrew installer  
Install the latest LTS version:
`brew install jenkins-lts`  
Start the Jenkins service:  
`brew services start jenkins-lts`  
Restart the Jenkins service**:  
`brew services restart jenkins-lts`  
Stop Jenkins service:  
`brew services stop jenkins-lts`  
Update the Jenkins version:  
`brew upgrade jenkins-lts`


## on Windows
...


## on Linux

#### Initial Step
you need to switch to root user:  
`sudo -i`  or. `sudo su root`

to use sudo to install it:  
`yum install sudo`

update the system:  	
`yum update -y`

#### Java Installation

**Note:**
To work with jenkins, java jdk  version should be 11, 17 or 21.
Install Java
```bash
sudo dnf install java-21-amazon-corretto -y
```
confirm installation
`java --version`

#### Jenkins Server Installation

Add Jenkins repo to the `yum` repository
```bash
sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo
```
import a key file from Jenkins-CI to enable installation from the package:
```bash
sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io-2023.key
```
```bash
sudo yum upgrade
```
Install Jenkins
```bash
sudo yum install jenkins -y
```
enable Jenkins service so that Jenkins service can restart automatically after reboots.
```bash
systemctl enable jenkins
```

### Run Jenkins
to start jenkins server:  
`systemctl start jenkins`
to stop jenkins:  
`systemctl stop jenkins`
to restart it:  
`systemctl restart jenkins`
to check the status:  
`systemctl status jenkins`


** accessing Jenkins
in local 		http://localhost:8080
in ec2 		http://{ec2-public-ip}:8080


## Jenkins Setup And Configurations

Unlock Jenkins  get the password from given path file and enter
install suggested plugins
setup username and password, otherwise it is required to use 'admin' as username and pasword that used before
It is done!

### Recommended Plugins

Github Integraton  
Maven Integration  
Build Pipeline  
AnsiColor  
Cucumber Report  
Locale (for language settings)  
Amazon EC2 (for cloud usage)  
BlueOcean	(provide more efective interface to use pipeline and freestyle jobs)  

**Locale Plugin**
Manage Jenkins >> Appearance  
you can set the language from here  

### Maven Configuration
You may need maven configuration in Jenkins to run maven project, due to version problem.  
To do that first add Maven Integration plugin.  
Than If you want to have Jenkins install Maven for you  
You must go to Jenkins Tool Configuration, and configure a Maven version with automatic installer (from the web), give a name.  
This version should be suitable with your project maven version  
In Job configuration, for Maven Version, you must select that particular version that you've just configured.  

### Github Credential Configuration  

If your Github repository is private, you have add credentials of github to access it.  
Github does not support email password access anymore, so you have to use another way:  
Using SSH Key  
Using Github OAuth app  


### Github Integration with EC2 Jenkins Server By Using SSH
We will use SSH Key Authentication to reach Github account  
To do that first you have to generate SSH Key in the instance, to do that type this command:  

**Step 1: Generate SSH Key**
to generate SSH key in Linux 
``` 
ssh-keygen
```
You have to add the public key of this SSH key to github account  
how to view ssh key files (you have to be root user)  
```
ls -al ~/.ssh
```
**Step 2: Add SSH Key to Github Account**
to view ssh public key  
```
cat ~/.ssh/id_rsa.pub
```
For that go to the settings of your GitHub, on the left choose SSH and GPG keys, click on New SSH key, give the name under Title, and paste the  
public key under the Key section we previously generated on the EC2 server.  

**Step 3: Add SSH Key to Jenkins Credentials**
After adding the ssh key to our GitHub account we will add the credentials in Jenkins. For that, under credentials click on Add button and click on Jenkins in the drop-down option.  
to view ssh priavete key in EC2 Linux Machine  
```
cat ~/.ssh/id_rsa.pub
```
copy all text with begin and end phrases  
Give a name to it, paste the key into private key section  
pay attention to branch name in jenkins config page that should be same with repo.  
Save. Now it should work when you choose this credential with your github repo  






