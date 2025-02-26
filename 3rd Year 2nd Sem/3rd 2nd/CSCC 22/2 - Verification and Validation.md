---
Course: CSCC 22
Year Level: 3rd
Semester: 2nd
---
---

## Difference between Verification and Validation
---
> [!TERM] Software Verification and Validation (V&V)
> - a technical discipline of systems engineering.
> - parallel with software development, *not* at the end of development
> 

_"a systems engineering process employing a rigorous methodology for evaluating the correctness and quality of software product through the software life cycle."_ 
													- Stauffer and Fuji (1986)

| ***Verification***                                                                                                   | ***Validation***                                                                               |
| -------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| It is a static process of verifying documents, design, and code.                                                     | It is a dynamic process of validating/testing the actual product.                              |
| It does not involve executing the code.                                                                              | It involves executing the code.                                                                |
| It is human based checking of documents/files.                                                                       | It is the computer-based execution of program.                                                 |
| Target is requirements specification, application architecture, high level and detailed design, and database design. | Target is actual product—a unit, a module, a set of integrated modules, and the final product. |
| It uses methods like inspections, walk throughs, desk-checking, etc.                                                 | It uses methods like black-box, gray-box, and white-box testing.                               |
| It, generally, comes first—before validation.                                                                        | It generally follows verification.                                                             |
| It answers the question—Are we building the product right?                                                           | It answers the question—Are we building the right product?                                     |
| It can catch errors that validation cannot catch.                                                                    | It can catch errors that verification cannot catch.                                            |
- Both of these are _essential_ and _complementary._ Each provides its own sets of _error filters._
- Each has its own way of finding the errors in the software

## Difference Between QA and QC
---
> [!Term] ***Quality assurance***
> - a planned and systematic activities implemented in a quality system so that quality requirements for a product or service

> [!Term] ***Quality control***
> - the observation techniques and activities used to fulfill requirements for quality.

Both are, however, *different to each other*. We tabulate The differences between them are shown below.

| Quality Assurance (QA)                                  | Quality Control (QC)                                                            |
| ------------------------------------------------------- | ------------------------------------------------------------------------------- |
| 1. It is process related.                               | 1. It is product related.                                                       |
| 2. It focuses on the process used to develop a product. | 2. It focuses on testing of a product developed or a product under development. |
| 3. It involves the quality of the processes.            | 3. It involves the quality of the products.                                     |
| 4. It is a preventive control.                          | 4. It is a detective control.                                                   |
| 5. Allegiance is to development.                        | 5. Allegiance is not to development.                                            |

## V & V Limitations
---
 Overall *objective* of software ***V&V approaches***:
 - ensure that the product is free from failures
 - meets user expectations

1. ***Theoretical Foundations***
	- Howden claims the *most important theoretical result* in program testing and analysis is that *no general purpose testing or analysis procedure can be used to prove program correctness.*
2. ***Impractically of Testing All Data***
	- For most programs, it is *impractical* to attempt to test the program with *all possible inputs due* to a *combinational explosion*.
	- For those inputs selected, a *testing oracle* is needed to determine the correctness of the output for a particular test input.
3. ***Impractically of Testing All Paths***
	- For most programs, it is *impractical* to attempt to *test all execution* paths through the product due to a *combinational explosion*. 
	- It is also not possible to develop an algorithm for generating test data for paths in an arbitrary product due to the mobility to determine path feasibility.
4. ***No Absolute Proof of Correctness***
	- Howden claims that there is *no such thing* as an *absolute proof of correctness*. 
	- However, there are *proofs of equivalency*, i.e., *proofs that one description of a product* is *equivalent to another description*. 
	- Hence, unless a formal specification can be shown to be correct and, indeed, reflects exactly the user's expectations, no claims of product correctness can be made

## Categorizing V&V Techniques
---
![[Pasted image 20250226133816.png]]

- ***white-box testing*** is that it checks for interface errors at the module level
- ***black-box testing*** can also be done at the module level by testing boundary conditions and low-level functions like correctly displaying error messages.

## Role of V&V in SDLC
---
***Traceability Analysis***
- traces each *software requirement* back to the *system requirements established* in the concept activity. 
- ensuring that each requirement correctly satisfies the system requirements and that no extraneous software requirements are added. 
- in this technique, it determines whether any derived requirements are consistent with the original objectives, physical laws, and the technologies described in system document.

***Interface Analysis***
- It is the detailed examination of the interface requirements specifications. 
- The evaluation criteria is the same as that for requirements specification. 
- The main focus is on the *interfaces* between *software*, *hardware*, *user*, and *external* *software*.

**Criticality Analysis**

Criticality is assigned to each software requirement. When requirements are combined into functions, the combined criticality of requirements form the criticality for the aggregate function. Criticality analysis is updated periodically as requirement changes are introduced. This is because such changes can cause an increase or decrease in a functions criticality which depends on how the revised requirement impacts system criticality.

Criticality analysis is a method used to locate and reduce high-risk problems and is performed at the beginning of the project. It identifies the functions and modules that are required to implement critical program functions or quality requirements like safety, security, etc.