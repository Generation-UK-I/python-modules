# Files and Exceptions
---

## Learning Objectives

- To learn how to store, modify, and access data in a text file from python program.
- Recap and Recall different file paths
- Understand exceptions and error handling

---

## I have a problem…

I have too many dinner items for weasley and noche! This makes my code longer and harder to work with, and difficult to change.

To solve my problem, I could store my data in a text file:

<img src="img/text_file.jpg" width="300" />

Then I can access the contents through my code, like a simple database. 

The example below reads from an entire text file. 

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

Python will look for this file in the directory where the program that’s currently being executed is stored, which is fine if you save both .py and .txt files in the same directory. You could also provide an absolute or relative path to the file if it's saved elsewhere.

### The read() method



