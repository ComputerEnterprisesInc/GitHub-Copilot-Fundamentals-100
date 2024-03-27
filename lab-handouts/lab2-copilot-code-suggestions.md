# Experimenting with JavaScript AI Code Suggestions

In this exercise, you will have the opportunity to experiment with in-file code suggestions, multiple suggestions, and comprehensive code suggestions with the assistance of GitHub Copilot and GitHub Copilot Chat.

## Task 1

1. reate a new file in the `lab-files` directory named `skills.js` and verify that it is empty

2. In the `skills.js` file, type the following function declaration. A whole function body will be suggested by GitHub Copilot (shown in gray text). Precise recommendations will vary

```
function calculateNumbers(var1, var2)
```

4. Press `Tab` to accept the suggestion provided by GitHub Copilot, review, and save the file

5. In the `skills.js` file, type the following function declaration for solving the quadratic function, again a whole function body will be suggested by GitHub Copilot (shown in gray text)

```
function quadraticFormula(a, b, c)
```

6. Press `Tab` to accept the suggestion provided by GitHub Copilot, review, and save the file

## Task 2 

1. Still in the `skills.js` file, type a comment to describe a function that calculates the price of a vehicle based on its gas mileage, year, and number of miles driven

```
// Create a function that calculates the price of a vehicle based on gas mileage, year and number of miles driven.
```

2. GitHub Copilot will provide suggestions for the function body. It is possible that the tool will provide multiple suggestions, iterate through them, by pressing the arrow `>` and press tab to accept the suggestion that you most prefer

3. Recommendations may look similar to the following code: 

```
function calculatePrice(milesPerGallon, year, milesDriven) {
  var price = 0;
  if (year < 2010) {
    price = 10000;
  } else {
    price = 20000;
  }
  if (milesPerGallon < 15) {
    price += 2000;
  }
  if (milesDriven > 10000) {
    price -= 5000;
  }
  return price;
}
```

## Task 3

1. Create a **New File**, name your file `index.js` and verify that the file is empty and in your `lab-files` directory

2. In `index.js` press `Ctrl + I` to open GitHub Copilot Chat and paste the following comments to create a basic markdown editor

```
Create a basic markdown editor in Next.js with the following features:
- Use react hooks
- Create a state for markdown with the default text "type markdown here"
- A text area where users can write markdown 
- Show a live preview of the markdown text as I type
- Support for basic markdown syntax like headers, bold, and italics 
- Use React markdown npm package 
- The markdown text and resulting HTML should be saved in the component's state and updated in real-time 
```
3. This should prompt GitHub Copilot to generate code to produce a simple, unstyled, markdown editor, accept the suggestion provided by GitHub Copilot

4. In the same `index.js` file, enter the following instructions for reversing a sentence into GitHub Copilot Chat

```
Create a function that takes a sentence as input, reverse the input sentence, the start of the sentence must start with a capital. This should be done in JavaScript.
```

5. The generated outcome should look similar to this: 

```
const reverseAndCapitalize = (sentence) => {
    const reversed = sentence.split(' ').reverse().join(' ');
    return reversed.charAt(0).toUpperCase() + recersed.slice(1);
}

console.log(reverseAndCapitalize('hello world')); 
console.log(reverseAndCapitalize('welcome to my test'));
```

## Task 4

1. Create a new file named `multiple.py` in the `lab-files` directory and verify that the file is empty

2. In the `multiple.py` file, type the following code to create a function that determines if a number is prime:

```
def prime(n):
```

3. Open a new tab with _multiple_ solutions by pressing `Ctrl + Enter`. GitHub Copilot will generate around 5 different code suggestions in a new tab. Here, you can view all of the solutions generated by the AI model (amounts may vary)

4. Accept a suggestion (by clicking on **Accept Solution**)

***Note:Some suggestions provided by GitHub Copilot will be more accurate to your use case than others, please review code carefully to ensure that you are accepting code that will work correctly for your development needs.**

5. In the same file `multiple.py`, type the following code to create a password generator function: 

```
def generate_password(length):
```

6. Open a new tab with _multiple_ solutions by pressing `Ctrl + Enter`. GitHub Copilot will generate around 8 different code suggestions in a new tab. Here, you can view all of the solutions generated by the AI model (amounts may vary)

7. Accept a suggestion (by clicking on **Accept Solution**), your suggestion _may_ look similar to the following code: 

```
def generate_password(length):
    return ''.join(random.choices(string.ascii_letters + string.digits, k=length))
```

**Note: Some suggestions provided by GitHub Copilot will be more accurate to your use case than others, please review code carefully to ensure that you are accepting code that will work correctly for your development needs.**

## Task 5

1. Save your files to the `lab-files` directory

2. Move onto the [next lab task](lab-handouts/lab3-scripting.md)