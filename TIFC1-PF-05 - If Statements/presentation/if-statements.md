# If Statements
---

## Learning Objectives: 
- What is an IF Statement and how are they used?
    - What is the correct syntax?
    - How do you structure if-elif-else to carry out multiple tests?
- What are Boolean Expressions?
- What are comparison operators?
- Using IF statements with Lists and Loops

---

## Back to Dinner… Weasley and Noche Problem
IMAGES HERE

## What Would Happen if I Ran This?

Think about what would happen if this piece of code ran. Walk through line by line and guess! The rest of this unit will break down the concepts seen in this piece of code and more. Let's dive in!

```py
foods = ['tuna', 'mackerel', 'salmon', 'sardines']

answer = input("What would you like to eat today boys?\n")

if answer.lower() == 'tuna':
    print(f"Okay, let's have {foods[0]} for dinner!" )
elif answer.lower() == 'mackerel':
    print(f"Okay, let's have {foods[1]} for dinner!")
elif answer.lower() == 'salmon':
    print(f"Okay, let's have {foods[2]} for dinner!")
elif answer == foods[3]:
    print(f"Okay, let's have {foods[3]} for dinner!")
else:
    print("Sorry boys! I only have chicken for dinner!")
```

---

## Boolean Expressions

This is a name for a conditional test - it is checking for whether or not something is TRUE or FALSE. 

You can imagine all of the use cases for this! 

## If Statements

If statements are conditional statements. They look for whether a statement is true or false, then it can do something based on the result. The correct syntax for the if statement is as follows: 

```
if condition:
    statements that will be executed if the  condition is evaluated as true
```

A good analogy of an if statement is visiting a coffee shop. 

Imagine you are walking into a coffee shop, hoping to get a coffee or a selection of treats. There are a few people ahead of you in the line, so while you are waiting you check out the menu. Latte, americano, cappucino... It all looks great!... Then your eyes fall on the selection of sweet treats on the counter. A warm cinnamon roll, freshly baked croissant, creamy cheese danish, and a slice of a rich brownie. It all looks delicious, so you start to think about what you would prefer to order from the selection of treats. You decide that you want something simple, a classic butter croissant. However, you notice that someone in the line has ordered a croissant - oh no! So you decide that if there are croissants left, then you will buy one. Otherwise, the warm cinnamon roll is calling your name so you may just order that instead. 

As the people in front of you in line make their orders, you also notice that the warm cinnamon rolls numbers are now dwindling. So you need to give yourself another option to choose from if the croissants and cinnamon rolls are sold out. You peer over the counter to see the rich cheese danish and chocolate brownie. You decide that if the butter croissant is avaiable, you will order this. Otherwise, if the cinnamon roll is available, you will order that. If both the cinnamon roll and the croissant is unavailable, then you will order the chocolate brownie but if that is unavailable then you will order the cheese danish. If all else fails and none of these options are available, you decide that it is not worth ordering anything and will leave the coffee shop. 

This scenario is very similar to how if statements work. If statements are looking for whether something is true or false, and then taking actions that you specify. Let's start with our first choice, the humble butter croissant: 

```py
if there is a croissant, 
    Then I will buy the croissant
```
Although the syntax is not technically correct, the concept of an if statement still applies. Python will look at that first line of code `if there is a croissant available` and will evaluate whether this is true or false. If the statement is evaluated as true, then Python will run the action `Then I will buy the croissant`. If there are no croissants available, then the statement will be evaluated as false and that action will not run. Now, let's take a look at an if statement with the correct syntax: 

```py
food = input("What would you like to order? \n")

if food.lower() == 'croissant':
    print("You have bought a croissant!")
```

Try running the above code. There is a couple concepts in here that we have not covered yet, but don't worry for now! Focus on the logic of how an if statement works, then the other concepts will be broken down later on in this powerpoint. 

The code will prompt you in the terminal to order something, try ordering a croissant. If you type in the word 'croissant', then you should see the response in the terminal is, ' You have bought a croissant!'. In the code, Python is reading the first line `food = input("What would you like to order? \n")`. This line has created a variable called food, and stored inside the variable is `input()` and a prompt. `input()` is a tool used for user input. Ther code will pause at this point and wait for a response from a user, or some kind of input. In this case, `input()` is waiting for you to order something. Once you have typed in your order, your repsonse will be stored in the variable 'food', and you can use this variable throughout the life of your code! We will be practicing `input` later on in this course, however it is good to mention now since it makes your if statements more interactive and interesting. In the case of this piece of code, we are using the `input()` within an if statement. 

