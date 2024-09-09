# Jenkins


# Jenkins Installations

## on Mac

### With Homebrew Installer
**Install the latest LTS version:**  `brew install jenkins-lts`  
**Start the Jenkins service:**  `brew services start jenkins-lts`  
**Restart the Jenkins service**:  `brew services restart jenkins-lts`  
**Stop Jenkins service:**  `brew services stop jenkins-lts`  
**Update the Jenkins version:**  `brew upgrade jenkins-lts`


## on Windows



## on Linux

### Initial Step
you need to switch to root user.
`sudo -i`  or. `sudo su root`

to use sudo to install it:
`yum install sudo`

update the system		
`yum update -y`

### Java Installation

**Note:**
To work with jenkins, java jdk  version should be 11, 17 or 21.
Install Java
```bash
sudo dnf install java-21-amazon-corretto -y
```
confirm installation
`java --version`

### Jenkins Server Installation

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
**to start jenkins server**	`systemctl start jenkins`
**to stop jenkins**				`systemctl stop jenkins`
**to restart it**						`systemctl restart jenkins`
**to check the status**		`systemctl status jenkins`


## Access jenkins

in local 		http://localhost:8080
in ec2 			http://{ec2-public-ip}:8080


## Setup Jenkins

Unlock Jenkins  get the password from given path file and enter
install suggested plugins
setup username and password, otherwise it is required to use 'admin' as username and pasword that used before
It is done!



