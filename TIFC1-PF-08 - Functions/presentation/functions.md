# Functions

## Learning Objectives

- Understand what a function is, how to define it, and when to use it
- Understanding the difference between an argument and a parameter
- Understanding when to use keyword and positional arguments

#### What are Functions?

Functions are blocks of code designed to do a specific job. 

#### How do I Use Functions?

If you want to use the function you have defined, you need to call on the function. 

#### Why are functions useful?

It means that instead of writing out block of code several times, you can just call on the function instead. You can create functions within your code, or you can also store your functions in different files and call on them from the main codebase. This can help you avoid creating long files which are difficult to work with.

## A Very Simple Function

```py
def greet_sausage():
    print("Hi Frankie")

greet_sausage()
```

This is a very simple function, but you can see the important syntax. we define `def` our new function and give it a name, `greet_sausage` in our case. We also have a pair of brackets we'll use shortly, but this function works without anything else. Then to call our function we simply use the name we gave it. 

### Making it More Useful

To make our functions more useful, we have to provide more information. Here's the same function with a few changes for us to explore.

```py
def greet_sausage(dog):
    print(f"Hi {dog.title()}")

greet_sausage('Scout')
greet_sausage('Frankie')
```

### Arguments and Parameters

So far, when we've written code, we've given that code data to work on, usually by assigning the data to a variable, then *passing* the variable through the code.

When we write a function, it's code only runs when the function is called, and the code stays within the function. 

A parameter is a value we can pass through to our function when we call it, and the function can use these values to provide more *functionality*.

We specify the required parameter(s), in this case `dog`, when we declare the function.

```py
def greet_sausage(dog):

```

We pass values through to the parameters 

In the example above we called the function twice, each time we passed through a different value. The value that we pass through to a parameter is called an argument. This may seem a bit confusing, but it's because we can call the function over and over again, like we did here, passing through different *arguments* to the same *parameter*.

You can also see in the above example how the parameter allowed us to make the function more useful. The first function could only say "Hi" to Frankie, but the second one can welcome anyone you provide as an argument.

### What is Object-Oriented Programming?