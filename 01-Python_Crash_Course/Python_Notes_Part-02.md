This Notes contains Week-03(Loops ( While, For, Recursion )) in python

# Week-03(Loops in Python(While loops and For loops) and (Recusrion))

What is while loop?

While loops instruct your computer to continuously execute your code based on the value of a condition. This works in a similar way to branching if statements. The difference here is that the body of the block can be executed multiple times instead of just once.


Note: whenever you're writing a loop check that you're initializing all the variables you want to use before you use them., The output might be different than what you want 

x = 0
while x < 5:
  print("Not there yet, x=" + str(x))
  x = x + 1
print("x=" + str(x))



 In the first line we're assigning the value of 0 to the variable x. We call this action initializing, to give an initial value to a variable. In the line after that, we're starting the while loop. We're setting a condition for this loop that x needs to be smaller than 5. Right now we know that x is 0 since we've just initialized it, so this condition is currently true. On the next two lines, we have a block that's indented to the right. Here, we can use what we learned about functions and conditionals to identify that this is the while loop's body. There are two lines in the body of the loop. In the first line, we print a message followed by the current value of x. In the second line, we increment the value of x. We do this by adding 1 to its current value and assigning it back to x. So after the first execution of the body of the loop, x will be 1 instead of 0. Because this is a loop, the computer doesn't just continue executing with the next line in the script. Instead, it loops back around to re-evaluate the condition for the while loop. And because 1 here is still smaller than 5, it executes the body of the loop again. It then prints the message and once more increments x by 1. So the x is now 2. The computer will keep doing this until the condition isn't true anymore. In this example, the condition will be false when x is no longer smaller than 5. Once the condition is false, the loop finishes, and the next line is executed. And finally, the last line of our code prints the last value of x.

So we had five lines with the message, Not there yet, and then at the end of the script the value of x was 5.

Anatomy of a While Loop
A while loop will continuously execute code depending on the value of a condition. It begins with the keyword while, followed by a comparison to be evaluated, then a colon. On the next line is the code block to be executed, indented to the right. Similar to an if statement, the code in the body will only be executed if the comparison is evaluated to be true. What sets a while loop apart, however, is that this code block will keep executing as long as the evaluation statement is true. Once the statement is no longer true, the loop exits and the next line of code will be executed.  

More While loop Examples:

A While loop Example Inside a Function:

Can you work out what this function does? Try passing different parameters to the attempts function to see what it does. 

def attempts(n):
    x = 1
    while x <= n:
        print("Attempt " + str(x))
        x += 1
    print("Done")
    
attempts(5)


Output:
Attempt 1
Attempt 2
Attempt 3
Attempt 4
Attempt 5
Done
---

In this above example, we start out by initializing a variable called x. In this case, we initialize it with a value of 1. Then, we enter our while loop which checks to see if the value inside of the x variable is less than the parameter n that the function received. If that comparison evaluates to true, then the code inside the while block is executed. Say we pass a value of 5 as a parameter to this function. In the first pass through the loop, x is always equal to 1, so the comparison: 1 smaller than or equal to 5 would be true and we then enter the body of the loop. In the body, we first print a message indicating that the current attempt number and then we increase the value of x by 1. To increment the number we're using a slightly different expression than before. x +=1 is a shorthand version of x = x+1. You can use either expression since they both mean the same thing. The process continues until the result of the comparison isn't true anymore, which happens when x is bigger than n.

Eg:

username = get_username()
while not valid_username(username):
  print("Invaild username")
  username = get_username()

In these past examples, we've used the simple conditions of a number being smaller, or smaller or equal than another number. These are common conditions, but they're by no means the only conditions you can have in a while loop. It's common, for example, to call a separate function that evaluates the condition, like this. In this case, there's a lot of code hidden behind functions and it's doing stuff we don't see. There's a get username function that asks the user for a username and a valid_username function that validates that username. And all this is happening in just a handful of characters. As you can see, you can pack a lot of punch into just a short line of code. In this case, the body of the while loop will be executed until the user enters a valid username. The important thing to remember is that the condition used by the while loop needs to evaluate to true or false. It doesn't matter if this is done by using comparison operators or calling additional functions. The conditions used in while loops can also become more complex if we use the logical operators that we encountered when looking into branching, and, or, and not. This lets us combine the values of several expressions to get the result we want. 



Why Initializing Variables Matters:

the most common mistakes people make when writing loops. One of the most common errors is forgetting to initialize variables with the right value. We've all made this mistake when starting to code. Remember how in the earlier examples we initialized our variable x to 0 in one case and to 1 in the other. When we forget to initialize the variable two different things can happen. The first possible outcome and the easiest to catch is that Python might raise an error telling us that we're using a variable we haven't defined, which looks like this. As we've done with other errors we've come across, we can look at the last line to understand what's going on. This error type is a name error, and the message that comes after it says we're using an undefined variable. It's straightforward to fix, we just need to initialize the variable before using it, like this:
Play video starting at :1:21 and follow transcript1:21
Fixed. Now, there's a second issue we might face if we forget to initialize variables with the right value. We might have already used the variable in our program. In this case, if we reuse the variable without setting the correct value from the start, it will still have the value from before. This can lead to some pretty unexpected behavior. Check out this script. Can you spot the problem? In the first block, we correctly initialize x to 1 and sum to 0 and then iterate until x equals 10, summing up all the values in between. So by the end of that block, sum equals the result of adding all the numbers from 1 to 10 and x is 10. In the second part of the code, the original intention was to get the product of all the numbers from 1 to 10. But if you look closely, you can see that we're initializing the product but forgetting to initialize x, so x is still 10. This means that when the while condition gets checked, x is already 10 at the start of the iteration. The while condition is false before it even starts and the body never executes. Let's see how this problem would look.

In this code, there's an initialization problem that's causing our function to behave incorrectly. Can you find the problem and fix it?

def count_down(start_number):
  while (current > 0):
    print(current)
    current -= 1
  print("Zero!")

count_down(3)


Ans:

current = 3
def count_down(start_number):
  while (current > 0):
    print(current)
    current -= 1
  print("Zero!")

count_down(3)

Common Pitfalls With Variable Initialization
You'll want to watch out for a common mistake: forgetting to initialize variables. If you try to use a variable without first initializing it, you'll run into a NameError. This is the Python interpreter catching the mistake and telling you that you’re using an undefined variable. The fix is pretty simple: initialize the variable by assigning the variable a value before you use it.

Another common mistake to watch out for that can be a little trickier to spot is forgetting to initialize variables with the correct value. If you use a variable earlier in your code and then reuse it later in a loop without first setting the value to something you want, your code may wind up doing something you didn't expect. Don't forget to initialize your variables before using them!

* Infinite Loops:

A Loop that keeps executing and never stops, untill we stop the code.

Eg:

while x % 2 == 0:
    x = x / 2

