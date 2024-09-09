# Setup and Configuration on Jenkins Server

### Recommended Plugins

Github Integraton
Maven Integration
Build Pipeline
AnsiColor
Cucumber Report
Locale (for language settings)

### Locale Plugin Config
Manage Jenkins >> Appearance
you can set the language from here

### Maven Configuration
You may need maven configuration in Jenkins to run maven project, due to version problem.
To do that first add Maven Integration plugin.
Than If you want to have Jenkins install Maven for you
You must go to Jenkins Tool Configuration, and configure a Maven version with automatic installer (from the web), give a name.
This version should be suitable with your project maven version
In Job configuration, for Maven Version, you must select that particular version that you've just configured.



