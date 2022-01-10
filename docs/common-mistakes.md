# Common mistakes during the task implementation

This document contains issues or mistakes that commonly made during the task implementation. Please pay attention to this list before submitting a pull request (for students) or merging a pull request (for reviewers). Make sure that none of these issues from this list are not relevant for your solution.<br/><br/>
All of the issues are tagged with two labels: *Probability* and *Impact*. Probability shows the chance of this issue to be in your code system and impact shows how much effort you have to make in order to fix it. Not all issues are equal in this regard:
|   | Low | Medium | High |
|---|---|---|---|
| Probability  |Occurs rarely in students' work.| Occurs approximately in 50% of the students' works.|Occurs almost in 100% of students' works. Sometimes missed not only by the student but by the reviewer as well.|
| Impact  | Minor changes required.|Changes up to 1 hour or 2 of work.|Major efforts required to fix that problem. Major efforts required to fix that problem. This might happen due to technical debt, bad architecture, or incorrect requirements interpretation.| 

Pay close attention to the issues with high Probability because they **will** be in your code and they have to be fixed.<br/>
It is recommended to start fixing issues marked as High impact because they can cause big rewrites in the system and will affect the final grade for the task.

## General
### 1) Pull request description according the [template](https://github.com/EPAM-Gomel-NET-Lab/Docs/blob/main/docs/pull_request_template.md]) is missed
**Probability**: High</br>
**Impact**: Low

### 2) Readme file is not filled via "Steps how to check", "Credentials" etc information
**Probability**: High</br>
**Impact**: Low

### 3) Dry run(build -> unit tests -> integration tests) is not performed before pull request creation
**Probability**: Medium</br>
**Impact**: Medium

### 4) [Workflow](https://github.com/EPAM-Gomel-NET-Lab/Docs/blob/main/docs/workflow.md) is not followed
**Probability**: Low</br>
**Impact**: Medium

## Task 1
### 1) SELECT * in queriees
**Probability**: High</br>
**Impact**: Low

### 2) Unit testing validation in isolation
**Probability**: High</br>
**Impact**: High

Extracting validation in separate classes is not an incorrect approach in itself, but it leads to incorrect assumptions about task requirements. The main idea of testing the validation via unit tests is to call service classes that use this validation and not validation classes in isolation. You won't learn principles like DI and implementation with interfaces.

Another mistake is to test validation logic via integration test. Most of the cases like checking the date in the past or unique values validation are tested via LINQ thus can be unit tested easily. So, convert these integration tests into unit tests. mock or fake all necessary dependencies and this will be accepted as a solution.

### 3) Storing connection string in a hardcoded variable
**Probability**: Medium</br>
**Impact**: Low

## Task 2
### 1) Smart controllers
**Probability**: High</br>
**Impact**: Medium

Controllers contains any logic instead of simple input validation and services call. For the issue fix should be introduced or presentation layer specific services, or some logic extracted to the bussines layer.

### 2) Controllers DRY violation
**Probability**: Medium</br>
**Impact**: Medium

Some specific logic(e.g. wotk with specific cookie) is duplicated between different controllers/services. Specific service must be introduced.
