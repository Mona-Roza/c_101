# C Basics

## Contents:

* [Variables](#variables)

    * [Variable Range Limits](#variable-range-limits)

    * [Variable Declaration](#variable-declaration)

    * [Considerations When Selecting Variable Names](#considerations-when-selecting-variable-names)

    * [Variable Specifiers](#variable-specifiers)

* [Constants](#constants)
    
    * [Defining Constants with #define](#defining-constants-with-define)

    * [Defining Constants with const](#defining-constants-with-const)

* [Operators](#operators)

    * [Assignment Operators:](#assignment-operators)

    * [Arithmetic Operators](#arithmetic-perators)

    * [Comparison Operators](#comparison-operators)

    * [Logical Operators](#logical-operators)

    * [Other Operators](#other-operators)

* [Usage of printf()](#usage-of-printf)

    * [Format Specifiers](#format-specifiers)

    * [Escape Sequences](#escape-sequences)

* [Usage of scanf()](#usage-of-scanf)

* [Arrays](#arraysarrays)

    * [One-dimensional Arrays](#one-dimensional-arrays)

    * [Multidimensional Arrays](#multidimensional-arrays)

* [Conditional Statements](#conditional-statements)

    * [If-Else Statement](#if-else-statement)

    * [Switch-Case Statement](#switch-case-statement)

* [Loop Statements](#loop-statements)

    * [for](#for)

    * [while](#while)

    * [do…while](#dowhile)

    * [break and continue Statements](#break-and-continue-statements)

    * [goto Statement and Label](#goto-statement-and-label)

* [Functions](#functions)

    * [Function Prototype](#function-prototype)

    * [Function Types](#function-types)

        * [Non-Value Returning Functions](#non-value-returning-functions)

        * [Returning Functions](#returning-functions)
    
    * [Recursive Functions](#recursive-functions)

    * [Sending Arrays as Function Parameters](#sending-arrays-as-function-parameters)
#
* [Algorithm Reinforcement Questions](#algorithm-reinforcement-questions)

    * [Variable Questions](#variable-questions)

    * [Conditional Statement Questions](#conditional-statement-questions)

    * [Loop Statement Questions:ı](#loop-statement-questions)

## Variables:
Variables are symbolic names given to information stored in memory. The values of variables can be changed within the program.
	
* Characters (Letters) -> char (e.g. a, b, c, e, f, ...) (1 byte-8 bit)

* Numbers: 

    * Integers -> int (e.g. 1,2,3,4, -1,-5,-10,...) (4 byte-32 bit)

    * Floating Point:

        - float (e.g. 0.55555) (4 byte- 32 bit)
    
        - double (e.g. 0.55555555) (8 byte- 64 bit)
        
* Words (Strings) -> string (e.g. "mona", "school", "computer",....) (4 byte-32 bit)
    
### Variable Range Limits:

Variables have a certain range limit due to the space they occupy. 

| Data Type | Bit Width | Range Limits |
|---|---|---| 
| char | 8 bit | [-128, 127] |
| int | 32 bit/ 16 bit | [-2 147 483 648, 2.147.483.649] |
| float | 32 bit | [1 17549e-038,  3 40282e+038] | 
| double | 64 bit | [2 22507e-038, 1 79769e+308] |
    
	
### Variable Declaration:

When declaring a variable, the data type/type of the variable must be specified first, then the symbolic name to be given to the variable must be determined. The value of the variable can be given during declaration or at any point in the program. Example usage:

```
    int num;
    num = 5;
```

or

```
    int num =5;
```

### Considerations When Selecting Variable Names:

i. Variable names should be descriptive.

ii. Variable names should not be keywords of the language. (int, char, main, ...)

iii. The first character should be an underscore or letter. (eg: _variable1, variable2, 3rdvariable -> cannot)

iv. No spaces characters.
        
### Variable Specifiers:

Variable specifiers create new data types by adding specifiers before basic variable type names. (eg: short int variable1)

• short: Reduces the value range. Only used for int. Decreases the bit width to 16 bits.

• long: Increases the value range. Only used for int.

• unsigned: Removes the sign bit and moves the range value to the positive sector without changing the range.

• signed: Every variable we define is signed.

• volatile: Prevents the compiler from making an optimization on the variable that is in front of it.

• static: Ensures that the variable in front of it is stored in memory and can be retrieved from the same location when called, so that memory is not exhausted again and again, by being stored in memory after being executed once and until the end of the program.

## Constants:

Constants are variables whose values cannot be changed during the program. The values of constants are given at declaration time and cannot be changed again during the program.
	
### Defining Constants with #define:

Constants defined with #define are recognized globally. As #define is a preprocessor command, constant values specified with #define are placed into the code at compile time and do not occupy memory. Example usage:

    `#define pi  3.14141592653589793`
    
### Defining Constants with const:

Constants defined with const are recognized in the scope where they are defined like variables, and are processed when called at runtime like variables, occupying memory. Example Usage:
    
    `const int pi = 3.141592653589793;`

## Operators:

Operators are characters used in arithmetic operations and control statements that have operation values.

### Assignment Operators:

| Operator | Meaning |
|----|----|
| = | Assignment operator. Assign right-side to the left-side (in compiled languages).|
| sayi1 += sayi2    | sayi1 = sayi1 + sayi2 | 
| sayi1 -= sayi2    | sayi1 = sayi1 - sayi2 |
| sayi1 /= sayi2    | sayi1 = sayi1 / sayi2 |
| sayi1 *= sayi2    | sayi1 = sayi1 * sayi2 |
| sayi1 \|= sayi2    | sayi1 = sayi1 \| sayi2 |
| sayi &= sayi2    | sayi1 = sayi1 & sayi2 |
| sayi1 ^= sayi1    | sayi1 XOR sayi1 |

### Arithmetic Operators:

| Operator | Meaning|
|----|----|
| + | Addition operator. Adds the two numbers on the right and left. |
| -	| Subtraction operator. Subtracts the number on the right from the number on the left.|
| * | Multiplication operator. Multiplies the two numbers on the right and left. |
| / | Division operator. Divides the number on the left by the number on the right. |
| % (Mod) |Modulo operation. (Remainder of division) |
| sayi++ |  Increases the number by one. (Order of operation depends on whether it is on the right or left of the number)|
| sayi-- | Decreases the number by one. (Order of operation depends on whether it is on the right or left of the number) |

### Comparison Operators:

| Operator | Meaning |
|----|----|
| < | Less Than |
| > | Greater Than |
| >= | Greater Than or Equal |
| <= | Less Than or Equal |
| == | Equal? |
| != | Not Equal? |

### Logical Operators:

| Operator | Meaning |
|----|----|
| && | AND |
| &	| Bitwise AND | 
| \|\| | OR(Alt Gr + <) |
| \| | Bitwise OR |
| ^ | Bitwise XOR |
| ! | NOT |
| ~ | Logical negation of the number in relation to (r-1) |

### Other Operators:

| Operator | Meaning |
|----|----|
| (Condition):(if it's true)?(if it's false); | This operator serves as a one-liner condition. |

## Usage of printf():

Used to output to the user. Example usage:

`printf("Text to be printed");`

### Format Specifiers:

| Data Type | Format Specifier |
|---|---|
| char | %c|
| int | %d|
| float | %f | 
| double | %f |
| long double | %Lf |
| pointer | %p |
| unsigned int | %u |
| string | %s |

:warning: Feature for %f: %.(number of decimal places)f

### Escape Sequences:

| Escape Sequence | Represented Symbol | 
|---|---|
| \a | Represents an alert (beep, bell) |
| \b | Backspace |
| \e | Escape character |
| \f | Form Feed Page End | 
| \n | New Line (Line Feed) |
| \r | Line Start |
| \t | Horizontal Tab |
| \v | Vertical Tab |
| \\\ | Backslash |
| \\' | Apostrophe or single quote mark |
| \\" | Double quote mark |
| \\? | Soru işareti (trigraphs) |
| \nnn | Used to precede Octal value represented by nnn |
| \xhh… | Byte represented by hh, hexadecimal number |
| \uhhhh | Unicode code point below 10000 hexadecimal value |
| \Uhhhhhhh | Unicode code point where h is a hexadecimal digit |
	

## Usage of scanf():

Used to receive data from the user. Example usage:

```	
int variable_name;
scanf("%d", &variable_name);
```

## Arrays:

Arrays are a set of variables of the same data type. Using arrays, multiple variables with the same name can be accessed and processed.

Arrays can be defined as one or multi-dimensional.

Arrays can only contain variable values of the same data type since arrays are defined with a specific data type.

### One-dimensional Arrays:

In programs, instead of defining many variables with the same data type and different names, using an array declaration makes it more practical and convenient to define the same number of variables using only one name. Once the array is defined, access to each element of the array can be achieved using the array name and an index value starting from 0 and used with the array name. General format:

```
data_type array_name[dimension];
array_name[0] = a;
array_name[1] = b;
...
array_name[dimension-1] = z;
```

or

`data_type array_name[] = {a, b, ..., z};`

### Multidimensional Arrays:

Multidimensional arrays can be thought of as matrices placed on coordinate planes with two or more axes. The general format of a two-dimensional array is:

```
data_type array_name[x][y];
array_name[0][0] = a;
array_name[0][1] = b;
...
array_name[x-1][y-1] = z;
```

or

`data_type array_name[][] = {{a, b, ..., z}, {a, b, ...,z}};`

:warning: The name of an array is also a pointer that points to the first element of the array.

## Conditional Statements:

Conditional statements are code blocks that change the flow of the program based on certain conditions.

### If-Else Statement:

The if-else statement is a conditional operation. If and else have a single comparison statement and the use of else is optional. If the condition is positive, the set after if is executed and the set after else is skipped; if it is negative, the set after if is skipped and the set after else, if any, is executed. General format:

```
if(condition)
{
    Operation lines
    .
    .
    .
}

else if(secondary_condition) 
{ 
    Operation lines
    .
    .
    .
}

else{ 

    Operation lines
    .
    .
    .

}
```

:warning: Two or more conditions can be combined with logical operators.

### Switch-Case Statement:

A comparison statement that redirects the flow of the program from many options to one based on the contents of a variable. General format:

```
switch(variable)
{
    case value1:
        Code block1;
        .
        .
        .
        break;
        
    case value2:
        Code block2;
        .
        .
        .
        break;
        
    .
    .
    .
    
    case valueN:
        Code blockN;
        .
        .
        .
        break;
    
    default:
        Code block1;
        .
        .
        .
        break;
}
```

:warning: If the value of the variable that is the condition of the switch is not any of the values specified by case, the default code block is executed.

## Loop Statements:

These types of statements are used to repeat a set under certain conditions. There are three types of loop statements in C language, while, do...while and for.

### for:
A set or a statement can be repeated many times using for. The condition check is performed at the beginning (or before entering the loop) of the iteration. To use the for loop, we need a loop counter. The starting value of the loop counter, stopping value, and arithmetic operation applied to the counter in the end of the iteration must be specified in the condition part of the for loop. General format:

```
int i;

for(i= start_value; condition; counter operation)
{
    Repeatable code block;
}
```
:warning: The iteration will be repeated as long as the condition is positive.

### while:

A repetition statement. A set or a statement can be repeated many times using while. The condition check is performed at the beginning of the iteration. General format:

```
while(condition)
{
    Repeatable code block;
}
```
:warning: The iteration will be repeated as long as the condition is positive.

:warning: The while loop can be used just like the for loop. To understand what we need to do, let's examine an example code block.

```
    int i =10;
    
    while(i>0)
    {
        printf("%d", i);
        i--;
    }
```
    
As seen from the example, a starting value is given to the loop variable, and the iteration continues as long as the value satisfies the condition.

:warning: The most important thing to consider in the while loop is assigning a starting value to the variable used in the condition. If no starting value is given to any variable, the content of the variable will take a random value, and if this value makes the condition negative, the loop will not enter. Another point is that the variable used in the condition must be changed within the loop.
		
### do…while:

The difference of this statement from while is that the condition is tested after the loop. In other words, the loop is entered before the condition is tested, and the loop set is executed at least once. General format:
	
```
do
{
    Repeatable set;
    
}while(condition);
```

### break and continue Statements:

While executing the contents inside the loop statements, if it is necessary to terminate the iteration or skip the current iteration and continue with the next one, break and continue statements can be used respectively.
	
* break Statement: When a "break" statement is encountered in a loop, the loop ends immediately, regardless of the condition, and the flow of the program jumps to the next statement or function after the loop. The "break" statement is used to exit from within a "while", "do...while", "for" or "switch" when a specific condition occurs.
		
	:warning: If used inside nested loops, it affects only the innermost loop, and the outer loop continues to run. 
			
* continue Statement: When encountering a "continue" statement in a loop, any statements or functions following it are skipped, and the loop enters the next iteration. It can be considered the opposite of "break". "Break" immediately ends the loop, while "continue" jumps to the next iteration.
		
### goto Statement and Label:
With the help of the "goto" statement, we can create loops. However, it makes the code difficult to read, so it is not recommended by programmers. Nevertheless, it may become necessary to use it at times.

:warning: The "goto" statement is used with a label. First, a label name is given, then the code block is written and the "goto" statement is used to go back to the location specified by the label name. General syntax:

```
int x=1;

etiket1:
    x++;
    if(x<100) 
    {
        goto etiket1;
    }
```

## Functions:

Functions are collections of code that are grouped together in an appropriate manner to perform a specific task. These code blocks can be called as desired. Thus, instead of repeating the same code, the function can be called, making the same code used repeatedly. General structure of a function:

```
return_data_type/void function_name([if any] parameters)
{
    [if any] local definitions
    ...
    code block
    ...
    [if any] return value;
}
```

* return_data_type: If the function is to return a value, the data type of the value to be returned is specified in the function signature.

* function_name: The identifier name used when calling the function. The rules to follow for variable names also apply here.

* parameters: If any, it includes the values and types required for use within the function. Each parameter is defined like a variable definition. If more than one parameter is used, they are separated by commas (,).

:warning: If the variables sent as parameters to the function are changed in value within the function, they will return to their original values when the function is finished. However, if the address of a variable is sent as a parameter to the function and its value is changed through this address, this change will be permanent.

* local definitions: definitions that are specific to the function, such as variables and constants. These variables are stored in memory during the function's execution and then deleted from memory.

### Function Prototype:

If a function is defined after the main function, a prototype must be written before the main function for that function. However, function prototypes are not necessary for functions defined before the main function. Its general structure is derived from the signature of the function:

`return_data_type/void function_name([if any] parameters);`

### Function Types:
There are two types of functions. These are value-returning functions and non-value returning functions.

#### Non-Value Returning Functions:

Non-value returning functions are used like subprograms and are called by the main function or other functions. The operations in the function are executed, but they do not return any value to the calling function. General structure:

```
void function_name([if any] parameters)
{
    ...
    code block
    ...
}
```

#### Returning Functions:

In returning functions, the value generated by the function is returned to the calling function with the return statement and this value is used there. Its general structure is:

```
return_type function_name([if any] parameters)
{
...
code block
...
return return_value;
}
```

:warning: The code written after the **return** statement is not processed, this statement immediately stops the function from running when processed.

### Recursive Functions:

Functions that directly or indirectly call themselves. In some applications, writing algorithms in recursive functions is easier and simpler. Applications written using loop statements can also be carried out using recursive functions. General structure:

```
return_type function_name([optional] parameters)
{
    ...
    code block
    ...

    if(condition)
    {
        return function_name([optional] parameters);
    }
    else
    {
        return value;
    }
    
}
```

### Sending Arrays as Function Parameters:

Within the context of what we've seen so far, it's not possible to change the values of parameters sent to functions because only the value of the variable is sent to the function. The parameter itself is not affected by the operations in the function. This is not the case with arrays. Normally, when an array is sent to a function, its elements can be changed because, as we stated in the arrays section, the name of an array is also a pointer that points to the first element of the array. As a result, when an array is sent, it is sent along with the addresses of its elements, so they are affected by any changes in the function. Its general structure:

```
return_type/void function_name(data_type parameter_array[])
{
    ...
    code block
    ...
    [optional] return value;
}
```
## Algorithm Reinforcement Questions:

### Variable Questions:
* Type a program that calculates the area of a triangle given the length of a side and its height.

* Type a program that displays the VAT-inclusive price after VAT (%18) is added to a given price.

* Type a program that calculates the circumference and area of a circle given its radius. (π = 3.14 and is taken as constant)

### Conditional Statement Questions:

* Type a program that displays whether a given number is positive or negative.
Algorithm and flowchart that displays which of two given numbers is smaller.

* Type a program that calculates the weighted average of a student's quiz and final grades. (Calculate the weighted average by taking 30% of the quiz score and 70% of the final score, will they pass or fail? If the final score is below 60, they fail, if the average is below 50, they fail)

* Type a program that calculates whether a given number is odd or even and displays the result.

* Type a program that calculates the absolute value of a given number and displays the result.

* Type a program that displays whether a given x is a multiple of another given y.

## Loop Statement Questions:

* Type a program that prints numbers from 1 to 1000.
s
* Type a program that calculates the sum of integers from 1 to N.

* Type a program that prints the multiplication table.

* Type a program that prints a part of the multiplication table (when 5 is entered, it prints 5's, when 10 is entered, it prints 10's).

* Type a program that calculates the user entered number raised to the power of another number entered by the user.

* Type a program that calculates the factorial of a positive integer entered by the user.

* Type a program that checks whether a given number is prime.

* Type a program that calculates the prime numbers from 1 to 100.

* Type a program that finds the divisors of a positive integer entered by the user and displays them on the screen.

* Type a program that calculates the prime factors of a given number.

* Type a program that prints the perfect numbers from 1 to 1000. (e.g.: 6=1+2+3, the sum of its divisors)

* Type a program that prints an empty square.

* Type a program that prints the first 10 elements of the Fibonacci sequence.

* Type a program that separates and prints the digits of a given number.

* Type a program that tells how many digits a given number has.

* Type a program that reverses a given number.

* Type a program that calculates the Armstrong numbers from 1 to 1000. (e.g.: 153 is 1 to the power of 3 + 5 to the power of 3 + 3 to the power of 3)

* Type a program that finds the palindrome numbers from 1 to 1000. (121)

* Type a program that prints the perfect numbers from 1 to 1000. (numbers that are equal to the sum of the factorials of their digits are called perfect numbers. e.g.: 145 = 145! + 4! + 5!)