# Week-04(Strings, List, Dictionaries)

In this module you'll dive into more advanced ways to manipulate strings using indexing, slicing, and advanced formatting. You'll also explore the more advanced data types: lists, tuples, and dictionaries. You'll learn to store, reference, and manipulate data in these structures, as well as combine them to store complex data structures.

Learning Objectives

. Manipulate strings using indexing, slicing, and formatting
. Use lists and tuples to store, reference, and manipulate data
. Leverage dictionaries to store more complex data, reference data by keys, and manipulate data stored
. Combine the String, List, and Dictionary data types to construct complex data structures

# strings:

* Basic structures of String:

A string is a data type in Python that's used to represent a piece of text. It's written between quotes, either double quotes or single quotes, your choice. It doesn't matter which type of quotes you use as long as they match. If we mix up double and single quotes, Python won't be too happy, and it'll return a syntax error, telling us it couldn't find the end of the string. 

name ="sasha"

name = 'Mirza'

Error:
Place = "Cambridge'

A string can be as short as zero characters, usually called an empty string or really long. Eg: pet = ""

pet = "looooooooooooooooooooooooooooooooooooooooooooong cat"

print("Name: " + name + ", Favorite colour: " + color
Name: Sasha, Favorite color: gold)

We also learned that we can use strings to build longer strings using the plus sign and action called concatenating. 

"example" * 3
exampleexampleexample

A less common operation is to multiply the string by a number, which multiplies the content of the string that many times like this. 

len(pet)

If we want to know how long a string is, we can use the len function which we saw in earlier videos. The len function tells us the number of characters contained in the string. 

We can use strings to represent a lot of different things. They can hold a username, the name of a machine, an email address, the name of a file, and any other text. A lot of the data that we'll interact with will be stored in strings, so it's important to know how to use them. There are tons of things we could do with strings in our scripts. For example, we can check if files are named a certain way by looking at the filename and seeing if they match our criteria, or we can create a list of emails by checking out the users of our system and concatenating our domain. 

I recently wrote a script that worked with a bunch of files and took different actions according to the name of each file. So the file ended in a certain extension say, .TXT , then my script would print it. If the file had a certain string and the name, say, test, then my script would ignore it and move on to the next thing and so on. The contents of a text file are also strings. A few months ago, I had to change the default values for a bunch of configuration options from true to false.

So I wrote a function that would find the string true in a file and replace it with false. You can probably think of more examples where your code needs to handle strings, but to use strings effectively, we need to know what options are available to us in Python. In the next few videos, we'll cover some of the operations we can perform over strings, including how to access parts of them and modify them.

* Parts of a string:

When we first came across the for loop, we called out that we can iterate over a string character by character. But what if we want to access just a specific character or characters? We might want to do this, for example, if we have a text that's too long to display and we want to show just a portion of it. Or if we want to make an acronym by taking the first letter of each word in a phrase. We can do that through an operation called string indexing.

name = "Jaylen"
print(name[1])
a

print(name[0])
J

Print(name[5])
n

print(name[6])
error as there are from 0 to 5 Jaylen

This operation lets us access the character in a given position or index using square brackets and the number of the position we want. Like this. This might seem confusing at first, like Python is acting up. We're asking for the first character, and it's giving us the second. What gives Python? Well, what's happening here is that Python starts counting indexes from 0 not 1. Just like it does with the range function. So if we want the first character, we need to access the one at index 0. Knowing that indexes start at 0, which one do you think will be the last index in the string? It'll always be one less than the length of the string. In this case, our string has six characters, so the last index will be 5. Let's try it out.

We see that the character in position five is the last character of the string. And if we try to access index six, we get an index error telling us that it's out of range. We can only go up to length minus 1. What if you want to print the last character of a string but you don't know how long it is? You can do that using negative indexes. Let's see that in a different example.

text = "Random string with a lot of charecters"
print(text[-1])
s
print(text[-2])
r

In this example, we don't know the length of the string, but it doesn't matter. Using negative indexes lets us access the positions in the string starting from the last. Nice, right?
On top of accessing individual characters, we can also access a slice of a string.

color = "Orange"
print(color[1:4])
'ran'

A slice is the portion of a string that can contain more than one character, also sometimes called a substring. We do that by creating a range using a colon as a separator. Let's see an example of this.

The range we use when accessing a slice of a string works just like the one created by the range function. It includes the first number, but goes up to one less than the last number. In this case, we start with indexed one, the second letter of the string, and go up to index three, the fourth letter of the string. Another option for the range is to include only one of the two indexes. In that case, it's assumed that the other index is either 0 for the first value or the length of the string for the second value. Check this out.

fruit = "Pineaplle"
print(fruit[:4])
Pine

print(fruit[4:])
apple

Accessing the slice from nothing to 4 takes the first four characters of the string, indexes 0 to 3. Accessing the slice from 4 to nothing takes everything from index four onward. All of this indexing might seem confusing at first. Don't worry, we all took time to wrap our heads around it. Just like all the challenges we've come across so far, the key is to keep practicing until you master it. And there are a bunch of exercises ahead to help you with that. Now that we know how to select, slice, and access the parts of the string we want, we're going to learn how to modify them. That's coming up next.
---

String Indexing and Slicing:

String indexing allows you to access individual characters in a string. You can do this by using square brackets and the location, or index, of the character you want to access. It's important to remember that Python starts indexes at 0. So to access the first character in a string, you would use the index [0]. If you try to access an index that’s larger than the length of your string, you’ll get an IndexError. This is because you’re trying to access something that doesn't exist! You can also access indexes from the end of the string going towards the start of the string by using negative values. The index [-1] would access the last character of the string, and the index [-2] would access the second-to-last character.

You can also access a portion of a string, called a slice or a substring. This allows you to access multiple characters of a string. You can do this by creating a range, using a colon as a separator between the start and end of the range, like [2:5]. 

This range is similar to the range() function we saw previously. It includes the first number, but goes to one less than the last number. For example:

>>> fruit = "Mangosteen"
>>> fruit[1:4]
'ang'

The slice includes the character at index 1, and excludes the character at index 4. You can also easily reference a substring at the start or end of the string by only specifying one end of the range. For example, only giving the end of the range:

>>> fruit[:5]
'Mango'

This gave us the characters from the start of the string through index 4, excluding index 5. On the other hand this example gives is the characters including index 5, through the end of the string:

>>> fruit[5:]
'steen'

You might have noticed that if you put both of those results together, you get the original string back!

>>> fruit[:5] + fruit[5:]
'Mangosteen'

Cool!


* Creating New strings:


In the last video, we saw how to access certain characters inside a string. Now, what if we wanted to change them? Imagine you have a string with a character that's wrong and you want to fix it, like this one. Taking into account what you learned about string indexing, you might be tempted to fix it by accessing the corresponding index and changing the character. Let's see what happens if we try that.

message = "A Kong string with a silly typo"
message[2] = "l"
o: error

These pesky type errors, right? In this case, we're told that strings don't support item assignment. This means that we can't change individual characters because strings in Python are immutable, which is just a fancy word meaning they can't be modified. What we can do is create a new string based on the old one, like this.

message = "A Kong string with a silly typo"
new_message = message[0:2] + "l" + message[3:]
print(new_message)

Nice, we fixed the typo. But does this mean the message variable can never change? Not really. We can assign a new value to the same variable. Let's do that a couple of times to see how it works.

message = "A Kong string with a silly typo"
new_message = message[0:2] + "l" + message[3:]
print(new_message)
message = "This is new message"
print("message")
O: This is a new message

What we're doing here, is giving the message variable a whole new value. We're not changing the underlying string that was assigned to it before. We're assigning a whole new string with different content. If this seems a bit complex, that's okay. You don't need to worry about this right now. We'll call this out whenever it's relevant for the programmer writing. So, we figured out how to create a new message from the old one. But how are we supposed to know which character to change? Let's try something different.

pets = "cats & Dogs"
print(pets.index("&"))

In this case, we're using a method to get the index of a certain character. A method is a function associated with a specific class. We'll talk a lot more about classes and methods later. For now, what you need to know is that this is a function that applies to a variable. And we can call it by following the variable with a dot. Let's try this a few more times.

pets = "Cats & Dogs"
pets.index("&")
5

pets.index("c")
0

pets.index("Dog")
7

So the index method returns the index of the given substring, inside the string. The substring that we pass, can be as long or as short as we want. What if there's more than one of the substring?

pets.index("s")
3

Here, we know there are two s characters, but we only get one value. That's because the index method returns just the first position that matches. And what happens if the string doesn't have the substring we're looking for? The index method can't return a number because the substring isn't there, so we get a value error instead.

Ex:

Try using the index method yourself now!
Using the index method, find out the position of "x" in "supercalifragilisticexpialidocious".

word = "supercalifragilisticexpialidocious"
print(___)

word = "supercalifragilisticexpialidocious"
print(word.index("x"))

We said that if the substring isn't there, we would get an error. So how can we know if a substring is contained in a string to avoid the error? Let's check this out.

pets = "cats & Dogs"
"Dragons" in pets
O: false

"cats" in pets
O: True

We can use the key word in to check if a substring is contained in a string. We came across the keyword in, when using four loops. In that case, it was used for iteration. Here, it's a conditional that can be either true or false. It'll be true if the substring is part of the string, and false if it's not. So here, the Dragons substring isn't part of the string, and sadly, we can't have a Dragon as a pet. All right, we just covered a bunch of new things and you're doing awesome. Let's put all the stuff together to solve a real-world problem. 


def replace_domain(email, old_domain, new_domain):
    if "@" + old_domain in email:
        index = email.index("@" + old_domain)
        new_email = email[:index] + "@" + new_domain
        return new_email
    return email


Imagine that your company has recently moved to using a new domain, but a lot of the company email addresses are still using the old one. You want to write a program that replaces this old domain with the new one in any outdated email addresses. 

The function to replace the domain would look like this. This function is a bit more complex than others, so let's go through it line by line. First, we define the replace_domain function which accepts three parameters. The email address to be checked, the old domain, and the new domain. Having all these values as parameters instead of directly in the code, makes our function reusable. We aren't just changing one domain to the other, we have a function that will work with all domains. Pretty sweet. In the first line of the body of the function, we check if the concatenation of the @ sign and the old domain are contained in the email address, using the keyword in. We check this to make sure the email has "old domain" on the portion that comes after the @ sign. If the condition is true, the email address needs to be updated. To do that, we first find out the index where the old domain, including the @ sign starts. 

We know that this index will be a valid number because we've already checked that the substring was present. So, using this index, we create the new email. This is a string that contains the first portion of the old email, up until the index we had calculated, followed by the @ sign and the new domain. Finally, we return this new email. If the email didn't contain the new domain, then we can just return it, which is what we do in the last line. Wow, that was a really complex function with a lot of new things in it. So don't worry if you're finding it a bit tricky. Re-watch the video and take your time. If there's a specific part that's tripping you up, remember, you can always ask your fellow learners for help in the discussion forum. You may even find that someone has asked and got the answer to the same question already. When you feel ready to move on, meet me over in the next video, where we're going to learn a lot more handy string methods.


* Basic String Methods:
In Python, strings are immutable. This means that they can't be modified. So if we wanted to fix a typo in a string, we can't simply modify the wrong character. We would have to create a new string with the typo corrected. We can also assign a new value to the variable holding our string.

If we aren't sure what the index of our typo is, we can use the string method index to locate it and return the index. Let's imagine we have the string "lions tigers and bears" in the variable animals. We can locate the index that contains the letter g using animals.index("g"), which will return the index; in this case 8. We can also use substrings to locate the index where the substring begins. animals.index("bears") would return 17, since that’s the start of the substring. If there’s more than one match for a substring, the index method will return the first match. If we try to locate a substring that doesn't exist in the string, we’ll receive a ValueError explaining that the substring was not found.

We can avoid a ValueError by first checking if the substring exists in the string. This can be done using the in keyword. We saw this keyword earlier when we covered for loops. In this case, it's a conditional that will be either True or False. If the substring is found in the string, it will be True. If the substring is not found in the string, it will be False. Using our previous variable animals, we can do "horses" in animals to check if the substring "horses" is found in our variable. In this case, it would evaluate to False, since horses aren’t included in our example string. If we did "tigers" in animals, we'd get True, since this substring is contained in our string.

* More string Methods:

# DIFFERENT TYPES OF STRING METHODS:

we've seen ways you can access portions of strings using the indexing technique, create new strings by slicing and concatenating, find characters and strings using the index method, and even test if one string contains another. On top of all this string processing power, the string class provides a bunch of other methods for working with text. Now, we'll show you how to use some of these methods.

