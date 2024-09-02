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

What do+
-you think will happen if this code were to run?

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
    print(food)
```

When the code runs, it will iterate through each item listed in the favorite_foods list until there are no more items in the list to print out. Think of this code as: For each food in the list of favorite foods, print our each food item. 

In the code, 'food' can be seen as a temporary variable that allows each item in the favorite_foods list to pass through and be used within the for loop. 

Need a break from all the cats and cat foods? No worries, let's take a look at another example with some other furry friends: 

```py
dogs = ['frankie', 'otto', 'daisy', 'flossie']

for dog in dogs:
    print(dog)
```

This works the exact same way as the previous example, just with a different list and different variable names. Think of this as: For each dog in the dogs list, print their name. Python will loop through each dog in the list and print their name.

Now take a look at the example from the start of this lesson: 

```py
foods = ["tuna", "salmon", "mackerel", "trout"]

print("Okay Weasley, you can eat any of the following for dinner:")

for food in foods:
    print("You can have " + food + " for dinner. ")
    print("or....")
   
print("Nothing!")
```
The for loop works exactly the same as the previous examples! We start with a list of foods, then the for loop will iterate through each item in our list of foods but will include the item in a statement. Try running this code to see how it works! 

STOP AND CODE: Try modifying one of the previous examples to make your own code using a for loop. The best way to learn Python is to practice and make mistakes! 
TOP TIP: Always remember to add your colon ( : )!


### Let's Take a Math Break!
---
#### Making Numerical Lists

Cats and dogs aside, sometimes you might need to make lists using numbers. To make a list using numbers, you do exactly what you have seen with our list of cat food and dogs:

```py
numbers = [1, 2, 3, 4, 5]

for number in numbers:
    print(number)
```
But you can do so much more with numbers and lists!

#### 'range()' function

Python’s range() function makes it easy to generate a series of numbers within a given range of numbers you provide. The syntax to use range() is as follows: 

```py
range(start, stop, step)
OR
range(<starting point>,<what you want to go up until>,<how many you go up by>)
```
The start and step integers are optional, only the stop integer is mandatory. The start integer is what number you want to start from, by default the starting number is 0 unless specified. The stop integer is where you  want to end or what you wnat to count until. Finally, the step number specifies the incrementation or what would you like to count up by. Take a lok below for some example use cases for each of these. 

In the following code, we use a for loop to loop through a specific range of numbers. To use range, specify the starting number first and then the final number last. In this case, the code will run through the numbers, 1, 2, 3... Try running the following to see how range works:

```py
for value in range(1,5):
    print(value)
```
Did you notice anything strange when running it?

You may have noticed that the output shown when running the above code was as follows: 

```py
1
2
3
4
```

Why do you think it does that? 

Python has a 'one off' behavior, so will not show last value, only up until 4. The reason goes back to zero-based indexing, which was discussed in the last module. Recall that Python starts counting from 0, so if we want to access the first element within a list, we need to start from 0. The reasoning behind why Python has this 'one off' behavior is the same. To see an example of this, try running the following code: 

```py
for value in range(5):
    print(value)
```
Instead of specifying a starting number, only a final number was given. Notice that if a starting number is not given, then the output will be: 

```py
0
1
2
3
4
```
Python did count up to 5 numbers, but starts from 0 when counting. If you would like to count from 1-5 exactly, you will need to put the final number as 6 rather than 5. Try running this code: 

```py
for value in range(1,6):
    print(value)
```

The output is now: 

```py
1
2
3
4
5
```

We have dscussed using the start and stopping integers when using range(), but what about the step integer? Try running the following code: 

```py
for value in range(2,21,2):
    print(value)
```
In this code, the starting integer is 2 and the stopping integer is 21. On its own, python would count from 2-20. However, this code has added a 2 as a step integer. This means, then we can count up by a number that we specify. In this case, the output would be: 

```py
2
4
6
8
10
12
14
16
18
20
```
If the step integer was changed, we could count up by other numbers such as 3: 

```py
for value in range(2,21,3):
    print(value)
```
The output would be: 

```py
2
5
8
11
14
17
20
```

STOP AND CODE:Try changing the start, stop, and step integers to see how range() works! 


#### `list()` function

`list()` is a Python function that makes a new list, which is like a container that can hold a collection of items in a specific order. The syntax for using this, is as follows: 

```py
list([iterable])
```
Iterables are an optional parameter that can be any iterable (like a list, tuple, set, or string). If no argument is provided, it creates an empty list. For example:

```py
new_list = list()
```
This piece of code create an empty list that you can append items into. If you would like to create a list from an iterable, you could try: 

```py
my_list = list('hello noche')

