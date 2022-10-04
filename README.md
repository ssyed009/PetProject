# PetProject


**Summary:** The project is implemented using open source api automation framework called Karate. Karate tests can be written in BDD syntax , easy to understand for non-programmers too.

**Pre-requisites:**
To implement this framework, install following tools to get started:
- Java (at least java 8)
- Maven
- Git
- Visual Studio Code (IDE)
- VS Code Plugins
  - Cucumber (Gherkin) Full support
  - Karate Runner
  - Java Extension pack
  - Maven for Java

**Project Setup:** 
Create a local repository folder (for example: C:\petproject)
Download the petproject.zip from repository https://github.com/ssyed009/PetProject/
Extract all files in local repository.
Open VSCode and select File >> Open Folder , select the local folder and click Select Folder.

**Framework Implementation:**

The petproject has multiple folders as shown below:

![image](https://user-images.githubusercontent.com/111313561/193898922-6d764970-413f-4479-9e68-98f49f4f0973.png)

**POM.XML:**
The POM.XML has all the dependencies and plugin information.

**Karate-config.js:**
Karate framework expects a config file, and this file contains the environment information like URL, global variables, user login details and authorization token information.

**Helpers Folder:**
This folder contains the common feature files or resusable code needed to execute tests. 
For example, login.feature which is run only once initially at the start of test and and DataGenerator.java is independent of functionality that generates random test data.

**Pets folder:** Pets folder contains all feature files, test data and test runner file.

**testdata:**
testdata folder within pets contains the external files that are used as payload or test files for API testing. For example, json, csv, excel, images .. etc

**Target folder:**

Reports generated after running the tests are stored in target folder. This project implements both Junit and Cucumber reports.

Execute the Test framework:

Note: Maven is used as a bulld tool to run the tests , if Maven_Home is not setup, please add maven to path in system environment variables.

**Feature File/Scenarios:** 
Petproject has one feature file validatepetAPIMethods.feature with following scenarios:
upload a pet Image.
Add a new pet to the store and get the pet by PetId
Update an existing pet.
Find Pets by Status.
Update a pet in the store with form data.
Delete a pet


**Instructions to execute the tests:**

1. Open the project in VsCode
2. Navigate to pets folder
3. Select validatepetAPIMethods.feature
4. To run the scenarios individually , Clcik Run option provided by Karate Runner extension.
5. To run all the tests , navigate to the terminal in VSCode and enter  mvn test
6. Once the tests are successfully run , the reports will be generated in target folder.

**Reports:**
HTML Report will be published to petproject\target\karate-reports folder

![image](https://user-images.githubusercontent.com/111313561/193901632-65ba6db1-f995-42ba-9e7e-0a4508caba06.png)

Cucumber HTML Reports will be published to petproject\target\cucumber-html-reports

![image](https://user-images.githubusercontent.com/111313561/193901482-4b446c19-18a9-4d66-a90f-3e0cc8c392ee.png)
