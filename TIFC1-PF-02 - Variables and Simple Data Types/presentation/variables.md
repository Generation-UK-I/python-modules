# Variables, Strings, and Simple Data Types
---

## Learning Objectives

- Explain what a variable is and why they’re used
- Be able to identify a number of variable types
- Select the appropriate variable type for a given scenario
- Store and recall data using a variable
  
---

## I have a cat named Noche

<img src="img/shocked_noche.jpg" width="300" />

Noche will be one of our main characters when learning Python. Much of the coding examples in this module will cover Noche's favorite time of day: dinner time. 

---

## Take a Look...

What would happen if I ran the following piece of code? 

```py
name = "noche"

print("My cat, " + name.title() + ", is a very picky eater.")
print("Today, all I have for dinner is tuna with seaweed.")
```

As we go through through this unit, we will break down this piece of code and what each of its components are. 

---

## Variables

Variables are just containers that hold a value that you can use later on in your program. You will frequently use variables in programming to store many different things! 

Let's take a look at some examples of variables... 

## A Simple Variable

```py
cat = "Noche"

print(cat)
```

Take a look at the code above. Here we have a very simple example of how to use a variable. 

Recall, that a variable is a container that can hold a value that we can use later on in our program. In this example, 'cat' is our variable and the value it holds is 'Noche'. On the final line of code, we use the print() statement with our variable wrapped inside. We are telling python that we want to print the value of our variable. 

STOP AND RUN: Try running this code to see how it works! Change the value and name of the variable to see what happens! 

Now, let's refer back to our code from the start of this presentation: 

```py
name = "noche"

print("My cat, " + name.title() + ", is a very picky eater.")
print("Today, all I have for dinner is tuna with seaweed.")
```

Can you identify the variable and value in this piece of code?

The first variable is 'name' on the first line, and its value is 'noche'. The variable in this piece of code is being used in a print() statement, except now it is being used in something called a string. We will take a look at strings in a moment. First, we need to look at the rules when using variables...

## Naming Rules for Variables and Errors

There are some rules when naming variables to look out for. If these rules are broken, then you might encounter some errors! Here are a few common errors you might come across: 

- A traceback is a record of where the interpreter ran into trouble when trying to execute your code. 
- TypeError: When you try and do an operation on a data type that is not the correct operation for that data type.
- Syntax Error: Something has gone wrong with your Python Syntax! 

Below are the rules to keep in mind when naming your variables and what errors occur when you break them:

- Variable names can contain only letters, numbers, and underscores. They can start with a letter or an underscore, but not with a number.

```py
1Noche = "cat"
print(1Noche)
```

- Spaces are not allowed in variable names, but underscores can be used to separate words in variable names.

```py
Super Noche = "cat"
print(Super Noche)
```

- Avoid using Python keywords and function names as variable names; that is, do not use words that Python has reserved for a particular programmatic purpose, such as the word print.

```py
print = "cat"
print(print)
```

- Variable names should be short but descriptive.

```py
my_cat_noche_is_the_best_cat_in_the_whole_world = "cat"
print(my_cat_noche_is_the_best_cat_in_the_whole_world)
```

- Be careful when using the lowercase letter l and the uppercase letter O because they could be confused with the numbers 1 and 0

```py
N0CHE_lOVE1 = "cat"
print(N0CHE_lOVE1)
```

No stress if you get an error though - they are there to help you figure out what went wrong!

## Strings

A string is simply a series of characters inside quotes. Python recognises single or double quotes to declare your strings. 

```py
print("Hello Noche! How are you feeling today?")
```

When you need to use apostrophes or quotation marks in your string, use the opposite symbol to declare it. Below are a couple examples, one showing an error and the other showing how to correct the error. 

- With an error:
    ```py
  print("Noche said, "meow!" angrily when I tried to feed him chicken.")
    ```
- Without an error:
  ```py
  print('Noche said, "meow!" angrily when I tried to feed him chicken.')
  ```

Strings are useful when you have numbers that should not be treated mathematically - like a phone number. You will never need to take a phone number and divide it by 2 for example.


## Changing the Case in a String

.title() - Capitalises first characters of words
.upper() - uppercase all characters
.lower() - lowercases all characters

An example of this can be shown in the code introduced at the start of this lesson: 

```py
name = "noche"

print("My cat, " + name.title() + ", is a very picky eater.")
print("Today, all I have for dinner is tuna with seaweed.")
```
STOP AND CODE: Try taking away the .title() in the code above to see what happens! Then, replace it with upper() and lower() to see how "noche" changes in case!

There are many different methods that can be used to modify your strings, review some of them here: https://www.w3schools.com/python/python_ref_string.asp

## Concatenating Strings

Python uses the plus symbol (+) to combine strings. This concept is used in our code from the start of this lesson, but here is another example: 

```py

cat = "noche"

print("I have a cat named " + cat.title() + " he loves to sleep and have his belly rubbed." )

```
Another way to concatenate strings is through f-strings! Take a look at the example below: 

```py
name = "noche"

print(f"My cat, {name.title()}, is a very picky eater. Today, all I have for dinner is tuna with seaweed.")

```
Notice the syntax here, we begin our string with an 'f' which signals the beginning of our f-string in Python. To use variables within our string, instead of adding a plus wign we wrap our variable in curly brackets {}. No need for any plus signs! Another fun fact about f-strings, is it automatically turns numbers into strings. An example: 

