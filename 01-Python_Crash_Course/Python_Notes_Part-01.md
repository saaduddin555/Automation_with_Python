Python Crash Course of IT Automation, Week 1 and Week2 Notes.

# Week_1

Key Terms:
Programming code - Programming code is a set of written computer instructions, guided by rules, using a computer programming language. It might help to think of the computer instructions as a detailed, step-by-step recipe for performing tasks. The instructions tell computers and machines how to perform an action. Programming code may also be referred to as source code or scripts.

Programming languages - Programming languages are similar to human spoken languages in that they both use syntax and semantics. Programming languages are used to write computer programs.  Some common programming languages include Python, Java, C, C++, C#, and R.

Syntax - Syntax is a set of rules for how statements are constructed in both human and computer languages. Programming syntax includes rules for the order of elements in programming instructions, as well as the use of special characters and their placements in statements. This concept is similar to the syntax rules for grammar and punctuation in human language.

Semantics - Semantics refers to the intended meaning or effect of statements, or collections of words, in both human and computer languages. Semantic errors are also referred to as logical errors.

Computer program - A computer program is a step-by-step list of instructions that a computer follows to reach an intended goal. It is important to be clear and precise about the actions a computer program is supposed to perform because computers will do exactly what they are instructed to do. Computer programs can be long, complex, and accomplish a variety of tasks. They are often developed by computer programmers and software engineers, but anyone can learn to create them. Computer programs may involve a structured development cycle. They can be written in a wide variety of programming languages, such as Python, Java, C++,  R, and more. The completed format of a program is often a single executable file.

Script - Scripts are usually shorter and less complex than computer programs. Scripts are often used to automate specific tasks. However, they can be used for complex tasks if needed. Scripts are often written by IT professionals, but anyone can learn to write scripts. Scripts have a shorter, less structured development cycle as compared to the development of complex computer programs and software. Scripts can be written in a variety of programming languages, like Python, Javascript, Ruby, Bash, and more. Some scripting languages are interpreted languages and are only compatible with certain platforms.

Automation - Automation is used to replace a repetitive manual step with one that happens automatically. 

Output - Output is the end result of a task performed by a function or computer program. Output can include a single value, a report, entries into a database, and more. 

Input - Input is information that is provided to a program by the end user. Input can be text, voice, images, biometrics, and more.   

Functions - A function is a reusable block of code that performs a specific task.

Variables - Variables are used to temporarily store changeable values in programming code. 
print ("I'm programming in Python!")
---

A Note on Syntax and Code Blocks
When writing code, using correct syntax is critical. Even a small typo, like a missing parenthesis bracket or an extra comma, can cause a syntax error and the code won't execute at all. If your code results in an error or an exception, pay close attention to syntax and watch out for minor mistakes. A single wrong character could take hours to identify in long code so it is important to be mindful of syntax when writing code. 

Common syntax errors:
Misspellings

Incorrect indentations

Missing or incorrect key characters:

Bracket types - ( curved ), [ square ], { curly }

Quote types - "straight-double" or 'straight-single', “curly-double” or ‘curly-single’

Block introduction characters, like colons - :

Data type mismatches

Missing, incorrectly used, or misplaced Python reserved words

Using the wrong case (uppercase/lowercase) - Python is a case-sensitive language 

If your syntax is correct, but the script has unexpected behavior or output, this may be due to a semantic problem. Syntax is like the vocabulary, grammar, spelling, and punctuation of code. Semantics are the meaning and logic of coded statements. It is possible to have syntactically correct code that runs successfully, but doesn't do what we want it to do.

Common semantic errors:
Creating functional code, but getting unintentional output

Poor logic structures in the design of the code

When working with the code blocks in exercises for this course, be mindful of syntax and semantic (logic) errors, along with the overall result of your code. Just because you fixed an error doesn't mean that the code will have the desired effect when it runs! Once you’ve fixed an error in your code, don't forget to click Run to check your work.
---

Study Guide: First Programming Concepts
This study guide provides a quick-reference summary of what you learned in this lesson and serves as a guide for the upcoming practice quiz.  

Functions 
A function is a piece of code that performs a unit of work. In the examples you've seen so far, you have only encountered the print() function, which outputs a message to the screen. You will use this function frequently in this course to check the results of your code. The syntax of the print() function is modeled in the example below. 

123
#Syntax for printing a string of text. Click Run to check the result.

print("Hello world!")
Reset
Keywords
A keyword is a reserved word in a programming language that performs a specific purpose. In your first Python example, you briefly encountered the keywords for and in.  Note that keywords will often appear in bold in this course. 

In the next few weeks, you will also learn the following keywords:

Values: True, False, None
Conditions: if, elif, else
Logical operators: and, or, not
Loops: for, in, while, break, continue
Functions: def, return  

You don't need to learn this whole list now. We'll dive into each keyword as we encounter them. There are additional reserved keywords in Python. If you would like to read about them, please visit the linked “Python Keywords” article in the Resources section at the end of this study guide. 

Arithmetic operators
Python can calculate numbers using common mathematical operators, along with some special operators, too:  

