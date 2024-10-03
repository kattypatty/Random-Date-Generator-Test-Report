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
| :-------- | ------------ | -------- | :-------: | :---: | -------  | ---- | ----- | ---- |
| The input field of the calendar date generator | `TC-001` | Generates a chosen number of dates | 10 |   | Should generate 10 dates | Generated 10 dates | Pass |  |
|          | `TC-002` | Generates a chosen number of dates |  | -10 | Should not fall below 0 | It's scrolling below 0 | Fail | https://github.com/kattypatty/Random-Date-Generator-Test-Report/issues/1 |
| Date output format field | `TC-003` | Generate date for the past date input | YYYY-MM-DD hh:mm:ss |   | 2020-08-12 04:15:18 | 2020-08-12 04:15:18 | Pass |  |
| | `TC-004` | Generate date for future date input | MM-DD-YYYY |   | 02-17-2029 | 02-17-2029 | Pass |  |
|  | `TC-005` | Handle leap year date| YYYY/MM/DD |   | 2024/02/29 | 2024/02/28 | Fail | https://github.com/kattypatty/Random-Date-Generator-Test-Report/issues/3 |
|  | `TC-006` | The correct result is not produced in the date output format field "Year Date Month" | Year Date Month |   | 2024 10 February | 2024 February 10 | Fail | https://github.com/kattypatty/Random-Date-Generator-Test-Report/issues/2 |
|  | `TC-007` | Invalid date input handling | | 2024-12-35 | Error message | Date generator doesn't generate a result | Pass |  |
|  | `TC-008` | End of year boundary | 2022-12-31| | 2022-12-31 | 2022-12-31 | Pass |  |
|  | `TC-009` | End of month boundary |2022-12-31| | Date genearator should generate a last day of the month | Date generator doesn't generate a result | Fail | https://github.com/kattypatty/Random-Date-Generator-Test-Report/issues/6 |
| Custom date format use field | `TC-010` | Handle custom date format use | YYYY/month/DD |   | 2024/December/17 | 2024/Dece32ber/17 | Fail | https://github.com/kattypatty/Random-Date-Generator-Test-Report/issues/4 |
|  | `TC-011` | Invalid date input handling with input days value |  | YYYY/MM/d  | Error Message | 2024/December/17 | Fail | https://github.com/kattypatty/Random-Date-Generator-Test-Report/issues/7 |
|  | `TC-012` | Invalid date input handling with hours |  | YYYY/MM/DD h:mm:ss| 2022/12/09 4:07:05 | 2022/12/09 4:07:05 | Pass |  |
|  | `TC-013` | Invalid date input handling with a month value |  | YYYY/mm/DD| 2022/12/09 |2022/48/19 | Fail | https://github.com/kattypatty/Random-Date-Generator-Test-Report/issues/8 |
|  | `TC-014` | Invalid date input handling with the seconds value |  | YYYY/MM/DD h:mm:s | Error Message |2022/12/12 06:39:0 | Fail | https://github.com/kattypatty/Random-Date-Generator-Test-Report/issues/9 |


# Bugs/Issues Found:
Bug ID | Test Case ID | Test Description | Priority | Status | Comment |
| ----------- | ------ | --------- | ----- | ------- | ------ |
|   BUG-001 | `TC-002` | The input field of the calendar date generator allows the user to scroll a negative number | High | To Do | https://github.com/kattypatty/Random-Date-Generator-Test-Report/issues/1 |
|   BUG-002 | `TC-006` | The correct result is not produced in the date output format field "Year Date Month" | Medium | To Do | https://github.com/kattypatty/Random-Date-Generator-Test-Report/issues/2 |
|   BUG-003 | `TC-005` | The program doesn't generate a day of the leap year | High | To Do | https://github.com/kattypatty/Random-Date-Generator-Test-Report/issues/3 |
|   BUG-004 | `TC-0010` | The program doesn't handle correctly format date YYYY/month/DD in custom date  | High | To Do | https://github.com/kattypatty/Random-Date-Generator-Test-Report/issues/4|
|   BUG-005 | `TC-009` | The program doesn't generate a last day of the month  | High | To Do | https://github.com/kattypatty/Random-Date-Generator-Test-Report/issues/6|
|   BUG-006 | `TC-0011` | The program generates days values with insufficient input value  | Medium | To Do | https://github.com/kattypatty/Random-Date-Generator-Test-Report/issues/7|
|   BUG-007 | `TC-0013` | The program generates a random number of the months without of month boundary | High | To Do | https://github.com/kattypatty/Random-Date-Generator-Test-Report/issues/8|
|   BUG-008 | `TC-0013` | The program generates seconds values with insufficient input value | Medium | To Do | https://github.com/kattypatty/Random-Date-Generator-Test-Report/issues/9|

# Conclusion:
Overall, the random date generator performs as expected for valid inputs, with the exception of leap day generation, and handles mostly edge cases other than the month-end day. As expected, the program doesn't handle invalid inputs or insufficient inputs. For other edge cases, additional testing is recommended to ensure long-term stability.
