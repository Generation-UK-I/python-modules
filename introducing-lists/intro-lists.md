# Introducing Lists
---

## Learning Objectives

- Explain what a Python list is and why they’re used
- Be able to create a list and populate it with elements
- Add, remove, and modify items in a list
- Apply a number of methods to manipulate or summarise lists

---

## I Also Have Another Cat Named Weasley...

<img src="img/happy_weasley.jpg" width="300" />

Weasley's favorite time of day is also dinner time! Weasley's dinner time problems will help us with learning lists. 

Don't worry, Noche will come back too 

## Take a Look...

```py
foods = ["tuna", "salmon", "mackerel", "trout"]

print("Okay Weasley, you can eat any of the following for dinner:")
print(f"You can eat {foods[0]} for dinner.")
print(f"You can eat {foods[1]} for dinner.")
print(f"You can eat {foods[2]} for dinner.")
print(f"You can eat {foods[3]} for dinner.")
```
What would happen if I ran this code? As we go through this lesson, we will be breaking down the concepts shown in this piece of code. 

## Lists

Well, what is it? A list is one way of storing multiple pieces of data in a single variable. A list is a collection of items in a particular order. You can make a list that includes the letters of the alphabet, the digits from 0–9, or the names of all the people in your family (for me, my cats). In Python, square brackets `[ ]` indicate a list, and individual elements in the list are separated by commas. Here is an example of a simple list:

```py
#this is an example of a list
foods = ['tuna', 'chicken', 'beef', 'salmon']

print(foods)
```

Take a look at our code from the start of this lesson: 
```py
foods = ["tuna", "salmon", "mackerel", "trout"]

print("Okay Weasley, you can eat any of the following for dinner:")
print(f"You can eat {foods[0]} for dinner.")
print(f"You can eat {foods[1]} for dinner.")
print(f"You can eat {foods[2]} for dinner.")
print(f"You can eat {foods[3]} for dinner.")
```

You can see here that where our list is located and that it is encased in square brackets. But what does the rest of the code do?

## Accessing Elements Within a List

Lists are ordered collections, so you can access any element in a list by telling Python the position, or index, of the item desired. To access an element in a list, write the name of the list followed by the index of the item enclosed in square brackets, known as the index number. What is meant by 'index position'? In Python when we create a list hold items like numbers or words, each item in the list gets a number to show its position within the list. This number is called an "index." If you were asked to determine each index for the items in the following list, what would you say?

```py
foods = ["tuna", "salmon", "mackerel", "trout"]
```
One might think that tuna = `1`, salmon = `2`, mackerel = `3`, trout = `4`... However, in Python (and many other programming languages) this is not the case. Python follows a zero-based indexing convention, which means that that start of a list will be `0`, rather than `1` like one might think of when counting things in everyday life. So: tuna = `0`, salmon = `1`, mackerel = `2`, trout = `3`. 

STOP AND RUN: Try the following code and change the numbers in the brackets. You will see you can access different elements within a list!

```py
#this is an example of accessing items in a list
foods = ["tuna", "salmon", "mackerel", "trout"]

print(foods[0])

```
FYI: The index positions start at 0, not 1* You can use negative numbers to access items in a list from the opposite direction - This means that [-1] will always retrieve the last item, even if you don’t know the length of the list. This is an important point which will pop up often in the future. Give it a try in the above code to see how this works!

Going back to our code from the start...
```py
foods = ["tuna", "salmon", "mackerel", "trout"]

print("Okay Weasley, you can eat any of the following for dinner:")
print(f"You can eat {foods[0]} for dinner.")
print(f"You can eat {foods[1]} for dinner.")
print(f"You can eat {foods[2]} for dinner.")
print(f"You can eat {foods[3]} for dinner.")
```
you can see how lines 4-7 accesses different elements within my list of foods! 

Make sure to avoid index errors in a list. Index errors can occur if you try to access an index that does not exist. Look at the following example: 

```py
#this is an example of an index error
foods = ['tuna', 'salmon', 'mackerel', 'trout']
print(foods[4])
```
You should see from this code that an index error has occurred. Can you fix this?

This is great, but what if I ran out of one of the items in the list? Is there a way I can modify or delete an item? What about add any additional items?

## Changing/Modifying Elements in a List

The syntax for modifying an element is similar to the syntax for accessing an element in a list. To change an element, use the name of the list followed by the index of the element you want to change, and then provide the new value you want that item to have.
Here is a simple example: 
```py
#a simple example of how to modify an element in a list
foods = ["tuna", "salmon", "mackerel", "trout"]
print(foods)

foods[0] = 'chicken'
print(foods)
```

Here is another example, but a little more complex:

```py
#this is an example of modifying items in a list
#remember, you can change the value of any item in a list, not just the first item
foods = ["tuna", "salmon", "mackerel", "trout"]

print(f"Would you like to eat {foods[1]} today, Noche?")

foods[0] = "chicken"
print(foods)

```
STOP AND CODE: Try changing the numbers to access different elements within the list. Remember, you can change the value of any item in a list, not just the first item!

## Adding Elements to a List

Use `.append()` to add an item to the end of the list, it will not affect any of the other items. 