x + y            Addition + operator returns the sum of x plus y
x - y             Subtraction - operator returns the difference of x minus y
x * y            Multiplication * operator returns the product of x times y
x / y             Division / operator returns the quotient of x divided by y
x**e            Exponent ** operator returns the result of raising x to the power of e 
x**2            Square expression returns x squared
x**3            Cube expression returns x cubed
x**(1/2)    Square root (½) or (0.5) fractional exponent operator returns the square root of x
x // y           Floor division operator returns the integer part of the integer division of x by y
x % y          Modulo operator returns the remainder part of the integer division of x by y

Order of operations
The order of operations are to be calculated from left to right in the following order: 

Parentheses ( ), { }, [ ]

Exponents xe   (x**e)

Multiplication * and Division /  

Addition + and Subtraction -    

 You might find the PEMDAS mnemonic device to be helpful in remembering the order.   


Resources for more information
For more information about the concepts covered in this reading, please visit:

Built-in Functions - Lists and summarizes Python’s built-in functions.

Python Keywords - Lists Python’s reserved keywords and a brief description of what each keyword does.

Different Arithmetic operators in Python - Provides more examples of the proper syntax for using arithmetic operators in Python.
---
Syntax for printing a string of text. Click Run to check the result.

print("Hello world!")

Examples of Python code:

print (2+10)
To add 2 and 10 we define as above

print (2-10)
To subtract 2 and 10 we define as above

print (2/10)
To divide 2 times of 10 we define as above

print (2*10)
To Multiple 2 times of 10 we define as above

print (2**10)
To define power 2 to power of 10, we write syntax as above

print (-2/-10)
we can use negetive and postive values and write code to get output

print (((1+2)*3)/4)
we can combine multiple operators such as add subract divide multiple in a single expression as above and get result
Here the () the parantheses is used to segreegate the values from one another and get desired output as above example.

Syntax for printing a string of text
print("I love Python!")


Syntax for printing numeric values
print(360)
print(32*45)


Syntax for printing the value of a variable
value = 8*6
print(value)

Question 1
What are functions in Python?
Functions are pieces of code that perform a unit of work.

What are keywords in Python?
Keywords are reserved words that are used to construct instructions.

What does the print function do in Python?
The print function outputs messages to the screen

Problem:
Complete the code so that the string "I am writing Python code!" will print to the screen. Remember that syntax precision is important in programming languages. A missing capital letter, spelling error, or punctuation mark can produce errors. 

Replace the blanks with the correct code and syntax:
print("I am writing Python code!")

Should print: I am writing Python code!

What should be the output of the expression below?
print(6*2-5/(1+4)+3**2)

Problem: Keeping in mind there are 86400 seconds per day, write a program that calculates how many seconds there are in a week, if a week is 7 days.  Print the result to the screen. Note: Your result should be in the format of just a number, not a sentence.

Seconds = 86400
week = 7
print (Seconds*week)

Hint: Should print 604800

* Problem
Mercury has a diameter of approximately 1,516 miles.  Earth has a diameter of approximately 3,959 miles.  Use Python to calculate how much larger Earth’s diameter is than Mercury's (in miles). Note: Your result should be in the format of a number, not a sentence.

Earth_Diameter = 3959
Mercury_Diameter = 1516
print (Earth_Diameter-Mercury_Diameter)
Should print 2443

* Consider this scenario about using Python to make calculations:
In a managed computing environment, there are 200 remote computers that must download 200 MB (megabytes) of updates each month.  There are 1024 KB (kilobytes) in each MB.  

Fill in the blank in the code below to compute the number of total kilobytes downloaded by these computers from the remote update server each month.

download_size_kb = 200*1024
total_computers = 200
total_kbs = (download_size_kb*total_computers)

print(total_kbs) # Should print 40960000.0

END of Week_1
----

# Week 2

Topic: Expressions and Variables

Data_types= String, Integer, float, Boolean

You can add string + string 

You can add integer + Integer


but 

you cannot use any operator to calculate with one to other data type like String + Integer = error as it understands similar data type automatically

TO know which data type an interpreter is understanding for a particular line of expression or code
we can use 

print(type(value_here)) to know which datatype it is ...

Eg: 

print(type(102533))

print(type("I am writing a datatypes"))

print(type(2.5))

In Python, text in between quotes -- either single or double quotes -- is a string data type. An integer is a whole number, without a fraction, while a float is a real number that can contain a fractional part. For example, 1, 7, 342 are all integers, while 5.3, 3.14159 and 6.0 are all floats. When attempting to mix incompatible data types, you may encounter a TypeError. You can always check the data type of something using the type() function.

Eg: To check data type: 
print(type(102533))

Q1:
print("1234"+5678)
Because Python doesn't know how to add an integer or float data type to a string.

* Assignment: The process of storing a value inside a variable is called as assignment.
* Expression: A combination of numbers, symbols, or other variables that produce a result when evaluated.

variable later to read or modify the value. Let's see this in action. Imagine a simple script that calculates the area of a rectangle using the formula area equals length times width. Area, length and width can all be represented by variables like this. length = 10 width = 2 area = length * width In this script we are creating three variables and storing different values in each. The process of storing a value inside a variable is called assignment. 

