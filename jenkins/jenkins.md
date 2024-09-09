# Jenkins



## Java Installation in Amazon Linux EC2

Note: latest jenkins version supports  only java 17 and 21.  
check the supported version from jenkins website  

Amazon Linux utilizes RPM Package Manager (YUM) to install and manage software packages.  
You will need to run the installation commands as the root user or use sudo.  


Ensure YUM has the most up-to-date package info:  
```bash
sudo yum update
	```

Install Java  
```bash
sudo yum install java-17.0
``` 
or  
```bash
sudo yum install java -y
``` 

Confirm Installation  
```bash
java --version
```

// other installation commands \\  

``` sudo dnf install java-17-amazon-corretto -y ``` 
or  
``` bash
amazon-linux-extras install java-openjdk11 -y
yum install java-devel -y
``` 

\\\\\\\\\\\\\\\\\    ///////////////////  

 to uninstal a java version  
```bash 
sudo yum remove java-1.7.0-openjdk -y
``` 


## Jenkins Installation in Amazon Linux EC2  
 	
Way 1:  

Add Jenkins repo to the `yum` repository  
```bash
sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat/jenkins.repo
``` 

Import a key file from Jenkins-CI to enable installation from the package  
```bash
sudo rpm --import https://pkg.jenkins.io/redhat/jenkins.io.key
``` 

Install Jenkins  
``` bash
sudo yum install jenkins -y
``` 

Enable Jenkins service so that Jenkins service can restart automatically after reboots. 
``` bash
sudo systemctl enable jenkins
``` 

start jenkins server  
```bash
systemctl enable jenkins
``` 


Way 2:  

Install Jenkins on Amazon Linux 2 (EC2) with `war` File  
Download Jenkins application
```bash
wget https://get.jenkins.io/war-stable/2.263.4/jenkins.war
wget http://mirrors.jenkins.io/war-stable/latest/jenkins.war
```

Jenkins Configurations

Get the initial administrative password.
```bash
sudo cat /var/lib/jenkins/secrets/initialAdminPassword
```

Enter the temporary password to unlock the Jenkins.  

Install suggested plugins.  
  
Create first admin user  

Check the URL, then save and finish the installation.  



## Jenkins Commands

Check if the Jenkins service is up and running.
```
sudo systemctl status jenkins
```

To stop jenkins  
```bash
sudo service jenkins stop
```



