# Dictionaries

## Learning Objectives

- What are dictionaries in Python?
- What are Key Value Pairs?
- How can KVPs be used to model objects?
- How are dictionaries declared and used?

## Introducing Dictionaries

Dictionaries are containers for collections of key value pairs. 

A key value pair (KVP) is just a set of values that are associated with each other. Dictionaries can store an almost limitless amount of pairs.

Although the syntax is a little trickier, dictionaries are quite similar to lists, except each item has two components, the key and value. We can add, remove, edit, and retrieve keys, values, or both. We can also loop through our dictionaries just like lists. 

We declare dictonaries using curly brackets {}

### The Return of Weasley, Noche, and... Mr. Bigglesworth?

We've already met Dumb and Dumber, but they also have a friend... some sort of uglier, wrinklier, house elf???

<img src="img/cat_trio.jpg" width="600" />

A common use of dictionaries is to represent real world objects, here is one representing Weasley.

```py
weasley = {'fur': 'white and ginger', 'eyes': 'yellow', 'toes': 'pink'}
```

It is common to write your dictionary across several lines for improved readability because the keys all line up.

```py
weasley = { 
    'fur': 'white and ginger',
    'eyes': 'yellow',
    'toes': 'pink'
    }
```
