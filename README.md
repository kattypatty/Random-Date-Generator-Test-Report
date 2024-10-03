# Random-Date-Generator-Test-Report

# Objective
The goal of this test is to validate the performance of the random date generator against a variety of inputs, including a custom date format and edge cases. 
This test focuses on both functional and boundary conditions to ensure that the generated dates and times are accurate and comply with the given predefined rules.

# Test Environment:
* **Operating System:** Windows 10
* **Browser:** Chrome, Firefox
* **Tools Used:** Manual Testing
* **Test Data:** Various valid and invalid dates and inputs, edge cases

# Validation of input data
# Test Cases:
| Test Case | Test Case ID | Test Description | Valid Input | Invalid Input | Expected Output | Actual Result | Status | Comment |
| -------- | ------ | -------- | ------- | ----- | ------- | ------ | ---- | ----- |
| Generates a given number of dates | TC-001 | Generates a chosen number of dates | 10 |   | Should generate 10 dates | Generated 10 dates | Pass |  |
|          | TC-002 | Generates a chosen number of dates |  | -10 | Should not fall below 0 | It's scrolling below 0 | Fail |   |