Ex_script:

length = 10
width = 2
area = length * width
print(area)

Q2: Fill in the blanks to calculate the area of a triangle of base 5, height 3 and output the result.  Reminder:  the area of a triangle is (base*height)/2.

base = 5
height = 3
area = ((base * height)/2)

print(area)

* Valid and InVaild Variables

i_am_a_variable is valid
i_am_a_variable2 is valid
1_is_a_number is invalid        (This is invalid because )
apples_&_oranges is invalid     (This is invalid because it is using the special charecter)

You might have noticed that we assign a value to a variable by using the equal sign in the form of variable equals value. Generally, you can name variables whatever you like but there are some restrictions. First, you shouldn't use as variable names any of the key words or functions that Python reserves for its own, like print. Using these reserved terms will make your program confusing to read and will result in errors. Python also has some restrictions on the characters you can use to define a variable. Variable names can't have any spaces and they must start with either a letter or an underscore. Also, they can only be made up of letters, numbers and underscores. Let's check out some examples of valid and invalid variable names to understand this better.

I_am_a_variable is the valid variable name.

I_am_a_variable2 is also a valid variable name. 

1_is_a_number is invalid because variable names must start with a letter or underscore. Apples_&_oranges is invalid because it uses the special character ampersand. Last thing, remember that precision is important when programming. 

Python variables are case sensitive, so capitalization matters. Lowercasename, uppercasename and ALLCAPSNAME are all valid and different variable names, and that rule on variables is invariable.

* Expressions, Numbers, and Type Conversions.

Implicit Conversion: The Interpreter automatically converts one datatype into another.

we can add 
strings to one another like alphabets and Numbers and symbols too

Eg:
print("this "+ "is "+ "pretty "+ "neat!")

We can combine one datatype to another using Explicit conversion.
we can call str() function to do this using explicit conversion, it is basically calling a datatype function to do the output.

Eg:

total = 2048 + 4357 + 97658 + 125 + 8
files = 5
average = total / files
print("The average size is: " + str(average))

Here, average is a variable which gives an output to the calculative value at end as string.

hence we can use alphabets and Numbers as string by explicit conversion, as we know numbers are generally either float or Integer.
---
Implicit vs Explicit Conversion: 
As we saw earlier in the video, some data types can be mixed and matched due to implicit conversion. Implicit conversion is where the interpreter helps us out and automatically converts one data type into another, without having to explicitly tell it to do so.

By contrast, explicit conversion is where we manually convert from one data type to another by calling the relevant function for the data type we want to convert to. We used this in our video example when we wanted to print a number alongside some text. Before we could do that, we needed to call the str() function to convert the number into a string. Once the number was explicitly converted to a string, we could join it with the rest of our textual string and print the result.
---

Study Guide: Expressions and Variables
This study guide provides a quick-reference summary of what you learned in this lesson and serves as a guide for the upcoming practice quiz.  

In the Expressions and Variables segment, you learned about expressions, variables, and the data types: string, integer, and float. You learned how to convert a value from one data type to another and you learned how to resolve a few common errors in Python.

Terms
expression - a combination of numbers, symbols, or other values that produce a result when evaluated

data types - classes of data (e.g., string, int, float, Boolean, etc.), which include the properties and behaviors of instances of the data type (variables)

variable - an instance of a data type class, represented by a unique name within the code, that stores changeable values of the specific data type

implicit conversion - when the Python interpreter automatically converts one data type to another

explicit conversion - when code is written to manually convert one data type to another using a data type conversion function:

str() - converts a value (often numeric) to a string data type

int() - converts a value (usually a float) to an integer data type

float() - converts a value (usually an integer) to a float data type

 

Coding skills
Skill Group 1

Use the assignment operator =  to assign values to variables

Use basic arithmetic operators with variables to create expressions

Use explicit conversion to change a data type from float to string

  
Eg:

* The following lines assign the variable to the left of the = 
  assignment operator with the values and arithmetic expressions 
  on the right side of the = assignment operator.

hotel_room = 100
tax = hotel_room * 0.08
total = hotel_room + tax
room_guests = 4
share_per_person = total/room_guests 
 
* This line outputs the result of the final calculation stored
in the variable "share_per_person"
print("Each person needs to pay: " + str(share_per_person)) # change a data type



Skill Group 2

Output multiple string variables on a single line to form a sentence

Use the plus (+) connector or a comma to connect strings in a print() function

Create spaces between variables in  a print() function

* The following 5 lines assign strings to a list of variables.
salutation = "Dr."
first_name = "Prisha"
middle_name = "Jai"
last_name = "Agarwal"
suffix = "Ph.D."
 
print(salutation + " " + first_name + " " + middle_name + " " + last_name + ", " + suffix) 
The comma as a string ", " adds the conventional use of a comma plus a 
space to separate the last name from the suffix.
 
Alternatively, you could use commas in place of the + connector:
print(salutation, first_name, middle_name, last_name,",", suffix)

However, you will find that this produces a space before a comma within a string

Skill Group 3
Resolve TypeError caused by a data type mismatch issue
Use an explicit conversion function

