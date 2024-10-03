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
| :-------- | --------- | -------- | :-------: | :---: | -------  | ---- | ----- | ---- |
| The input field of the calendar date generator | `TC-001` | Generates a chosen number of dates | 10 |   | Should generate 10 dates | Generated 10 dates | Pass |  |
|          | `TC-002` | Generates a chosen number of dates |  | -10 | Should not fall below 0 | It's scrolling below 0 | Fail | https://github.com/kattypatty/Random-Date-Generator-Test-Report/issues/1 |
| Date output format field | `TC-003` | Generate date for the past date input | YYYY-MM-DD hh:mm:ss |   | 2020-08-12 04:15:18 | 2020-08-12 04:15:18 | Pass |  |
| | `TC-004` | Generate date for future date input | MM-DD-YYYY |   | 02-17-2029 | 02-17-2029 | Pass |  |
|  | `TC-005` | The correct result is not produced in the date output format field "Year Date Month" | Year Date Month |   | 2024 10 February | 2024 February 10 | Fail | https://github.com/kattypatty/Random-Date-Generator-Test-Report/issues/2 |
|  | `TC-006` | Handle leap year date| YYYY/MM/DD |   | 2024/02/29 | 2024/02/28 | Fail |  |
| Custom date format use field | `TC-007` | Handle custom date format use | YYYY/month/DD |   | 2024/December/17 | 2024/Dece32ber/17 | Fail |  |


# Bugs/Issues Found:
Bug ID | Test Case ID | Test Description | Priority | Status | Comment |
| ----------- | ------ | --------- | ----- | ------- | ------ |
|   BUG-001 | `TC-002` | The input field of the calendar date generator allows the user to scroll a negative number | High | To Do | https://github.com/kattypatty/Random-Date-Generator-Test-Report/issues/1 |
|   BUG-002 | `TC-005` | The correct result is not produced in the date output format field "Year Date Month" | Medium | To Do | https://github.com/kattypatty/Random-Date-Generator-Test-Report/issues/2 |
|   BUG-003 | `TC-005` | The correct result is not produced in the date output format field "Year Date Month" | Medium | To Do | https://github.com/kattypatty/Random-Date-Generator-Test-Report/issues/2 |
