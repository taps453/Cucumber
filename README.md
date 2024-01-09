## BDD Cucumber - 

- Cucumber BDD - Behavior Driven Development
- Gherkins Language - It's a feature language
- BDD is all about behavior.
- In BDD, Tests are written in plain descriptive english type grammar.

```java
 
"""
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
"""
```

### Cucumber have 4 components 
- Feature file
- Step Definition file
- Test runner


### Feature file  
- It should have ".feature" extension.
- It have all keywords.(feature, Given, When, Then,As, *)
- It contain scenario related to that feature.

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


------------------------------------------------------------------------
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