print("5 * 3 = " + str(5*3)) 
 
* Resolution: 
print("5 * 3 = " + str(5*3))
To avoid a type error between the string and the integer within the
print() function, you can make an explicit data type conversion by
using the str() function to convert the integer to a string.  

Skill Group 4
Resolve a ZeroDivisionError caused by an attempt to divide by 0

numerator = 7
denominator = 2   # Possible resolution: Change the denominator value 
result = numerator / denominator
print(result)
 
One possible assumption for a number divided by zero error might
include the issue of a null value as a denominator (could happen when
using a loop to iterate over values in a database). In such cases, the
desired outcome may be to leave the numerator value intact. The
numerator value can be preserved by reassigning the denominator with 
the integer value of 1. The result would then equal the numerator.
---

* Functions in Python

Define Functions: 

Examples of Built in functions
print()
type()
str()

How to write a greeting function, you can give any function name instead of greeting: 

def greeeting(name):
    print("Welcome, " + name)                 This is a basic function 

TO call a function in python code,

greeting("Mirza")

The output will be:

Welcome, Mirza

def greeeting(name):
    print("Welcome, " + name)

 In this piece of code, [on screen] def greeting(name): we're defining a function. [on screen] print("Welcome, " + name) Our function takes the parameter, here that parameter is name and prints a greeting for that name. This snippet is small but it already shows a lot of important points about how we define functions in Python. Let's go through this step-by-step. To define a function, we use the def keyword. The name of the function is what comes after the keyword. In this example, the function's name is greeting. So to call the function later in the script, we'll use the word greeting. After the name, we have the parameters of the function which are written between parentheses. In this example, we only have one parameter, name, followed by a colon at the end of the line. After the colon, we have the body of the function. That's where we state what we want our function to do. Note how the body is indented to the right. This is a key characteristic of Python and we'll come across it a bunch. For now, just keep in mind that the body of the function must be to the right of the definition. In this example, the body contains just one line that calls the print function.


Eg2:

def greeting(name, department):
    print("Welcome, " + name)
    print("You are part of " + department)

greeting ("Mirza", "DevOps_Enginner")

The Output will be:

Welcome, Mirza
You are part of DevOps_Enginner

We can combine multiple things and write a function as per above example.

The Functions can do alot more than just printing things..

Defining Functions:

We looked at a few examples of built-in functions in Python, but being able to define your own functions is incredibly powerful. We start a function definition with the def keyword, followed by the name we want to give our function. After the name, we have the parameters, also called arguments, for the function enclosed in parentheses. A function can have no parameters, or it can have multiple parameters. Parameters allow us to call a function and pass it data, with the data being available inside the function as variables with the same name as the parameters. Lastly, we put a colon at the end of the line.

After the colon, the function body starts. It’s important to note that in Python the function body is delimited by indentation. This means that all code indented to the right following a function definition is part of the function body. The first line that’s no longer indented is the boundary of the function body. It’s up to you how many spaces you use when indenting -- just make sure to be consistent. So if you choose to indent with four spaces, you need to use four spaces everywhere in your code.

* Returning Values in functions

Return values are used to return a value multiple times in a code
The return values is defined with keyword "return"

As per below example"

base=6
height=3
area=(base*height)/2

Earlier we use to define like this to calculate are of a traingle, what if, if we want to use the same area multiple times in a code or if we would like to calculate more that one traingles area

so, we use return keyword to hold that value so that we can use that value in later part of code again and again,

def area_triangle(base, height):
    return base*height/2

we tell python to return a value as a variable in a function.

def area_triangle(base, height):
    return base*height/2

area_a = area_triangle(5,4)
area_b = area_triangle(7,3)
sum = area_a + area_b
print("The sum of both area is: " + str(sum))

The Output for both triangles of are is 20.5

Eg2:

def convert_seconds(seconds):
    hours = seconds // 3600
    minutes = (seconds - hours * 3600) // 60
    remaing_seconds = seconds - hours *3600 - minutes * 60
    return hours, minutes, remaining_seconds

hours, minutes, seconds = convert_seconds(5000)
print(hours, minutes, seconds)

// This doubel slash operator is called as floor division., This operator eliminates the decimal values

Eg: 2.5 as result with decimal form is eliminated, if we use // operator we get reult as 2 instead of decimal value as 2.5

* none : This is also a data type which print none results without any value.
None is a very special data type in Python used to indicate that things are empty or that they return nothing.

def greeting(name):
    print("Welcome, " + name)
result = greeting("Mirza")
Welcome, Christine

print(result)

output:none.

Returning Values Using Functions:

Sometimes we don't want a function to simply run and finish. We may want a function to manipulate data we passed it and then return the result to us. This is where the concept of return values comes in handy. We use the return keyword in a function, which tells the function to pass data back. When we call the function, we can store the returned value in a variable. Return values allow our functions to be more flexible and powerful, so they can be reused and called multiple times.

Functions can even return multiple values. Just don't forget to store all returned values in variables! You could also have a function return nothing, in which case the function simply exits.

* The priciples of code reuse

Functions are logical blocks which can resuse, Helps to organize the code efficiently

Eg:

