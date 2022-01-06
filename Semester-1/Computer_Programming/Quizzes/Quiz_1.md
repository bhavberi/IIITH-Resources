# Computer Programming (CS0.101)
### [Monsoon 2021-22]
---
## Quiz - 1
---
1.  Select all the correct answers from below.
  - [ ] A pointer contains the address of a variable on the hard disk.
  - [x] A pointer contains the address of a variable in the main memory.
  - [x] An array variable contains the base address of the array.
  - [x] Memory is allocated to a 2D array row by row consecutively.

2. Select all the correct options.
  - [ ] The data of a program are stored in the main memory in hexadecimal format.
  - [ ] The instructions of a program are stored in the main memory in hexadecimal format.
  - [x] The instructions of a program are stored on the hard disk using bits.
  - [x] It is possible for a program to run forever without halting.

3. An array is being passed as a parameter to a function. Pick the correct options from below.
  - [x] Only the base address of the array is passed.
  - [ ] The whole array will be copied to the local memory of the function.
  - [ ] Since the call-by-value parameter passing mechanism is used, any changes to the array elements will not be reflected in the original array.

4. Select the correct statements from the below.
  - [ ] #define -- statement declares a new variable.
  - [ ] math.h contains the code for all the math library functions.
  - [ ] The binary representation of 2 and 2.0 is the same.
  - [ ] The Return type of printf statement is void
  - [x] Any line in your C program which starts with # symbol is precessed by the preprocessor (cpp) program.

5. Select the hardware components required to execute a program.
  - [x] RAM
  - [ ] Display
  - [x] CPU
  - [ ] KeyBoard

6. Write a C Program that read a positive integer as input and outputs **YES** if it is a prime number. Else, it outputs **NO**.

``` C
#include <stdio.h>

int main()
{
    int n; //Our Number for input from User
    int check = 1; //Store whether n is prime or not with initially assuming it as prime ( =1 )

    //Input the number from User
    printf("Please enter the number -> ");
    scanf("%d",&n);

    //Checking that the number is positive
    if ( n<= 0 )
        printf("Sorry, the given number ( %d ) is not a positive number.\nHence, it can't be computed for prime number.",n);
    
    //Checking for Prime Number by checking for any of its factors between 2 and n-1.
    for (int i = 2; i < n; i++)
    {
        if (n%i == 0)
        {
            check = 0;
            break;
        }
    }

    //Displaying the result.
    if (check == 0)
        printf("NO");
    else
        printf("YES");

    printf("\n");
    return 0;
}

```