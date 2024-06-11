

# QA Automation Project Example

#### Codes and Tests Prepared by:
*Senol Demir*

QA Test Automation Engineer

senoldemir@ymail.com

www.linkedin.com/in/demirsenol


*- Build Tool:* Maven
## Test RUN

Notes: To run all Scenarios in Transactions.feature, use `@Regression` tag in the CukesRunner class/Cucumber Options

#### Way:
- Clone the projects
- Import maven dependencies from POM\
  **For UI
- Go *src -> test > java > inspired > runners > CukesRunner* and RUN\
  **For API
- Go *src -> test > java > inspired > runners > ApiRunner* and RUN
- To generate "HTML Maven Cucumber Report" ;
  > Open Maven right side panel
  > Double Click Project's Lifecycle
  > Click "verify"

#### System Requirements:
- Java 8+ SDK

#### Recommended Plugins for IDE
1 - Cucumber for Java from JetBrains\
2 - Gherkin from JetBrains

## Test Framework Cucumber BBD and DDT(Json File)
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



## Test Reports Locations
1- Cucumber HTML Plugin Reports
*target -> cucumber-html-reports > overview-steps.html*
(Right Click and Open in any Browser )
