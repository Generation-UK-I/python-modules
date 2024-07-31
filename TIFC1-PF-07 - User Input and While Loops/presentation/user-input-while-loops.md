# User Input and While Loops
---

## Learning Objectives

- To understand the purpose of while loops and when it can be helpful
- To understand the use case of the input() function 
- To be able to use continue, break, and flags within a while loop

---

## Recap and Recall

Make sure you remember: Python interprets everything the user inputs as a string!
`int()` function = tells Python to treat the input as a numerical value, not as a string. 

```py
age = input("How old are you? ")

if int(age) <= 18:
    print("You are too young to play!")
else:
    print("You are allowed to play, you are old.")
```
---
## Take a Look at the Code... What Would Happen if it were to run?

```py
prompt = "Hello Weasley and Noche! What would you like to eat today?"
prompt += "\nThis is what we have: tuna, chicken, salmon, and clams. Type 'done' when you are finished! \n"

while True:
    answer = input(prompt)
    if answer.lower() == 'tuna':
        print("That sounds great! I will make tuna for you now.")
    elif answer.lower() == 'chicken':
        print("I am surprised you chose chicken!")
    elif answer.lower() == 'salmon':
        print("Salmon is so special, yum!")
    elif answer.lower() == 'clams':
        print("Wow! Fancy clams!")
    elif answer.lower() == 'done':
        break
    else:
        print("Sorry! We do not have that.")

```
## `input()` Function 

The input() function pauses your program and waits for the user to enter some text. Once Python receives the user’s input, it stores it in a variable to make it convenient for you to work with.
Make sure you are very clear on what you want the user to answer. 

```py
answer = input("What would you like to eat today Noche? ")

print("Great! We will have " + answer.lower() + " today!")
```

```py
#Multi line strings example
prompt = "Today we are going to learn about user input and while loops..."
prompt += "Are you excited? "

answer = input(prompt)
print(f"You answered: {answer}!")
```
---

## While Loops

The while loop runs as long as, or while, a certain condition is true.
```py
current_number = 1

while current_number <= 5:
    print(current_number)
    current_number += 1
```

## Letting a User Choose When to Quit

To allow a  user to quit, you will need to assign a quit value.

```py
prompt = "\nTell me something, and I will repeat it back to you:"
prompt += "\nEnter 'quit' to end the program. "
message = ""

while message != 'quit':
    message = input(prompt)
    print(message)
```

## Flags

For a program that should run only as long as many conditions are true, you can define one variable that determines whether or not the entire program is active. This variable, called a flag, acts as a signal to the program.
For example….

### Break Statements
```py
while True:
    print("Menu: fruit, tacos, walnuts, bacon. \n type exit to leave")
    message = input("What would you like to eat today?")
    if message.lower() == 'fruit':
        print("yum")
    elif message.lower() == 'tacos':
        print("my favorite!")
    elif message.lower() == 'walnuts':
        print("It is the holidays!")
    elif message.lower() == 'bacon':
        print("I am vegetarian!")  
    else:
        break
```

### Continue Statements

Using continue is just a ‘skip’ over to the next option in the loop.

```py
#This is an example of using continue in a for loop
for letter in 'Noche':     
   if letter == 'h':
      continue
   print('Current Letter :', letter)
```

### Make sure you add a break in your while loops! Otherwise you could be stuck in an INFINITE LOOP!

### Infinite loop example… CAUTION!

```py
#infinite loop... BE WARNED!
prompt = "What would you like to eat today?"

while True:
    answer = input(prompt)
    print("yum! Sounds good!")
```

## Back to Our Original Code!

```py
prompt = "Hello Weasley and Noche! What would you like to eat today?"
prompt += "\nThis is what we have: tuna, chicken, salmon, and clams. Type 'done' when you are finished! \n"

while True:
    answer = input(prompt)
    if answer.lower() == 'tuna':
        print("That sounds great! I will make tuna for you now.")
    elif answer.lower() == 'chicken':
        print("I am surprised you chose chicken!")
    elif answer.lower() == 'salmon':
        print("Salmon is so special, yum!")
    elif answer.lower() == 'clams':
        print("Wow! Fancy clams!")
    elif answer.lower() == 'done':
        break
    else:
        print("Sorry! We do not have that.")
```
