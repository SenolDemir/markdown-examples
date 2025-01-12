#  Jenkins Setups in  EC2 Linux Instance (2024)

## Initial Step

you need to swicht to root user. 
`sudo -i`  or. `sudo su root`

to use sudo to install it:
`yum install sudo`

update the system		
`yum update -y`

## Java Installation

**Note:** 
To work with jenkins, java jdk  version should be 11, 17 or 21.

Install Java
```bash
sudo dnf install java-17-amazon-corretto -y
```
confirm installation
`java --version`

## Maven Setup

```
cd /opt
wget https://downloads.apache.org/maven/maven-3/3.9.7/binaries/apache-maven-3.9.7-bin.tar.gz

tar -zxvf $(ls | grep apache-maven-*-bin.tar.gz)
rm -rf $(ls | grep apache-maven-*-bin.tar.gz)
ln -s $(ls | grep apache-maven*) maven
echo 'export M2_HOME=/opt/maven' > /etc/profile.d/maven.sh
echo 'export PATH=${M2_HOME}/bin:${PATH}' >> /etc/profile.d/maven.sh
source /etc/profile.d/maven.sh
```
## Install Git
```bash
sudo yum install git -y
git version
```


## Jenkins Server Setup

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

### Access to Jenkins Server
using the public DNS of your ec2 on port 8080
`http://{ec2-public-ip}:8080`


**Note :** Here you might have to allow port 8080 in your security group settings

### Unlock Jenkins
To get initial password look at the commnad prompt or type this command:
```bash
sudo cat /var/lib/jenkins/secrets/initialAdminPassword
```
You will see password in command line copy and paste to line in the browser page of jenkins
Install suggested plugins.
Create first admin user.
Check the URL, then save and finish the installation

### To uninstall Jenkins
```bash
sudo service jenkins stop
sudo yum remove jenkins
sudo rm -r /var/lib/jenkins
```






