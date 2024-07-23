# Files and Exceptions
---

## Learning Objectives

- To learn how to store, modify, and access data in a text file from python program.
- Recap and Recall different file paths
- Understand exceptions and error handling

## I have a problem…  

I have too many dinner items for weasley and noche! This makes my code longer and harder to work with, and difficult to change.  

To solve my problem, I could store my data in a text file:  

<img src="img/text_file.jpg" width="300" />

Then I can access the contents through my code, like a simple database.  

The example below reads and prints the entire text file:  

```py
with open('foods.txt') as file_object:
    contents = file_object.read()
    print(contents)
```

There is a lot going on here though so let’s break it down.

---

### The open() function

```py
with open('foods.txt') as file_object:
```

To do anything with a file, you first need to open it, even if it is something as simple as printing the contents.

The `open()` function only requires one argument - what you want to open!

In our case, whatever is inside the text file can be referenced by a variable called `file_object` this allows us to work with the file in our code, without opening it over and over again.

Python will look for the file in the directory where the program that’s currently being executed is stored, which is fine if you save both .py and .txt files in the same directory.

### The read() method

```py
contents = file_object.read()
```

The `read()` method is exactly what it sounds like, it allows us to read the data in our file. 

To clarify, `open()` gives your code access to the file, but once we have access to it there could be various things we want to do, so far we're just using `read()` to view the file contents.

#### What if I want to store my text file in another directory?  

A ***relative*** file path tells Python to look for a given location relative to the directory where the currently running program file is stored. Just like in Linux! 

Depending on the OS, you will need to change the slashes!

<img src="img/rel_path_lin_vs_win.jpg" width="700" />

This can be particularly useful as your application grows and contains many different files, and you need to organise and structure your resources.

***Absolute*** paths allow you to tell Python the exact path to get to your file, from the root of the file system, so it doesn't matter where your file is stored. 

<img src="img/absolute_path.jpg" width="700" />

---

### Some More File Methods



#### Read a File Line by Line:

```py
with open('foods.txt') as file_object:
    for line in file_object:
        print(line)
```

Notice we're using a for loop to iterate through each `line` in the `file_object` until all of the lines have been printed.

#### Making a List From a File

```py
with open('foods.txt') as file_object:
    lines = file_object.readlines()

for line in lines:
    print(line)
```

When you use `with`, the file content returned by `open()` is only available inside the ‘with-block’. If you want to have access to the content outside of the with-block, you can store it in a list then work with this list in the rest of the program. 

#### Writing to an Empty File

```py
filename = 'foods.txt'

with open(filename, 'w') as file_object:
    file_object.write("I love programming!")
    file_object.write("Noche and Weasley are hungry!")
```

Here we've put the name of the file into a variable, then we `open()` the file in ***write*** mode by using the `'w'` flag. Again it's opened as `file_object`, and we write two strings to the file using the `write()` method.

***Note:*** *If the file exists any content will be overwritten; If it doesn't exist it will be created.*

---

## Exceptions
