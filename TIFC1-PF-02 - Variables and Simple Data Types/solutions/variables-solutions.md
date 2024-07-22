# Variables and Data Types Exercise Solutions

---

## Exercise 1

1. Store a name or message in a variable, then print that name or message.

Name example:

```py
first_name = "Jess"
print(first_name)
```

Message example:

```py
favorite_food = "My favorite food is tacos."
print(favorite_food)
```

2. Create two variables. one with your first name and the other with your last name. Then combine (or concatenate) both variables and print the result

```py
first_name = "Jess"
last_name = "Snead"
print(first_name + last_name)
```

3. Store a message in a variable, and print that message. Then change the value of your variable to a new message, and print the new message.

```py
favorite_food = "My favorite food is tacos."
print(favorite_food)

favorite_food = "My new favorite food is tamales."
print(favorite_food)
```
  
4. Store a person’s name in a variable, and print a message to that person.

```py
my_cat = "Noche"
print(my_cat + ", you will have tuna for dinner tonight.")
```

5. Store a person’s name in a variable, and then print that person’s name in lowercase, uppercase, and titlecase.

```py
name = "jess"
print(name.title())
print(name.lower())
print(name.upper())
```

6. Write addition, subtraction, multiplication, and division operations that each result in the number 8. Be sure to enclose your operations in print statements to see the results.

```py
addition = 4 + 4
subtraction = 10 - 2
multiplication = 4 * 2
division = 16 / 2

print(addition)
print(subtraction)
print(multiplication)
print(division)
```


7. Store your favorite number in a variable. Then, using that variable, create a message that reveals your favorite number. Print that message.

```py
favorite_num = 3
print("My favorite number is " + str(favorite_num))
```

---

## Stretch and Challenge 

- Use an f-string to print out a message with a variable.

```py
my_cat = "Noche"
print(f"my cat's name is {my_cat}")
```

- Use multiple variables in one string.

```py
first_cat = "Noche"
second_cat = "Weasley"
print(f"I have two cats, their names are {first_cat} and {second_cat}.")
```