You may remember by now that while loops use a condition to check when to exit. The body of the while loop needs to make sure that the condition being checked will change. If it doesn't change, the loop may never finish and we get what's called an infinite loop, a loop that keeps executing and never stops. Check out this example. It uses the modulo operator that we saw a while back. This cycle will finish for positive and negative values of x. But what would happen if x was zero? The remainder of 0 divided by 2 is 0, so the condition would be true. The result of dividing 0 by 2 would also be zero, so the value of x wouldn't change. This loop would go on forever, and so we'd get an infinite loop. If our code was called with x having the value of zero, the computer would just waste resources doing a division that would never lead to the loop stopping. The program would be stuck in an infinite loop circling background endlessly, and we don't want that. All that looping might make your computer dizzy. To avoid this, we need to think about what needs to happen for a loop to be successful.

if x != 0:
while x % 2 == 0:
x = x / 2

 in this example. This makes sure we only enter the body of the loop for values of x that are both different than zero and even. Talking about infinite loops reminds me of one of the first times I used while loops myself. I wrote a script that emailed me as a way of verifying that the code worked, and while some condition was true, I forgot to exit the loop. Turns out those e-mails get sent faster than once per second. As you can imagine, I got about 500 e-mails before I realized what was going on. Infinitely grateful for that little lesson.

remember, when you're writing loops, it's a good idea to take a moment to consider the different values a variable can take. This helps you make sure your loop won't get stuck. If you see that your program is running forever without finishing, have a second look at your loops to check there's no infinite loop hiding somewhere in the code.

Q:

The following code causes an infinite loop. Can you figure out what’s missing and how to fix it?

def print_range(start, end):
	# Loop through the numbers from start to end
	n = start
	while n <= end:
		print(n)

print_range(1, 5)  # Should print 1 2 3 4 5 (each number on its own line) 


Infinite loops and Code Blocks:
Another easy mistake that can happen when using loops is introducing an infinite loop. An infinite loop means the code block in the loop will continue to execute and never stop. This can happen when the condition being evaluated in a while loop doesn't change. Pay close attention to your variables and what possible values they can take. Think about unexpected values, like zero.

In the Coursera code blocks, you may see an error message that reads "Evaluation took more than 5 seconds to complete." This means that the code encountered an infinite loop, and it timed out after 5 seconds. You should take a closer look at the code and variables to spot where the infinite loop is.
---


# Study Guide: while Loops
This study guide provides a quick-reference summary of what you learned in this segment and serves as a guide for the upcoming practice quiz.  

In the while Loops segment, you learned about the logical structure and syntax of while loops. You also learned about the importance of initializing variables and how to resolve infinite while loops with the break keyword.  


while Loops
A while loop executes the body of the loop while a specified condition remains True. They are commonly used when there’s an unknown number of operations to be performed, and a condition needs to be checked at each iteration.

Syntax:

while specified condition is True:
    body of loop



Example while loop:

multiplier = 1
result = multiplier*5
while result <= 50:
  print(result)
  multiplier += 1
  result = multiplier*5
print("Done")

# This while loop prints the multiples of 5 between 1 and 50. The
# "multiplier" variable is initialized with the starting value of 1. 
# The "result" variable is initialized with the value of the 
# "multiplier" variable times 5. 
 
# The while loop specifies that the loop must iterate while it is True 
# that the "result" is less than or equal to 50. Within the while loop, 
# the code tells the Python interpreter to print the value of the 
# "result" variable. Then, the "multiplier" is incremented by 1 and the
# "result" is assigned the new value of the "multiplier" times 5. 
 
# The end of the while loop is indicated by the indentation of the next 
# line of code moving one tab to the left. At this point, the Python
# interpreter automatically loops back to the beginning of the while
# loop to check the condition again with the new value of the "result"
# variable. When the while loop condition becomes False (meaning
# "result" is no longer less than or equal to 50), the interpreter exits
# the loop and reads the next line of code outside of the loop. In this 
# case, that next line tells the interpreter to print the string "Done". 
 
# Click the "Run" button to check the result of this while loop.  


Common Errors in while Loops:
If you get an error message on a loop or it appears to hang, your debugging checklist should include the following checks:

  Failure to initialize variables. Make sure all the variables used in the loop’s condition are initialized before the loop.

  Unintended infinite loops. Make sure that the body of the loop modifies the variables used in the condition, so that the loop will eventually end for all possible values of the variables. You can often prevent an infinite loop by using the break keyword or by adding end criteria to the condition part of the while loop.

 

while Loop Terms:

  while loop - Tells the computer to execute a set of instructions while a specified condition is True. In other words, while loops keep executing the same group of instructions until the condition becomes False.

  infinite loop - Missing a method for exiting the loop, causing the loop to run forever.

  break - A keyword that can be used to end a loop at a specific point. 


Math Concepts on the Practice Quiz

The coding problems on the upcoming practice quiz will involve a few math concepts. Don’t worry if you are rusty on math. You will have plenty of support with these concepts on the quiz. The following is a quick overview of the math terms you will encounter on the quiz:  

  prime numbers - Integers that have only two factors, which are the number itself multiplied by 1. The lowest prime number is 2.

  prime factors - Prime numbers that are factors of an integer. For example, the prime numbers 2 and 5 are the prime factors of the number 10 (2x5=10). The prime factors of an integer will not produce a remainder when used to divide that integer. 

  divisor - A number (denominator) that is used to divide another number (numerator). For example, if the number 10 is divided by 5, the number 5 is the divisor.

  sum of all divisors of a number - The result of adding all of the divisors of a number together.  

  multiplication table - An integer multiplied by a series of numbers and their results formatted as a table or a list. For example:

                 4x1=4
                 4x2=8
                 4x3=12
                 4x4=16
                 4x5=20



Coding skills

Skill Group 1

. Initialize a variable

. Use a while loop that runs while a specific condition is true

. Ensure the while loop will not be an infinite loop

. Increment a value within a while loop



# This function counts the number of integer factors for a 
# "given_number" variable, passed through the function’s parameters.
# The "count" return value includes the "given_number" itself as a 
# factor (n*1). 
def count_factors(given_number):
 
  # To include the "given_number" variable as a "factor", initialize
  # the "factor" variable with the value 1 (if the "factor" variable
  # were to start at 2, the "given_number" itself would be excluded). 
  factor = 1
  count = 1
 
  # This "if" block will run if the "given_number" equals 0.
  if given_number == 0:
    # If True, the return value will be 0 factors. 
    return 0
 
  # The while loop will run while the "factor" is still less than
  # the "given_number" variable.
  while factor < given_number:
    # This "if" block checks if the "given_number" can be divided by
    # the "factor" variable without leaving a remainder. The modulo
    # operator % is used to test for a remainder.
    if given_number % factor == 0:
      # If True, then the "factor" variable is added to the count of
      # the "given_number"’s integer factors.
      count += 1
    # When exiting the if block, increment the "factor" variable by 1
    # to divide the "given_number" variable by a new "factor" value
    # inside the while loop.
    factor += 1
 
  # When the interpreter exits either the while loop or the top if
  # block, it will return the value of the "count" variable.
  return count
 
