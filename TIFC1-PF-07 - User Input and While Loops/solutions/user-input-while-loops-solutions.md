# Exercise 7: User Input and While Loops Solutions

Please work through as many of the following exercises as you’re able to in the allotted time and upload the results of the last task you were able to complete.

### 1.
Write a program that asks the user what kind of rental car they would like. Print a message about that car, such as “Let me see if I can find you a Subaru.”

```py
# Ask the user for their preferred rental car
car_preference = input("What kind of rental car would you like? ")

# Print a message about the chosen car
print("Let me see if I can find you a " + car_preference + ".")
```

### 2.
Write a program that asks the user how many people are in their dinner group. If the answer is more than eight, print a message saying they’ll have to wait for a table. Otherwise, report that their table is ready.

```py
# Ask the user for the number of people in their dinner group
number_of_people = int(input("How many people are in your dinner group? "))

# Print a message based on the number of people
if number_of_people > 8:
    print("You'll have to wait for a table.")
else:
    print("Your table is ready.")
```

### 3.
Ask the user for a number, and then report whether the number is a multiple of 10 or not.

```py
# Ask the user for a number
number = int(input("Enter a number: "))

# Check if the number is a multiple of 10
if number % 10 == 0:
    print(f"{number} is a multiple of 10.")
else:
    print(f"{number} is not a multiple of 10.")
```

### 4.
Write a loop that prompts the user to enter a series of pizza toppings until they enter a 'quit' value. As they enter each topping, print a message saying you’ll add that topping to their pizza.

```py
# Loop to prompt user for pizza toppings
while True:
    # Ask the user for a pizza topping
    topping = input("Enter a pizza topping (or 'quit' to finish): ").strip().lower()
    
    # Check if the user wants to quit
    if topping == 'quit':
        print("Finished adding toppings.")
        break
    else:
        print(f"I'll add {topping} to your pizza.")
```

### 5.
A movie theater charges different ticket prices depending on a person’s age. If a person is under the age of 3, the ticket is free; if they are between 3 and 12, the ticket is $10; and if they are over age 12, the ticket is $15. Write a loop in which you ask users their age, and then tell them the cost of their movie ticket.

```py
while True:
    # Ask the user for their age
    age = input("Enter your age (or 'quit' to exit): ")
    
    # Check if the user wants to quit
    if age == 'quit':
        print("Goodbye!")
        break
    
    # Convert age to an integer
    try:
        age = int(age)
        
        # Determine the ticket price based on age
        if age < 3:
            ticket_price = 0
        elif 3 <= age <= 12:
            ticket_price = 10
        else:
            ticket_price = 15
        
        print(f"The cost of your ticket is ${ticket_price}.")
    
    except ValueError:
        print("Please enter a valid age or 'quit' to exit.")
```

### 6.
Write a loop that never ends, and run it (if you dare!). (To end the loop, press ctrl-C or close the window displaying the output.)

```py
while True:
    print("This loop will run forever. Press Ctrl-C to stop.")
```

## Stretch and Challenge
If you complete the previous steps within the allotted time please move on to the following.

### 7.
Make a list called sandwich_orders and fill it with the names of various sandwiches. Then make an empty list called finished_sandwiches. Loop through the list of sandwich orders and print a message for each order, such as I made your tuna sandwich. As each sandwich is made, move it to the list of finished sandwiches. After all the sandwiches have been made, print a message listing each sandwich that was made.

-	Using the list sandwich_orders from Exercise 7-8, make sure the sandwich 'pastrami' appears in the list at least three times. Add code near the beginning of your program to print a message saying the deli has run out of pastrami, and then use a while loop to remove all occurrences of 'pastrami' from sandwich_orders. Make sure no pastrami sandwiches end up in finished_sandwiches.

```py
# List of sandwich orders with 'pastrami' appearing multiple times
sandwich_orders = ['tuna', 'pastrami', 'veggie', 'pastrami', 'chicken', 'pastrami', 'ham']

# Empty list for finished sandwiches
finished_sandwiches = []

# Print a message that the deli has run out of pastrami
print("The deli has run out of pastrami.")

# Remove all occurrences of 'pastrami' from sandwich_orders
while 'pastrami' in sandwich_orders:
    sandwich_orders.remove('pastrami')

# Process the remaining sandwich orders
while sandwich_orders:
    # Take the first sandwich from the orders
    sandwich = sandwich_orders.pop(0)
    # Print a message about making the sandwich
    print(f"I made your {sandwich} sandwich.")
    # Add the sandwich to the finished list
    finished_sandwiches.append(sandwich)

# Print a message listing each sandwich that was made
print("\nThe following sandwiches have been made:")
for sandwich in finished_sandwiches:
    print(f"- {sandwich}")
```

### 8.
Write a program that polls users about their dream vacation. Write a prompt similar to If you could visit one place in the world, where would you go? Include a block of code that prints the results of the poll.

```py
# List to store responses
responses = []

# Poll users for their dream vacation destination
while True:
    # Ask the user where they would go for their dream vacation
    response = input("If you could visit one place in the world, where would you go? ")
    
    # Add the response to the list
    responses.append(response)
    
    # Ask if they want to continue polling
    continue_polling = input("Would you like to add another response? (yes/no) ").strip().lower()
    
    # Check if the user wants to stop polling
    if continue_polling == 'no':
        break
    else:
        print("Great! Let's add another response.")

# Print the results of the poll
print("\nPoll Results:")
for response in responses:
    print(f"- {response}")
```
