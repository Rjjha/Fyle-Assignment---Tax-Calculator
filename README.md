# Tax-Calculator
This is a simple tax calculator implemented in JavaScript. It calculates the overall income after considering gross income, extra income, age group and deductions. Additionally, it provides validation for input fields.

## References & Requirements
- The tax calculation works based on this formula -
    - Overall income (after deductions) under 8 (≤) Lakhs is not taxed.
        - Ex - if Gross Annual Income + Extra Income - Deductions =  6 Lakhs, no tax
        - if Gross Annual Income + Extra Income - Deductions =  9 Lakhs, tax
    - Income over 8 (>) Lakhs, the amount over 8 Lakhs is taxed at
        - 30% for people with age < 40
        - 40% for people with age ≥ 40 but < 60
        - 10% for people with age ≥ 60
        - Example
            - Age = 34, Income = 40 Lakhs, no deductions, tax = .3 * (40 - 8) = .3 * 32 = 9.6 Lakhs
- Do not restrict the user from entering incorrect values like characters in the number fields
    - Highlight an error icon to the right of the input field (shown as an example in the above image as a circle with `!`). Hovering over it should show the error in a tooltip
    - If no errors are present, don't show the error icon
    - This should be present in all the number fields
- The age dropdown field should have 3 values -
    - <40
    - ≥ 40 & < 60
    - ≥ 60
    - If the user has not entered this value and clicks on submit, show an error icon hovering over which should show that the input field is mandatory
- Error icons should not be visible in the form by default.
- Clicking on submit should show a modal which would show the final values based on the above calculations.

## Assumptions
- **Input Validation:**
  - Input values are validated on focus, change, and when the submit button is clicked.
  - Errors are displayed to the user under the following conditions:
    - Typing a number less than zero results in an error message "Please type non-negative numbers".
    - Clicking on an input field and not typing anything or leaving any field empty and clicking the submit button results in an error message "This input field is mandatory".
    - Typing anything other than a number results in an error message "Please type numbers only".
- **Overall Income Calculation:**
  - If the sum of gross income, extra income, and deductions is less than or equal to 8 lakhs, the overall income is displayed as the sum of gross income and extra income.

## Run Locally
To run your application locally, follow these steps:
1. **Download the Code**: Download the HTML, CSS, and JavaScript files to your local machine.
2. **Open HTML File**: Open the HTML file in your preferred web browser. You can do this by double-clicking the HTML file or right-clicking and selecting "Open with" and choosing your web browser.
3. **Ensure Internet Connection**: Since your application uses Bootstrap icons via CDN links, ensure that you have an internet connection while running the application locally. If you don't have an internet connection, the icons may not be visible.
4. **Interact with the Application**: Once the HTML file is opened in your web browser, you can interact with the tax calculator just like you would on a live website. Input values, click the submit button, and verify that the calculations and error messages work as expected.

## Usage
To use the tax calculator:
- Input the gross income, extra income, age group, and total deductions.
- Click the submit button to calculate the overall income and display the result.
- If any input is invalid, error messages will be shown to guide the user on how to correct the inputs.

## Test Cases
**Case 1: Tooltip is shown when hovering over the question mark icons**

<img src="https://github.com/Rjjha/Fyle-Assignment---Tax-Calculator/assets/96972257/fc3690bb-ed41-40d6-a711-ef697bbb5527" alt="Case 1" width="500"/><br/>

**Case 2: Display error icons if the user clicks the submit button without entering input. Error message states "This input field is mandatory"**<br/>
*Image 1: After clicking the submit button for empty fields

![pic2](https://github.com/Rjjha/Fyle-Assignment---Tax-Calculator/assets/96972257/6f313a26-af3a-49d6-8834-ef0fd432b2f9)


**Case 3: Error icons will appear if a negative value is entered in the Number fields. These fields only accept 0 or positive numbers. Error message states "Please enter non-negative numbers only"**

<img src="https://github.com/Rjjha/Fyle-Assignment---Tax-Calculator/assets/96972257/6b6b83c7-4c75-412d-b8f1-ac28212e62d0" alt="Case 3" width="500"/><br/>

**Case 4: Error icons will appear if characters are entered in the Number fields instead of a number. Error message states "Please enter numbers only."**

<img src="https://github.com/Rjjha/Fyle-Assignment---Tax-Calculator/assets/96972257/2e3e2c6c-777b-424e-a809-4d5ff02549dc" alt="Case 4" width="500"/><br/>

**Case 5: Display error icons when all number fields are filled, but the age group is not selected. Error message states "This input field is mandatory."**

<img src="https://github.com/Rjjha/Fyle-Assignment---Tax-Calculator/assets/96972257/1322eb01-2f36-4c6b-a08d-64b56af69cb7" alt="Case 5" width="500"/><br/>

**Case 6: If Gross Income +  Extra Income - Total Deductions is ≤ 8 lakhs then no income tax is applicable. So overall income will be Gross Income +  Extra Income.**

![Untitled design](https://github.com/Rjjha/Fyle-Assignment---Tax-Calculator/assets/96972257/f377d9e4-cfc8-4d26-a3c2-d53e6355cc8f)


**Case 7: If Gross Income +  Extra Income - Total Deductions is > 8 lakhs then income tax is applicable based on age group. So overall income will be calculated accordingly.**<br/>
*1. Age < 40*

![image](https://github.com/KamiyaGaikwad/Tax-Calculator/assets/79163529/a9188665-8a8b-4268-8f84-26f5f04a2c2b)

*2. Age ≥ 40 & < 60*

![image](https://github.com/KamiyaGaikwad/Tax-Calculator/assets/79163529/90798032-3d62-40bb-ba9a-dd14ce28b2a3)

*3. Age ≥ 60*

![image](https://github.com/KamiyaGaikwad/Tax-Calculator/assets/79163529/a2f0867e-4d9e-4fbc-af15-eb408b1e1b50)


