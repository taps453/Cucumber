#### 1- Cucumber Advantages

#### 2- Before keyword in Cucumber -
- In the Cucumber tool, the Background keyword is used to group multiple given statements into a single group. The keyword is mostly used when the same set of given statements are repeated in each scenario of the feature file.

#### 3- What is BDD

#### 4- Write feature file for gmail application.

#### 5-  Scenario Outline -
  - Scenario outline is used as a parameter of scenarios.
  - This is used when the same scenario needs to be executed for multiple sets of data; however, the test steps remain the same.
  - Scenario Outline must be followed by the keyword 'Examples', which specify the set of values for each parameter.

#### 6- TDD - Test-Driven Development
  - create the test cases first and then write the code underlying those test cases.

#### 7- dryrun -
  - Cucumber dry run is used to compile cucumber features files and step definitions.
  - It is run to find any compilation errors. If it finds anyone, it will show when we use dry run.

#### 8- TestRunner class
  - Cucumber testing approach, the TestRunner class provides the link between the feature file and the step definition file. 
  - The TestRunner class is generally an empty class with no class definition. 
  - [@RunWith and @CucumberOptions]

#### 9- Options tag 
- Options tag is a part of the TestRunner file and comes in the form of an annotation called @CucumberOptions.
- It contains two parameters feature and glue.
- 
```java

   [
	@CucumberOptions (  
	features = "src/test/java/features ",  
	glue = {"stepDefinitions"}  
	)   ]
```
  

#### 10- Hooks - 
  - Hooks are used to control the flow of the program and optimize lines of code.
  - [@Before and @After annotations]
