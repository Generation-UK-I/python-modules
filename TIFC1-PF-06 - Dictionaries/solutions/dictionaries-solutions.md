# Exercise 6: Dictionaries
Please work through as many of the following exercises as you’re able to in the allotted time and upload the results of the last task you were able to complete.

### 1.
Use a dictionary to store information about a person you know. Store their first name, last name, age, and the city in which they live. You should have keys such as first_name, last_name, age, and city. Print each piece of information stored in your dictionary.

```py
# Dictionary storing information about a person
person = {
    'first_name': 'John',
    'last_name': 'Doe',
    'age': 30,
    'city': 'New York'
}

# Print each piece of information
print("First name: " + person['first_name'])
print("Last name: " + person['last_name'])
print("Age: " + str(person['age']))
print("City: " + person['city'])
```

### 2.
Use a dictionary to store people’s favorite numbers. Think of five names, and use them as keys in your dictionary. Think of a favorite number for each person, and store each as a value in your dictionary. Print each person’s name and their favorite number. For even more fun, poll a few friends and get some actual data for your program.

```py
# Dictionary storing people's favorite numbers
favorite_numbers = {
    'Alice': 7,
    'Bob': 13,
    'Charlie': 22,
    'Diana': 5,
    'Eve': 9
}

# Print each person's name and their favorite number
for name, number in favorite_numbers.items():
    print(name + "'s favorite number is " + str(number) + ".")
```

### 3.
Make a dictionary containing three major rivers and the country each river runs through. One key-value pair might be 'nile': 'egypt'. 

- Use a loop to print a sentence about each river, such as The Nile runs through Egypt. 
- Use a loop to print the name of each river included in the dictionary. 
- Use a loop to print the name of each country included in the dictionary

```py
# Dictionary containing rivers and the countries they run through
rivers = {
    'nile': 'egypt',
    'amazon': 'brazil',
    'yangtze': 'china'
}

# Loop to print a sentence about each river
for river, country in rivers.items():
    print("The " + river.title() + " runs through " + country.title() + ".")

# Loop to print the name of each river
print("\nRivers included:")
for river in rivers.keys():
    print(river.title())

# Loop to print the name of each country
print("\nCountries included:")
for country in rivers.values():
    print(country.title())
```

### 4.
Make several dictionaries, where the name of each dictionary is the name of a pet. In each dictionary, include the kind of animal and the owner’s name. Store these dictionaries in a list called pets. Next, loop through your list and as you do print everything you know about each pet.

```py
# Dictionaries for each pet
weasley = {'animal': 'cat', 'owner': 'jessica'}
noche = {'animal': 'cat', 'owner': 'jessica'}

# List of pets
pets = [weasley, noche]

# Loop through the list and print information about each pet
for pet in pets:
    print("This is a " + pet['animal'] + " and the owner is " + pet['owner'].title() + ".")
```

### 5.
Make a dictionary called favorite_places. Think of three names to use as keys in the dictionary, and store one to three favorite places for each person. To make this exercise a bit more interesting, ask some friends to name a few of their favorite places. Loop through the dictionary, and print each person’s name and their favorite places.

```py
# Dictionary containing favorite places
favorite_places = {
    'Alice': ['Paris', 'London', 'New York'],
    'Bob': ['Tokyo', 'Sydney'],
    'Charlie': ['Rome', 'Barcelona', 'Berlin']
}

# Loop through the dictionary and print each person's name and their favorite places
for person, places in favorite_places.items():
    print(person + "'s favorite places are:")
    for place in places:
        print("- " + place)
    print()  # Print a blank line for better readability
```

### 6.
Make a dictionary called cities. Use the names of three cities as keys in your dictionary. Create a dictionary of information about each city and include the country that the city is in, its approximate population, and one fact about that city. The keys for each city’s dictionary should be something like country, population, and fact. Print the name of each city and all of the information you have stored about it.

```py
# Dictionary containing information about cities
cities = {
    'Paris': {
        'country': 'France',
        'population': 2148000,
        'fact': 'Paris is known as the City of Light.'
    },
    'Tokyo': {
        'country': 'Japan',
        'population': 13929286,
        'fact': 'Tokyo is the most populous city in the world.'
    },
    'New York': {
        'country': 'USA',
        'population': 8419000,
        'fact': 'New York City is known as the Big Apple.'
    }
}

# Loop through the dictionary and print each city and its information
for city, info in cities.items():
    print(f"City: {city}")
    print(f"  Country: {info['country']}")
    print(f"  Population: {info['population']}")
    print(f"  Fact: {info['fact']}")
    print()  # Print a blank line for better readability
```

## Stretch and Challenge
If you complete the previous steps within the allotted time please move on to the following.

- A Python dictionary can be used to model an actual dictionary. However, to avoid confusion, let’s call it a glossary. 

- Think of five programming words you’ve learned about in the previous chapters. Use these words as the keys in your glossary, and store their meanings as values. 

- Print each word and its meaning as neatly formatted output. You might print the word followed by a colon and then its meaning, or print the word on one line and then print its meaning indented on a second line. Use the newline character (\n) to insert a blank line between each word-meaning pair in your output.

- We’re now working with examples that are complex enough that they can be extended in any number of ways. Use one of the example programs from this chapter, and extend it by adding new keys and values, changing the context of the program or improving the formatting of the output.
