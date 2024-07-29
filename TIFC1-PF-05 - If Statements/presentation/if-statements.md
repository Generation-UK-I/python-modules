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

If statements are conditional statements. They look for whether a statement is true or false, then it can do something based on the result. 

A really good example, is making a decision for a meal at a restaurant….

---
## Comparison Operators

IMAGE HERE

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
