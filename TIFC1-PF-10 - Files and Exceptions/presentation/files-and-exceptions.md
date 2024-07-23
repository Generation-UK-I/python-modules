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






