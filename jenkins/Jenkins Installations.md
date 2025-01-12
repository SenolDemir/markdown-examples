
# Jenkins Installation and Setup in Mac, Windows

## on Mac

#### With Homebrew installer  
Install the latest LTS version:    
```brew install jenkins-lts```  
Start the Jenkins service:  
```brew services start jenkins-lts```  
Restart the Jenkins service:    
`brew services restart jenkins-lts`    
Stop Jenkins service:  
`brew services stop jenkins-lts`  
Update the Jenkins version:  
`brew upgrade jenkins-lts`


## on Windows
...



### Run Jenkins
to start jenkins server:  
`systemctl start jenkins`  
to stop jenkins:  
`systemctl stop jenkins`  
to restart it:  
`systemctl restart jenkins`  
to check the status:  
`systemctl status jenkins`


** Access to Jenkins Server
in local 		http://localhost:8080
in ec2 		http://{ec2-public-ip}:8080


## Setup And Configurations

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








