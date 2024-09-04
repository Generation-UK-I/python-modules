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

The second part of this code is the if statement itself. The statement reads as: if food is equal to croissant, then print 'You have bought a croissant!'. The if statements always start with 'if' and then a condition to evaluate. In this case, the if statement is evaluating your order against the word 'croissant'. There is another bit in this code that has not been covered though, and this is the comparison operator `==`. A comparison operator in Python is used to compare two values and returns True or False based on the comparison. Here is a list of Python operators you can use: 

- Equal (==): Checks if two values are equal.
- Not Equal (!=): Checks if two values are not equal.
- Greater Than (>): Checks if the value on the left is greater than the one on the right.
- Less Than (<): Checks if the value on the left is less than the one on the right.
- Greater Than or Equal To (>=): Checks if the value on the left is greater than or equal to the one on the right.
- Less Than or Equal To (<=): Checks if the value on the left is less than or equal to the one on the right.

In our croissant example, the equal (==) operator is used to check to see if the value of the 'food' variable is equal to the word 'croissant'. Try re-running the code again, but think about the other menu items from our scenario. Try ordering a brownie, for example. Notice that when you type in 'brownie' nothing happens! You are taken back to the command prompt. This is because the condition within the if statement evaluated to False, so the action was not taken. Nothing happens because we have not given Python anything to do if the condition was evaluated to False... So let's give it something. 

```py
food = input("What would you like to order? \n")

if food.lower() == 'croissant':
    print("You have bought a croissant!")
else:
    print(f"You have ordered {food}")
```

Try running this piece of code and at the input prompt, type in brownie again as your menu item and observe what happens. 

We have added an 'else' statement. How this code reads, is now: if the food is equal to the word croissant, then print out "You have bought a croissant!". For all else, print out "You have ordered (whatever the food you have ordered)".



There is so much more we can do with lists though! We can combine it wil topics we have learned before, for example!

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

---

## if-elif-else

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