print(count_factors(0)) # Count value will be 0
print(count_factors(3)) # Should count 2 factors (1x3)
print(count_factors(10)) # Should count 4 factors (1x10, 2x5)
print(count_factors(24)) # Should count 8 factors (1x24, 2x12, 3x8,
# and 4x6). 


Skill Group 2

. Initialize variables to assign data types before they are used in a while loop 

. Use the break keyword as an exit point for a while loop


# This function outputs an addition table. It is written to end after
# printing 5 lines of the addition table, but it will break out of the
# loop if the "my_sum" variable exceeds 20. 
 
# The function accepts a "given_number" variable through its 
# parameters.
def addition_table(given_number):
 
    # The "iterated_number" and "my_sum" variables are initialized with
    # the value of 1. Although the "my_sum" variable does not need any
    # specific initial value, it still must be assigned a data type
    # before being used in the while loop. By initializing "my_sum"
    # with any integer, the data type will be set to int.
    iterated_number = 1
    my_sum = 1
 
    # The while loop will run while it is True that the   
    # "iterated_number" is less than or equal to 5.
    while iterated_number <= 5:
 
        # The "my_sum" variable is assigned the value of the
        # "given_number" plus the "iterated_number" variables.
        my_sum = given_number + iterated_number
 
        # Test to see if the "my_sum" variable is greater than 20.
        if my_sum > 20:
            # If True, then use the break keyword to exit the loop. 
            break
        # If False, the Python interpreter will move to the next line 
        # in the while loop after the if-statement has ended.  
 
        # The print function will output the "given_number" plus
        # the "iterated_number" equals "my_sum".
        print(str(given_number), "+", str(iterated_number), "=", str(my_sum))
 
        # Increment the "iterated_number" before the while loop starts
        # over again to print a new "my_sum" value.
        iterated_number += 1
 
 
addition_table(5)
addition_table(17)
addition_table(30)

# Expected output:
# 5 + 1 = 6
# 5 + 2 = 7
# 5 + 3 = 8
# 5 + 4 = 9
# 5 + 5 = 10
# 17 + 1 = 18
# 17 + 2 = 19
# 17 + 3 = 20
# None

Practice Quiz: While Loops

Question 3
 The following code contains an infinite loop, meaning the Python interpreter does not know when to exit the loop once the task is complete. To solve the problem, you will need to:  

Find the error in the code

Fix the while loop so there is an exit condition

Hint: Try running your function with the number 0 as the input and observe the result. 

Note that Coursera’s code blocks will time out after 5 seconds of running an infinite loop. If you get this timeout error message, it means the infinite loop has not been fixed. 


def is_power_of_two(number):
  # This while loop checks if the "number" can be divided by two
  # without leaving a remainder. How can you change the while loop to
  # avoid a Python ZeroDivisionError?
  while number % 2 == 0:
    number = number / 2
  # If after dividing by 2 "number" equals 1, then "number" is a power
  # of 2.
  if number == 1:
    return True
  return False
  

# Calls to the function
print(is_power_of_two(0)) # Should be False
print(is_power_of_two(1)) # Should be True
print(is_power_of_two(8)) # Should be True
print(is_power_of_two(9)) # Should be False



Q:

Fill in the blanks to complete the while loop so that it returns the sum of all the divisors of a number, without including the number itself. As a reminder, a divisor is a number that divides into another without a remainder. To do this, you will need to:

Initialize the "divisor" and "total" variables with starting values

Complete the while loop condition

Increment the "divisor" variable inside the while loop

Complete the return statement

# Fill in the blanks so that the while loop continues to run while the
# "divisor" variable is less than the "number" parameter.

def sum_divisors(number):
# Initialize the appropriate variables
  ___ = ___
  ___ = ___

  # Avoid dividing by 0 and negative numbers 
  # in the while loop by exiting the function
  # if "number" is less than one
  if number < 1:
    return 0 

  # Complete the while loop
  while ___:
    if number % divisor == 0:
      total += divisor
    # Increment the correct variable
    ___ += 1

  # Return the correct variable 
  return ___


print(sum_divisors(0)) # Should print 0
print(sum_divisors(3)) # Should print 1
# 1
print(sum_divisors(36)) # Should print 1+2+3+4+6+9+12+18
# 55
print(sum_divisors(102)) # Should print 1+2+3+6+17+34+51
# 114


5.
Question 5
Fill in the blanks to complete the function, which should output a multiplication table. The function accepts a variable “number” through its parameters. This “number” variable should be multiplied by the numbers 1 through 5, and printed in a format similar to “1x6=6” (“number” x “multiplier” = “result”). The code should also limit the “result” to not exceed 25. To satisfy these conditions, you will need to:

Initialize the “multiplier" variable with the starting value

Complete the while loop condition

Add an exit point for the loop

Increment the “multiplier" variable inside the while loop

def multiplication_table(number):
    # Initialize the appropriate variable
    ___ = ___

    # Complete the while loop condition.
    while ___:
        result = number * multiplier 
        if  result > 25 :
            # Enter the action to take if the result is greater than 25
            ___
        print(str(number) + "x" + str(multiplier) + "=" + str(result))
        
        # Increment the appropriate variable
        ___ += 1


multiplication_table(3) 
# Should print: 
# 3x1=3 
# 3x2=6 
# 3x3=9 
# 3x4=12 
# 3x5=15

multiplication_table(5) 
# Should print: 
# 5x1=5
# 5x2=10
# 5x3=15
# 5x4=20
# 5x5=25

multiplication_table(8) 
# Should print:
# 8x1=8
# 8x2=16
# 8x3=24
---



# For Loops:

What is a for loop?

Itreates over a sequence of Values, The For loop is to iterate over a squence of numbers, like this

for x in range(5):
    print(x)

A very simple example of a for loop is to iterate over a sequence of numbers, like this. Notice how the structure is kind of similar to the structures we've already seen. The first line indicates the distinguishing keyword. In this case, that's for. And it ends with a colon. The body of the loop is indented to the right, like we saw in the while loop, the if block, and the function definitions. What's different in this case is that we have the keyword in. Also, between the for keyword and in keyword, we have the name of a variable. This variable will take each of the values in the sequence that loop iterates through. So in this example, it'll iterate through a sequence of numbers generated using the range function. There are two important things I want to call out about this range function. First,

 In Python and a lot of other programming languages, a range of numbers will start with the value 0 by default. Second, the list of numbers generated will be one less than the given value. In the simple example here, x will take the values 0, 1, 2, 3, and 4. Let's check this out.


So there, we have a very basic for loop. It iterates over a sequence of numbers generated by the range function. When using a for loop, we point the variable defined between for and in, in this case, x, at each element of the sequence. This means on the first iteration x points at 1. On the second iteration, it points at 2, and so on. Whatever code we put in the body of the loop will be executed on each of the values, one value at a time.

 Well, the power of the for loop is that we can use it to iterate over a sequence of values of any type, not just a range of numbers.


friends = ['Mansoor', 'Alex', 'Mirza', 'Syed']
for friend in friends:
    print("Hi " + Friend)