The second part of this code is the if statement itself. The statement reads as: if food is equal to croissant, then print 'You have bought a croissant!'. The if statements always start with 'if' and then a condition to evaluate. In this case, the if statement is evaluating your order against the word 'croissant'. There is another bit in this code that has not been covered though, and this is the comparison operator `==`. 

## Comparison Operators in the Cafe

A comparison operator in Python is used to compare two values and returns True or False based on the comparison. Below is a list of Python operators you can use with some example. Try running each of the examples to see the behavior of the code. You could also try changing the numbers to see how the code would react differently!

- Equal (==): Checks if two values are equal.
```py
x = 10
if x == 10:
    print("x is equal to 10")
```

- Not Equal (!=): Checks if two values are not equal.
```py
y = 5
if y != 10:
    print("y is not equal to 10")
```

- Greater Than (>): Checks if the value on the left is greater than the one on the right.
```py
a = 15
if a > 10:
    print("a is greater than 10")
```

- Less Than (<): Checks if the value on the left is less than the one on the right.
```py
b = 3
if b < 10:
    print("b is less than 10")
```

- Greater Than or Equal To (>=): Checks if the value on the left is greater than or equal to the one on the right.
```py
c = 7
if c >= 5:
    print("c is greater than or equal to 5")
```

- Less Than or Equal To (<=): Checks if the value on the left is less than or equal to the one on the right.
```py
d = 4
if d <= 4:
    print("d is less than or equal to 4")
```

The comparison operators shown above are actually the same as what you would use in Math, so hopefully they are not too unfamiliar. Sometimes, you might also come across some word-based operators in Python. These each have differen use cases like the ones above. Take a look at some of them below and some examples:

- and: Combines two conditions and returns True only if both are true.
```py
number = 15

if number > 10 and number < 20:
    print("The number is between 10 and 20.")
```

- or: Combines two conditions and returns True if at least one of them is true.
```py
number = 3

if number < 5 or number > 100:
    print("The number is either less than 5 or greater than 100.")
```

- not: Negates a condition, returning True if the condition is false and False if it's true.
```py
number = 7

if number != 10:
    print("The number is not 10.")
```

The above three operators can be used with any data types in Python. They can also be combined with any of the other operators to add more conditions to your statement. Here is an example of using all three: 
```py
number = 120

if (number < 5 or number > 100) and number != 50:
    print("The number is either less than 5 or greater than 100, and it's not 50.")
```

- is: Checks if two variables point to the same object.
```py
number = 10

if number is 10:
    print("The number is exactly 10.")
```

- is not: Checks if two variables point to different objects.
```py
number = 20

if number is not 10:
    print("The number is not 10.")
```

- in: Checks if a value is present within an iterable (like a list, string, etc.). The following example will not be using a list, but usually this operator would be used to find a value within a list, tuple, etc... This example shows a value within a string.
```py
text = "hello world"

if "hello" in text:
    print("'hello' is found in the text.")
```

- not in: Checks if a value is not present within an iterable.
```py
text = "hello world"

if "goodbye" not in text:
    print("'goodbye' is not found in the text.")
```

There are any different operators Python uses to compare. The beauty of Python, is that the operators are very versatile and can be used in different use cases and wih different data types. In our croissant example, the equal (==) operator is used to check to see if the value of the 'food' variable is equal to the word 'croissant'. Let's take a look at our previous code about our coffee shop options:

```py
food = input("What would you like to order? \n")

if food.lower() == 'croissant':
    print("You have bought a croissant!")
```

Try re-running the code again, but think about the other menu items from our scenario. Try ordering a brownie, for example. Notice that when you type in 'brownie' nothing happens! You are taken back to the command prompt. This is because the condition within the if statement evaluated to False, so the action was not taken. Nothing happens because we have not given Python anything to do if the condition was evaluated to False... So let's give it something. 

```py
food = input("What would you like to order? \n")

if food.lower() == 'croissant':
    print("You have bought a croissant!")
else:
    print(f"You have ordered {food}")
```

Try running this piece of code and at the input prompt, type in brownie again as your menu item and observe what happens. 