```py
age = 2

print(f"Noche is {age} years old.")
```

If we were to use + to concatenate our strings instead of an f-string, we would get an error: 

```py
age = 2

print("Noche is " + age + " years old.")
```

Do you have an idea on how to fix this? 
We would need to specify to Python that 'age' is a string in order to use it in this context: 

```py
age = 2

print("Noche is " + str(age) + " years old.")
```

Addition formatting can be applied to your strings using escape characters:
- You can add tabs to your strings using: \t
  ```py
  print("Noche loves: \tcheese\t tuna \tflies \tcurry")
  ```
- You can print on a new line using: \n
  ```py
  print("Noche loves: \ncheese \ntuna \nflies \ncurry")
  ```
When Python encounters the backslash in your string it recognises the next character is an instruction, not part of the string. 

See some additional escape characters here: https://www.w3schools.com/python/gloss_python_escape_characters.asp

## Stripping Whitespace

In programming, whitespace refers to any nonprinting character, such as spaces, tabs, and end-of-line symbols. You typically plan for whitespace to organize your output so it’s easier for users to read.

It’s important to think about whitespace. Many typists have a habit of automatically pressing space after each word. Often you’ll want to compare two strings to determine whether they are the same, for example:
- Checking people’s usernames when they log in to a website.
- Confirming a choice against available options

Python can look for extra whitespace on the right and left sides of a string. 
- Remove whitespace from the left or right end of a string using the lstrip() or rstrip() methods.

STOP AND RUN: Try this example to see rstrip():
```py
cats = "    weasley  "

print(f"I played with {cats.title().rstrip()} all night long and he is still not tired!")
```

STOP AND RUN: Try this example to see lstrip():
```py
cats = "    weasley  "

print(f"I played with {cats.title().lstrip()} all night long and he is still not tired!")
```
 
- Strip whitespace from both sides at once using strip()
STOP AND RUN: Try this example to see strip():
```py
cats = "    weasley  "

print(f"I played with {cats.title().strip()} all night long and he is still not tired!")
```

## Adding Comments

Using # to add comments to help you write notes in your program. Whatever you write past '#' will not effect the rest of your code, it is omly for you to use. Here is an example:

```py
#This code shows how to use variables and strings
name = "noche"

print("My cat, " + name.title() + ", is a very picky eater.")
print("Today, all I have for dinner is tuna with seaweed.")

```

You can also write multi-line comment by using docstrings. These are characterized by used three single quotes. Just like the single line comments mentioned above, anything written within the docstring will also not effect your code, it is purely for documentation purposes. Here is an example: 

```py
'''
This
code shows
how to use
variables
and strings!!
'''

name = "noche"

print("My cat, " + name.title() + ", is a very picky eater.")
print("Today, all I have for dinner is tuna with seaweed.")
```

## Now That You Know It All... Try Modifying the Following Code to Make it Your Own! When you are done, post your code into your chat channel!

STOP AND CODE: Feel free to make this piece of code your own - whether you want to keep it simple or improve on it! Remember this is just practice, and is supposed to be fun! Good luck.  

```py
#This code shows how to use variables and strings
name = "noche"

print("My cat, " + name.title() + ", is a very picky eater.")
print("Today, all I have for dinner is tuna with seaweed.")

```

## Numbers

You can add (+), subtract (-), multiply (*), and divide (/) integers in Python. You can either do this in a python file or via a terminal session, which would just return the result of the operation. See an example of using each of these math operators below: 

- add (+)
  ```py
  operation = 4 + 8

  print(operation)

  ``
- subtract (-)
  ```py
  operation = 8 - 2

  print(operation)
  ``
- multiply (*)
  ```py
  operation = 8 * 2

  print(operation)
  ```
- divide (/)
  ```py
  operation = 8 / 2

  print(operation)
  ```

Python uses two multiplication symbols (**) to represent exponents (raised to the power of…). An example of this is here: 

```py
operation = 8**2

print(operation)
```

TOP TIP: When writing numbers with multiple zeros, you can add underscores to make it more legible! E.g. 1000000000 = 1_000_000_000

## Integers and Floats

Python calls any whole, positive or negative number, an integer and Python calls any number with a decimal point a float. When using integers declared as floats, keep in mind that Python will always automatically display the answer as a float, even when the answer is actually a whole number. 

## Avoiding TypeErrors with the str() Function

A type error means Python can’t recognize or utilise the type of data you’re providing. For example:
- Providing a str() for an integer (mathematical) operation
  ```py
  num1 = 2
  num2 = '2'

  print(num1 + num2)
  ```
- Providing a number for a string method
  - Type error example: 
  ```py
  age = 23 
  message = "Happy " + age + "rd Birthday!" 
  print(message)
  ```
  - Fixed example:
  ```py
  age = 23 
  message = "Happy " + str(age) + "rd Birthday!" 
  print(message)

  ```
str() will tell Python to represent non-string values as strings. 
  - Without str()
  ```py
  #This will give an error
  tuna_cans = 1_000_000
  print("If noche could eat " + tuna_cans + "cans of tuna he would not hesitate.")
  ```
  - With str()
  ```py
  #This will not give an error
  tuna_cans = 1_000_000
  print("If noche could eat " + str(tuna_cans) + " cans of tuna he would not hesitate.")

  ```

## Let’s do some exercises to practice what we’ve learned! Complete exercise 1: Variables, Strings, and Data Types