* Upper & lower class:

answer = 'yes'
if answer.lower() =="yes":
    print("user said yes")

output:
used said yes

Some string methods let you perform transformations or formatting on the string text, like upper, and its opposite, lower. These methods are really useful when you're handling user input. Let's say you wanted to check if the user answered yes to a question. How would you know if the user typed it using upper or lower case? You don't need to, you just transform the answer to the case you want.

* strip method:

" yes " .strip()

output:
'yes'

" yes " .lstrip()

output:
'yes '

" yes " .rstrip()

output:
' yes'

Another useful method when dealing with user input is the strip method. This method will get rid of surrounding spaces in the string. If we ask the user for an answer, we usually don't care about any surrounding spaces. So it's a good idea to use the strip method to get rid of any white space. This means that strip doesn't just remove spaces, it also removes tabs and new line characters, which are all characters we don't usually want in user-provided strings. There are two more versions of this method, lstrip rstrip, to get rid of the whitespace characters just to the left or to the right of the string instead of both sides.

* count of substring inside a string:

"the number of times e occurs in this string is 4".count("e")

output:
4

The method count returns how many times a given substring appears within a string.

* endswith string:

"forest".endswith("rest")

output:
true

The method endswith returns whether the string ends with a certain substring.

* isnumeric:

"forest".isnumeric()

output:
false

"12345".isnumeric()

output:
true

The method isnumeric returns whether the string's made up of just numbers. Adding to that, if we have a string that is numeric, we can use the int function to convert it to an actual number.like this

