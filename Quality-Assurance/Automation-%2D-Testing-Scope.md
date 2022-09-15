# Overview
Software Testing is evaluation of the software against requirements gathered from users and system          specifications. Testing is conducted at the phase level in software development life cycle or at module level in program code. Software testing comprises of Validation and Verification

## QA Scope
- We will include:
 Sanity Testing/Funcional testing/API testing/Integration testing/Regression testing/Automation

- Out of Scope
At the moment Performance testing is out of the scope 



## QA Process
###1. Understand Requirements
- Grooming meeting 
- Understand and clarify the Requirements
- Re-assessing the relative priority of stories
- Estimates to stories


###2. QA:  Create Sub-Task - Test Cases

### - Help define acceptance criteria
- With Dev/PO define the acceptance criteria for each story

###- Create scenarios 
- QA works on **Test Plan** module in Azure, here QA create and design scenarios & test cases
- We can set if the Test Cases is candidate to be Automated
- We can control the state of the test cases to be Automated, with this we will create a metrics and mesure the advance and do improvements in the process  
- Scope of testing: Define the scope of each story or feature (Multiple stories)  

###3. Automation testing CI/CD

###- Automation Framework 
- The selected framework for automation is Cypress: All-in-one testing framework, assertion library
- This library will live inside DAS(product) project, this way we can increase the quality of the scripts and have better control of the test

###-Automation Process
- Once we evaluate the correct functionality of a feature (story) with manual testing
we can proceed to the creation of a Automation script
- The test suites runs with every deployment, this way we can guarantee we don't insert new bugs/issues to the stable application 
- Test suite will be increase on each sprint  



