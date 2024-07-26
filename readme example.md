# Template Test Project

(Description) A concise yet descriptive title and an overview of the project’s purpose.

- Build Tool: Maven
- Test Framework: Cucumber BBD (with JUnit Assertions)

## Prerequisites

#### System Requirements
Java 8+ JDK
Apache Maven (to be able to run tests by command line)

#### Recommended Plugins for IDE
Cucumber for Java from JetBrains\
Gherkin from JetBrains

## Environment: 
`https://bstackdemo.com/`

## Installation
clone the project from github by using following command
```bash
git clone <url>
```
import maven dependencies from POM

## Usage | Running Test


> [!NOTE]
> *To run all scenarios in login.feature, use `@Regression` tag in the CukesRunner class/Cucumber Options*

#### Way 1

 - Clone the projects
 - Import maven dependencies from POM
 - Go **src -> test > java > Runners > CukesRunner** and Run
 - To generate "HTML Maven Cucumber Report" ; 
    > Open Maven right side panel
    > Double Click Project's Lifecycle
    > Click "verify"




#### Way 2
Run from command line invoke:
```bash
mvn clean verify
```
It provides generated HTML reports, as well.  
## Test Reports Locations
1- Cucumber HTML Plugin Reports
**target -> cucumber-html-reports > overview-steps.html** 
(Right click and open in any browser )

2- When you run the project, Cucumber will create automatically online report link. You can click the link
with in the 24 hours and check the all test steps and status.


## Features
#### Testing Framework with Cucumber BBD and DDT (Json File)
- I am using Page Object Modelling to enhance test maintenance and reducing code duplication. This is one of the most famous Selenium approaches.
- I used Maven to manage and centralize my dependencies which I have pom.xml
- I used rest-assured library which supports GET, POST, PUT, PATCH, DELETE, OPTIONS and HEAD requests and can be used to validate and verify the response of   these requests.
- I used Gson library which has JsonParser class which helped to read Json file in my framework.
- I use Page Object Classes to store and identify the elements that I work on
- I am using Cucumber and Gherkin language for non-technical people to understand what is going on in testing
- To interact with browsers, I am utilizing Selenium WebDriver
- I used a Cucumber Scenario outline and example feature
- In the Feature folder, I store my feature files separately, and it helps in the usability of the codes
- I added a screenshot interface; when the scenario fails, it takes a screenshot
- For assertions/verifications, to compare expected and actual results I utilize Hamcrest Matcher and Junit assertions
- I use hook class as pre-and post-test implementations

## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.

Please make sure to update tests as appropriate.





## Prepared By
**Senol Demir**

*Software Development Engineer In Test (SDET)*

`senoldemir@ymail.com`

<a href="https://www.linkedin.com/in/senoldemir/" target="_blank">linkedin</a>



July 2024


## License
[MIT](https://choosealicense.com/licenses/mit/)