We have added an 'else' statement. How this code reads, is now: if the food is equal to the word croissant, then print out "You have bought a croissant!". For all else, print out "You have ordered (whatever the food you have ordered)". The else statement provides an alternative action if the condition in the if statement is False (meaning food is not "croissant"). If the if condition is False, `print(f"You have ordered {food}")` is executed instead. It prints a message saying "You have ordered" followed by the input response's value of food. 

But wait, there's more! We have other items from our scenerio to consider that we might want to introduce different actions for. This is where to 'elif' statement comes in. Take a look at our revised code below:

```py
food = input("What would you like to order? \n")

if food.lower() == 'croissant':
    print("You have bought a croissant!")
elif food.lower() == 'cinnamon roll':
    print("You have ordered a cinnamon roll warmed up!")
else:
    print("This is not available... So I will go home!")
```

The elif statement stands for "else if." It provides an additional condition to check if the first if condition is False. If the first if condition is False and this elif condition is True (meaning the user input matches "cinnamon roll" in any case), the code inside this elif block action will be executed. If the elif condition is True, this line prints the message: You have ordered a cinnamon roll warmed up!. 

The else block provides a fallback action if none of the preceding if or elif conditions are True. If both the if and elif conditions are False, the code inside the else block will run. If the user's input does not match either "croissant" or "cinnamon roll," this line prints: This is not available... So I will go home!.

Now, think back to our scenario from the beginning. Let's put our entire scenario together into a single piece of code, adding all the options: 

```py
food = input("What would you like to order? \n")

if food.lower() == 'croissant':
    print("You have bought a croissant!")
elif food.lower() == 'cinnamon roll':
    print("You have ordered a cinnamon roll warmed up!")
elif food.lower() == ' brownie':
    print("You have ordered a brownie, warmed up with a scoop of ice cream.")
elif food.lower() == 'cheese danish':
    print("You have ordered a cheese danish to go!")
else:
    print("This is not available... So I will go home!")
```
In this code we have added more options to emulate the scenario we had before. For each of the different options, we have added another elif statement to create individual actions to execute in the event you choose brownie, cheese danish, or one of the other options. Your else statement is a fallback, so if any other foods are chosen the the else block will be executed, saying that the item is not available. Try running the above code to see how it works, keep notice of the behavior of the code. 

There is so much more we can do with lists though! We can combine it with topics we have learned before, for example!

## Checking Whether an Item is not in a list

```py
foods = ['tuna', 'sardines', 'chicken', 'beef']
unhappy_foods = 'avocado'

if unhappy_foods not in foods:
    print(unhappy_foods + " is not on the list, sorry!")
```

```py
foods = ['tuna', 'sardines', 'chicken', 'beef', 'avocado']
unhappy_foods = 'avocado'

if unhappy_foods not in foods:
    print(unhappy_foods + " is not on the list, sorry!")
else:
    print("Hooray we have it!")
```

## Using if statements with loops and lists

```py
foods = ['tuna', 'sardines', 'chicken', 'beef', 'avocado']

for food in foods:
    if food == 'chicken':
        print(f"I know you don't like chicken, but this is good for you!")
    else:
        print(f"We have {food} in the pantry, let's eat!")
       
print("No more food! Goodbye!")
```

## Having Multiple Lists!

```py
available_foods = ['tuna', 'sardines', 'halloumi', 'chicken', 'beef', 'salmon', 'avocado']
disliked_foods = ['chicken', 'beef', 'turkey', 'bacon']

for food in available_foods:
    if food in disliked_foods:
        print(f"I know you don't like this, but it is good for you!!")
    else:
        print(f"Yay! We have something you like!")
       
print("No more food! Goodbye!")
```


## Back to Our Code from the Start!

```py
foods = ['tuna', 'mackerel', 'salmon', 'sardines']

answer = input("What would you like to eat today boys?\n")

if answer.lower() == 'tuna':
    print(f"Okay, let's have {foods[0]} for dinner!" )
elif answer.lower() == 'mackerel':
    print(f"Okay, let's have {foods[1]} for dinner!")
elif answer.lower() == 'salmon':
    print(f"Okay, let's have {foods[2]} for dinner!")
elif answer == foods[3]:
    print(f"Okay, let's have {foods[3]} for dinner!")
else:
    print("Sorry boys! I only have chicken for dinner!")
```

# Next Up: Complete the Exercises!!