name = "kay"
number = len(name) * 9

print("Hello " + name + ". Your lucky number is " +str(number))

name = "Mirza"
number = len(name) * 9

print("Hello " + name + ". Your lucky number is " +str(number))

As per above code, we wrote repeated lines, How come we can define a function and pass values and wrie in simple form
Here as per above len is a pre defined function, which calculate length of letters of a name.

def lucky_number(name):
    number = len(name) * 9
    print("Hello " + name + ". Your lucky number is " +str(number))

lucky_number("kay")
lucky_number("Mirza")

* Code Style:

Comments: Using comments we can document the code and we can make understand even other person

The symbol used to comment is #

# this is comment for python as python ignores the comments inside the code and it is used for documentation.

Eg: For Clean and Messy code

def calculate(d):
    q = 3.14
    z = q * (d ** 2)
    print(z)
calculate(5)

output is: 78.5

As per the above example the code is not clean enough and we tend to take time to figure out what is happening inside the code
Hence we should follow self documentation and precise and clear method of writting code using comments and proper use assign of variables like below

# We are calculating area of a circle
def circle_area(radius):
    pi = 3.14  
    area = pi * (radius ** 2)
    print (area)
# circle_area function is used to print area of a circle with radius**2
circle_area(5)

The output is 78.5
The above code is clear enough to understand.
---

Study Guide: Functions
This study guide provides a quick-reference summary of what you learned in this lesson and serves as a guide for the upcoming practice quiz.  

In the Functions segment, you learned how to define and call functions, utilize a function’s parameters, and return data from a function. You also learned how to differentiate and convert between different data types utilizing variables. Plus, you learned a few best practices for writing reusable and readable code. 

Terms
return value - the value or variable returned as the end result of a function

parameter (argument) -  a value passed into a function for use within the function

refactoring code - a process to restructure code without changing functionality

Knowledge
The purpose of the def() keyword is to define a new function. 

Best practices for writing code that is readable and reusable:

Create a reusable function - Replace duplicate code with one reusable function to make the code easier to read and repurpose.

Refactor code - Update code so that it is self-documenting and the intent of the code is clear.

Add comments - Adding comments is part of creating self-documenting code. Using comments allows you to leave notes to yourself and/or other programmers to make the purpose of the code clear.

Coding skills
Skill Group 1

Use a function that accepts multiple parameters
Return a result value

# This function calculates the number of days in a variable number of 
# years, months, and days. These variables are provided by the user and
# are passed to the function through the function’s parameters.
def find_total_days(years, months, days):
# Assign a variable to hold the calculations for the number of days in
# a year (years*365) plus the number of days in a month (months*30) plus
# the number of days provided through the "days" parameter variable.
    my_days = (years*365) + (months*30) + days
# Use the "return" keyword to send the result of the "my_days"  
# calculation to the function call. 
    return my_days
# Function call with user provided parameter values. 
print(find_total_days(2,5,23))
---

Skill Group 2

Use a function to return the result of a measurement conversion
Use arithmetic operators to perform a calculation
Combine text with a function call within a print() statement
Convert the return value from a float data type to a string for the print() function
Call the function and perform a calculation on the return value within a print() statement

. This function converts fluid ounces to milliliters and returns the 
. result of the conversion.
def convert_volume(fluid_ounce):
. Calculate value of the "ml" variable using the parameter variable 
. "fluid_ounce". There are approximately 29.5 milliliters in 1 fluid
. ounce.
    ml = fluid_ounce * 29.5  
. Return the result of the calculation.  
    return ml
 
. Call the conversion from within the print() function using 2 fluid 
. ounces. Convert the return value from a float to a string.  
print("The volume in millimeters is " + str(convert_volume(2)))
 
. Call the function again and double the 2 fluid ounces from within
. the print function.
print("The volume in millimeters is " + str(convert_volume(2)*2))
. Alternative calculation:
. print("The volume in millimeters is " + str(convert_volume(4)))


Q1:

This function converts miles to kilometers (km).

Complete the code to return the result of the conversion.

NOTE: The following items occur outside of the function. Do not try to change the indentations on the associated code or you will receive an error. 

Call the function to convert the trip distance from miles to kilometers. 

Fill in the blank to print the result of the conversion. 

Calculate the round-trip in kilometers by doubling the result, and fill in the blank to print the result. 

Ans:

# 1) Complete the function to return the result of the conversion
def convert_distance(miles):
	km = miles * 1.6  # approximately 1.6 km in 1 mile
	return km

# Do not indent any of the following lines of code as they are 
# meant to be located outside of the function above

my_trip_miles = 55

# 2) Convert my_trip_miles to kilometers by calling the function above
my_trip_km = (my_trip_miles) * 1.6

# 3) Fill in the blank to print the result of the my_trip_km conversion
print("The distance in kilometers is " + str(my_trip_km))

# 4) Calculate the round-trip in kilometers by doubling the result of
#    my_trip_km. Fill in the blank to print the result.
print("The round-trip in kilometers is " + str(my_trip_km*2))


Question 4
Complete the first line of the “print_seconds” function so that it accepts three parameters: hours, minutes, and seconds. Remember to use the “def” keyword to tell the Python interpreter the block of code is intended to define a function. 

