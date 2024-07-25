# Files and Exceptions

## Learning Objectives

- Explain what a class is, how to create one, and what the purpose of them is
- Introduce practical uses of a class (accessing attributes, etc)
- Explore the concept of inheritance and practice using child classes
- How to import classes into another piece of code

## What are Classes?

To understand Classes, first let's start with a more abstract concept...

### What is Object-Oriented Programming?

Python is an example of an object-oriented programming language. 

In object-oriented programming (OOP) we create and work with objects, which are unique instances of *something*!

- If I want to create an app for managing my pet's worm and flea treatments, I need *something* in the app which represents and stores info for each pet. 

- If I want to create a game which has lots of enemies, I need *something* to represent each one, allowing each individual enemy to have it's own characteristics like a health bar, different weapons, etc.

- If I make an app for a coffee shop, each individual coffee, with it's specific options, needs to be tracked from ordering to completion.

These are all examples where object-oriented programming can be useful. Each pet is an object; Each enemy in the game can be an object; Each coffee can be an object; And so on. This approach allows us to write code which works with our objects.

So, if a customer selects Caramel Syrup in their coffee, we can write a line of code which adds that option to the specific object that requires it, but not every object - OOP allows individual objects to be handled differently, such as to be personalised.

### Back to Classes

Classes are how we make objects, they're like object constructors, or a blueprint for creating new objects.

### Creating and Using a Class

You can model almost anything using a class. To start, you use the keyword ‘class’. You just need to think about what you are modelling.

#### Bring in the CATS

<img src="img/weasleyandnoche.jpg" width="600" />

Think about what a cat is... They have a name, fur, age... They also do things like sleep and climb on stuff they shouldn't!

We will create a class that will store the name of a cat, the age of the cat and give the cat the ability to climb and sleep.



```py
class Cat():
    #an attempt to model a cat
    def __init__(self, name, age):
        #assign the cats name and age
        self.name = name
        self.age = age

    def sleep(self):
        #The cat can sleep
        print(f"{self.name} is fast asleep like a little angel")

    def climb(self):
        #The cat can sleep
        print(f"Quick! {self.name} is climbing on the roof!")
```

There is a lot going on here though so let’s break it down.

---

### The open() function
