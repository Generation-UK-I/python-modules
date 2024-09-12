# Exercise 4: Working with Lists

Please work through as many of the following exercises as you’re able to in the allotted time and upload the results of the last task you were able to complete.

### 1.	
Think of at least three kinds of your favorite pizza. Store these pizza names in a list, and then use a for loop to print the name of each pizza. 

- Modify your for loop to print a sentence using the name of the pizza instead of printing just the name of the pizza. For each pizza you should have one line of output containing a simple statement like I like pepperoni pizza. 

- Add a line at the end of your program, outside the for loop, that states how much you like pizza. The output should consist of three or more lines about the kinds of pizza you like and then an additional sentence, such as I really love pizza!

```py
# Step 1: Create a list of your favorite pizzas
favorite_pizzas = ["pepperoni", "margherita", "bbq chicken"]

# Step 2: Use a for loop to print a sentence about each pizza
for pizza in favorite_pizzas:
    print(f"I really like {pizza} pizza.")

# Step 3: Add a statement at the end of the program expressing love for pizza
print("\nI just love pizza so much!")
print("Pizza is my favorite food ever.")
print("I could eat pizza every day!")
```

Ensure you don’t discard your code, you’ll come back to it later.

### 2.
Think of at least three different animals that have a common characteristic. Store the names of these animals in a list, and then use a for loop to print out the name of each animal. 

- Modify your program to print a statement about each animal, such as A dog would make a great pet. 

- Add a line at the end of your program stating what these animals have in common. You could print a sentence such as Any of these animals would make a great pet!

```py
# Step 1: Create a list of animals that share a common characteristic
animals = ["dog", "cat", "rabbit"]

# Step 2: Use a for loop to print a statement about each animal
for animal in animals:
    print(f"A {animal} would make a great pet.")

# Step 3: Add a statement about what the animals have in common
print("\nAny of these animals would make a great pet!")
```

### 3.
Use a for loop to print the numbers from 1 to 20, inclusive.

```py
# Use a for loop to print numbers from 1 to 20
for number in range(1, 21):
    print(number)
```

### 4.
Make a list of the numbers from one to one million, and then use min() and max() to make sure your list actually starts at one and ends at one million. Also, use the sum() function to see how quickly Python can add a million numbers.

```py
# Create a list of numbers from 1 to 1 million
numbers = list(range(1, 1000001))

# Use min() and max() to verify the list starts at 1 and ends at 1 million
print(f"Minimum number: {min(numbers)}")
print(f"Maximum number: {max(numbers)}")

# Use sum() to calculate the sum of all numbers from 1 to 1 million
print(f"Sum of all numbers: {sum(numbers)}")
```

### 5.
Make a list of the multiples of 3 from 3 to 30. Use a for loop to print the numbers in your list

```py
# Create a list of multiples of 3 from 3 to 30
multiples_of_three = list(range(3, 31, 3))

# Use a for loop to print each multiple of 3
for number in multiples_of_three:
    print(number)
```

## Stretch and Challenge

If you complete the previous steps within the allotted time please move on to the following.

### 6.
Start with your program from question 1. Make a copy of the list of pizzas, and call it friend_pizzas. Then, do the following: 

- Add a new pizza to the original list. 
- Add a different pizza to the list friend_pizzas. 
- Prove that you have two separate lists. Print the message, My favorite pizzas are:, and then use a for loop to print the first list. Print the message, My friend’s favorite pizzas are:, and then use a for loop to print the second list. Make sure each new pizza is stored in the appropriate list.

```py
# Original list of favorite pizzas
favorite_pizzas = ["pepperoni", "margherita", "bbq chicken"]

# Make a copy of the list and call it friend_pizzas
friend_pizzas = favorite_pizzas[:]

# Add a new pizza to the original list
favorite_pizzas.append("hawaiian")

# Add a different pizza to the friend_pizzas list
friend_pizzas.append("veggie")

# Prove that you have two separate lists by printing them

# Print the original list
print("My favorite pizzas are:")
for pizza in favorite_pizzas:
    print(pizza)

# Print the friend's list
print("\nMy friend's favorite pizzas are:")
for pizza in friend_pizzas:
    print(pizza)
```

### 7.
A buffet-style restaurant offers only five basic foods. Think of five simple foods, and store them in a tuple. 

- Use a for loop to print each food the restaurant offers. 
- Try to modify one of the items, and make sure that Python rejects the change. 
- The restaurant changes its menu, replacing two of the items with different foods. Add a block of code that rewrites the tuple, and then use a for loop to print each of the items on the revised menu

```py
# Step 1: Store five basic foods in a tuple
buffet_foods = ("pizza", "salad", "pasta", "soup", "bread")

# Step 2: Use a for loop to print each food the restaurant offers
print("Original menu:")
for food in buffet_foods:
    print(food)

# Step 3: Try to modify one of the items (this should raise an error)
# Uncommenting the following line will raise an error because tuples are immutable:
# buffet_foods[0] = "sushi"  # This line would cause a TypeError

# Step 4: The restaurant changes its menu by replacing two items
buffet_foods = ("pizza", "sushi", "pasta", "burger", "bread")

# Step 5: Use a for loop to print each item on the revised menu
print("\nRevised menu:")
for food in buffet_foods:
    print(food)
```