def print_seconds(hours, minutes, seconds):
    print(hours*3600+minutes*60+seconds)

print_seconds(1,2,3)

Output: 

3723
3723
None
Here is your output:
3723

Correct. The formula should multiply the hours variable by
3600 and the minutes variable by 60, then add these two
products to the seconds variable.

Q:

This function compares two numbers and returns them in increasing order.

Fill in the blanks, so the print statement displays the result of the function call in order.

Hint: if a function returns multiple values, don't forget to store these values in multiple variables

# This function compares two numbers and returns them
# in increasing order.
def order_numbers(number1, number2):
	if number2 > number1:
		return number1, number2
	else:
		return number2, number1

# 1) Fill in the blanks so the print statement displays the result
#    of the function call
smaller,bigger = order_numbers(100, 99)
print(smaller, bigger)

---

* Conditionals

Logical Operators:

The following examples demonstrate how to use comparison operators with the data types int (integers, whole numbers) and float (number with a decimal point or fractional value). Comparison operators return Boolean results. As you learned previously, Boolean is a data type that can hold only one of two values: True or False.  

The comparison operators include: 

==    (equality)               a == b          a is equal to b

!=    (not equal to)           a != b          a is not equal to b

>     (greater than)           a > b           a is larger than b

<      (less than)             a < b           a is smaller than b

>=    (greater than or equal to)   a >= b      a is larger than or equal to b

<=    (less than or equal to)      a <= b      a is smaller than or equal to b


PART 1: Equality == and Not Equal To != Operators
In Python, you can use comparison operators to compare values. When a comparison is made, Python returns a Boolean result: True or False. Note that Boolean data types are not string data types (Boolean True is not equal to the string "True").  

To check if two values are the same, use the equality operator: == 

To check if two values are not the same, use the not equal to operator: != 

The print() function can be used to display the results of the comparisons.

print(32 == 30+2)   # The == operator checks if the 2 values are 
True                # equal to each other. If they are equal, 
                    # Python returns a True result.


print(5+10 == 6+7)  # If the two values are not equal, as in the
False               # expression 5+10 == 6+7 (or 15 == 13), Python          
                    # returns a False result.


print(10-4 != 10+4) # The != operator checks if the 2 values are
True                # NOT equal to each other. If true, Python              
                    # returns a True result. 


print(9/3 != 3*1)   # In this last example, 9/3 != 3*1 (or 3 != 3)
False               # is false. So, Python returns a False value.

The equality == operator versus the equals = operator 
It is important to note that the equality == comparison operator performs a different task than the equals = assignment operator. The equals = operator assigns the value on the right side of the equals = to the object (e.g., a variable) on the left side of the equals = operator. 

# The = equals assignment operator is used to assign a value to a 
# variable.

my_variable = 3*5           # Assigns a value to my_variable      
print(my_variable)          # Printing the variable returns the 
15                          # value assigned to the variable.


                              
# The == equality comparison operator checks if the values of the two
# expressions on either side of the == operator are equivalent to one 
# another.
      
print(my_variable == 3*5)   # Printing the variable returns a Boolean 
True                        # True or False result.


PART 2: Greater Than > and Less Than < Operators

The comparison operators greater than > and less than < also return a True or False Boolean result after comparing two values.

To check if one value is larger than another value, use the greater than operator: > 

To check if one value is smaller than another value, use the less than operator: < 

Examples:

print(11 > 3*3)         # The > operator checks if the left value is
True                    # greater than the right value. If true, it
                        # returns a True result.


print(4/2 > 8-4)        # If the > operator finds that the left value
False                   # is NOT greater than the right value, the
                        # comparison will return a False result.


print(4/2 < 8-4)        # The < operator checks  if the left value is
True                    # less than the right side. If true, the
                        # comparison returns a True result.


print(11 < 3*3)         # If the < operator finds that the left side is False                   # NOT less than the right value, Python returns
                        # a False result.

PART 3: 

Greater Than or Equal to >= and Less Than or Equal to <= Operators
Like the other comparison operators, the greater than or equal to >= and less than or equal to <= operators return a True or False Boolean result when a comparison is made.

To check if one value is larger than or equal to another value, use the greater than or equal to operator: >= 

To check if one value is smaller than or equal to another value, use the less than or equal to operator: <= 

Examples:

print(12*2 >= 24)   # The >= operator checks if the left value is
True                # greater than or equal to the right value. 
                    # If one of these conditions is true,  
                    # Python returns a True result. In this case  
                    # the two values are equal. So, the comparison
                    # returns a True result.


print(18/2 >= 15)   # If the >= comparison determines that the left False
False               # value is NOT greater than or equal to the
                    # right, it returns a False result.

print(12*2 <= 30)   # The <= operator checks if the left value is
True                # less than or equal to the right value. In 
                    # this case, the left value is less than the
                    # right value. Again, if one of the two 
                    # conditions is true, Python returns a True
                    # result.


print(15 <= 18/2)   # If the <= comparison determines that the left 
False               # value is NOT less than or equal to the right
                    # value, the comparison returns a False result. 
