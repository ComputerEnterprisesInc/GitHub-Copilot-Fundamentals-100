# Code Refactoring with GitHub Copilot

GitHub code refactoring refers to the process of restructuring and improving the quality of code in a GitHub repository without changing its external behaviour. Code refactoring aims to enhance readability, maintainability, and performance while reducing technical debt and potential bugs. In this lab, you will participate in a learning or practice activity where your main goal will be to use GitHub Copilot for code refactoring using the C# programming language.

## Task 1

1. Look at the example of poorly written C# code in the `poorly_written.cs` file in the `lab-files` directory and analyze it. Take note of how could this code could be improved.

**Here are a few code-related issues:**
- The code begins with the inclusion of the System namespace for essential input and output operations.
- It defines a constant MAX with a value of 100 to represent the maximum number of elements allowed.
- The Sum method calculates the sum of elements in an array.
- In the Main method:
    - It prompts the user to enter the number of elements (between 1 and 100) and validates the input.
    - Allocates an array 'arr' to store the entered integers.
    - Prompts the user to enter the specified number of integers and validates each input.
    - Calculates the sum of the entered integers using the Sum method.
    - Outputs the sum to the console.
    - There's no need to manually free memory in C# because it manages memory automatically.

2. Select all of the code in the `poorly_written.cs` file and open GitHub Copilot Chat. Prompt GitHub Copilot Chat to identify any code-related issues without suggesting improvements. 

```
Identify the code-related issues in the selected code
```

3. GitHub Copilot may provide a list similar to the following: 
  - Lack of Error Handling
  - Inefficient Array Size Declaration
  - Magic Number Usage
  - String Concatenation

4. Compare the identified problems from Step 1 to the identified problems from Step 2, noting where GitHub Copilot had similar or different observations

## Task 2

1. Open the GitHub Copilot Chat window by clicking the **Chat** extension icon

2. Select the code in `poorly_written.cs` and type the prompt `Refactor the selected code`

3. GitHub Copilot chat will give a response that should look similar to the code below: 

```
using System;

class Program
{
    const int MAX = 100;

    static int Sum(int[] arr)
    {
        int result = 0;
        foreach (int numb in arr)
        {
            result += num;
        }
        return result;
    }

    static void Main()
    {
        int n;
        Console.Write("Enter the number of elements (1-100): ");
        if (!int.TryParse(Console.ReadLine(), out n) || n < 1 || n > MAX)
        {
            Console.WriteLine("Invalid input.")
            Environment.Exit(1);
        }

        int[] arr = new int[n];

        Console.WriteLine("Enter " + n + " integers:");
        for (int i = 0; i < n; i++)
        {
            if (!int.TryParse(Console.ReadLine(), out arr[i]))
            {
                if (!int.TryParse(Console.ReadLine(), out arr[i]))
                {
                    Console.WriteLine("Invalid input. Please enter valid integers.");
                    Environment.Exit(1);
                }
            }
        
        int total = Sum(arr);

        Console.WriteLine(Sum of the numbers: " + total);
        }
    }
}
```

**Note: The code provided by GitHub Copilot may not be perfect. You may need to make some adjustments to the code to ensure it works correctly. The code may also look differently than the above example**

4. Analyze the changes made to the code by GitHub Copilot Chat. What has changed?

- Here, GitHub Copilot removed the n parameter from the Sum method since it's not needed. Instead, the Copilot used a for-each loop to iterate over the array. As a result, the code is easier to comprehend and more concise.
- This includes the system namespace for input and output operations.
- Defines a constant MAX with a value of 100 for the maximum number of elements allowed in an array.
- The Sum method calculates the sum of elements in an integer array using a for-each loop.
- In the Main method:
    - Asks the user to input the number of elements and validate it.
    - Creates an integer array to store user-entered values.
    - Prompts the user to enter integers, validates the input, and stores them in the array.
    - Calculates the sum of the integers using the Sum method.
    - Shows the sum on the console.
    - The code includes input validation and provides the sum of user-entered integers.

5. Insert the code into a new file named `well_written.cs` into the `lab-files` directory

## Task 3

1. Open the file named `codechat.cs`


2. Ask Copilot to use if-else statements instead of the current switch statement. Identify the second of code where the switch is present, and select it

3. Right-click on the code window and select **Copilot**, from the presented list of options, select **Start Code Chat**

4. Type the prompt `Use if-else statements instead of the switch statement`. Click `>` or press `Enter`

5. Review the response that Copilot provided, click **Accept** or **Discard** based on the code provided

6. Save the changes made to `codechat.cs`

## Task 4 

1. Save your files ensuring that they are in the `lab-files` directory

2. Move onto the [next lab task](lab-handouts/lab5-unit-testing.md)