Think all the way back to our very first Python example in this course. Remember our trusty "hi friends" script? In it, we saw a for loop that iterated over a list of strings. It looks like this. We'll talk a lot more about lists later on. But for now, you only need to know that we can construct lists using square brackets, and separate the elements in them with commas.

In this example, we're iterating a list of strings. And for each of the strings in the list, we're printing a greeting

The sequence that the for loop iterates over could contain any type of element, not just strings. For example, we could iterate over a list of numbers to calculate the total sum and average. Here's one way of doing this. Here, we're defining a list of values. After that, we're initializing two variables, sum and length, that will update in the body of the for loop. In the for loop, we're iterating over each of the values in the list, adding the current value to the sum of values, and then also adding 1 to length, which calculates how many elements there are in the list. Once we've gone through the whole list, we print out the sum and the average. We'll keep using for loops in our examples every time we want to iterate over the elements of any sequence and operate with them. Some examples of sequences that we can iterate are the files in a directory, the lines in a file, the processes running on a machine. And there's a bunch of others. So as an IT specialist, you'll use for loops to automate tons of stuff. For example, you might use them to copy files to machines, process the contents of files, automatically install software, and a lot more. A few weeks ago, I had to update a lot of files with different values depending on their contents. So I used a for loop in a script to iterate over all the files. Then, my script took different actions based on an if condition and updated all of those files for me. It would have taken me forever if I had done this manually file by file. If you're wondering when you should use for loops and when you should use while loops, there's a way to tell. Use for loops when there's a sequence of elements that you want to iterate. Use while loops when you want to repeat an action until a condition changes. And if whatever you're trying to do can be done with either for or while loops, just use whichever one's your favorite. 



* For Loops Recap:

For loops allow you to iterate over a sequence of values. Let's take the example from the beginning of the video:

for x in range(5):

  print(x)

Similar to if statements and while loops, for loops begin with the keyword for with a colon at the end of the line. Just like in function definitions, while loops and if statements, the body of the for loop begins on the next line and is indented to the right. But what about the stuff in between the for keyword and the colon? In our example, we’re using the range() function to create a sequence of numbers that our for loop can iterate over. In this case, our variable x points to the current element in the sequence as the for loop iterates over the sequence of numbers. Keep in mind that in Python and many programming languages, a range of numbers will start at 0, and the list of numbers generated will be one less than the provided value. So range(5) will generate a sequence of numbers from 0 to 4, for a total of 5 numbers.

Bringing this all together, the range(5) function will create a sequence of numbers from 0 to 4. Our for loop will iterate over this sequence of numbers, one at a time, making the numbers accessible via the variable x and the code within our loop body will execute for each iteration through the sequence. So for the first loop, x will contain 0, the next loop, 1, and so on until it reaches 4. Once the end of the sequence comes up, the loop will exit and the code will continue.

The power of for loops comes from the fact that it can iterate over a sequence of any kind of data, not just a range of numbers. You can use for loops to iterate over a list of strings, such as usernames or lines in a file.

Not sure whether to use a for loop or a while loop? Remember that a while loop is great for performing an action over and over until a condition has changed. A for loop works well when you want to iterate over a sequence of elements.  


More For Loop Examples:

Eg:

product = 1
for n in range(1,10):
  product = product * n

print(product)

we talked about the range function, and how it generates a sequence of numbers starting with zero. Sometimes, though, we don't want to start with zero. For these situations, the range function also allows us to specify the first element of the list to generate. We do that by passing two parameters to the function instead of one, like in the next example. Product = 1 for n in range(1,10): product = product * n print(product). In this example, we're calculating the products of all numbers from 1 to 10. For this operation, it's important that we start with one and not with zero. If we'd started with zero, the whole product would be zero. Additionally, we can specify a third parameter to change the size of each step. This means that instead of going one by one, we could have a larger difference between the elements.


E2:

def to celsius(x):
  return (x-32)*5/9

for x in range(0,101,10):
  print(x, to_celsius(x))

Let's check out this example when you might want to do something like this. First, we're defining a function that converts a temperature value from Fahrenheit to Celsius, and we're simply using a conversion formula to do that. Then we have a for loop that starts at zero, and goes up to 100 in steps of 10. Notice that we're using 101 for the upper limit instead of 100. We're doing this because the range never includes the last element, and we want to include 100 in our range. The body of the for-loop prints the value in Fahrenheit and the value in Celsius creating a conversion table. Let's see this in action.

That example got you feeling the heat. Don't worry, there's a quick rundown of what we've learned. The range function can receive one, two or three parameters. If it receives one parameter, it will create a sequence one by one from zero until one less than the parameter received. If it receives two parameters, it will create a sequence one by one from the first parameter until one less than the second parameter. Finally, if it receives three parameters, it will create a sequence starting from the first number and moving towards the second number. But this time, the jumps between the numbers will be the size of the third number, and again, it will stop before the second number.
---


A Closer Look at the Range() Function
The in keyword, when used with the range() function, generates a sequence of integer numbers, which can be used with a for loop to control the start point, the end point, and the incremental values of the loop.  

Syntax:

for n in range(x, y, z):
    print(n)


The range() function uses a set of indices that point to integer values, which start at the number 0. The numeric values 0, 1, 2, 3, 4 correlate to ordinal index positions 1st, 2nd, 3rd, 4th, 5th. So, when a range call to the 5th index position is made using range(5) the index is pointing to the numeric value of 4.


Index Number                                      Value

1st index                                           0

2nd index                                           1

3rd index                                           2

4th index                                           3

5th index                                           4


The range() function can take up to three parameters:  range(start, stop, step) 

Start 
The first item in the range() function parameters is the starting position of the range. The default is the first index position, which points to the numeric value 0. This value is included in the range. 

Stop
The second item in the range() function parameters is the ending position of the range. There is no default index position, so this index number must be given to the range() parameters. For example, the line for n in range(4) will loop 4 times with the n variable starting at 0 and looping 4 index positions: 0, 1, 2, 3. As you can see, range(4) (meaning index position 4) ends at the numeric value 3. In Python, this structure may be phrased as “the end-of-range value is excluded from the range.” In order to include the value 4 in  range(4), the syntax can be written as range(4+1) or range(5). Both of these ranges will produce the numeric values 0, 1, 2, 3, 4. 

Step
The third item in the range() function parameters is the incremental step value. The default increment is +1. The default value can be overridden with any valid increment. However, note that the loop will still end at the end-of-range index position, regardless of the incremental value. For example, if you have a loop with the range: for n in range(1, 5, 6), the range will only produce the numeric value 1. This is because the incremental value of 6 exceeded the ending point of the range.


Practice Exercise:

You can use the code block below to test the values of n with various range() parameters. A few suggestions to test are:

range(stop)

. range(3) 

. range(3+1) 

range(start, stop)

. range(2, 6)     

. range(5,10+1) 

range(start, stop, step)

. range(4, 15+1, 2)         

. range(2*2, 25, 3+2) 

