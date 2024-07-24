## Working with Lists
---

#### Learning Objectives:
- In this session we will:
- Understand and use For Loops
- Use the Range function
- Use some more list functions
- Slice and Copy lists
- Understand Tuples vs. Lists
---

#### Take a Look!

What doe you think will happen if this code were to run?

```py
foods = ["tuna", "salmon", "mackerel", "trout"]

print("Okay Weasley, you can eat any of the following for dinner:")

for food in foods:
    print("You can have " + food + " for dinner. ")
    print("or....")
   
print("Nothing!")
```
Let's break down the content from this piece of code. 

---
#### for loops
A for loop is used for iterating over a sequence. What Python will do is loop through each of the items in a list that you have provided, rather than accessing each item in the list individually. For example, imagine we have a list of Noche and Weasley's favorite food items: 

``` py
favorite_foods = ['tuna', 'salmon', 'sardines', 'mackerel']
```
As we learned last lesson, to access individual items within a list we can code: 

```py
print(favorite_foods[0])
```
This can be time consuming to code over and overagain, and can also cause a lot of clutter in your code. Instead of accessing each food item individually, use a for loop! The syntax for a for loop is as follows: 

```py
for <each item> in <list of items>:
    <code to run on each item>
    <more code to run on each item>
```
STOP AND RUN: Let's apply this syntax to access each element in the favorite_foods list. Try running the code below to see how it works!

```py
favorite_foods = ['tuna', 'salmon', 'sardines', 'mackerel']

for food in favorite_foods:
    print(f"Okay Weasley and Noche! You can have {food} for dinner!")
```

When the code runs, it will iterate through each item listed in the favorite_foods list along with a statement. In the code, 'food' can be seen as a temporary variable that allows each item in the favorite_foods list to pass through and be used within the for loop. 

Now take a look at the example from the start of this lesson: 

```py
foods = ["tuna", "salmon", "mackerel", "trout"]

print("Okay Weasley, you can eat any of the following for dinner:")

for food in foods:
    print("You can have " + food + " for dinner. ")
    print("or....")
   
print("Nothing!")
```


TOP TIP: Always remember to add your colon ( : )!


### Let's Take a Math Break!
---
#### Making Numerical Lists

#### 'range()' function

#### `list()` function

#### Finding min, max, and sum of digits

### Back to Our Teaching Assistants!

---
#### Slicing a List


#### Looping Through a Slice

#### Copying a List


#### Tuples


#### Redefining a Tuple

### Back to our code from the start!

### Well done! Now move onto the Working with Lists Exercises!
