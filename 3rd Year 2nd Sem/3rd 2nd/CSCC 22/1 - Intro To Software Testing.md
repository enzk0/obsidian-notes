---
Course: CSCC 22
Year Level: 3rd
Semester: 2nd
---
## What is testing?
---
*to be added*
Testing Process
Testing is different from debugging
- happens from the start
- intended for quality assurance

## Software Testing
---
1. Debug
2. Demonstrate
3. Verify
4. Validate
5. Prevent

Done with the intent of ***finding errors***

**Positive Testing:**
- looks on the bright side, and feeds correct data to see the right behavior of a software
**Negative Testing:**
- opposite to positive testing, in where we feed incorrect data and ensure that errors will be present
**Positive view of Negative Testing:**
- Discovering errors before the user does
- MAKE THE SYSTEM FAIL!

$$ SoftwareTesting = Software Verification + Software Validation$$

##### Software Verification
 - Verifies if requirements are fulfilled during **development phase**
 - according to the requirements
 - *am I developing the product right?*
##### Software Validation
 - Verifies if requirements are fulfilled **after the development phase**
 - expectations of the client
 - *am I developing the right product?*
- already the **end** product

*Verified but not Validated*

### Test Cases
---
1. Technical Case
	- Affects the *reputation* of the Developer
2. Business Case
	- Doesn't compromise *quality*
	- Users might not use your product because it is faulty
	- Most **Costly** due to post-release debugging. Developing right *back from the start*, *another iteration*
	- Affects the *reputation* of the Company
3. Professional Case
	- Testing is a rewarding task
	- Systematic Testing is Good Testing
		- **systematic testing** - a structured and thorough testing plan that is in the context of the project.
	- Developer confidence due to quality work
4. Economics Case
	- defects get introduced in ever phase of SDLC
	- *Phase Containment of Errors* - detecting errors on its introduction
		*When meeting the client:*
			a. provide a solution
			b. the client should be the one to talk
			c. provide questions to ask the client about what they want, their challenges, their needs
			d. just listen
		 *"The wrong thing to do is ask the budget first, do it at later times"*
		 - aim to compute cost after going through the specifics and context of the project
		*Deliverables of **Requirements Analysis**:*
			a. SRS: System Requirements Specifications
			b. project scopes and limitations
	Verification and validation early on
	Quality assurance is on testing but should be done pre and post
	- To Improve Quality
	- For Verification and Validation
	- For Reliability Estimation
	- *HAD **1st QUIZ** AT THIS POINT*
5. For Quality Improvement
	- monitoring the health of your system
	- test doesn't end when you release the software
6. For Verification and Validation
	![[Pasted image 20250210085357.png]]
7. For Reliability Estimation


### Epic Software Failures
---
1. **Solarwinds**
	- FireEye, a cybersecurity company, and Microsoft, affected by the Solarwinds vulnerability
2. **Yahoo** **Breach**
	- credentials exploited
3. **Nest** **Thermostat** **Freeze**
	- uncomfortable and uncontrollable temperature, due to firmware update
	- *"make sure to do testing in all scenarios, across different platforms"*
4. **HSBC's Payment Glitch**
	- failure of electronic payment system

### Why software failures happen?
---
- software testing 40% and 25% budget
- *lack of time*, *inadequate testing*
- loss of client trust, to the company, and to the leader
- software is a ubiquitous product, 90% of people use software
- loss of smaller companies, due to not enough attention to software quality and conducting the right amount of testing
- new technologies, new test cases

## Who Should do Testing
---
- testing starts from the very beginning
- testing is a team effort
- developers test by unit testing
- designers do design review

### How much should we test
---
- there is no 100% testing, as testing is not 100% exhaustive
- there's an infinite number of test cases

**Prioritize:**
- core components

#### Selection of Good Test Cases
---
- test cases come from use cases
- crafting test cases is an artwork
- test suite - collection of test cases
- test case - a question that you ask of the program

#### When to stop testing
---
- testing is potentially endless
- testing is a trade-off between budget, time, and quality
- project manager exists to ensure that member works on the timeline