```py
#this is an example of adding items to a list
foods = ["tuna", "salmon", "mackerel", "trout"]

print(foods)

foods.append('chicken')
print(foods)

```

You can even take it a step further and make this piece of code more interactive by adding user input!

```py
#this is an example of adding items to a list with user input
foods = ["tuna", "salmon", "mackerel", "trout"]

print(foods)

foods.append(input("Add another food item: "))
print(foods)
```

## Inserting Elements into a List

`.append()` always adds to the end of a list. What if you want to insert elements in the middle of a list? What about the start of a list? You can do this using `.insert()` and knowing what index position you want to insert the new element into the list. 

STOP AND RUN: Take a look at the following code and think about the syntax for inserting elements into a list. We start by choosing the list we want to insert a new item into followed by `.insert()`. Within the `.insert()` brackets, insert the index position you want to place the new item into and the item you want to place.  Try running the following code to see how it works:

```py
#this is an example of inserting items anywhere to a list
foods = ["tuna", "salmon", "mackerel", "trout"]

print(foods)

foods.insert(1, 'chicken')
print(foods)
```
Try changing the index number to see how 'chicken' can be placed into different positions. You can also try using negative numbers too!

## Removing an Item in a List

There are a few ways to be able to remove an item from a list. You can use:
- `.pop()` - remove the last item
- `del` - remove an item by index number
- `.remove()` - remove an item by value 

Below you will see some example of each: 

## Del Statements

If you know the position of the element you wish to delete from a list, you can use the `del` statement. However, after you use the `del` statement you can no longer access that element in the list for the rest of the code!

```py
#this is an example of using the del statement
foods = ["tuna", "salmon", "mackerel", "trout"]
print(foods)

del foods[1]
print(foods)
```

## The .pop() Method

You can also use the `.pop()` method to remove an item from a list. This will remove the last item in your list, but also lets you continue working with that item after removing it. Think of this like a stack of books - you take (or pop!) one book off the stack and start reading it, when done you may put it somewhere else, or discard it.

By default the `.pop()` method removes the last item, or an item from any position if you know the index number of the element to remove: 

```py
#this is an example of using the pop() method in default mode
foods = ["tuna", "salmon", "mackerel", "trout"]
print(foods)

popped_food = foods.pop() #storing the food that was popped into the variable popped_food
print(foods)
print(popped_food) #notice here you can still access the element that was popped!
```

```py
#this is an example of using the pop() method
#This will show how to remove an item from a specified position
foods = ["tuna", "salmon", "mackerel", "trout"]
print(foods)

popped_food = foods.pop(1)
print(f"Sorry Noche, we do not have {popped_food} anymore!")
print(foods)
```

## The remove() Method
If you do not know the position of the element you wish to remove from a list, only the value, then use the `.remove()` method. 

```py
#this is an example of using the remove() method
foods = ["tuna", "salmon", "mackerel", "trout"]
print(foods)

foods.remove('mackerel')
print(foods)
```
Try changing the 'mackerel' to other items in the list to remove them!

A more advanced use case of `.remove()`:

```py
#this is an example of using the remove() method
#this shows that I can still use removed elements from a list
foods = ["tuna", "salmon", "mackerel", "trout"]
print(foods)

removed_food = "mackerel" #assigning value to remove to a variable
foods.remove(removed_food) #telling Python this is the value we want to remove
print(removed_food) #showing that the value is removed, but also still accessible through new variable
print(foods) #showing the value is no longer apart of the list

print(f"Sorry Noche, we do not have {removed_food} anymore.") #we can still use the removed value from the new stored variable
```

We have learned how to modify, delete, and update a list… But can I organize a list?

## The sort() Method

If you want to sort list permanently, use the `.sort()` method!

```py
#this is an example of using the sort() method
foods = ["tuna", "salmon", "mackerel", "trout"]
print(foods)
foods.sort()
print(foods)
```

## The sorted() function

To sort a list temporarily, use the `sorted()` function.

```py
#Example of using the sorted() function
foods = ["tuna", "salmon", "mackerel", "trout"]
print(foods)

print(sorted(foods))

print(foods)
```

## reverse()

To print a list in reverse order, use `.reverse()`

```py
#this is an example of printing a list in reverse order
foods = ["tuna", "salmon", "mackerel", "trout"]
print(foods)

foods.reverse()
print(foods)
```

## len()

If you would like to find the length of a list, use `len()`.

```py
foods = ["tuna", "salmon", "mackerel", "trout"]
print(foods)
print(len(foods))
```

## Now That You Know It All... Try Modifying the Following Code to Make it Your Own! When you are done, post your code into your chat channel!

STOP AND CODE: Feel free to make this piece of code your own - whether you want to keep it simple or improve on it! Remember this is just practice, and is supposed to be fun! Good luck. 

```py
foods = ["tuna", "salmon", "mackerel", "trout"]

print("Okay Weasley, you can eat any of the following for dinner:")
print(f"You can eat {foods[0]} for dinner.")
print(f"You can eat {foods[1]} for dinner.")
print(f"You can eat {foods[2]} for dinner.")
print(f"You can eat {foods[3]} for dinner.")
```

## Next up… Exercise 2: Introducing Lists!
