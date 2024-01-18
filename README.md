## BDD Cucumber - 

- Cucumber BDD - Behavior Driven Development
- Gherkins Language - It's a feature language
- BDD is all about behavior.
- In BDD, Tests are written in plain descriptive english type grammar.

```java
 
Feature: sign up

Scenario - seccessful sign up

Given
When
Then
And

Scenario: Duplicate email

Given 
When 
Then
And

```

### Cucumber have 3 components 
- Feature file
- Step Definition file
- Test runner


### Feature file  
- It should have ".feature" extension.
- It have all keywords.(feature, Given, When, Then,As, *)
- It contain scenario related to that feature.
- 
 ```bash

  Feature: It describes the current test script which has to be executed.
  Scenario: It is steps and expected outcome for a specific test case.
  Scenario outline: Scenario can be executed for multiple sets of data using scenario outline.
  Given: It specifies the context of the text to be executed.
  When: specifies the test action which has to perform.
  Then: Expected outcome of the test can be represented by “Then”
  
```

### Step file
- This file contain test step Code (Selenium + Java + Annotations    (cucu..annotations)).
 
### Test Runner (JUnit, Reports, Output)
- It's used to Execute test cases.
- Use Junit to execute the Code.
- Use to run Feature.
- To Generate report & output.


### How to setup Cucumber framework
- create Maven Project
- Add Dependencies (Lastest Junit , Cucumber Dependencies , Eclipse Natural Plugin)

<hr>

### Report in cucumber 

- format = {"pretty", html:test-output}


### Cucumber Options
@CucumberOptions are the property file/system file for the test case.


- dryRun : check if all the Steps have Step definition
- Features : path of feature file
- Tags : what tags in the feature file should be executed
- Glue : path of Step Definition file
- MonoChrome : display the console output in readable way
- Format : report format
- Strict : will fail Execution if there are pending steps.

  <hr>


### Cucumber Data Driven Framework
##### we can Implement BDD cucumber by 3 ways
- Simple data approach - No Use Examples Keyword
- Scenario Outline 
- Data Table 

#### Simple Data Approach

```java

Feature: Login Application

Scenario outline: User Loogin Scenario
	Given User is on Application Home apge
	When Application page title is Free CRM
	Then User enters "abc@gmail" and "ABC@007"
	And User click Login button
	When User nevigate to user profile page
```

#### Scenario Outline 

```java

Feature: Login Application

Scenario outline: User Loogin Scenario
	Given User is on Application Home apge
	When Application page title is Free CRM
	Then user enters"<username>" and "<password">
	And User click Login button
	When User nevigate to user profile page

Examples:
	| username | password |
	| abc@gmail.com | ABC@007 |
```

#### Data Table


<hr>

### Tag in Cucumber - same as grouping in TestNG

```java

Feature: Login user in app

@SmokeTest @RegressionTest
Scenario: Login with valid Credentials
	  Given user is on Application Homepage

@FunctionalTest @SanityTest
Scenario: Create new user
	  given user is able to create new user

@Regression @FunctionalTest
Scenario: Delete newly created user
	  Given user is able to delete the user
```


#### For running Specfic group of test cases - 
- In TestRunner file uder the Tags name mention the group name
- //  tags = {"@SmokeTest , @RegressionTest"} - OR Condition
- //  tags = {"@SmokeTest" , "@RegressionTest"} - AND Condition


<hr>

### Hooks in Cucumber - same as annotataions in TestNG

```java

// @Before
   public void OpenBrowser(){
}
// @After
   public void closeBrowser(){
}
```
