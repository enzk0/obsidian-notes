---
Course: CSCC 22
Year Level: 3rd
Semester: 2nd
---
---
- ***Testing***, a process of executing a program with the *intent* of finding **faults**
- 70% of development time is *spent* on *testing*

## The Testing Process
---
- ***testing*** is *different* from ***debugging***
- should test both *valid* and *invalid* *inputs*
- ***testing*** starts from the requirements phase only and goes to the last maintenance phase
	- on ***requirements analysis phase***
		- we do *static testing* to get the **SRS**
		- code reviews, code inspections, walkthroughs, and software technical reviews are methods *static testing*
	- if ***code is ready*** or a ***module is ready***
		- we do *dynamic testing* to test code
		- methods are black-box, gray-box, white-box

> **debugging**, removing errors from your program.
> **testing**, aims to locate undiscovered errors.
> **SRS**, System Requirements Specification.
> **static testing**,  testing without executing the actual code
> **dynamic testing**, testing with executing the code, runtime behavior

## What is Software Testing
---
1. **Debug**, successful correction of failure
2. **Demonstrate**, process of showing major features work with input
3. **Verify**, process of finding many faults in the ***application under test*** or ***AUT***
4. **Validate**, process of finding many faults in *requirements*, *design*, and *AUT*
5. **Prevent**, avoid errors in requirements, design, and implementation by self-checking techniques, like "test before design"

*"Software testing is the process of executing a program or system with the intent of finding errors"* - Myers

#### What is Not Testing
- ***Not*** a process of demonstrating software errors are not present
- ***Not*** a process of showing that program functions runs correctly
- ***Not*** a process of establishing confidence that a program works correctly

*"Testing is basically a task of locating errors"*

1. ***Positive Testing***, operate the application as it should be operated
2. ***Negative Testing***, Test for abnormal operations. ex. not correct inputs
3. ***Positive View of Negative Testing***, job of testing is to discover errors before users. A *good tester* makes the program fail. **DESTROY!!!**

$$ SoftwareTesting = Software Verification + Software Validation$$

##### Software Verification
 - Verifies if requirements are fulfilled during **development phase**
 - according to the requirements, SRS, design
 - *am I developing the product right?*
##### Software Validation
 - Verifies if requirements are fulfilled **after the development phase**
 - expectations of the client
 - *am I developing the right product?*
- already the **end** product

![[Pasted image 20250220210112.png]]

*Verified but not Validated*