---

Comparison Operators with strings:

In this reading, you will learn more about what comparison operators can and cannot do. If you use the == (equality) and != (not equal to) operators with strings, you can check if two strings contain the same text or not. You can also alphabetize strings using > (greater than), < (less than), >= (greater than or equal to), <= (less than or equal to) comparison operators. As with numeric data types, comparison operators used with strings will return Boolean (True, False) results.  

PART 1: Equality == and Not Equal to != Operators with Strings
In Python, you can use comparison operators to compare strings. The equality == and the not equal to != operators are helpful when you need to search for a specific string in a body of text, a log file, a spreadsheet, a database, and more. You can also check user input strings to compare them to another string. Note that Boolean data types are not string data types (Boolean True is not equal to the string "True").  

Examples:

# The == operator can check if two strings are equal to each other. 
# If they are equal, the Python interpreter returns a True result.
print("a string" == "a string")
True


# In this example, the equality == comparison is between "4 + 5" and
# 4 + 5. Since the left data type is a string and the right data type
# is an integer, the two values cannot be equal. So, the comparison
# returns a False result.
print("4 + 5" == 4 + 5)
False


# The != operator can check if the two strings are NOT equal to each
# other. If they are indeed not equal, then Python returns a True result.
print("rabbit" != "frog")
True


# In this example, the variable event_city has been assigned the string 
# value "Shanghai". This variable is compared to a static string, 
# "Shanghai", using the != operator. As, the strings "Shanghai" and 
# "Shanghai" are the same, the comparison of "Shanghai" != "Shanghai" 
# is false. Accordingly, Python will return a False result.
event_city = "Shanghai"
print(event_city != "Shanghai")
False

# This last example illustrates the result of trying to compare two
# items of different data types using the equality == operator. The
# two items are not equal, so the comparison returns False.
print("three" == 3)
False

PART 2: The Greater Than > and Less Than < Operators
The comparison operators greater than > and less than < can be used to alphabetize words in Python. The letters of the alphabet have numeric codes in Unicode (also known as ASCII values). The uppercase letters A to Z are represented by the Unicode values 65 to 90. The lowercase letters a to z are represented by the Unicode values 97 to 122. 

# The greater than > operator checks if the left string has a higher 
# Unicode value than the right string. If true, the Python interpreter
# returns a True result. Since W has a Unicode value of 87, and you can 
# easily calculate that F has a Unicode value of 70, this comparison is
# the same as 87 > 70. As this is true, Python will return a True 
# result.
print("Wednesday" > "Friday")
True
 
 
# The less than < operator checks if the left string has a lower 
# Unicode value than the right string. If you reference the Unicode 
# chart above, you can see that all lowercase letters have higher 
# Unicode values than uppercase letters. We can see that B has a 
# Unicode value of 66 and b has a Unicode value of 98. This 
# comparison is the same as 66 < 98, which is true. So, Python will 
# return a True result.
print("Brown" < "brown")
True


# If the strings have the same first few letters, the comparison will 
# cycle through each letter of each string, from left to right until it 
# finds two letters that have different Unicode values. In this example, 
# both strings share the initial substring "sun", but then have 
# different letters with different Unicode values in the fourth place 
# in each string. So, the fourth letters 'b' and 't' of the two
# strings are used for the comparison. Since 'b' does not have a higher
# Unicode value than 't', the comparison returns a False result.
print("sunbathe" > "suntan")
False


# If two identical strings are compared using the less than < comparison
# operator, this will produce a False result because they are equal.
print("Lima" < "Lima")
False


