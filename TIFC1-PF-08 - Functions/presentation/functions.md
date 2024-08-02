# Functions

## Learning Objectives

- Understand what a function is, how to define it, and when to use it
- Understanding the difference between an argument and a parameter
- Understanding when to use keyword and positional arguments

#### What are Functions?

Functions are blocks of code designed to do a specific job. 

#### How do I Use Functions?

If you want to use the function you have defined, you need to call on the function. You can create functions within your code, or you can also store your functions in different files (modules) and call on them from the main codebase. 

#### Why are functions useful?

It means that instead of writing out block of the same or similar code several times resulting in lots of duplication, you can write one function and call it as necessary instead. This can help you avoid creating long files which are difficult to work with.

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

So far, when we've written code, we've given that code data to work on, usually by assigning the data to a variable, then *passing* the variable through the code. When we run our code Python executes it from top to bottom, following our loops and branches.

But the code in a functione only runs when the function is called.

A **Parameter** is a value we can pass through to our function when we call it, and the function can use these values to provide more *functionality*.

We specify the required parameter(s), in this case `dog`, in the brackets when we declare the function, when calling a function we need to provide a value for the parameter(s). 

The value that we pass through is called an **Argument**. This may seem a bit confusing, but it's because we can call the function over and over again, passing through different *arguments* to the same *parameter*.

### Passing Arguments

Our simple function just takes the parameter and prints it out in a welcome message

```py
def greet_sausage(dog):
    print(f"Hi {dog.title()}")

greet_sausage('Scout')
greet_sausage('Frankie')
```

To call the function we use it's name and provide any required arguments. Here we call the function twice, each time we pass through a different argument to the `dog` parameter, first `Scout` then `Frankie`. 

This illustrates how the parameter allowed us to make the function more useful. The first function could only say "Hi" to Frankie, but the second one can welcome anyone you provide as an argument.

## More Complex Functions

We can create more useful functions by providing more parameters and arguments, in addition to writing more advanced code to process this data.

### Positional Arguments

When using functions with multiple parameters there are a few things to consider. 

```py
def describe_pet(animal_type, pet_name):
    print("\nI have a " + animal_type + ".")
    print("My " + animal_type + "'s name is " + pet_name.title() + ".")

describe_pet('dachshund', 'scout')
describe_pet('scout', 'dachshund')
```

Order matters! When you call a function and provide the necessary arguments, they populate the parameters in the order you provide them, i.e. argument 1 = parameter 1, argument 2 = parameter 2, and so on.

### Keyword Arguments

Another way to pass your arguments is to specify the name of the relevant parameter, with this approach the order of your arguments doesn't matter. 

```py
def describe_pet(animal_type, pet_name):
    print("\nI have a " + animal_type + ".")
    print("My " + animal_type + "'s name is " + pet_name.title() + ".")

describe_pet(animal_type='dachshund', pet_name='scout')
describe_pet(pet_name='scout', animal_type='dachshund')
```

### Default Values

You may also provide a default value for a parameter which will be used if an argument is not provided, which could also be useful when the argument will be the same for *most* of the function calls. You can still provide an argument to override the default.

```py
def describe_pet(animal_type, pet_name='dachshund'):
    print("\nI have a " + animal_type + ".")
    print("My " + animal_type + "'s name is " + pet_name.title() + ".")

describe_pet(pet_name='scout')
```

### Return Values

A function doesn’t always have to display its output directly with print statements, instead it can process some data, then return the data back to the main code for further processing. 

```py
def describe_pet(pet_name, animal_type):
    pet_info = pet_name + ", " + animal_type
    return pet_info

my_pet = describe_pet('scout', 'dachshund')
print(my_pet)
```

This function is similar to the previous ones, but the function doesn't print anything. Instead, it creates a variable `pet_info` comprised of the parameters, then uses a `return` statement to pass the variable and data within back to the line that called the function. Once returned the variable `my_pet` contains the variable `pet_info`, which is then printed out.

### Optional Arguments

By default Python will return an error if a function is called and the number of arguments and parameters doesn't match. But you may want to create an optional parameter which can be used, but doesn't need to be, for example, a parameter for middle name.

```py
def describe_pet(pet_name, animal_type, pet_last_name=' '):
    if pet_last_name:
        pet_info = pet_name + ', ' + pet_last_name + ', ' + animal_type
    else:
        pet_info = pet_name + ', ' + animal_type
    return pet_info

my_pet = describe_pet('Frankie', 'dachshund')
print(my_pet)

my_pet = describe_pet('Frankie', 'dachshund', 'Furter')
print(my_pet)
```

Here we assign an empty default value to the `pet_last_name` parameter when declaring the variable, followed by an `if` statement which branches based on whether there is any value passed to `pet_last_name`. Either way, the resultant `pet_info` object is returned by the function.

## Functions With Other Python Features

Writing functions and calling them on demand as needed is a very common strategy in application development. All of the features we've learned about so far may be utilised as part of your functions. 

### Functions and Dictionaries

In this example the function builds and returns a dictionary from the provided arguments.