print(my_list)
```
STOP AND RUN: Try running the above code to see how it works! Try changing the message within the list to see different outputs!

That is not all you can do with `list()`! If you want to make a list of numbers, you can convert the results of range() directly into a list using the list() function. When you wrap list() around a call to the range() function, the output will be a list of numbers. Here is an example of this: 

```py
numbers = list(range(1,6))
print(numbers)
```
The output of this will be: 
```py
[1, 2, 3, 4, 5]
```
You could even use these functions to skip numbers in a given range using `list()`! Here is an example of this: 

```py
even_numbers = list(range(2,11,2))
print(even_numbers)
```

`list()` is a very useful function when working with lists. There is much more you can do with this! For now, we will continue to learn about other concepts. 

#### Finding min, max, and sum of digits

Sometimes, you may need to find the minimum, maximum and the sum of digits. Python has built-in tools that allow you to do this! Take a look at the following example: 

```py
digits = [1, 2, 3, 4, 5, 6, 7, 8, 9, 0]
print(min(digits))
print(max(digits))
print(sum(digits))
```

This piece of code starts with a list of digits from 0-9. min(digits) calculates the smallest value in the digits list, which is 0. max(digits) calculates the largest value in the digits list, which is 9. sum(digits) calculates the total sum of all the values in the digits list. The sum is 1 + 2 + 3 + 4 + 5 + 6 + 7 + 8 + 9 + 0 = 45. So, the output of this code would be: 

```py
0
9
45
```
STOP AND CODE: Try creating a list, then use `min()`, `max()`, and `sum()` to print different outputs! Good luck!

### Back to Our Teaching Assistants!
<img src="img/happy_weasley.jpg" width="300" />

---
#### Slicing a List

Slicing a list in Python means making a new list by taking a part of the original list. You can choose where to start, where to stop, and how many steps to take between elements. The syntax is very similar to what we learned with `range()`, just not was are using index numbers to manipulate what list items are in the output. The syntax for slicing a list is as follows: 

```py
your_list[start:stop:step]
```

Let's take a look at Weasley and Noche's list of dinner items to show some examples. We will start with a list of their favorite foods, then will practice slicing the list. RUN each of the following example codes to see how it works. Feel free to change the index numbers to see what happens! Here is an example of omitting the start or stop index number:


```py
foods = ["tuna", "salmon", "mackerel", "trout"]

print(foods[:2])
```

In the above code, only the stop index number was provided. Therefore, the output will begin from the start of the list. The slice was made at index number 2 of our list. This means that the output will be: 

```py
['tuna', 'salmon']
```

Try changing the stop index number to see how you can manipulate the output. 

The next piece of code is an example of omitting the stop index and only using the start index number. 

```py
foods = ["tuna", "salmon", "mackerel", "trout"]

print(foods[1:])
```
This works very similarly to the first example, a single slice is made to our list except the slice is not made at index number 1. This means that our output will be: 

```py
['salmon', 'mackerel', 'trout']
```

NEED TO FINISH

#### Looping Through a Slice

You can use a slice in a for loop if you want to loop through a subset of the elements in a list. 

```py
foods = ["tuna", "salmon", "mackerel", "trout"]

print("Alright Weasley and Noche, this is what we can have for dinner: ")
for food in foods[0:4]:
    print(food.title())
```

Another example: 

```py
plants = ['hawthoria', 'palm', 'pothos', 'barrel cactus', 'prayer plant']
print("Here are my favorite plants out of my list:")
for plant in plants[0:4]:
    print(plant.title())
```

NEED TO FINISH

#### Copying a List

To copy a list, you can make a slice that includes the entire original list by omitting the first index and the second index ([:]). This tells Python to make a slice that starts at the first item and ends with the last item, producing a copy of the entire list. 

```py
weasley_foods = ["tuna", "salmon", "mackerel", "trout"]
noche_foods = weasley_foods[:]

weasley_foods.append('chicken')
noche_foods.append('cheese')

print("The foods Weasley likes to eat is: ")
print(weasley_foods)

print("The foods Noche likes to eat is: ")
print(noche_foods)
```

#### Tuples

A tuple looks just like a list except you use parentheses instead of square brackets.

The reason why you use this - if you want to list things out but not change it. Think about a permanent menu option that you always want to keep up. 

Tuples are known as the immutable lists, or a list that cannot change. 

```py
#a simple tuple
foods = ("tuna", "salmon", "mackerel", "trout")
print(foods)
```

```py
#a simple tuple; accessing element
foods = ("tuna", "salmon", "mackerel", "trout")
print(foods)
print(foods[2])
```

Another example: 

```py
#defining a simple tuple
plants = ('cacti', 'pothos', 'eucalyptus')
print(plants)
```

```py
#accessing an element in a tuple is the same as accessing one in a list
plants = ('cacti', 'pothos', 'eucalyptus')
print(plants[0])
```


#### Redefining a Tuple

Although you cannot change the elements in a tuple, you can assign a new value to a variable that represents a tuple.
Use them if you do not want the values to changes throughout the life of a program. 

```py
plants = ('cacti', 'pothos', 'eucalyptus')
for plant in plants:
    print(plant)

plants = ('palm', 'tree', 'lily pad')
for plant in plants:
    print(plant)
   
print(plants)
```

### Back to our code from the start!

Try running the code to see how it works. Then, modify this code to make it your own! 

```py
foods = ["tuna", "salmon", "mackerel", "trout"]

print("Okay Weasley, you can eat any of the following for dinner:")

for food in foods:
    print("You can have " + food + " for dinner. ")
    print("or....")
   
print("Nothing!")
```

### Well done! Now move onto the Working with Lists Exercises!