. range(10, 0, -2)  


for n in range(1, 5, 6):  
    print(n)


Examples of the range() function in code:

# This loop iterates on the value of the "n" variable in a range
# of 0 to 10 (the value of the end-of-range index 11 is excluded).
# The incremental value for the loop is 2. The print() function will 
# output the resulting value of "n" as the loop counts from 0 to 10 
# (end-of-range index 11) in incremental steps of 2. This is one 
# method that can be used in Python to print a list of even numbers.


for n in range(0,11,2):
    print(n)


# The loop should print 0, 2, 4, 6, 8, 10


Example 2  

# This loop iterates on the value of the "number" variable in a range
# of 2 to 7+1 (the value of the end-of-range index 7 is excluded, so 
# +1 has been added to the parameter to include the numeric value 7 in 
# the range). The incremental value for the loop is the default of +1.
# The print() function will output the resulting value of "number" 
# multiplied by 3.


for number in range(2,7+1):
    print(number*3)


# The loop should print 6, 9, 12, 15, 18, 21


Example 3  

# This loop iterates on the value of the "x" variable in a range
# of 2 to -1 (the end-of-range index -2 is excluded). The third 
# parameter is also a negative number, making it a decremental value
# of -1. The print() function will output the resulting value of
# "x" as it starts at 2 and counts down to -1 (index -2).


for x in range(2, -2, -1):
    print(x)


# The loop should print 2, 1, 0, -1


Key takeaways
The roles of the range(start, stop, step) function parameters are:

Start - Beginning of range

value included in range

default = 0

Stop - End of range

value excluded from range (to include, use stop+1)

no default

must provide the ending index number 

Step - Incremental value 

default = 1

https://www.geeksforgeeks.org/python-range-function/


* Nested For Loops:

You're doing great getting your head around all these loops. I think you're ready for something a little bit more complex. We're going to explore what happens when you get loops inside of loops. Does that make your head spin? Don't worry, we're about to break it down for you with a couple of examples. Have you ever played dominoes before? There's a bunch of fun games you can play with these tiles. In case you're not familiar, each Domino Tiles has two numbers represented by a collection of dots carved on each half of the tile. The numbers go from zero to six. Tiles can be rotated so that each combination of numbers is represented only once in a set of Domino Tiles. In other words, the two-three tile is the same as the three-two tile, and there's only one per set. Now, imagine we wanted to write a program that prints each Domino Tile in a set. If we take all of the tiles that have zero on the left, we can print tiles with numbers from zero to six on the right. That should be easy to do with a for loop. But what about tiles that have one on the left? Well, we need to skip the one zero tile, because that one was already printed as zero one. So we can print a list of tiles with one on the left and numbers from one to six on the right. When we look at two, we would need to skip both zero and one, and so on. Are you following along? How do you think we'd write the code for this? Turning this into code means that we'd need to write two for loops, one inside the other. This is what we call nested for loops. Check out how this looks on Python code. for left in range(7):

for left in range(7):
  for right in range(left, 7):
    print("[" + str(left) + " | " + str(right) + "]", end=" ")
  print()


In this code, we're using a new parameter that we passed to the print function. This parameter is called end=" ". Normally, once print has taken the content we passed and written it to the screen, then it writes a special character that creates a new line called the newline character. If we want print to write something else instead of the newline character, we use the end=" " parameter, like we see in this example. Notice how the second for loop iterates over a different number of elements each time it's called as the value of left changes. Depending on what you want to achieve with your nested loops, you may want both loops to always go through the same number of elements. Or you might want the second loop to connect to the first one. Let's look at a different example.

