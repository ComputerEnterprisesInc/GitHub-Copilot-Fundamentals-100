# Creating Unit Test Functions with GitHub Copilot Chat

GitHub Copilot can be used to generate unit test functions for a variety of programming languages. This lab will guide you through the process of creating a calculator program and generating unit tests for each function using GitHub Copilot Chat.

### Task 1

1. Create a new file named `calculator.js`

2. Navigate to GitHub Copilot Chat and give the following prompt:

```
Compose a full JavaScript program for constructing a calculator. This program should have multiple functions to perform the tasks of addition, subtraction, multiplication, division, taking user input, and providing output
```

3. Copy and paste the provided code into the `calculator.js` file that you just created

### Task 2

1. Within `calculator.js` select all of the code and prompt inline GitHub Copilot Chat (Ctrl+I) to extend the program to include square root and exponent functions

```
Extend the program to include a square root function
```

2. Accept the code suggestion provided by GitHub Copilot

3. Repeat the process for the exponent function

```
Extend the program to include an exponent function
```

4. Accept the code suggestion provided by GitHub Copilot

### Task 3

1. Select all of the functions within `calculator.js` and open GitHub Copilot Chat

2. Prompt GitHub Copilot Chat to generate unit tests for the selected code:

```
/tests
```

3. GitHub Copilot Chat will generate a test case for all of the calculator functions, insert this into a new file named `test.js`

4. Once the original suggestions have been accepted, select all of the code in `test.js` and prompt GitHub Copilot Chat to analyze the existing test cases:

```
What scenarios are missing from the existing test cases?
```

5. GitHub Copilot Chat will provide an explanation of the missing test cases, reprompt the tool to generate the missing test cases and insert them into the `test.js` file

### Task 4 

1. Run the test cases in `test.js` to ensure that all of the functions in `calculator.js` are working as expected: 
  - Open the terminal
  - Navigate to the `lab-files` directory
  - run `node test.js`

2. Save your files ensuring that they are in the `lab-files` directory

3. Move onto the [next lab task](lab6-generating-documentation.md)