# This last example illustrates the result of trying to compare two
# items of different data types using the less than < operator. The 
# greater than > and less than operators < cannot be used to compare
# two different data types. 
print("Five" < 6)
'''
Error on line 1:
    print("Five" < 6)
TypeError: '<' not supported between instances of 'str' and 'int'


PART 3: The Greater Than or Equal To >= and Less Than or Equal To <= Operators
The greater than or equal to >= and less than or equal to <= operators can be used with strings as well. Like the other comparison operators, they will return a True or False Boolean result when a comparison is made between two strings. 

To check if a string has a larger or equal Unicode value than the first letter(s) of another string, use the greater than or equal to operator: >= 

To check if a string has a smaller or equal Unicode value than the first letter(s) of another string, use the less than or equal to operator: <=

At this point, you should be familiar with how comparison operators work in Python. Can you determine what the results will be from the comparisons listed below? When you are ready to check your answers, click Run.

"my computer" >= "my chair"

"Spring" <= "Winter"

"pineapple" >= "pineapple"

# Use the Unicode chart in Part 2 to determine if the Unicode values of 
# the first letters of each string are higher, lower, or equal to one
# another. 


var1 = "my computer" >= "my chair"
var2 = "Spring" <= "Winter"
var3 = "pineapple" >= "pineapple"
 
print("Is \"my computer\" greater than or equal to \"my chair\"? Result: ", var1)
print("Is \"Spring\" less than or equal to \"Winter\"? Result: ", var2)
print("Is \"pineapple\" less than or equal to \"pineapple\"? Result: ", var3)



"a" == "a"
If string "a" is identical to string "a", returns True. Else, returns False

"a" != "b"
If string "a" is not identical to string "b"

"a" > "b"
If string "a" has a larger Unicode value than string "b"

"a" >= "b"
If the Unicode value for string "a" is greater than or equal to the Unicode value of string "b"

"a" < "b"
If string "a"  has a smaller Unicode value than string "b"

"a" <= "b"
If the Unicode value for string "a" is smaller than or equal to the Unicode value of string "b"
---

* Logical Operators
Logical operators are used to construct more complex expressions. You can make complex comparisons by joining comparison statements together using the logical operators: and, or, not. Complex comparisons return a Boolean (True or False) result. 

and 

Both sides of the statement being evaluated must be True for the whole statement to be True. 

Example: (5 > 1 and 5 < 10) = True

or 

If either side of the comparison is True, then the whole statement is True. 

Example: (color = "blue" or color = "green") = True

not 

Inverts the Boolean result of the statement immediately following it. So, if a statement evaluates to True, and we put the not operator in front of it, it would become False. 

Example: (not "A" == "A") = False


PART 1: The and Logical Operator
In Python, you can use the logical operator and to connect more than one comparison. This type of complex comparison is used to check if two comparison statements are both True or not. You might use the and operator when you need to execute a block of code, but only if two different conditions are true. For example, you might want to write a script  that automates sending you an emergency alert if a server stops responding and there is an unusual increase in employees opening trouble tickets.  

Example 1:

The following model demonstrates the use of the and logical operator to join comparisons between two mathematical expressions. The description below the example explains the order in which Python will process the line of code. 

# Example 1

print((6*3 >= 18) and (9+9 <= 36/2))

Python solves the numerical expressions using the order of operations. (6*3 >= 18) and (9+9 <= 36/2) becomes (18 >= 18) and (18 <= 18)

Python compares the results of the numerical expressions using the comparison operators (in this case >= and <=). (18 >= 18) and (18 <= 18) becomes True and True

Python checks if both sides of the logical operator "and" are true. True and True become True

Python returns a Boolean value: True or False. The complex comparison returns a True result.

# Example 2: 
In this next example, "Nairobi" < "Milan" and "Nairobi" > "Hanoi", the and logical operator is connecting two string comparison statements. You learned previously that using the greater than and less than operators on strings will test the alphabetical order (technically Unicode values) of the strings. So, this complex comparison is checking if "Nairobi" is alphabetized before "Milan" (False) AND after "Hanoi" (True). 

This comparison returns a False result because both sides of the logical operator are not True. A comparison statement like this might be used to iterate through a list of names to check if they are alphabetized in the correct order.

# Example 2

print("Nairobi" < "Milan" and "Nairobi" > "Hanoi")

PART 2: The or Logical Operator
The or logical operator tests two conditions to determine if at least one side of the or logical operator is True. The result of the test can be used to trigger a block of code if at least one condition is present.

Syntax:
Expression1 or Expression2

Returns Booleans: 

Expression1              Expression2                       Returns Result
True                        True                                True
True                        False                               True
False                       True                                True
False                       False                               False

Examples:

# True or True returns True
print((15/3 < 2+4) or (0 >= 6-7))
True

# False or True returns True
print(country == "New York City" or city == "New York City")
True

# True or False returns True
print(16 <= 4**2 or 9**(0.5) != 3)
True

# False or False returns False
print("B_name" > "C_name" or "B_name" < "A_name”)
False

PART 3: The not Logical Operator
The not logical operator inverts the value of the comparison expression. This is a helpful tool when you want to execute a block of code as long as a certain condition is not present.

If the conditional  expression is True, the not logical operator can be added to make the expression not True (False). 

If the conditional  expression is False, the not logical operator can be added to make the expression not False (True).  

Syntax:
not expression

Example 1:
# Test Example 1:

x = 2*3 > 6
print("The value of x is:")
print(x)

print("")  # Prints a blank line

print("The inverse value of x is:")
print(not x)
 
Example 2:

# What happens when you negate a False statement? 
# Click Run when you are ready to check your answer.


today = "Monday"
print(not today == "Tuesday") 

# The "today" variable states today is Monday. This makes the comparison
# "today == Tuesday" False. The logical operator "not" inverts the False
# result to become True. In other words, this expression asks if it is
# false that today is not Tuesday. More succinctly, "not False" means 
# True."

Key takeaways
When Python logical operators are used with comparison operators, the interpreter will return Boolean results (True or False):

Expression                       Description
a == a and a != b                True if both sides are True, otherwise False.
a > b or a <= c                  True if either side is True. False if both sides are False.
not a == b                       True if the statement is False, False if the statement is True.

https://www.digitalocean.com/community/tutorials/understanding-boolean-logic-in-python-3
---

* Branching with if statements

We can use the concept of branching to have our code alter its execution sequence depending on the values of variables. We can use an if statement to evaluate a comparison. We start with the if keyword, followed by our comparison. We end the line with a colon. The body of the if statement is then indented to the right. If the comparison is True, the code inside the if body is executed. If the comparison evaluates to False, then the code block is skipped and will not be run.

