teams = ['Dragons', 'Wolves', 'Pandas', 'Unicorns']
for home_team in teams:
  for away_team in teams:
    if home_team != away_team:
      print(home_team + " vs " + away_team)


 Let's say you run a local girl's basketball league in your town. You have four teams that will play against each other in the league, both at home and away. You've stored the names of the teams in a list, like this: teams = [ ‘Dragons’, ‘Wolves’, ‘Pandas’, ‘Unicorns’] We want to write a script that will output all possible team pairings. For this, the order of the names matters because for each game, the first name will be the home team and the second name is the away team. Of course, what we don't want to do is have a team playing against itself. So what statement do we need to use to avoid that? To do this, we need to use a conditional that makes sure we only print the pairing when the names are different. Check out what this looks like. for home_team in teams: for away_team in teams: if home_team != away_team: print(home_team +


print(home_team + “ vs ” + away_team) Success! As you can see, nested loops are super useful for solving certain problems, like pairing teams. What it doesn't solve is the question: who would win in a face-off between dragons and unicorns? If only there were some code for that. Anyway, we've seen that nested loops are a handy tool, but we need to be careful not to just blindly apply them to any problem. Why? Well, because the longer the list your code needs to iterate through, the longer it takes your computer to complete the task. Let's say your manager asks you to do an operation that will run through a list of 10,000 elements. If the operation takes one millisecond per element, the whole loop would take one millisecond times 10,000 to complete, which is 10 seconds. Now, imagine we add a nested loop that has to go over the same 10,000 elements. This means that each iteration of the outside loop would do a full iteration of the inside loop, which again, would take ten seconds to go through the whole list. So now, the whole iteration takes 10,000 times 10 seconds, which is 100,000 seconds, that's over 27 hours. I have the patience of a gnat, so that would definitely not work for me. This doesn't mean we shouldn't use nested loops. They are a useful tool when solving problems that require them, but we need to be careful of where and how we use them. Throughout this course, and one is coming up, we'll look at a lot of techniques that can help us pick the right tool to use for each type of problem. Up next, we'll look into some common errors that you might come across when writing your for loops and what to do about them.


* Common Errors in for loops:

We've now seen how to write for loops, combine them with functions, nest a for loop inside a different loop, and even combine a nested loop with conditionals. Nice job, you're chugging right along. But before we're done with for loops, let's check out some common mistakes you may come across while trying this yourself. As we've called out already, for loops iterate over sequences. The interpreter will refuse to iterate over a single element. As you see here: for x in 25: print(x) In this example,

for x in 25:
  print(x)

 we're trying to iterate over the number 25. Python prints a TypeError telling us that integers are not iterable. There are two solutions to this problem, depending on what we're trying to do. If we want to go from zero to 25, then we use the range function: 
 
for x in range(25): 
    print(x), 

but if we're trying to iterate over a list that has 25 as the only element, then it needs to be a list and that means writing it between square brackets: for x in [25]: for x in [25]: print(x) You might be wondering why you'd ever want to iterate over a list of one element and that's a good question. Well, this kind of issue usually happens when you have a function with a for loop inside it, which is iterating over the elements of a list received by parameter. Say for example, you have a function that fixes the permissions of a list of files received by parameter, and you want to call this function to fix the permissions of just one specific file. To do that, you need to pass the file as the single element of a list. Let's check this out with some code we're familiar with, our friendliest of Python examples, 

def greet_friends(friends):
    for friend in friends:
        print("Hi " + friend)

greet_freinds(['Taylor', 'Luisa', 'Jammal', 'Eli'])

hi, friends. We're going to modify it to have the greetings inside a function. We've defined a greet friends function, that receives a list by parameter and iterates over that list, greeting each friend. But what if we only want to greet one friend instead of four? Well, we still need to define a list, but with only one element. But first, let's see what would happen if we don't do that: 

greet_friends("Barry")

Huh, not what we expected, right? Well, what's going on here? This happens because strings are iterable, the for loop will go over each letter of the string and do the operation we asked it to do, which in this case, print a greeting. Depending on what you're trying to do, you may actually want to iterate through the letters of a string. But in this case, we don't. So to sum it up, if you get an error that a certain type isn't iterable, you need to make sure the for loop is using a sequence of elements and not just one, and if you find your code iterating through each letter of a string when you want it to do it for the whole string, you probably want to have that string be a part of a list. We've now learned how to write while loops and for loops. You might remember, for loops are best when you want to iterate over a known sequence of elements but when you want to operate while a certain condition is true, while loops are the best choice. Next up, we've got a super useful cheat sheet for you that puts all this into one handy resource. After that, head over to the practice quiz to test your knowledge and check in on how you're doing.



Study Guide: for Loops

This study guide provides a summary of what you learned in this segment and serves as a guide for the upcoming practice quiz.  

In the for Loops segment, you learned about the logical structure and syntax of for loops. You took a closer look at the range() function. You learned about nested for loops and complex nested for loops with if statements. You also learned how to fix common errors in for loops.

for Loops vs. while Loops
for loops and while loops share several characteristics. Both loops can be used with a variety of data types, both can be nested, and both can be used with the keywords break and continue. However, there are important differences between the two types of loops: 

while loops are used when a segment of code needs to execute repeatedly while a condition is true

for loops iterate over a sequence of elements, executing the body of the loop for each element in the sequence

Syntax 
The syntax of a for loop with the in keyword:

for variable in sequence:
    body of loop

Common for Loop Structures 
for Loop with range()
The in keyword with the range() function generates a sequence of integer numbers, which can be used with a for loop to configure the iterations of the code. The range of numbers [0, 1, 2] correlates to ordinal index positions (1st, 2nd, 3rd), rather than the cardinal (quantity) values of the numbers 0, 1, and 2. For example, range(5) means the five index positions in the range [0, 1, 2, 3, 4]. 

The range() function can take up to three parameters. The roles of the three possible range(x,y,z) parameters are:

x = Start - Starting index position of the range 

    Default index position is 0.

    The starting index position is included in the range. 

    Example syntax: range(2, y, z) or range(x+3, y, z) 

y = Stop - Ending index position of range

    No default index position. Must include the ending index position in the range() parameters.

      Example syntax: range(y)

 The value of the ending index position is excluded from the range. 

 To include the ending index number, use the expression: y+1 (index + 1)

   Example syntax: range(x, y+1, z)

   Alternatively, if y = 10, you can write: range(x, 11, z)

z = Step - Incremental value

   Default increment is +1.
 
   The default value can be overridden with any valid increment.

   The incremental value will end the for loop before it reaches the end of range index position (end of range index minus 1).  

Example of a for loop with the in keyword and the range() function:

# This loop iterates on the value of the "number" variable in a range
# of 1 to 6+1 (the upper range limit of 6 is excluded, so +1 has
# been added to it to include 6 in the range). The incremental value
# for the loop is 2 (number+2). The print() function will output the
# resulting value of "number" multiplied by 3.


for number in range(1,6+1,2):
    print(number*3)


# The loop should print 3, 9, 15

Common pitfalls when using the range() function:
    Forgetting that the upper limit of a range() isn’t included in the range.

    Iterating over non-sequences. For example, strings are iterable letter by letter, but not word by word. 

# This loop iterates on the value of the "number" variable in a range
# of 2 to 7 (the upper range limit of 8 is excluded). The print() 
# function will output the resulting value of "number" squared.


for number in range(2,8):
    print(number**2)


# The loop should print 4, 9, 16, 25, 36, 49



Nested for Loops 
The syntax of nested for loops:

for x in sequence:
    # start of the outer loop body
    for y in sequence:
        # start of the inner loop body

        # end of of the inner loop body
    # continue body of the outer loop
    # end of the outer loop body


 Example of nested for loops:  

# This code demonstrates the outer and inner loop iterations of a pair 
# of nested for loops. Click "Run" to see the results. The outer loop
# will run twice for the range pointer positions [0, 1] in range(2).
# The inner loop will run 4 times for the range pointer positions 
# [0, 1, 2, 3] in range(3+1) or range(4) each time the outer loop runs.
# So, the inner loop will execute 8 times in total.


for x in range(2):
    print("This is the outer loop iteration number " + str(x))
    for y in range(3+1):
        print("Inner loop iteration number " + str(y))
    print("Exit inner loop") 


for Loop with nested if Statement
The syntax of a for Loop with nested if Statement:

for x in sequence:
    # start of body of for loop
    if condition is true:
        # start of body of if-statement

        # end of body of if-statement
    # continue body of for loop
    # end of body of for loop

Example of a for Loop with Nested if Statement:  

# This for loop iterates through the numbers 0 to 6. The if statement
# uses the modulo operator to test if the "x" variable is divisible by
# 2. If True, the if statement will print the value of "x" and exit
# back into the for loop for the next iteration of "x". Since no 
# incremental value is specified in the range() parameters, the default
# increment is +1. 


for x in range(7):
    if x % 2 == 0:
        print(x)


# The loop should print 0, 2, 4, 6


* Practice Quiz:

Question 2
Which option would fix this for loop to print the numbers 12, 18, 24, 30, 36?

for n in range(6,18,3):
    print(n*2)

option A:  

for n in range(6,18,3):
    print(n+2)

Option B:
for n in range(6,18+1,3):
    print(n*2)

Option C:
for n in range(12,36,6):
    print(n*2)

Option D:
for n in range(0,36+1,6):
    print(n)



Question 3
Which for loops will print all even numbers from 0 to 18? Select all that apply.

for n in range(19):
    if n % 2 == 0:
        print(n)


Fill in the blanks so that the for loop will print the first 10 cube numbers (x**3) in a range that starts with x=1 and ends with x=10.

for __ in range(__,__):
  print(__)


Question 5
Write a for loop with a three parameter range() function that prints the multiples of 7 between 0 and 100. Print one multiple per line and avoid printing any numbers that aren't multiples of 7. Remember that 0 is also a multiple of 7. 

for ___: 
    print(___)

---


# Recusrsion

In computer science, recursion is a method of solving a computational problem where the solution depends on solutions to smaller instances of the same problem. Recursion solves such recursive problems by using functions that call themselves from within their own code.


Additional Recursion Sources:
In the past videos, we visited the basic concepts of recursive functions.

A recursive function must include a recursive case and base case. The recursive case calls the function again, with a different value. The base case returns a value without calling the same function.

A recursive function will usually have this structure:


def recursive_function(parameters):
    if base_case_condition(parameters):
        return base_case_value
    recursive_function(modified_parameters)

Practice Quiz: Recursion:

Question 3
Fill in the blanks to make the is_power_of function return whether the number is a power of the given base. Note: base is assumed to be a positive number. Tip: for functions that return a boolean value, you can return the result of a comparison.

def is_power_of(number, base):
  # Base case: when number is smaller than base.
  if number < base:
    # If number is equal to 1, it's a power (base**0).
    return __

  # Recursive case: keep dividing number by base.
  return is_power_of(__, ___)

print(is_power_of(8,2)) # Should be True
print(is_power_of(64,4)) # Should be True
print(is_power_of(70,10)) # Should be False

4:

The count_users function recursively counts the amount of users that belong to a group in the company system, by going through each of the members of a group and if one of them is a group, recursively calling the function and counting the members. But it has a bug! Can you spot the problem and fix it?

def count_users(group):
  count = 0
  for member in get_members(group):
    count += 1
    if is_group(member):
      count += count_users(member)
  return count

print(count_users("sales")) # Should be 3
print(count_users("engineering")) # Should be 8
print(count_users("everyone")) # Should be 18

Question 5
Implement the sum_positive_numbers function, as a recursive function that returns the sum of all positive numbers between the number n received and 1. For example, when n is 3 it should return 1+2+3=6, and when n is 5 it should return 1+2+3+4+5=15.

def sum_positive_numbers(n):
  return 0

print(sum_positive_numbers(3)) # Should be 6
print(sum_positive_numbers(5)) # Should be 15
---


Study Guide: Week 3 Graded Quiz
It is time to prepare for the Week 3 Graded Quiz. Please review the following items from this module before beginning the Week 3 Graded Quiz. If you would like to refresh your memory on these materials, please also revisit the while Loop Study Guide and the for Loop Study Guide located before the Practice Quizzes in Week 3. You will not be tested on the Recursion lesson content, which is optional in this module.

Knowledge
Terms
  variables - Know how to properly initialize or increment a variable. You will also need to recognize a coding error due to the failure to properly initialize or increment a variable.

  infinite loops - Know how to recognize infinite loops and use common solutions to prevent them. For example, check loop conditions, ranges, iterators, control statements, etc. to ensure that at least one of these controls are in place to prevent an infinite loop.

  iterators - Know the various options available for iterating a variable (e.g., using assignment operators, using the third range() function parameter). You will also need to analyze where the iteration should occur. A misplaced iterator could produce the wrong output or create an infinite loop.  

  control statements - Know how and when to use the break and continue control statements to prevent infinite loops.  


Common Functions:

range() Function Parameters - Know the roles of the three possible range(x, y, z) function parameters:

   x Start of Range (included)

   y End of Range (excluded index) 
 
     To include the end of range index, use the expression y+1

     The end of range must be included in the range() parameters.

  z Incremental value

Example 1: range(4, 12+1, 2)

  This example creates a range that starts at 4 and ends at 12 (without the +1, the range would end at 11). 

  The third parameter increments the range iteration by 2, as opposed to the default increment of 1. The  range(4, 12+1, 2) expression would produce the values: 4, 6, 8, 10, 12 

Example 2: range(10, 2-1, -2)

  This example creates a range that starts at 10 and ends at 2-1, with a decremental value of -2. When counting down, to include the value of the end of the range index, use -1 (end of range minus 1). This range produces the sequence: 10, 8, 6, 4, 2 

print() Function Default Behavior - Know the default behavior of the print() function is to insert a new line character after the print statement runs.

  To override the insertion of the new line character and replace it with a space, add end=" " as the last item in the print() parameters. This makes it possible to add the next print output to the same line, separated by a space. You might use this technique when a print() function is part of a for or while loop. Example syntax:  print(x+1, end=" ")


Coding Skills
Skill 1: Using for loops with the range() function

  Use a for loop with the range() function with the end-of-range value included in the range.

# This function will accept an integer variable "end" and count by 10
# from 0 to the "end" value.
def count_by_10(end):
    # Initializeq the "count" variable as a string.
    count = ""

    # The range function parameters instruct Python to start the count  
    # at 0 and stop at the variable given as the upper end of the range. 
    # Since the value of the high end of a range is excluded by default,  
    # you can make Python include the "end" value by adding +1 to it. 
    # The third parameter tells Python to increment the count by 10.
    for number in range(0,end+1,10):

        # Although the variable "count" will hold a count of integers,  
        # this example will be converted to a string using "str(number)" 
        # in order to display the incremental count from 0 to the "end" 
        # value on the same line with a space " " separating each 
        # number.  
        count += str(number) + " "
        
    # The .strip() method will trim the final space " " from the end of 
    # the string "count"  
    return count.strip()


# Call the function with 1 integer parameter.
print(count_by_10(100))
# Should print 0 10 20 30 40 50 60 70 80 90 100


. Use a set of nested for loops with the range() function to create a matrix of numbers. 

. Include the upper range value in the range() function using end+1.


# This function uses a set of nested for loops with the range() function 
# to create a matrix of numbers. The upper range value in the range() 
# function should be included in the matrix. The matrix should consist 
# of a set of numbers that fill both rows and columns.
def matrix(initial_number, end_of_first_row):


    # It is an optional code style to assign the long variable names in the
    # function parameters to shorter variable names. 
    n1 = initial_number 
    n2 = end_of_first_row+1  # include the upper range value with +1

    # The first for loop will create the columns.
    for column in range(n1, n2):

        # The nested for loop will create the rows.
        for row in range(n1, n2):

            # To make the matrix of numbers easier to read, include a space
            # between each number in the rows until the loop reaches the 
            # end of the row. You can override the default behavior of the 
            # print() function (which inserts a new line character after 
            # the print command runs) by using the "end=" "" parameter 
            # inside the print() function.  
              print(column*row, end=" ")

        # The row ends when the upper range value is encountered within the 
        # nested for loop. The outer (column) for loop should insert a new line
        # to create the next row. Use the print() function new line default 
        # behavior with an empty print() function:
        print()


# Call the function with 2 integer parameters. 
matrix(1, 4)
# Should print:
# 1 2 3 4 
# 2 4 6 8 
# 3 6 9 12 
# 4 8 12 16 


.  Predict the final value of a nested for loop with range() functions.  

# For this example, the outer for loop uses an end of range index of 
# 10. The value of index 10 will be 10-1, or 9.  
for outer_loop in range(10):

    # Using the "outer_loop" variable as the end of range for the  
    # inner loop, means the end of range index will be 9. The value 
    # of index 9 will be 9-1, or 8.
    for inner_loop in range(outer_loop):

        # The printed result is the value of "inner_loop". Since  
        # there aren’t any calculations in this loop, there is a 
        # simple shortcut for solving what the final value printed 
        # by the "inner_loop" will be. The solution is to simply use 
        # the value of the "inner_loop" index, which is 8.
        print(inner_loop)
        

. Find and fix an error in a for loop with range() function.  

# This function should count down by -2 from 11 to 1, so that it only
# prints odd numbers. 

# This range(11, -2) tells the for loop to start at 11 and end at index
# position -2 (which corresponds to the numeric value of -1). Since the
# third incremental or decremental value is missing, the loop will 
# increment by the default of +1 instead of the intended -2 decrement.
# Starting at index position 11 and incrementing by +1 will end the loop 
# automatically, because the index is not counting down towards -2 as 
# the end of the range. 

# To fix this problem, the range() needs three parameters:
# First parameter should be the starting index position of 11.
# Second parameter should be the ending index position of 0 (value 1).
# Third parameter should be decrementing by -2.
# So, the range should be configured as range(11, 0, -2).

# Fix this loop with the corrected range parameters and click Run.
for n in range(11, -2):
    if n % 2 != 0:
        print(n, end=" ")

# Should print: 11, 9, 7, 5, 3, 1 once the problem is fixed.
---


Skill 2: Using while loops
    . Use a while loop to print a sequence of numbers .

# For this example, the while loop will count down by threes starting 
# from 18 and ending at 0.
starting_number = 18

# The while loop will continue to loop until it reaches 0.
while starting_number >= 0:

    # To make the sequence of numbers easier to read, include a space
    # between each number in the sequence. You can override the default 
    # behavior of the print() function by using the "end=" parameter with
    # the print() function. The syntax for adding a space is: end=" " 
    print(starting_number, end=" ")
    
    # Decrement the "starting_number" variable by -3.
    starting_number -= 3

# Should print 18 15 12 9 6 3 0 

. Use a while loop to count the number of digits in a numerical value   

# This function accepts a CEO's salary as a variable. 
# It counts the number of digits in the salary and 
# returns the sentence like:
# "The CEO has a 6-figure salary."
def X_figure(salary):
    
    # Initializes the counter as an integer.
    tally = 0

    # The if-statement checks if the variable "salary" 
    # is equal to 0.
    if salary == 0:
        # If true, then it increments the counter to 
        # show there is 1 digit in 0.
        tally += 1

    # The while loop starts to run while the "salary"
    # is greater than or equal to 1 (the loop will 
    # not run if the "salary" is 0).
    while salary >= 1:

        # The body of the while loop counts the digits 
        # in "salary" by counting the number of times 
        # "salary" can be divided by 10 until "salary" 
        # is no longer >= 1.
        salary = salary/10

        # Add 1 to the counter to tally the number of 
        # times the loop runs.
        tally += 1

    # Return the results of the "tally" of the number
    # of digits in "salary".
    return tally
 
# Call the X_figure function with 1 parameter, converted to a string,
# inside a print function with additional strings.
print("The CEO has a " + str(X_figure(2300000)) + "-figure salary.")

# Should print"The CEO has a 7-figure salary."


Skill 3: Using while loops with if-else statements
Use a function to accept two variable integers. 

Use nested if-else statements and while loops to count up or count down from the first variable to the second variable.  

# This function will accept two integer variables: the floor
# number that a passenger "enter"s an elevator and the floor
# number the passenger is going to "exit". Then, the function
# counts up or down from the two floor numbers.
def elevator_floor(enter, exit):
    # The "floor" variable will be used as a counter and to  
    # print the floor numbers. The "elevator_direction"
    # variable will hold the string "Going up: " or 
    # "Going down: " plus the count up or down of the 
    # "floor" numbers.
    floor = enter
    elevator_direction = ""

    # If the passenger enters the elevator on a floor that  
    # is higher than the destination floor:
    if enter > exit:
        
        # Then the "elevator_direction" string will be 
        # initialized with the string "Going down: ".
        elevator_direction = "Going down: "

        # While the "floor" number is greater than or  
        # equal to the exit floor number:
        while floor >= exit:
            # The "floor" number is converted to a string 
            # and is appended to the string variable 
            # "elevator_direction".
            elevator_direction += str(floor)

            # If the "floor" number is still greater than  
            # the exit floor number:
            if floor > exit:

                # A pipe | character is added between each  
                # floor number in the string variable  
                # "elevator_direction" to provide a visual  
                # divider between numbers. The if-statement 
                # above (if floor > exit) prevents the pipe 
                # character from appearing after the "floor" 
                # number is no longer greater than the "exit" 
                # variable. 
                elevator_direction += " | "
                
                # Decrement the "floor" number as the elevator 
                # goes down.
            floor -= 1

    # Else, it is implied that the passenger is entering the  
    # elevator on a floor that is lower than the destination 
    # floor.
    else:

        # The "elevator_direction" string will be initialized 
        # with the string "Going up: ".
        elevator_direction = "Going up: "
        
        # While the "floor" number is less than or equal to the 
        # "exit" floor number:
        while floor <= exit:

            # Convert the the "floor" number to a string and append 
            # it to the string variable "elevator_direction".
            elevator_direction += str(floor)

            # If the entry floor number is still less than the exit 
            # floor number:
            if floor < exit:

                # The pipe | character is added between each  
                # floor number in the string variable  
                # "elevator_direction" to provide a visual  
                # divider between numbers. The if-statement 
                # above (if floor < exit) prevents the pipe 
                # character from appearing after the "floor" 
                # number is no longer less than the "exit" 
                # variable. 
                elevator_direction += " | "

            # Increments the "floor" number as the elevator goes up.
            floor += 1

    # Returns the string holding the elevator direction (Going down or 
    # Going up) along with the floor countdown or count up.
    return elevator_direction


# Call the function with 2 integer parameters. 
print(elevator_floor(1,4)) # Should print Going up: 1 | 2 | 3 | 4
print(elevator_floor(6,2)) # Should print Going down: 6 | 5 | 4 | 3 | 2


Reminder: Correct syntax is critical
Using precise syntax is critical when writing code in any programming language, including Python. Even a small typo can cause a syntax error and the automated Python-coded quiz grader will mark your code as incorrect. This reflects real life coding errors in the sense that a single error in spelling, case, punctuation, etc. can cause your code to fail. Coding problems caused by imprecise syntax will always be an issue whether you are learning a programming language or you are using programming skills on the job. So, it is critical to start the habit of being precise in your code now. 

No credit will be given if there are any coding errors on the automated graded quizzes - including minor errors. Fortunately, you have 3 optional retake opportunities on the graded quizzes in this course. Additionally, you have unlimited retakes on practice quizzes and can review the videos and readings as many times as you need to master the concepts in this course.  

Now, before starting the graded quiz, please review this list of common syntax errors coders make when writing code.


Common syntax errors:

  Misspellings

  Incorrect indentations

  Missing or incorrect key characters:

    Parenthetical types - ( curved ), [ square ], { curly }

    Quote types - "straight-double" or 'straight-single', “curly-double” or ‘curly-single’

    Block introduction characters, like colons - :

  Data type mismatches

  Missing, incorrectly used, or misplaced Python reserved words

  Using the wrong case (uppercase/lowercase) - Python is a case-sensitive language 

# Week 3 Final Graded Assessment


