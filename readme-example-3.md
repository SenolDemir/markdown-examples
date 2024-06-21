

UI Automation Skeleton Assessment

#### Codes and Test was prepared by:
**Senol Demir*

*Software QA Engineer*

senoldemir@ymail.com

www.linkedin.com/in/demirsenol


**- Build Tool:** Maven

**- Test Framework:** Cucumber BBD (with JUnit Assertions)

------------
##### Environment: 
`https://www.moneycorp.com/en-us/currency-zone/`

------------
#### System Requirements: 
- Java 8 + JDK

- <script src="https://gist.github.com/SenolDemir/879da9c9577a215c67530f80ccfb5266.js"></script>

------------
## Test RUN 

Note: To run the scenario, use `@dropdown` tag for testing Graphs Dropdown Options.

#### 1. Way:
 - Clone the projects
 - Import maven dependencies from POM
 - Go **src -> test > java > Runners > CukesRunner** and Run
 - To generate "HTML Maven Cucumber Report" ; 
    > Open Maven right side panel
    > Double Click Project's Lifecycle
    > Click "verify"
                                                  
#### 2. Way:
 - Run from command line invoke `mvn clean verify` 

------------

## Test Reports Locations
1- Cucumber HTML Plugin Reports
**target -> cucumber-html-reports > overview-steps.html** 
(Right Click and Open in any Browser )

2- When you run my project, Cucumber will create automatically online report link. You can click the link
with in the 24 hours and check the all test steps and status. 

------------
 
## Cucumber Test Feature Scenario:

<<<<<<< Graphs Dropdown Options 
####) Validate the dropdown options in the main page for currency graph.

 a- In this Scenario, it verifies the dropdown options for currency graph.
 
 b- To run this scenario, use the `@dropdown` tag in the CukesRunner class/Cucumber Options
 
 
------------

2024 June;


### End

------------