```py
def describe_pet(pet_first_name, pet_last_name):
    my_pet = {'first': pet_first_name, 'last': pet_last_name}
    return my_pet

dog = describe_pet('Frankie', 'Furter')
print(dog)

for x, y in dog.items():
    print(y)
```
*There is also a `for` loop to iterate through the items in the returned dictionary - that's just there as a reminder*

### Functions and Lists

When you pass a list to a function, the function gets direct access to the contents of the list. In this example a `for` loop is used to iterate through the items in the list, which is passed through to the `foods` parameter.

```py
def dog_food(foods):
    for food in foods:
        dinner = f"Do you fancy {food} for dinner tonight?"
        print(dinner)

fridge = ['chicken', 'beef', 'sausages']
dog_food(fridge)
```

In addition to iterating through a list, you might also want to modify it with your function. In the below example we iterate through a `cooked` list, remove items from a `fridge` list, and add the items to the `empty_items` list.

```py
fridge = ['chicken', 'beef', 'sausages']
empty_items = []

def eat_food(name, foods):
    print(foods)
    for food in foods:
        print(f"{name} is eating {food}")  
        empty_items.append(food)
        fridge.remove(food)

cooked = fridge[:]
eat_food('Scout', cooked)
for item in empty_items:
    print(f"You've eaten all of the {item}!")
if not fridge:
    print("\nYou've eaten everything in the house!")
```

Try to identify the following points in the code above:
- Create a list of foods and an empty list
- Makes a copy of the list of foods and pass it through when calling the function
- Eat each item
- Remove each eaten item from the fridge, and add it to the empty list
- Print out each eaten item
- Confirm the fridge is empty

### Passing an Arbitrary Number of Arguments

Sometimes you won’t know ahead of time how many arguments a function needs to accept. Fortunately, Python allows a function to collect an arbitrary number of arguments from the calling statement. 

```py
def dog_dinner(amount, *meats):
    """What goes into the dog's bowls?"""
    for meat in meats:
        print(f"I'm putting {amount} scoops of {meat} in each of your bowls")
        #print(meats)

dog_dinner(2, 'chicken', 'kibble', 'gravy')
```

The arguments passed through to the parameter are added into a **tuple** (un-comment the `print(meats)` line, or try to modify `meats` to verify).

Notice, we also used both *positional* and *arbitrary* arguments in this example.

### Arbitrary Keyword Arguments

Previously we used *keyword arguments* to pass through values to specific parameters, but sometimes you’ll want to accept an arbitrary number of keyword arguments, and you don't know what parameters would be needed. 

Whereas a single `*` creates an empty tuple hold your items, double `**` makes an empty dictionary and adds your keyword arguments as keys and values.

```py
def build_profile(first, last, **user_info):
    user_info['first_name'] = first
    user_info['last_name'] = last
    return user_info

new_user = build_profile('Antony', 'Foy', Age=41, Height="6'", Location='Manchester', Subject='Cloud')
print(new_user)
```

In this case a collection of keyword arguments are passed through, which are then added to a `user_info` dictionary, which is created when you call the function. The function then adds the positional arguments `first` and `last` into the dictionary too, but this is just to give you a syntax reminder. There's no reason they couldn't just be added straight to the dictionary as keyword arguments like all of the others. 

## Modules

In our examples we've just created one function at a time and called that function to demonstrate the behaviours. However, as you create more complex app's, with more and more features, you can end up with lots of different functions, and your files become very long and difficult to work with.

One way to avoid this is by storing your functions in a separate file called a module, and then importing that module into your main program. There's nothing different about the module, it's just a .py file, full of your named functions.

An import statement tells Python to make the functions in a module available to the currently running program file.

```py
import my_module

my_function('argument1', 'argument2')
```

This example calls a function called `my_function` from a module called `my_module` which was imported at the beginning of the file. `my_function`, saved in `my_module` could be very long and complex, but this bit of code looks very simple and is easy to work with.

### Importing Specific Functions

If you don't need to import all of the functions in a module, you can just import the function you need. 

```py
from my_module import my_function

my_function('argument1', 'argument2')
```

You can import all functions from a module using `*`

```py
from my_module import *

my_function('argument1', 'argument2')
another_function('argument1', 'argument2')
```

### Function Aliases

Sometimes you might have lots of functions, and to ensure that you can find the one you need, they're given long descriptive names. This can make your code look messy and tricky to read, especially if you use the function many times. Aliases allow you to assign an alternative name to reference and call the function.

```py
from my_module import my_function as mf

mf('argument1', 'argument2')
```
---

If you've followed all of this then great job. Writing and using functions is a crucial part of app' development and the logic of what we've covered applies to many different languages. 

To understand the value of functions a bit more, consider you are programming a game. You want you character to be able to move forward, backward, left, right; You want to jump, duck, interact with things you're pointing at; Pretty much everything you want to do in the game could be a function in your code, which is called when the player presses the appropriate button.

## Practice

Classes, which we're looking at next build upon the concept of functions, so please attempt the functions exercises before we move on.