int("12345) + int("54321")

output:

66666

* join method:

" ".join(["this","is","a","phrase","joined","by","spaces"])

output:
this is a phrase joined by spaces

"...".join(["this","is","a","phrase","joined","by","dots"])

output:
this...is...a...phrase...joined...by...dots

To use the join method, we have to call it on the string that'll be used for joining. In this case, we're using a string with a space in it. The method receives a list of strings and returns one string with each of the strings joined by the initial string. Let's check out another example.

* split method:

"this is another example".split()

output:
['this','is','another','example']

The split method returns a list of all the words in the initial string and it automatically splits by any whitespace. It can optionally take a parameter and split the strings by another character, like a comma or a dot.


* Advanced String Methods:

Advanced String Methods
We've covered a bunch of String class methods already, so let's keep building on those and run down some more advanced methods.

The string method lower will return the string with all characters changed to lowercase. The inverse of this is the upper method, which will return the string all in uppercase. Just like with previous methods, we call these on a string using dot notation, like "this is a string".upper(). This would return the string "THIS IS A STRING". This can be super handy when checking user input, since someone might type in all lowercase, all uppercase, or even a mixture of cases.

You can use the strip method to remove surrounding whitespace from a string. Whitespace includes spaces, tabs, and newline characters. You can also use the methods  lstrip and rstrip to remove whitespace only from the left or the right side of the string, respectively.

The method count can be used to return the number of times a substring appears in a string. This can be handy for finding out how many characters appear in a string, or counting the number of times a certain word appears in a sentence or paragraph.

If you wanted to check if a string ends with a given substring, you can use the method endswith. This will return True if the substring is found at the end of the string, and False if not.

The isnumeric method can check if a string is composed of only numbers. If the string contains only numbers, this method will return True. We can use this to check if a string contains numbers before passing the string to the int() function to convert it to an integer, avoiding an error. Useful!

We took a look at string concatenation using the plus sign, earlier. We can also use the join method to concatenate strings. This method is called on a string that will be used to join a list of strings. The method takes a list of strings to be joined as a parameter, and returns a new string composed of each of the strings from our list joined using the initial string. For example, " ".join(["This","is","a","sentence"]) would return the string "This is a sentence".

The inverse of the join method is the split method. This allows us to split a string into a list of strings. By default, it splits by any whitespace characters. You can also split by any other characters by passing a parameter.


* Formatting Strings:

Up to now we've been making strings using the plus sign to just concatenate the parts of the string we wanted to create. And we've used the str function to convert numbers into strings so that we can concatenate them, too. This works, but it's not ideal, especially when the operations you want to do with the string or on the tricky side. There's a better way to do this using the format method. Let's see a couple of examples.

name = "manny"
number = len(name) * 3
print("Hello {}, your lucky number is {}".format(name, number))
Hello Many, Your lucky number is 15

In this example, we have two variables, name and number. We generate a string that has those variables in it by using the curly brackets placeholder to show where the variables should be written. We then pass the variables as a parameter to the format method. See how it doesn't matter that name is a string and number is an integer? The format method deals with that, so we don't have to. Pretty neat, right? The curly brackets aren't always empty. By using certain expressions inside those brackets, we can take advantage of the full power of the format expression. Heads up, this can get complex fast. If at any point, you get confused, don't panic, you only really need to understand the basic usage of the format method we just saw. One of the things we can put inside the curly brackets is the name of the variable we want in that position to make the whole string more readable. This is particularly relevant when the text can get rewritten or translated and the variables might switch places. In our earlier example, we could rewrite the message to make the variables appear in a different order. In that case, we'd need to pass the parameters to format in a slightly different way.

name = "manny"
number = len(name) * 3
print("Hello {}, your lucky number is {}".format(name, number))
O:Hello Many, Your lucky number is 15
print("Your lucky number is {number}, {name}.".format(name=name, number=len(name)*3))
O:Your lucky number is 15, Manny

Because we're using placeholders with variable names, the order in which the variables are passed to the format function doesn't matter. But for this to work, we need to set the names we're going to use and assign a value to them inside the parameters to format. And that's just the tip of the iceberg of what we can do with the format method. Want to dive a little deeper? Great, let's keep on going. 

price = 7.5
with_tax = price * 1.09
print(price, with_tax)
O:7.5 8.175
print("Base price: ${:.2f}. With Tax: ${:.2f}".format(price, with_tax))
O:Base price: $7.50. With Tax: $8.18


We're going to check out a different example. Let's say you want to output the price of an item with and without tax. Depending on what the tax rate is, the number might be a long number with a bunch of decimals. So if something costs $7.5 without tax and the tax rate is 9%, the price with tax would be $8.175. First off, ouch, and also, since there's no such thing as half a penny anymore, that number doesn't make sense. So to fix this we can make the format function print only two decimals, like this.


In this case between the curly brackets we're writing a formatting expression. There are a bunch of different expressions we can write. These expressions are needed when we want to tell Python to format our values in a way that's different from the default. The expression starts with a colon to separate it from the field name that we saw before. After the colon, we write .2f. This means we're going to format a float number and that there should be two digits after the decimal dot. So no matter what the price is, our function always prints two decimals.

def to_celsius(x):
    return (x-32)*5/9
for x in range(0,101,10):
    print("[:>3] F | {:>6.2f} C".format(x, to_celsius(x)))


Remember when we did the table to convert from Fahrenheit to Celsius temperatures? Our table looked kind of ugly because it was full of float numbers that had way too many decimal digits. Using the format function, we can make it look a lot nicer. In these two expressions we're using the greater than operator to align text to the right so that the output is neatly aligned. In the first expression we're saying we want the numbers to be aligned to the right for a total of three spaces. In the second expression we're saying we want the number to always have exactly two decimal places and we want to align it to the right at six spaces. We can use string formatting like this to make the output of our program look nice and also to generate useful logging and debugging messages. Over the course of my sysadmin career, I've grown used to formatting strings to create more informative error messages. They help me understand what's going on with a script that's failing. There's a ton more formatting options you can use when you need them. But don't worry about learning them all at once, we'll explain any others as they come along and we'll put everything in a cheat sheet that you can refer to whenever you need a formatting expression. Let's take a look at that now and then we'll have a quiz to help you get more familiar with all this new knowledge.


Practice:

Modify the student_grade function using the format method, so that it returns the phrase "X received Y% on the exam". For example, student_grade("Reed", 80) should return "Reed received 80% on the exam".

def student_grade(name, grade):
	return ""

print(student_grade("Reed", 80))
print(student_grade("Paige", 92))
print(student_grade("Jesse", 85))


* String Formatting:
You can use the format method on strings to concatenate and format strings in all kinds of powerful ways. To do this, create a string containing curly brackets, {}, as a placeholder, to be replaced. Then call the format method on the string using .format() and pass variables as parameters. The variables passed to the method will then be used to replace the curly bracket placeholders. This method automatically handles any conversion between data types for us. 

If the curly brackets are empty, they’ll be populated with the variables passed in the order in which they're passed. However, you can put certain expressions inside the curly brackets to do even more powerful string formatting operations. You can put the name of a variable into the curly brackets, then use the names in the parameters. This allows for more easily readable code, and for more flexibility with the order of variables.

You can also put a formatting expression inside the curly brackets, which lets you alter the way the string is formatted. For example, the formatting expression {:.2f} means that you’d format this as a float number, with two digits after the decimal dot. The colon acts as a separator from the field name, if you had specified one. You can also specify text alignment using the greater than operator: >. For example, the expression {:>3.2f} would align the text three spaces to the right, as well as specify a float number with two decimal places. String formatting can be very handy for outputting easy-to-read textual output.


* String Reference Guide:

In Python, there are a lot of things you can do with strings. In this guide, you’ll find the most common string operations and string methods.

String operations
len(string) - Returns the length of the string

for character in string - Iterates over each character in the string

if substring in string - Checks whether the substring is part of the string

string[i] - Accesses the character at index i of the string, starting at zero

string[i:j] - Accesses the substring starting at index i, ending at index j minus 1. If i is omitted, its value defaults to 0. If j is omitted, the value will default to len(string).



String methods
string.lower() - Returns a copy of the string with all lowercase characters

string.upper() - Returns a copy of the string with all uppercase characters

string.lstrip() - Returns a copy of the string with the left-side whitespace removed

string.rstrip() - Returns a copy of the string with the right-side whitespace removed

string.strip() - Returns a copy of the string with both the left and right-side whitespace removed

string.count(substring) - Returns the number of times substring is present in the string

string.isnumeric() - Returns True if there are only numeric characters in the string. If not, returns False.

string.isalpha() - Returns True if there are only alphabetic characters in the string. If not, returns False.

string.split() - Returns a list of substrings that were separated by whitespace (whitespace can be a space, tab, or new line)

string.split(delimiter) - Returns a list of substrings that were separated by whitespace or a delimiter

string.replace(old, new) - Returns a new string where all occurrences of old have been replaced by new.

delimiter.join(list of strings) - Returns a new string with all the strings joined by the delimiter 

Check out the official documentation for all available String methods.  https://docs.python.org/3/library/stdtypes.html#string-methods


* Formatting Strings Guide:

Python offers different ways to format strings. In the video, we explained the format() method. In this reading, we'll highlight three different ways of formatting strings. For this course you only need to know the format() method. But on the internet, you might find any of the three, so it's a good idea to know that the others exist.

Using the format() method
The format method returns a copy of the string where the {} placeholders have been replaced with the values of the variables. These variables are converted to strings if they weren't strings already. Empty placeholders are replaced by the variables passed to format in the same order.


# "base string with {} placeholders".format(variables)

example = "format() method"

formatted_string = "this is an example of using the {} on a string".format(example)

print(formatted_string)

"""Outputs:
this is an example of using the format() method on a string
"""

* If the placeholders indicate a number, they’re replaced by the variable corresponding to that order (starting at zero).

# "{0} {1}".format(first, second)

first = "apple"
second = "banana"
third = "carrot"

formatted_string = "{0} {2} {1}".format(first, second, third)

print(formatted_string)

"""Outputs:
apple carrot banana
"""

* If the placeholders indicate a field name, they’re replaced by the variable corresponding to that field name. This means that parameters to format need to be passed indicating the field name.

# "{var1} {var2}".format(var1=value1, var2=value2)


"{:exp1} {:exp2}".format(value1, value2)



* If the placeholders include a colon, what comes after the colon is a formatting expression. See below for the expression reference.

Official documentation for the format string syntax

# {:d} integer value
'{:d}'.format(10.5) → '10'


Formatting expressions

Expr                    Meaning                                                           Example

{:d}                    integer value                                               '{:d}'.format(10.5) → '10'

{:.2f}                  floating point with that many decimals                      '{:.2f}'.format(0.5) → '0.50'

{:.2s}                  string with that many characters                             '{:.2s}'.format('Python') → 'Py'

{:<6s}                  string aligned to the left that many spaces                 '{:<6s}'.format('Py') → 'Py    '

{:>6s}                  string aligned to the right that many spaces                '{:>6s}'.format('Py') → '    Py'

{:^6s}                  string centered in that many spaces                         '{:^6s}'.format('Py') → '  Py  '


 Check out the official documentation for all available expressions.

https://docs.python.org/3/library/string.html#format-specification-mini-language


Old string formatting (Optional)
The format() method was introduced in Python 2.6. Before that, the % (modulo) operator could be used to get a similar result. While this method is no longer recommended for new code, you might come across it in someone else's code. This is what it looks like:

 "base string with %s placeholder" % variable

The % (modulo) operator returns a copy of the string where the placeholders indicated by %  followed by a formatting expression are replaced by the variables after the operator.


 "base string with %d and %d placeholders" % (value1, value2)

To replace more than one value, the values need to be written between parentheses. The formatting expression needs to match the value type.

 

"%(var1) %(var2)" % {var1:value1, var2:value2}

Variables can be replaced by name using a dictionary syntax (we’ll learn about dictionaries in an upcoming video).

 

"Item: %s - Amount: %d - Price: %.2f" % (item, amount, price)

The formatting expressions are mostly the same as those of the format() method. 

Check out the official documentation for old string formatting.

Formatted string literals (Optional)
This feature was added in Python 3.6 and isn’t used a lot yet. Again, it's included here in case you run into it in the future, but it's not needed for this or any upcoming courses.

A formatted string literal or f-string is a string that starts with 'f' or 'F' before the quotes. These strings might contain {} placeholders using expressions like the ones used for format method strings.

The important difference with the format method is that it takes the value of the variables from the current context, instead of taking the values from parameters.

 Examples:

>>> name = "Micah"

>>> print(f'Hello {name}')

Hello Micah

 

>>> item = "Purple Cup"

>>> amount = 5

>>> price = amount * 3.25

>>> print(f'Item: {item} - Amount: {amount} - Price: {price:.2f}')

Item: Purple Cup - Amount: 5 - Price: 16.25

 Check out the official documentation for f-strings. https://docs.python.org/3/reference/lexical_analysis.html#f-strings
----


Study Guide: Strings

This study guide provides a quick-reference summary of what you learned in this lesson and serves as a guide for the upcoming practice quiz. The string readings in this section are great syntax guides to help you on the Strings Practice Quiz.

In the Strings segment, you learned about the parts of a string, string indexing and slicing, creating new strings, string methods and operations, and formatting strings. 


Knowledge

String Operations and Methods

    * .format() - String method that can be used to concatenate and format strings. 

            * {:.2f} - Within the .format() method, limits a floating point variable to 2 decimal places. The number of decimal places can be customized.

* len(string) - String operation that returns the length of the string.

* string[x] - String operation that accesses the character at index [x] of the string, where indexing starts at zero.

* string[x:y] - String operation that accesses a substring starting at index [x] and ending at index [y-1]. If x is omitted, its value defaults to 0. If y is omitted, the value will default to len(string).

* string.replace(old, new) - String method that returns a new string where all occurrences of an old substring have been replaced by a new substring.

* string.lower() - String method that returns a copy of the string with all lowercase characters.


Coding skills:

Skill Group 1:
. Use a for loop to iterate through each letter of a string.

. Add a character to the front of a string.

. Add a character to the end of a string.

. Use the .lower() string method to convert the case (uppercase/lowercase) of the letters within a string variable. This method is often used to eliminate cases as a factor when comparing two strings. For example, all lowercase “cat” is not equal to “Cat” because “Cat” contains an uppercase letter. To be able to compare the two strings to see if they are the same word, you can use the .lower() string method to remove capitalization as a factor in the string comparison.


# This function accepts a given string and checks each character of 
# the string to see if it is a letter or not. If the character is a
# letter, that letter is added to the end of the string variable
# "forwards" and to the beginning of the string variable "backwards".
def mirrored_string(my_string):

    # Two variables are initialized as string data types using empty 
    # quotes. The variable "forwards" will hold the "my_string"
    # minus any character that is not a letter. The "backwards" 
    # variable will hold the same letters as "forwards", but in  
    # in reverse order.
    forwards = ""
    backwards = ""

    # The for loop iterates through each character of the "my_string"
    for character in my_string:

        # The if-statement checks if the character is not a space.
        if character.isalpha():

            # If True, the body of the loop adds the character to the
            # to the end of "forwards" and to the front of
            # "backwards". 
            forwards += character
            backwards = character + backwards

        # If False (meaning the character is not a letter), no action
        # is needed. This coding approach results prevents any 
        # non-alphabetical characters from being written to the
        # "forwards" and "backwards" variables. The for loop will 
        # restart until all characters in "my_string" have been
        # processed.
        
    # The final if-statement compares the "forwards" and "backwards"
    # strings to see if the letters are the same both forwards and
    # backwards. Since Python is case sensitive, the two strings will 
    # need to be converted to use the same case for this comparison. 
    if forwards.lower() == backwards.lower():
        return True
    return False
 
print(mirrored_string("12 Noon")) # Should be True
print(mirrored_string("Was it a car or cat I saw")) # Should be False
print(mirrored_string("'eve, Madam Eve")) # Should be True


Skill Group 2:

. Use the format() method, with {} placeholders for variable data, to create a new string.

. Use a formatting expression, like {:.2f}, to format a float variable and configure the number of decimal places to display for the float. 

# This function converts measurement equivalents. Output is formatted 
# as, "x ounces equals y pounds", with y limited to 2 decimal places. 
def convert_weight(ounces):

    # Conversion formula: 1 pound = 16 ounces
    pounds = ounces/16 
    
    # The result is composed using the .format() method. There are two
    # placeholders in the string: the first is for the "ounces" 
    # variable and the second is for the "pounds" variable. The second
    # placeholder formats the float result of the conversion 
    # calculation to be limited to 2 decimal places.
    result = "{} ounces equals {:.2f} pounds".format(ounces,pounds)
    return result


print(convert_weight(12)) # Should be: 12 ounces equals 0.75 pounds
print(convert_weight(50.5)) # Should be: 50.5 ounces equals 3.16 pounds
print(convert_weight(16)) # Should be: 16 ounces equals 1.00 pounds


 Skill Group 3  

. Within the format() parameters, select characters at specific index [ ] positions from a variable string.  

. Use the format() method, with {} placeholders for variable data, to create a new string.

# This function generates a username using the first 3 letters of a
# user’s last name plus their birth year. 
def username(last_name, birth_year):
    
    # The .format() method will use the first 3 letters at index 
    # positions [0,1,2] of the "last_name" variable for the first
    # {} placeholder. The second {} placeholder concatenates the user’s
    #  "birth_year" to that string to form a new string username.
    return("{}{}".format(last_name[0:3],birth_year))


print(username("Ivanov", "1985")) 
# Should display "Iva1985" 
print(username("Rodríguez", "2000")) 
# Should display "Rod2000" 
print(username("Deng", "1991")) 
# Should display "Den1991"



Skill Group 4:

. Use the .replace() method to replace part of a string.  

. Use the len() function to get the number of index positions in a string.

. Slice a string at a specific index position.



# This function checks a given schedule entry for an old date and, if 
# found, the function replaces it with a new date. 
def replace_date(schedule, old_date, new_date):

    # Check if the given "old_date" appears at the end of the given 
    # string variable "schedule". 
    if schedule.endswith(old_date):

        # If True, the body of the if-block will run. The variable "n" is
        # used to hold the slicing index position. The len() function
        # is used to measure the length of the string "new_date".
        p = len(old_date)

        # The "new_schedule" string holds the updated string with the 
        # old date replaced by the new date. The schedule[:-p] part of 
        # the code trims the "old_date" substring from "schedule" 
        # starting at the final index position (or right-side) counting
        # towards the left the same number of index positions as 
        # calculated from len(old_date). Then, the code schedule[-p:]
        # starts the indexing position at the slot where the first
        # character of the "old_date" used to be positioned. The 
        # .replace(old_date, new_date) code inserts the "new_date" into
        # the position where the "old_date" used to exist.  
        new_schedule = schedule[:-p] + schedule[-p:].replace(old_date, new_date)

        # Returns the schedule with the new date.
        return new_schedule
        
    # If the schedule does not end with the old date, then return the
    # original sentence without any modifications.
    return schedule
 
 
print(replace_date("Last year’s annual report will be released in March 2023", "2023", "2024")) 
# Should display "Last year’s annual report will be released in March 2024"
print(replace_date("In April, the CEO will hold a conference", "April", "May")) 
# Should display "In April, the CEO will hold a conference"
print(replace_date("The convention is scheduled for October", "October", "June")) 
# Should display "The convention is scheduled for June"


Practice Quiz: 

Question 1
Fill in the blanks to complete the is_palindrome function. This function checks if a given string is a palindrome. A palindrome is a string that contains the same letters in the same order, whether the word is read from left to right or right to left. Examples of palindromes are words like kayak and radar, and phrases like "Never Odd or Even". The function should ignore blank spaces and capitalization when checking if the given string is a palindrome. Complete this function to return True if the passed string is a palindrome, False if not. 

def is_palindrome(input_string):
    # Two variables are initialized as string date types using empty 
    # quotes: "reverse_string" to hold the "input_string" in reverse
    # order and "new_string" to hold the "input_string" minus the 
    # spaces between words, if any are found.
    new_string = ""
    reverse_string = ""

    # Complete the for loop to iterate through each letter of the
    # "input_string"
    for ___:

        # The if-statement checks if the "letter" is not a space.
        if letter != " ":

            # If True, add the "letter" to the end of "new_string" and
            # to the front of "reverse_string". If False (if a space
            # is detected), no action is needed. Exit the if-block.
            new_string = ___
            reverse_string = ___

    # Complete the if-statement to compare the "new_string" to the
    # "reverse_string". Remember that Python is case-sensitive when
    # creating the string comparison code. 
    if ___:

        # If True, the "input_string" contains a palindrome.
        return True
		
    # Otherwise, return False.
    return False


print(is_palindrome("Never Odd or Even")) # Should be True
print(is_palindrome("abc")) # Should be False
print(is_palindrome("kayak")) # Should be True


q:

Using the format method, fill in the gaps in the convert_distance function so that it returns the phrase "X miles equals Y km", with Y having only 1 decimal place. For example, convert_distance(12) should return "12 miles equals 19.2 km".

def convert_distance(miles):
    km = miles * 1.6 
    result = "{} miles equals {___} km".___
    return result


print(convert_distance(12)) # Should be: 12 miles equals 19.2 km
print(convert_distance(5.5)) # Should be: 5.5 miles equals 8.8 km
print(convert_distance(11)) # Should be: 11 miles equals 17.6 km


q:

If we have a string variable named Weather = "Rainfall", which of the following will print the substring "Rain" or all characters before the "f"?


print(Weather[:4])


print(Weather[4:])


print(Weather[1:4])


print(Weather[:"f"])


q:

Question 4
Fill in the gaps in the nametag function so that it uses the format method to return first_name and the first initial of last_name followed by a period. For example, nametag("Jane", "Smith") should return "Jane S."

def nametag(first_name, last_name):
    return("___.".format(___))


print(nametag("Jane", "Smith")) 
# Should display "Jane S." 
print(nametag("Francesco", "Rinaldi")) 
# Should display "Francesco R." 
print(nametag("Jean-Luc", "Grand-Pierre")) 
# Should display "Jean-Luc G." 


q:

The replace_ending function replaces a specified substring at the end of a given sentence with a new substring. If the specified substring does not appear at the end of the given sentence, no action is performed and the original sentence is returned. If there is more than one occurrence of the specified substring in the sentence, only the substring at the end of the sentence is replaced. For example, replace_ending("abcabc", "abc", "xyz") should return abcxyz, not xyzxyz or xyzabc. The string comparison is case-sensitive, so replace_ending("abcabc", "ABC", "xyz") should return abcabc (no changes made).  


def replace_ending(sentence, old, new):
    # Check if the old substring is at the end of the sentence 
    if ___:
        # Using i as the slicing index, combine the part
        # of the sentence up to the matched string at the 
        # end with the new string
        i = ___
        new_sentence = ___
        return new_sentence


    # Return the original sentence if there is no match 
    return sentence
    
print(replace_ending("It's raining cats and cats", "cats", "dogs")) 
# Should display "It's raining cats and dogs"
print(replace_ending("She sells seashells by the seashore", "seashells", "donuts")) 
# Should display "She sells seashells by the seashore"
print(replace_ending("The weather is nice in May", "may", "april")) 
# Should display "The weather is nice in May"
print(replace_ending("The weather is nice in May", "May", "April")) 
# Should display "The weather is nice in April"
---

# Lists and Tuples:

x = ["Now", "we", "are", "cooking!"]
type(x)
O:<class 'list'>
print(x)
O:["Now", "we", "are", "cooking!"]
len(x)
O:4
print("are" in x)
O:True
print("ToDAY" in x)
O:False
print(x[0])
O:Now
print(x[3])
O:cooking!
print(x[4])
O:Index error: list index out of range
print(x[1:3])
O:['we', 'are']
x[:2]
O:['Now', 'we']



As you know by now, Python comes with a lot of ready-to-use data types. We've seen integers, floats, Booleans, and strings in detail. But those data types can only take you so far. Eventually in your scripts, you want to develop code that manipulates collections of items like a list of strings representing all the file names in a directory or a list of integers representing the size of network packets. This is where the list data type comes in handy. You can think of lists as long boxes with the space inside the box divided up into different slots. Each slot can contain a different value. Like we mentioned earlier when we first came across the list, in Python, we use square brackets to indicate where the list starts and ends. Let's check out an example.

Here, we've created a new variable called x and set its contents to be a list of strings. We can check the type of x using the type function we saw a little while ago. Nice. Python tells us this is a list. In the same way, we've done with other variables, we can show the contents of the whole list using the print function. The length of the list is how many elements it has. To get that value, we'll use the same len function we used for strings. That's right. Our list has four elements. When calling Len for the list, it doesn't matter how long each string is on its own. What matters is how many elements the list has. To check if a list contains a certain element, you can use the keyword "in" like in these examples.

Again, like when we use this with strings, the result of this check is a Boolean, which we can use as a condition for branching or looping. We can also use indexing to access individual elements depending on their position in the list. To do that, we use the square brackets and the index we want to access, exactly like we did with strings. Remember that the first element is given the index zero. This means the last index of the list will be the length of the list minus one. What happens if we try to access an element after the end of the list?

You might have seen this coming. We get an index error. We can't go over the end of the list. Remember that because list indexes start at zero, accessing the item at index four means we're trying to access the fifth element in the list. There are only four elements. So we're out of range if we try to access the index number four. Does this seem a bit confusing? If it does, this visualization might help you out. As you can see, index four doesn't point at anything since there's no slot four in our list. As with strings, we can also use indexes to create a slice of the list. For this, we use ranges of two numbers separated by a colon. Again, the second element isn't included in the slice. So the range goes to the second index minus one. Here, we start at index one and go up to one less than three, which is two. We can also leave out one of the range indexes empty. The first value defaults to zero and the second value to the length of the list. Makes sense? If all this sounds really familiar to what we said about strings, then this course is working as intended. That's because strings and lists are very similar data types. In Python, strings and lists are both examples of sequences.

for element in sequence

sequence[x]

len(sequence)

sequence + sequence

element in sequence

There are other sequences too, and they all share a bunch of operations like iterating over them using for-loops, indexing using the len function to know the length of the sequence, using plus to concatenate two sequences and using in to verify if the sequence contains an element. So this is great news. While understanding indexing is hard, once you know it for one data type, you've pretty much mastered it for every data type. So you actually know way more than you thought. Wow, now, we're really cooking. Next up, we're going to look at some more list operations. This time, actually specific to lists.

Practice:

Using the "split" string method from the preceding lesson, complete the get_word function to return the {n}th word from a passed sentence. For example, get_word("This is a lesson about lists", 4) should return "lesson", which is the 4th word in this sentence. Hint: remember that list indexes start at 0, not 1. 

def get_word(sentence, n):
	# Only proceed if n is positive 
	if n > 0:
		words = ___
		# Only proceed if n is not more than the number of words 
		if n <= len(words):
			return(___)
	return("")

print(get_word("This is a lesson about lists", 4)) # Should print: lesson
print(get_word("This is a lesson about lists", -4)) # Nothing
print(get_word("Now we are cooking!", 1)) # Should print: Now
print(get_word("Now we are cooking!", 5)) # Nothing


Lists Defined:

Lists in Python are defined using square brackets, with the elements stored in the list separated by commas: list = ["This", "is", "a", "list"]. You can use the len() function to return the number of elements in a list: len(list) would return 4. You can also use the in keyword to check if a list contains a certain element. If the element is present, it will return a True boolean. If the element is not found in the list, it will return False. For example, "This" in list would return True in our example. Similar to strings, lists can also use indexing to access specific elements in a list based on their position. You can access the first element in a list by doing list[0], which would allow you to access the string "This".

In Python, lists and strings are quite similar. They’re both examples of sequences of data. Sequences have similar properties, like (1) being able to iterate over them using for loops; (2) support indexing; (3) using the len function to find the length of the sequence; (4) using the plus operator + in order to concatenate; and (5) using the in keyword to check if the sequence contains a value. Understanding these concepts allows you to apply them to other sequence types as well.

* Modifying the Contents of the list:

One of the ways that lists and strings are different is that lists are mutable. Which is another fancy word to say that they can change. This means we can add, remove, or modify elements in a list. Let's go back to our example of thinking of a list as a long box. Changing the list means we keep the same box and we add, remove, or change the elements inside that box. We'll now go through the methods that let us modify the list one by one. If all these details seem a little overwhelming, that's okay. As usual, there will be a cheat sheet at the end and you'll have lots of chances to practice each of these methods as we go along. You don't need to learn all those by heart, and of course you can always review anything that isn't clear. So don't worry, we got your back. We'll start with the simplest change; adding an element to a list using the append method. Let's check this out in the tastiest example yet.

* appened method

fruits = ["Pineapple" , "Banana", "Apple", "Melon" ]
fruits. append("Kiwi")
print(fruits)
O:['Pineapple', 'Banana' , 'Apple' , 'Melon', 'Kiwi']


The append method adds a new element at the end of the list. It doesn't matter how long the list is. The element always gets added to the end. You could start with an empty list and add all of its items using append. If you want to insert an element in a different position, instead of at the end, you can use the insert method.

* insert Method
fruits = ["Pineapple" , "Banana", "Apple", "Melon" ]
fruits. insert(0, "Orange")
print(fruits)
# This will take position of index in the list
O: ['Orange', 'Pineapple', 'Banana', 'Apple', 'Melon', 'Kiwi']

The insert method takes an index as the first parameter and an element as the second parameter. It adds the element at that index in the list. To add it as the first element, we use index zero and we can use any other number. What happens if we use a number larger than the length of the list?

fruits.insert(25, "Peach")
print(fruits)
O:['Orange', 'Pineapple', 'Banana', 'Apple', 'Melon', 'Kiwi', 'Peach']

No errors. You can say that it even worked just peachy. If we use an index higher than the current length, the element just gets added to the end. You can pass any number to insert but usually, you either add at the beginning using insert at the zero index or at the end using append. We can also remove elements from the list. We can do it using the value of the element we want to remove. Can you guess what method we would use? You got it, use the remove method.

fruits.remove("Melon")
print(fruits)
O:['Orange', 'Pineapple', 'Banana', 'Apple', 'Kiwi', 'Peach']

The remove method removes from the list the first occurrence of the element we pass to it. What happens if the element is not in the list?

fruits.remove("Pear")
O: Value error: list.remove(x): x not in list

That went pear-shaped. We got a value error, telling us the element isn't in the list. Another way we can remove elements is by using the pop method, which receives an index.

fruits.pop(3)
O:"Apple"

The pop method returns the element that was removed at the index that was passed. In the last way to modify the contents of a list is to change an item by assigning something else to that position, like this.

print(fruits)
['Orange', 'Pineapple', 'Banana', 'Melon', 'Kiwi', 'Peach']

fruits[2] = "Strawberry"
print(fruits)
['Orange', 'Pineapple', 'Strawberry', 'Kiwi', 'Peach']

Wow, the contents of our fruits variable have changed a lot since we started this video. But it's always the same variable, the same box. We've just modified what's inside. Modifying the contents of lists will come up in tons of scripts as we operate with them. If the list contains hosts on a network, you could add or remove hosts as they come online or offline. If the list contains users authorized to run a certain process, you could add or remove users when permissions are granted or removed and so on. You've now seen a number of methods that let us modify the contents of a list, adding, removing, and changing the elements that are stored inside the list. Whenever you need to write a program that'll handle a variable amount of elements, you'll use a list. What if you need a sequence of a fixed amount of elements? That's coming up in our next video.


* Modifying Lists:

While lists and strings are both sequences, a big difference between them is that lists are mutable. This means that the contents of the list can be changed, unlike strings, which are immutable. You can add, remove, or modify elements in a list.

You can add elements to the end of a list using the append method. You call this method on a list using dot notation, and pass in the element to be added as a parameter. For example, list.append("New data") would add the string "New data" to the end of the list called list.

If you want to add an element to a list in a specific position, you can use the method insert. The method takes two parameters: the first specifies the index in the list, and the second is the element to be added to the list. So list.insert(0, "New data") would add the string "New data" to the front of the list. This wouldn't overwrite the existing element at the start of the list. It would just shift all the other elements by one. If you specify an index that’s larger than the length of the list, the element will simply be added to the end of the list.

You can remove elements from the list using the remove method. This method takes an element as a parameter, and removes the first occurrence of the element. If the element isn’t found in the list, you’ll get a ValueError error explaining that the element was not found in the list.

You can also remove elements from a list using the pop method. This method differs from the remove method in that it takes an index as a parameter, and returns the element that was removed. This can be useful if you don't know what the value is, but you know where it’s located. This can also be useful when you need to access the data and also want to remove it from the list.

Finally, you can change an element in a list by using indexing to overwrite the value stored at the specified index. For example, you can enter list[0] = "Old data" to overwrite the first element in a list with the new string "Old data".

* list and Tuples

As we called out before, there are a number of data types in Python that are all sequences. Strings are sequences of characters and are immutable. 

Lists are sequences of elements of any type and are mutable. 

A third data type that's a sequence and also closely related to lists is the tuple. Tuples are sequences of elements of any type that are immutable. 

We write tuples in parentheses() instead of square brackets[].

fullname = ('Grace', 'M', 'Hopper')

You might be wondering, why do we even need another sequence type? Weren't lists great? Yes, lists are great. They can hold any number of elements and we can add, remove and modify their contents as much as we want, but there are cases when we want to make sure an element in a certain position or index refers to one specific thing and won't change. In these situations, lists won't help us. Thanks for nothing lists. In our example,


fullname = ('Grace', 'M', 'Hopper')


we have a tuple that represents someone's full name. The first element of the tuple is the first-name. The second element is the middle initial, and the third element is the last-name. If we add another element somewhere in there, what would that element represent? It would just be confusing and our code wouldn't know what to do with it, and that's why modifying isn't allowed. In other words, when using tuples the position of the elements inside the tuple have meaning. 

Tuples are used for lots of different things in Python. One common example is the return value of functions. When a function returns more than one value, it's actually returning a tuple. Remember the function to convert seconds to hours, minutes, and seconds that we saw a while back? Here just to remind you. This function returns three values. In other words, it returns a tuple of three elements. Let's give it a try.

Example: 

def convert_seconds(seconds):
    hours = seconds // 3600
    minutes = (seconds - hours *3600) // 60
    remaining_seconds = seconds - hours * 3600 - minutes * 60
    return hours, minutes, remaing_seconds

result = convert_seconds(5000)
type(result)
O:<class "tuple">
print(result)
O:(1, 23, 20)
hours, minutes, seconds = result
print(hours, minutes, seconds)
O: 1 23 20
hours, minutes, seconds = convert_seconds(1000)
print(hours, minutes, seconds)
O: 0 16 40

We see the result is a tuple. What if we print it? We see that it has the three elements we expect it to have. Remember, since this is a tuple, the order matters. The first element represents the hours, the second one represents the minutes, and the third represents the seconds. One interesting thing we can do with tuples is unpack them. This means that we can turn a tuple of three elements into three separate variables. Because the order won't change, we know what those variables are present, like this.

So now we've split the tuple into three separate values. We've seen before that we can also do this directly when calling the function without the intermediate result variable.

In Python, it's really common to use tuples to represent data that has more than one value and that needs to be kept together. For example, you could use a tuple to have a filename and it's size, or you could store the name and email address of a person, or a date and time and the general health of the system at any point in time. Can you see how these different data types could help you automate some of your IT work? Pretty cool, right? Knowing when to use tuples and when to use lists can seem a little fuzzy at first, but don't worry, it'll get clearer as we tackle more examples.


Practice:
Let's use tuples to store information about a file: its name, its type and its size in bytes. Fill in the gaps in this code to return the size in kilobytes (a kilobyte is 1024 bytes) up to 2 decimal places. 

def file_size(file_info):
	___, ___, ___= file_info
	return("{:.2f}".format(___ / 1024))

print(file_size(('Class Assignment', 'docx', 17875))) # Should print 17.46
print(file_size(('Notes', 'txt', 496))) # Should print 0.48
print(file_size(('Program', 'py', 1239))) # Should print 1.21
---

* Tuples Defination:
As we mentioned earlier, strings and lists are both examples of sequences. Strings are sequences of characters, and are immutable. Lists are sequences of elements of any data type, and are mutable. The third sequence type is the tuple. Tuples are like lists, since they can contain elements of any data type. But unlike lists, tuples are immutable. They’re specified using parentheses instead of square brackets.

You might be wondering why tuples are a thing, given how similar they are to lists. Tuples can be useful when we need to ensure that an element is in a certain position and will not change. Since lists are mutable, the order of the elements can be changed on us. Since the order of the elements in a tuple can't be changed, the position of the element in a tuple can have meaning. A good example of this is when a function returns multiple values. In this case, what gets returned is a tuple, with the return values as elements in the tuple. The order of the returned values is important, and a tuple ensures that the order isn’t going to change. Storing the elements of a tuple in separate variables is called unpacking. This allows you to take multiple returned values from a function and store each value in its own variable.


* Iterating Over Lists and Tuples:

When we covered for loops, we showed the example of iterating over a list. This lets you iterate over each element in the list, exposing the element to the for loop as a variable. But what if you want to access the elements in a list, along with the index of the element in question? You can do this using the enumerate() function. The enumerate() function takes a list as a parameter and returns a tuple for each element in the list. The first value of the tuple is the index and the second value is the element itself.

EX:

animals = ["lion", "zebra", "dolphin", "monkey"]
chars = 0
for animal in animals:
    char += len(animals)

print("Total characters: {}, average length: {}".format(chars, chars/len(animals)))

Explanantion:In this code, we're iterating over a list of strings. For each of the strings, we get its length and add it to the total amount of characters. At the end we print the total and the average which we get by dividing the total by the length of the list. You can see we're using the len function twice, once to get the length of the string and then again to get the amount of elements in the list. What if you wanted to know the index of an element while going through the list? You could use the range function and then use indexing to access the elements at the index that range returned. You could use a range function and then use indexing to access the elements at the index that range just returned or you could just use the enumerate function.

* Enumerate:

winners = ["Ashley", "Dylan", "Reese"]
for index, person in enumerate(winners):
    print("{} - {}".format(index + 1, person))


Winners equals, we'll make a list, Ashley, Dylan, and Reese and close the list for index, person in enumerate winners.print curly brackets dash curly brackets.format index plus one person.The enumerate function returns a tuple for each element in the list. The first value in the tuple is the index of the element in the sequence. The second value in the tuple is the element in the sequence. You're the real winner with the enumerate function. It does all the work for you.

EX2:

def full_emails(people):
    result = []
    for email, name in people:
        result.append("{} <{}>".format(name, email))
    return result
print(full_emails([("mirza@gmail.com", "mirza"),("saad@gmai.com", "saad")]))

Explananation:
Say you have a list of tuples containing two strings each. The first string is an email address and the second is the full name of the person with that email address. You want to write a function that creates a new list containing one string per person including their name and the email address between angled brackets. the format usually used in emails like this. So what do we need to do?We'll start by defining a function that receives a list of people, def full_emails, takes the argument people.Remember, people is a list of tuples where the first element is the email address and the second one is the full name. So in our function, we'll first create the variable that we'll use as a return value which will be a list and we'll call it result. Result equals empty list. We'll then iterate over the list of people. We know this list contains tuples of two strings each. So we'll unpack the values directly when iterating in variables that we'll call email and name for email and name in people. Now, our result variable is a list and it should contain strings. So we'll append to the resulting string to the results list, result.append. The string that will append will be formatted in the way we want. To do that, we'll use the format method with the two variables of our iteration. So curly brackets, curly brackets.format, name, and email.Once we're done with the iteration, we'll return the list which should now contain all the necessary emails, return result.Will this work? What do you think? Let's try it out. Print full emails Alex@example.com, Alex Diego.Shay@example.com is the email and we'll call Shay Brandt as the name.Yes, this worked as expected. Before we move on, a quick word of caution about some common errors when dealing with lists in Python. Because we use the range function so much with for loops, you might be tempted to use it for iterating over indexes of a list and then to access the elements through indexing. You could be particularly inclined to do this if you're used to other programming languages before. Because in some languages, the only way to access an element of a list is by using indexes. Real talk, this works but looks ugly. It's more idiomatic in Python to iterate through the elements of the list directly or using enumerate when you need the indexes like we've done so far.

* QUESTION:
Try out the enumerate function for yourself in this quick exercise. Complete the skip_elements function to return every other element from the list, this time using the enumerate function to check if an element is in an even position or an odd position.

def skip_elements(elements):
	# code goes here
	
	return ___

print(skip_elements(["a", "b", "c", "d", "e", "f", "g"])) # Should be ['a', 'c', 'e', 'g']
print(skip_elements(['Orange', 'Pineapple', 'Strawberry', 'Kiwi', 'Peach'])) # Should be ['Orange', 'Strawberry', 'Peach']


* Iterating Over Lists Using Enumerate:

When we covered for loops, we showed the example of iterating over a list. This lets you iterate over each element in the list, exposing the element to the for loop as a variable. But what if you want to access the elements in a list, along with the index of the element in question? You can do this using the enumerate() function. The enumerate() function takes a list as a parameter and returns a tuple for each element in the list. The first value of the tuple is the index and the second value is the element itself.

* Lists Comprehensions:

multiples = []
for x in range(1,11)
  multiple.append(x*7)

print(multiples)

Explanation:
creating lists based on sequences is such a common task Python provides a technique called list comprehension, that lets us do it in just one line. This is how we would do the same with list comprehension. Multiples =, we'll start the list, [ x * 7 for x in range(1,11)], and close the list. Print(multiples), it should be the same. List comprehensions let us create new lists based on sequences or ranges. So we can use this technique whenever we want to create a list based on a range like in this example. Or based on the contents of a list a tuple a string or any other Python sequence. The syntax tries to copy how you would express these concepts with natural language, although it can still be confusing sometimes. 

Ex:

languages = ["python", "perl", "ruby", "go", "java", "c"]
lengths = [len(language) for language in languages]
print(lenghths)

Explanation:
creating lists based on sequences is such a common task Python provides a technique called list comprehension, that lets us do it in just one line. This is how we would do the same with list comprehension. Multiples =, we'll start the list, [ x * 7 for x in range(1,11)], and close the list. Print(multiples), it should be the same. List comprehensions let us create new lists based on sequences or ranges. So we can use this technique whenever we want to create a list based on a range like in this example. Or based on the contents of a list a tuple a string or any other Python sequence. The syntax tries to copy how you would express these concepts with natural language, although it can still be confusing sometimes.

EX2:

z = [x for x in range (0,101) if x % 3 == 0]
print(z)            # this prints multiples of 3 because the if condition states there should not be any remainder

Say we wanted all the numbers that are divisible by 3 between 0 and a 100, we could create a list like this z = [x for x in range(0,101 ) if x module 3 == 0] print(z). In this case we just want the element x to be a part of the list, but we only want the numbers where the remainder of the division by 3 is 0. So we add the conditional clause after the range. Using list comprehensions when programming in Python is totally optional. 

* QUESTION:

The odd_numbers function returns a list of odd numbers between 1 and n, inclusively. Fill in the blanks in the function, using list comprehension. Hint: remember that list and range counters start at 0 and end at the limit minus 1.

def odd_numbers(n):
	return [x for x in ___ if ___]

print(odd_numbers(5))  # Should print [1, 3, 5]
print(odd_numbers(10)) # Should print [1, 3, 5, 7, 9]
print(odd_numbers(11)) # Should print [1, 3, 5, 7, 9, 11]
print(odd_numbers(1))  # Should print [1]
print(odd_numbers(-1)) # Should print []

* List Comprehensions Examples:

List Comprehension Examples
You can create a list from a sequence using a for loop, but there’s a more streamlined way to do this by using a list comprehension. List comprehensions allow you to create a new list from a sequence or a range in a single line.


Simple List Comprehension
For example, [ x*2 for x in range(1,11) ] is a simple list comprehension. This single line of code iterates over a range from 1 to 10, multiplies each element in the range by 2, and creates a new list from all multiples of 2 from 2 to 20.

### Simple List Comprehension
print("List comprehension result:")

# The following list comprehension compacts several lines 
# of code into one line:
print([x*2 for x in range(1,11)]) 


### Long form for loop
print("Long form code result:")

# The list comprehension above accomplishes the same result as
# the long form version of the code:
my_list = []
for x in range(1,11):
   my_list.append(x*2)
print(my_list)
# Click Run to compare the two results.

List Comprehension with Conditional Statement:

You can also use conditionals with list comprehensions to build even more complex and powerful statements. You can do this by appending an if statement to the end of the list comprehension. For example, [ x for x in range(1,101) if x % 10 == 0 ] generates a new list containing all the integers divisible by 10 from 1 to 100. The if statement evaluates each value in the range from 1 to 100 to check if it’s evenly divisible by 10. If it is, the number is added to a new list.

### List Comprehension with Conditional Statement
print("List comprehension result:")

# The following list comprehension compacts multiple lines 
# of code into one line:
print([ x for x in range(1,101) if x % 10 == 0 ])

### Long form for loop with nested if-statement
print("Long form code result:")

# The list comprehension above accomplishes the same result as
# the long form version of the code:
my_list = []
for x in range(1,101):
  if x % 10 == 0:
    my_list.append(x)
print(my_list)
# Click Run to observe the two results.

List comprehensions can be really powerful, but they can also be complex, resulting in code that’s hard to read. Be careful when using them, since it might make it more difficult for someone else looking at your code to easily understand what the code is doing. It is a best practice to add descriptive comments about any list comprehensions used in your code. This helps to communicate the purpose of list comprehensions to other coders. Comments will also help you remember the goal of the code when performing future code additions and maintenance.  



Practice exercise:
This exercise will walk you through how to write a list comprehension to create a list of squared numbers (n*n). It needs to return a list of squares of consecutive numbers between “start” and “end” inclusively. For example, squares(2, 3) should return a list containing [4, 9].

The function receives the variables “start” and “end” through the function parameters. 

In the return line, start by entering the list brackets [ ]

Between the brackets [ ], enter the arithmetic expression to square a variable “n”. 

To the right of the square expression, write a for loop that iterates over “n” in a range from the “start” to “end” variables.

Ensure the “end” range value is included in the range() by adding 1 to it.

Run your code to see if it works!  If needed, the solution to this code is included in the “Study Guide: List Operations and Methods” reading under “Skill Group 2” (list comprehensions). 

def squares(start, end):
    return ___ 


print(squares(2, 3))  # Should print [4, 9]
print(squares(1, 5))  # Should print [1, 4, 9, 16, 25]
print(squares(0, 10)) # Should print [0, 1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
---

Study Guide: Lists Operations and Methods:

This study guide provides a quick-reference summary of what you learned in this lesson and serves as a guide for the upcoming practice quiz. 

In the Lists and Tuples segment, you learned about the differences between lists and tuples, how to modify the contents of a list, how to iterate over lists and tuples, how to use the enumerate() function, and how to create list comprehensions. 


Knowledge
Common sequence operations
Lists and tuples are both sequences and they share a number of sequence operations. The following common sequence operations are used by both lists and tuples:

. len(sequence) - Returns the length of the sequence.

. for element in sequence - Iterates over each element in the sequence.

. if element in sequence - Checks whether the element is part of the sequence.

. sequence[x] - Accesses the element at index [x] of the sequence, starting at zero

. sequence[x:y] - Accesses a slice starting at index [x], ending at index [y-1]. If [x] is omitted, the index will start at 0 by default. If [y] is  omitted, the len(sequence) will set the ending index position by default.

. for index, element in enumerate(sequence) - Iterates over both the indices and the elements in the sequence at the same time.


List-specific operations and methods:

One major difference between lists and tuples is that lists are mutable (changeable) and tuples are immutable (not changeable). There are a few operations and methods that are specific to changing data within lists:

. list[index] = x - Replaces the element at index [n] with x.

. list.append(x) - Appends x to the end of the list.

. list.insert(index, x) - Inserts x at index position [index].

. list.pop(index) - Returns the element at [index] and removes it from the list. If [index] position is not in the list, the last element in the list is returned and removed.

. list.remove(x) - Removes the first occurrence of x in the list.

. list.sort() - Sorts the items in the list.

. list.reverse() - Reverses the order of items of the list.

. list.clear() - Deletes all items in the list.

. list.copy() - Creates a copy of the list.

. list.extend(other_list) - Appends all the elements of other_list at the end of list


List comprehensions:

A list comprehension is an efficient method for creating a new list from a sequence or a range in a single line of code. It is a best practice to add descriptive comments about any list comprehensions used in your code, as their purpose can be difficult to interpret by other coders.

. [expression for variable in sequence] - Creates a new list based on the given sequence. Each element in the new list is the result of the given expression.

. Example: my_list = [ x*2 for x in range(1,11) ]

. [expression for variable in sequence if condition] - Creates a new list based on a specified sequence. Each element is the result of the given  expression; elements are added only if the specified condition is true. 

    .Example: my_list = [ x for x in range(1,101) if x % 10 == 0 ]


Coding skills
Skill Group 1
. Use a for loop to modify elements of a list.

. Use the list.append(old,new) method.

. Use the string.endswith() and string.replace() methods to modify the elements within a list.

# This block of code changes the year on a list of dates.
# The "years" list is given with existing elements. 
years = ["January 2023", "May 2025", "April 2023", "August 2024", "September 2025", "December 2023"]


# The variable "updated_years" is initialized as a list data type 
# using empty square brackets []. This list will hold the new list
# with the updated years. 
updated_years = []

# The for loop checks each "year" element in the list "years".
for year in years:

    # The if-statement checks if the "year" element ends with the 
    # substring "2023". 
    if year.endswith("2023"):

        # If True, then a temporary variable "new" will hold the 
        # modified "year" element where the "2023" substring is 
        # replaced with the substring "2024".
        new = year.replace("2023","2024")

        # Then, the list "updated_years" is appended with the changed
        # element held in the temporary variable "new".
        updated_years.append(new)
        
    # If False, the original "year" element will be appended to the 
    # the "updated_years" list unchanged.
    else:
        updated_years.append(year)


print(updated_years) 
# Should print ["January 2024", "May 2025", "April 2024", "August 2024", "September 2025", "December 2024"]

Skill Group 2
. Use a list comprehension to return values

# This list comprehension creates a list of squared numbers (n*n). It
# accepts two integer variables through the function’s parameters.
def squares(start, end):
    
# The list comprehension calculates the square of a variable integer 
# "n", where "n" ranges from the "start" to "end" variables inclusively.
# To be inclusive in a range(), add +1 to the end of range variable.
    return [n*n for n in range(start,end+1)] 


print(squares(2, 3))  # Should print [4, 9]
print(squares(1, 5))  # Should print [1, 4, 9, 16, 25]
print(squares(0, 10)) # Should print [0, 1, 4, 9, 16, 25, 36, 49, 64, 81, 100]

Skill Group 3
. Use the string[index] method within a list comprehension.  

. Use a list comprehension to modify elements of a list.

. Use the string.replace() method within a list comprehension.

# This block of code also changes the year on a list of dates using a
# different approach than demonstrated in Skill Group 1. By using a 
# list comprehension, you can see how it is possible to refactor the
# code to a shorter, more efficient code block. 

# The "years" list is given with existing elements.
years = ["January 2023", "May 2025", "April 2023", "August 2024", "September 2025", "December 2023"]

# The list comprehension below creates a new list "updated_years" to
# hold the command to replace the "2023" substring of the "year"
# element with the substring "2024". This action will be executed if
# the last 4 indices of the "year" string is equal to the substring
# "2023". If false (else), the "year" element will be included in the
# new list "updated_years" unchanged.
updated_years = [year.replace("2023","2024") if year[-4:] == "2023" else year for year in years]


print(updated_years) 
# Should print ["January 2024", "May 2025", "April 2024", "August 2024", "September 2025", "December 2024"]

Skill Group 4
. Use the string.split() method to separate a string into a list of individual words.

. Iterate over the new list using a for loop.

. Modify each element in the list by slicing the element’s string at a given [1:] index position and appending the substring to the end of the element.

. Convert a list back into a string.

# This function splits a given string into a list of elements. Then, it
# modifies each element by moving the first character to the end of the 
# element and adds a dash between the element and the moved character. 
# For example, the element "2two" will be changed to "two-2". Finally,
# the function converts the list back to a string, and returns the
# new string.
def change_string(given_string):

# Initialize "new_string" as a string data type by using empty quotes.
    new_string = ""
    # Split the "given_string" into a "new_list", with each "element"
    # holding an individual word from the string.
    new_list = given_string.split()

    # The for loop iterates over each "element" in the "new_list".
    for element in new_list:

        # Convert the list into a "new_string" by using the assignment
        # operator += to concatenate the following items: 
        # + Each list "element" (starting at index position [1:]), 
        # + a dash "-", 
        # + append the first character of the "element" (using the index 
        # [0]) to the end of the "element", and finally,
        # + a space " " to separate each "element" in the "new_string".
        new_string += element[1:] + "-"  + element[0] + " "

    # Return the list that has been converted back into a string.
    return new_string


print(change_string("1one 2two 3three 4four 5five")) 
# Should print "one-1 two-2 three-3 four-4 five-5"  

 Skill Group 5  
 . Use the string.join() method to concatenate a string that provides a list name and its elements

# This function accepts a list name and a list of elements, and returns
# a string with the format: "The "list_name" list includes: element1, 
# element2, element3". 
def list_elements(list_name, elements):

    # This task can be completed in a single line of code. The 
    # concatenation of strings, "list_name", and the list "elements" can
    # occur on the return line. In this case, the string "The " is added 
    # to the "list_name", plus the string " list includes: ", then the
    # "elements" are joined using a comma to separate each element of the 
    # list.
    return "The " + list_name + " list includes: " + ", ".join(elements)


print(list_elements("Printers", ["Color Printer", "Black and White Printer", "3-D Printer"])) 
# Should print "The Printers list includes: Color Printer, Black and White Printer, 3-D Printer"

Resources
For additional information about list and tuple operations and methods, please visit:

Common Sequence Operations - Official python.org documentation for list, tuple, and range sequence operations. https://docs.python.org/3/library/stdtypes.html#sequence-types-list-tuple-range

Lists - Official python.org documentation for list operations and methods. https://docs.python.org/3/library/stdtypes.html#lists

Tuples - Official python.org documentation for tuple operations and methods https://docs.python.org/3/library/stdtypes.html#tuples 


Practice Quiz:

Q:
Given a list of filenames, we want to rename all the files with extension hpp to the extension h. To do this, we would like to generate a new list called newfilenames, consisting of the new filenames. Fill in the blanks in the code using any of the methods you’ve learned thus far, like a for loop or a list comprehension.

filenames = ["program.c", "stdio.hpp", "sample.hpp", "a.out", "math.hpp", "hpp.out"]
# Generate newfilenames as a list containing the new filenames
# using as many lines of code as your chosen method requires.
___  

print(newfilenames) 
# Should be ["program.c", "stdio.h", "sample.h", "a.out", "math.h", "hpp.out"]

Q:
Let's create a function that turns text into pig latin: a simple text transformation that modifies each word moving the first character to the end and appending "ay" to the end. For example, python ends up as ythonpay.

def pig_latin(text):
  say = ""
  # Separate the text into words
  words = ___
  for word in words:
    # Create the pig latin word and add it to the list
    ___
    # Turn the list back into a phrase
  return ___
		
print(pig_latin("hello how are you")) # Should be "ellohay owhay reaay ouyay"
print(pig_latin("programming in python is fun")) # Should be "rogrammingpay niay ythonpay siay unfay"

Q:
The permissions of a file in a Linux system are split into three sets of three permissions: read, write, and execute for the owner, group, and others. Each of the three values can be expressed as an octal number summing each permission, with 4 corresponding to read, 2 to write, and 1 to execute. Or it can be written with a string using the letters r, w, and x or - when the permission is not granted.
 For example: 
 640 is read/write for the owner, read for the group, and no permissions for the others; converted to a string, it would be: "rw-r-----"
 755 is read/write/execute for the owner, and read/execute for group and others; converted to a string, it would be: "rwxr-xr-x"
 Fill in the blanks to make the code convert a permission in octal format into a string format.
 
def octal_to_string(octal):
    result = ""
    value_letters = [(4,"r"),(2,"w"),(1,"x")]
    # Iterate over each of the digits in octal
    for ___ in [int(n) for n in str(octal)]:
        # Check for each of the permissions values
        for value, letter in value_letters:
            if ___ >= value:
                result += ___
                ___ -= value
            else:
                ___
    return result
    
print(octal_to_string(755)) # Should be rwxr-xr-x
print(octal_to_string(644)) # Should be rw-r--r--
print(octal_to_string(750)) # Should be rwxr-x---
print(octal_to_string(600)) # Should be rw-------

Q:
The group_list function accepts a group name and a list of members, and returns a string with the format: group_name: member1, member2, … For example, group_list("g", ["a","b","c"]) returns "g: a, b, c". Fill in the gaps in this function to do that.

def group_list(group, users):
  members = ___
  return ___

print(group_list("Marketing", ["Mike", "Karen", "Jake", "Tasha"])) # Should be "Marketing: Mike, Karen, Jake, Tasha"
print(group_list("Engineering", ["Kim", "Jay", "Tom"])) # Should be "Engineering: Kim, Jay, Tom"
print(group_list("Users", "")) # Should be "Users:"

Q:
The guest_list function reads in a list of tuples with the name, age, and profession of each party guest, and prints the sentence "Guest is X years old and works as __." for each one. For example, guest_list(('Ken', 30, "Chef"), ("Pat", 35, 'Lawyer'), ('Amanda', 25, "Engineer")) should print out: Ken is 30 years old and works as Chef. Pat is 35 years old and works as Lawyer. Amanda is 25 years old and works as Engineer. Fill in the gaps in this function to do that.

def guest_list(guests):
	for ___:
		___
		print(___.format(___))

guest_list([('Ken', 30, "Chef"), ("Pat", 35, 'Lawyer'), ('Amanda', 25, "Engineer")])

#Click Run to submit code
"""
Output should match:
Ken is 30 years old and works as Chef
Pat is 35 years old and works as Lawyer
Amanda is 25 years old and works as Engineer
"""
---
# Dictionaries:

* Dictionary:
Dictionaries are another data structure in Python. They’re similar to a list in that they can be used to organize data into collections. However, data in a dictionary isn't accessed based on its position. Data in a dictionary is organized into pairs of keys and values. You use the key to access the corresponding value. Where a list index is always a number, a dictionary key can be a different data type, like a string, integer, float, or even tuples.
When creating a dictionary, you use curly brackets: {}. When storing values in a dictionary, the key is specified first, followed by the corresponding value, separated by a colon. For example, animals = { "bears":10, "lions":1, "tigers":2 } creates a dictionary with three key value pairs, stored in the variable animals. The key "bears" points to the integer value 10, while the key "lions" points to the integer value 1, and "tigers" points to the integer 2. You can access the values by referencing the key, like this: animals["bears"]. This would return the integer 10, since that’s the corresponding value for this key.
You can also check if a key is contained in a dictionary using the in keyword. Just like other uses of this keyword, it will return True if the key is found in the dictionary; otherwise it will return False.
Dictionaries are mutable, meaning they can be modified by adding, removing, and replacing elements in a dictionary, similar to lists. You can add a new key value pair to a dictionary by assigning a value to the key, like this: animals["zebras"] = 2. This creates the new key in the animal dictionary called zebras, and stores the value 2. You can modify the value of an existing key by doing the same thing. So animals["bears"] = 11 would change the value stored in the bears key from 10 to 11. Lastly, you can remove elements from a dictionary by using the del keyword. By doing del animals["lions"] you would remove the key value pair from the animals dictionary.
EX:
x = {"mirza":2, "saad":4}
print(type(x))			# here we are defining a dictionary
x = {"mirza":2, "saad":4}
print("mirza" in x)		# we are checking whether mirza is present inside x, true or false
x = {"mirza":2, "saad":4}
print(x["mirza"])		# this returns the value assisnted to the key x.
* Deleting a dictionary: we can delete elements from a dictionary with the del keyword by passing the dictionary and the key to the element as if we were trying to access it.
x = {"mirza":2, "saad":4}
del x ["saad"]			# del function deletes the file inside the dictionary
print(x)
*Iterating over the Contents of a Dictionary:
x = {"jpg":2, "txt":4, "csv":23,"py":21}
for extension in x:			# So if you use a dictionary in a for loop, the iteration variable will go through the keys in the dictionary.
    print(extension)
---
 If you want to access the associated values, you can either use the keys as indexes of the dictionary or you can use the items method which returns a tuple for each element in the dictionary. The tuple's first element is the key. Its second element is the value. Let's try that with our example dictionary.
 
 
x = {"jpg":2, "txt":4, "csv":23,"py":21}
for ext, amount in x.items():		# 
    print("There are {} files with the .{} extension".format(amount,ext))
OT:
There are 2 files with the .jpg extension
There are 4 files with the .txt extension
There are 23 files with the .csv extension
There are 21 files with the .py extension
 For ext amount in file_counts.items(): print("there are and then {} files with the .{} extension".format(amount, ext)). Sometimes you might just be interested in the keys of a dictionary. Other times you might just want the values.
 
---
Sometimes you might just be interested in the keys of a dictionary. Other times you might just want the values. You can access both with their corresponding dictionary methods like this. file_counts.keys() file counts.values(). These methods return special data types related to the dictionary, but you don't need to worry about what they are exactly. You just need to iterate them as you would with any sequence. For value in file_counts.values(): print value. So we can use items to get key value pairs, keys to get the keys, and values to get just the values.like this
EX:
x = {"jpg":2, "txt":4, "csv":23,"py":21}
print(x.keys())				# just prints the value of key x
---
x = {"jpg":2, "txt":4, "csv":23,"py":21}
print(x.values())			# just prints the value of key x
---
x = {"jpg":2, "txt":4, "csv":23,"py":21}
for value in x.values():		# this prints the values of x
    print(value)
---
Practice
Complete the code to iterate through the keys and values of the cool_beasts dictionary. Remember that the items method returns a tuple of key, value for each element in the dictionary.
cool_beasts = {"octopuses":"tentacles", "dolphins":"fins", "rhinos":"horns"}
for ___ in cool_beasts.items():
    print("{} have {}".format(___))

---
Let's check out a simple example of counting how many times each letter appears in a piece of text.

def count_letters(text):
    result = {}
    for letter in text:
        if letter not in result:
            result[letter] = 0
        result[letter] += 1
    return result
print(count_letters("why are people lazy ?"))

In this code, we're first initializing an empty dictionary, then going through each letter in the given string. For each letter, we check if it's not already in the dictionary. And in that case, we initialize an entry in the dictionary with a value of zero. Finally, we increment the count for that letter in the dictionary. To sum up, we've created a dictionary where the keys are each of the letters present in the string and the values are how many times each letter is present.Here you can see how the dictionary can have any number of entries and the pairs of key values always count how many of each letter there are in the string. Also, do you see how our simple code doesn't distinguish between actual letters and special characters like a space? To only count the letters, we'd need to specify which characters we're taking into account. This technique might seem simple at first, but it can be really useful in a lot of cases. Let's say for example that you're analyzing logs in your server and you want to count how many times each type of error appears in the log file. You could easily do this with a dictionary by using the type of error as the key and then incrementing the associated value each time you come across that error type.

---
* EXTRA NOTES:You can iterate over dictionaries using a for loop, just like with strings, lists, and tuples. This will iterate over the sequence of keys in the dictionary. If you want to access the corresponding values associated with the keys, you could use the keys as indexes. Or you can use the items method on the dictionary, like dictionary.items(). This method returns a tuple for each element in the dictionary, where the first element in the tuple is the key and the second is the value.

If you only wanted to access the keys in a dictionary, you could use the keys() method on the dictionary: dictionary.keys(). If you only wanted the values, you could use the values() method: dictionary.values().

* Dictionaries vs. Lists:Dictionaries and lists are both really useful and each have strengths in different situations. So when is it best to use a list and when is the dictionary the way to go? Think about the kind of information you can represent in each data structure. If you've got a list of information you'd like to collect and use in your script then the list is probably the right approach. For example, if you want to store a series of IP addresses to ping, you could put them all into a list and iterate over them. Or if you had a list of host names and their corresponding IP addresses, you might want to pair them as key values in a dictionary. Because of the way dictionaries work, it's super easy and fast to search for an element in them. Let's say you have a dictionary that has usernames as keys, and the groups they belong to as values. It doesn't matter if you have 10 users or 10,000 users, accessing the entry for a given user will take the same time. 

 EX:
ip_address = ["192.25.23", "192.23.45","8.8.8.8"]
host_address = {"router": "192.25.23", "localhost": "192.23.45", "google":"8.8.8.8"}

 Amazing, but this isn't true for lists. If you've got a list of 10 elements, and you need to check if one element is in the list, it'll be a very fast check but if your list has 10,000 elements it'll take significantly longer to check if the element you're looking for is there. So in general, you want to use dictionaries when you plan on searching for a specific element. Another interesting difference is the types of values that we can store in lists and dictionaries. In lists, you can store any data type. In dictionaries, we can store any data type for the values but the keys are restricted to specific types. The reasoning behind which types are allowed can get complex and we don't want to bog you down with unnecessary details. So as a rule of thumb, you can use any immutable data type; numbers, booleans, strings and tuples as dictionary keys. But you can't use lists or dictionaries for that. On the flip side, like we said, the values associated with keys can be any type, including lists or even other dictionaries. You can use them to represent more complex data structures like directory trees in the file system. There's a ton of different key value pairs that we need to work with in system administration. So I use dictionaries all the time. They're especially useful with large data sets. When I need to write a script that gets specific keys out of it to manipulate or modify the associated value. But it doesn't always need to be that serious. One-time, just for fun, I wanted to be able to look up which Disney villain is associated with each protagonist. So I created a dictionary that stores a key like Snow White, with the value, evil queen. Pretty good. Mirror, mirror on my screen who's the best coder you've ever seen? There are even more data types available that we haven't checked out yet. One of these data types is a set which is a bit like a cross between a list and a dictionary. A set is used when you want to store a bunch of elements and be certain that there are only present once. Elements of a set must also be immutable. You can think of this as the keys of a dictionary with no associated values or you could see it as a list where what matters isn't the order of the elements but whether an element is in the list or not.


* EXTRA NOTES
Study Guide: Dictionary Methods
This study guide provides a quick-reference summary of what you learned in this lesson and serves as a guide for the upcoming practice quiz. 

In the Dictionary segment, you learned about the properties of the Python dictionary data type, how dictionaries differ from lists, how to iterate over the contents of a dictionary, and how to use dictionaries with lists and strings.


Knowledge
Python dictionaries are used to organize elements into collections. Dictionaries include one or more keys, with one or more values associated with each key. 

Syntax

my_dictionary = {keyA:value1,value2, keyB:value3,value4}

Operations
* len(dictionary) - Returns the number of items in a dictionary.

* for key in dictionary - Iterates over each key in a dictionary.

* for key, value in dictionary.items() - Iterates over each key,value pair in a dictionary.

* if key in dictionary - Checks whether a key is in a dictionary.

* dictionary[key] - Accesses a value using the associated key from a dictionary.

* dictionary[key] = value - Sets a value associated with a key.

* del dictionary[key] - Removes a value using the associated key from a dictionary.


Methods
* dictionary.get(key, default) - Returns the value corresponding to a key, or the default value if the specified key is not present.

* dictionary.keys() - Returns a sequence containing the keys in a dictionary.

* dictionary.values() - Returns a sequence containing the values in a dictionary.

* dictionary[key].append(value) - Appends a new value for an existing key.

* dictionary.update(other_dictionary) - Updates a dictionary with the items from another dictionary. Existing entries are replaced; new entries are added.

* dictionary.clear() - Deletes all items from a dictionary.

* dictionary.copy() - Makes a copy of a dictionary.


Dictionaries versus Lists 
* Dictionaries are similar to lists, but there are a few differences:

Both dictionaries and lists:
* are used to organize elements into collections;

* are used to initialize a new dictionary or list, use empty brackets;

* can iterate through the items or elements in the collection; and

* can use a variety of methods and operations to create and change the collections, like removing and inserting items or elements.

Dictionaries only:
* are unordered sets;

* have keys that can be a variety of data types, including strings, integers, floats, tuples;.

* can access dictionary values by keys;

* use square brackets inside curly brackets { [ ] };

* use colons between the key and the value(s);

* use commas to separate each key group and each value within a key group;

* make it quicker and easier for a Python interpreter to find specific elements, as compared to a list.

Dictionary Example:

pet_dictionary = {"dogs": ["Yorkie", "Collie", "Bulldog"], "cats": ["Persian", "Scottish Fold", "Siberian"], "rabbits": ["Angora", "Holland Lop", "Harlequin"]}  


print(pet_dictionary.get("dogs", 0))
# Should print ['Yorkie', 'Collie', 'Bulldog']

---
Lists only:
* are ordered sets;

* access list elements by index positions;

* require that these indices be integers;

* use square brackets [ ];

* use commas to separate each list element.

List Example:

pet_list  = ["Yorkie", "Collie", "Bulldog", "Persian", "Scottish Fold", "Siberian", "Angora", "Holland Lop", "Harlequin"]


print(pet_list[0:3])
# Should print ['Yorkie', 'Collie', 'Bulldog']

---
* Coding skills  
Skill Group 1  
* Iterate over the key and value pairs of a dictionary using a for loop with the dictionary.items() method to calculate the sum of the values in a dictionary. 

# This function returns the total time, with minutes represented as 
# decimals (example: 1 hour 30 minutes = 1.5), for all end user time
# spent accessing a server in a given day. 


def sum_server_use_time(Server):

    # Initialize the variable as a float data type, which will be used
    # to hold the sum of the total hours and minutes of server usage by
    # end users in a day.
    total_use_time = 0.0

    # Iterate through the "Server" dictionary’s key and value items 
    # using a for loop.
    for key,value in Server.items():

        # For each end user key, add the associated time value to the
        # total sum of all end user use time.
        total_use_time += Server[key]

    # Round the return value and limit to 2 decimal places.
    return round(total_use_time, 2)  

FileServer = {"EndUser1": 2.25, "EndUser2": 4.5, "EndUser3": 1, "EndUser4": 3.75, "EndUser5": 0.6, "EndUser6": 8}

print(sum_server_use_time(FileServer)) # Should print 20.1


Skill Group 2  
* Concatenate a value, a string, and the key for each item in the dictionary and append to the end of a new list[ ] using the list.append(x) method.  

* Iterate over keys with multiple values from a dictionary using nested for loops with the dictionary.items() method.

# This function receives a dictionary, which contains common employee 
# last names as keys, and a list of employee first names as values. 
# The function generates a new list that contains each employees’ full
# name (First_name Last_Name). For example, the key "Garcia" with the 
# values ["Maria", "Hugo", "Lucia"] should be converted to a list 
# that contains ["Maria Garcia", "Hugo Garcia", "Lucia Garcia"].


def list_full_names(employee_dictionary):
    # Initialize the "full_names" variable as a list data type using
    # empty [] square brackets.  
    full_names = []

    # The outer for loop iterates through each "last_name" key and 
    # associated "first_name" values, in the "employee_dictionary" items.
    for last_name, first_names in employee_dictionary.items():

        # The inner for loop iterates over each "first_name" value in 
        # the list of "first_names" for one "last_name" key at a time.
        for first_name in first_names:

            # Append the new "full_names" list with the "first_name" value
            # concatenated with a space " ", and the key "last_name". 
            full_names.append(first_name+" "+last_name)

    # Return the new "full_names" list once the outer for loop has 
    # completed all iterations. 
    return(full_names)


print(list_full_names({"Ali": ["Muhammad", "Amir", "Malik"], "Devi": ["Ram", "Amaira"], "Chen": ["Feng", "Li"]}))
# Should print ['Muhammad Ali', 'Amir Ali', 'Malik Ali', 'Ram Devi', 'Amaira Devi', 'Feng Chen', 'Li Chen']


Skill Group 3  

* Use the dictionary[key] = value operation to associate a value with a key in a dictionary.   

* Iterate over keys with multiple values from a dictionary, using nested for loops and an if-statement, and the dictionary.items() method.

* Use the dictionary[key].append(value) method to add the key, a string, and the key for each item in the dictionary.

# This function receives a dictionary, which contains resource 
# categories (keys) with a list of available resources (values) for a 
# company’s IT Department. The resources belong to multiple categories.
# The function should reverse the keys and values to show which 
# categories (values) each resource (key) belongs to. 


def invert_resource_dict(resource_dictionary):
  # Initialize a "new_dictionary" variable as a dict data type using
  # empty {} curly brackets. 
    new_dictionary = {}
    # The outer for loop iterates through each "resource_group" and 
    # associated "resources" in the "resource_dictionary" items.
    for resource_group, resources in resource_dictionary.items():
        # The inner for loop iterates over each "resource" value in 
        # the list of "resources" for one "resource_group" key at a time.
        for resource in resources:
            # The if-statement checks if the current "resource" value has 
            # been appended as a key to the "new_dictionary" yet.
            if resource in new_dictionary:
                # If True, then append the "resource_group" as a value to the
                # "resource", which is now the key.
                new_dictionary[resource].append(resource_group)
            # If False (else), then add the "resource" as a new key with the 
            # "resource_group" as a value for that key.
            else:
                new_dictionary[resource] = [resource_group]
    # Return the new dictionary once the outer for loop has completed  
    # all iterations.
    return(new_dictionary)


print(invert_resource_dict({"Hard Drives": ["IDE HDDs", "SCSI HDDs"],
        "PC Parts":  ["IDE HDDs", "SCSI HDDs", "High-end video cards", "Basic video cards"], "Video Cards": ["High-end video cards", "Basic video cards"]}))
# Should print {'IDE HDDs': ['Hard Drives', 'PC Parts'], 'SCSI HDDs': ['Hard Drives', 'PC Parts'], 'High-end video cards': ['PC Parts', 'Video Cards'], 'Basic video cards': ['PC Parts', 'Video Cards']}
---
Practice Quiz

1.
Question 1
The email_list function receives a dictionary, which contains domain names as keys, and a list of users as values. Fill in the blanks to generate a list that contains complete email addresses (e.g. diana.prince@gmail.com).

def email_list(domains):
	emails = []
	for ___:
	  for user in users:
	    emails.___
	return(emails)

print(email_list({"gmail.com": ["clark.kent", "diana.prince", "peter.parker"], "yahoo.com": ["barbara.gordon", "jean.grey"], "hotmail.com": ["bruce.wayne"]}))

2.
Question 2
The groups_per_user function receives a dictionary, which contains group names with the list of users. Users can belong to multiple groups. Fill in the blanks to return a dictionary with the users as keys and a list of their groups as values.

def groups_per_user(group_dictionary):
	user_groups = {}
	# Go through group_dictionary
	for ___:
		# Now go through the users in the group
		for ___:
			# Now add the group to the the list of
# groups for this user, creating the entry
# in the dictionary if necessary
	return(user_groups)
print(groups_per_user({"local": ["admin", "userA"],
		"public":  ["admin", "userB"],
		"administrator": ["admin"] }))
		
3.
Question 3
The dict.update method updates one dictionary with the items coming from the other dictionary, so that existing entries are replaced and new entries are added. What is the content of the dictionary “wardrobe“ at the end of the following code?
wardrobe = {'shirt': ['red', 'blue', 'white'], 'jeans': ['blue', 'black']}
new_items = {'jeans': ['white'], 'scarf': ['yellow'], 'socks': ['black', 'brown']}
wardrobe.update(new_items)
4.
Question 4
 What’s a major advantage of using dictionaries over lists?
* Dictionaries are ordered sets
* Dictionaries can be accessed by the index number of the element
* Elements can be removed and inserted into dictionaries
* It’s quicker and easier to find a specific element in a dictionary
5.
Question 5
The add_prices function returns the total price of all of the groceries in the  dictionary. Fill in the blanks to complete this function.
def add_prices(basket):
	# Initialize the variable that will be used for the calculation
	total = 0
	# Iterate through the dictionary items
	for ___:
		# Add each price to the total calculation
		# Hint: how do you access the values of
		# dictionary items?
		total += ___
	# Limit the return value to 2 decimal places
	return round(total, 2)  
groceries = {"bananas": 1.56, "apples": 2.50, "oranges": 0.99, "bread": 4.59, 
	"coffee": 6.99, "milk": 3.39, "eggs": 2.98, "cheese": 5.44}
print(add_prices(groceries)) # Should print 28.44


Study Guide: Week 4 Graded Quiz
 It is time to prepare for the Week 4 Graded Quiz. Please review the following items from this module before beginning the quiz. If you would like to refresh your memory on these materials, please also revisit the Study Guides located before each practice quiz in Week 4: Study Guide: Strings,  Study Guide: Lists Operations and Methods, and Study Guide: Dictionary Methods.

Knowledge

. How to output a list of the keys in a Python dictionary. 

. How to determine the output of a string index range used on a string.

. Determine what a list should contain after the .insert() method is used on the list.

. How to replace a specific word in a sentence with the same word in all uppercase letters.

. How to use a dictionary to count the frequency of letters in a string. 


Operations, Methods, and Functions

. String Methods, Operations, and Functions

    .upper()

    .lower()

    .split()

    .format()

    .isnumeric()

    .isalpha()

    .replace()

    . string index [ ]

    . len()


List Operations and Methods

    .reverse()

    .extend()

    .insert()

    .append()

    .remove()

    .sort()

    .list comprehensions [ ]

    .list comprehensions [ ] with if condition

Dictionary Operations and Methods

    .items()

    .update()

    .keys()

    .values()

    .copy()

    .dictionary[key]

    .dictionary[key] = value 



Coding Skills:

Skill 1: Using string methods

. Separate numerical values from text values in a string using .split(). 

. Iterate over the elements in a string.

. Test if the element contains letters with .isalpha().

. Assign the elements of the split string to new variables.

. Trim any extra white space using .strip().

. Format a string using .format() and { } variable placeholders.


def sales_prices(item_and_price):
    # Initialize variables "item" and "price" as strings
    item = ""
    price = ""
    # Create a variable "item_or_price" to hold the result of the split. 
    item_or_price = item_and_price.split()

    # For each element "x" in the split variable "item_or_price" 
    for x in item_or_price:

        # Check if the element is a number
        if x.isalpha():

            # If true, assign the element to the "item" string variable and add a space 
            # for any item names containing multiple words, like "Winter fleece jacket".
            item += x + " "

        # Else, if x is a number (if x.isalpha() is false): 
        else:
            # Assign the element to the "price" string variable. 
            price = x

    # Strip the extra space to the right of the last "item" word
    item = item.strip()

    # Return the item name and price formatted in a sentence 
    return "{} are on sale for ${}".format(item,price)


# Call to the function 
print(sales_prices("Winter fleece jackets 49.99"))
# Should print "Winter fleece jackets are on sale for $49.99"
---

. Use the len() function to measure a string.

# This function accepts a string variable "data_field".  
def count_words(data_field):

    # Splits the string into individual words. 
    split_data = data_field.split()
  
    # Then returns the number of words in the string using the len()
    # function. 
    return len(split_data)
    
    # Note that it is possible to combine the len() function and the 
    # .split() method into the same line of code by inserting the 
    # data_field.split() command into the the len() function parameters.

# Call to the function
count_words("Catalog item 3523: Organic raw pumpkin seeds in shell")
# Should print 9

---


Skill 2: Using list methods:

. Reverse the order of a list using the .reverse() method.

. Combine two lists using the .extend() method.


# This function accepts two variables, each containing a list of years.
# A current "recent_first" list contains [2022, 2018, 2011, 2006].
# An older "recent_last" list contains [1989, 1992, 1997, 2001].
# The lists need to be combined with the years in chronological order.
def record_profit_years(recent_first, recent_last):

    # Reverse the order of the "recent_first" list so that it is in 
    # chronological order.
    recent_first.reverse()

    # Extend the "recent_last" list by appending the newly reversed 
    # "recent_first" list.
    recent_last.extend(recent_first)

    # Return the "recent_last", which now contains the two lists 
    # combined in chronological order. 
    return recent_last

# Assign the two lists to the two variables to be passed to the 
# record_profit_years() function.
recent_first = [2022, 2018, 2011, 2006]
recent_last = [1989, 1992, 1997, 2001]



# Call the record_profit_years() function and pass the two lists as 
# parameters. 
print(record_profit_years(recent_first, recent_last))
# Should print [1989, 1992, 1997, 2001, 2006, 2011, 2018, 2022]


Skill 3: Using a list comprehension:

. Use a list comprehension [ ] as a shortcut for creating a new list from a range.

. Include a calculation with a for loop in a range with 2 parameters (lower, upper+1). 

# The function accepts two parameters: a start year and an end year.
def list_years(start, end):

    # It returns a list comprehension that creates a list of years in a for
    # loop using a range from the start year to the end year (inclusive of 
    # the upper range year, using end+1).
    return [year for year in range(start, end+1)]


# Call the years() function with two parameters.
print(list_years(1972, 1975)) 
# Should print [1972, 1973, 1974, 1975]
---

.  Use a list comprehension [ ] with a for loop and an if condition.   

# The function accepts two variable integers through the parameters and
# returns all odd numbers between x and y-1.
def odd_numbers(x, y):


# This list comprehension uses a for loop to iterate through values 
# of n in a range from x to y, with the value of y excluded (meaning
# keep the default range() function behavior to exclude the
# end-of-range value from the range). Since an incremental value is not 
# specified, the range function uses the default increment of +1.
# The if condition checks n to test if the number is odd using the
# modulo operator. This condition is written to check if n is divided 
# by 2, that the remainder is not 0. 
    return [n for n in range(x, y) if n % 2 != 0]


# Call the years() function with two parameters.
print(odd_numbers(5, 15)) 
# Should print [5, 7, 9, 11, 13]
---

Skill 4: Using dictionary methods:

. Iterate through the keys and values of a dictionary.

. Return the keys and values in a formatted string using the .format() function.


# The network() function accepts a dictionary "servers" as a parameter.
def network(servers):

    # A string variable is initialized to hold the "result". 
    result = ""

    # For each "hostname" (key) and "IP address" (value) in the "server" dictionary items...
    for hostname, IP_address in servers.items():

        # A string identifying the hostname and IP address for each server is added
        # to the "result" variable. The string .format() function and is used to plug
        # the hostname and IP_address variables into the designated {} placeholders
        # within the string.
        result += "The IP address of the {} server is {}".format(hostname, IP_address) + "\n"
    
    # Return the "result" variable string.
    return result 

# Call the "network" function with the dictionary. 
print(network({"Domain Name Server":"8.8.8.8", "Gateway Server":"192.168.1.1", "Print Server":"192.168.1.33", "Mail Server":"192.168.1.190"}))

# Should print:
# The IP address of the Domain Name Server server is 8.8.8.8
# The IP address of the Gateway Server server is 192.168.1.1
# The IP address of the Print Server server is 192.168.1.33
# The IP address of the Mail Server server is 192.168.1.190

. Create a copy of a dictionary.

. Iterate through the values of the new dictionary.

. Change each value in the new dictionary, while keeping the same keys. 

# The scores() function accepts a dictionary "game_scores" as a parameter.
def reset_scores(game_scores):

    # The .copy() dictionary method is used to create a new copy of the "game_scores".
    new_game_scores = game_scores.copy() 

    # The for loop iterates over new_game_scores items, with the player as the key
    # and the score as the value. 
    for player, score in new_game_scores.items():
    
        # The dictionary operation to assign a new value to a key is used
        # to reset the grade values to 0.
        new_game_scores[player] = 0
  
    return new_game_scores
 
# The dictionary is defined.
game1_scores = {"Arshi": 3, "Catalina": 7, "Diego": 6}
 
# Call the "reset_scores" function with the "game1_scores" dictionary. 
print(reset_scores(game1_scores))
# Should print {'Arshi': 0, 'Catalina': 0, 'Diego': 0}
---

Reminder: Correct syntax is critical
Using precise syntax is critical when writing code in any programming language, including Python. Even a small typo can cause a syntax error and the automated Python-coded quiz grader will mark your code as incorrect. This reflects real life coding errors in the sense that a single error in spelling, case, punctuation, etc. can cause your code to fail. Coding problems caused by imprecise syntax will always be an issue whether you are learning a programming language or you are using programming skills on the job. So, it is critical to start the habit of being precise in your code now. 

No credit will be given if there are any coding errors on the automated graded quizzes - including minor errors. Fortunately, you have 3 optional retake opportunities on the graded quizzes in this course. Additionally, you have unlimited retakes on practice quizzes and can review the videos and readings as many times as you need to master the concepts in this course.  

Now, before starting the graded quiz, please review this list of common syntax errors coders make when writing code.

Common syntax errors:

. Misspellings

. Incorrect indentations

. Missing or incorrect key characters:

        . Parenthetical types - ( curved ), [ square ], { curly }

        . Quote types - "straight-double" or 'straight-single', “curly-double” or ‘curly-single’

        . Block introduction characters, like colons - :

. Data type mismatches

. Missing, incorrectly used, or misplaced Python reserved words

. Using the wrong case (uppercase/lowercase) - Python is a case-sensitive language 

---
