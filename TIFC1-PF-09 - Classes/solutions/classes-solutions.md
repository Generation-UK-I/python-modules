# Exercise 9: Classes

Please work through as many of the following exercises as you’re able to in the allotted time and upload the results of the last task you were able to complete

### 1.
Make a class called, “Restaurant”. The `__init__()` method for Restaurant should store two attributes: `Restaurant_name` & `Cuisine_type`.

- Make a method called `describe_restaurant()` that prints these two pieces of information, and a method called `open_restaurant()` that prints a message indicating that the restaurant is open.
- Make an instance called, `restaurant1` from your class. Print the two attributes individually, and then call both methods.
- Create three different instances from the class with different names, and call `describe_restaurant()` for each instance.
- Add an attribute called `number_served` with a default value of `0`, create an instance called `restaurant2`. Print the number of customers the restaurant has served, and then update this value and print it again. 
- Add a method called set_number_served() that lets you update the `number_served` attribute. Call this method with a new number and print the value to confirm the change. 
- Add a method called `increment_number_served()` that lets you increment `number_served`. Call this method with a number representing how many customers were served in a day of business.

```py
class Restaurant:
    def __init__(self, restaurant_name, cuisine_type):
        self.restaurant_name = restaurant_name
        self.cuisine_type = cuisine_type
        self.number_served = 0

    def describe_restaurant(self):
        print(f"Restaurant Name: {self.restaurant_name}")
        print(f"Cuisine Type: {self.cuisine_type}")

    def open_restaurant(self):
        print(f"{self.restaurant_name} is open!")

    def set_number_served(self, number):
        self.number_served = number

    def increment_number_served(self, increment):
        self.number_served += increment

# Creating an instance of Restaurant
restaurant = Restaurant("Food Haven", "Italian")

# Printing individual attributes
print("Restaurant Name:", restaurant.restaurant_name)
print("Cuisine Type:", restaurant.cuisine_type)

# Calling methods
restaurant.describe_restaurant()
restaurant.open_restaurant()

# Stretch and Challenge
restaurant1 = Restaurant("Taste of India", "Indian")
restaurant2 = Restaurant("Sushi Palace", "Japanese")
restaurant3 = Restaurant("Mexican Fiesta", "Mexican")

restaurants = [restaurant1, restaurant2, restaurant3]
for res in restaurants:
    res.describe_restaurant()
```

### 2.
Make a class called `User` and give it two attributes called `first_name` and `last_name`. Create several other attributes that are typically stored in a user profile. 
- Make a method called `describe_user()` that prints a summary of the user’s information. 
- Make a method called `greet_user()` that prints a personalized greeting.
- Create several instances representing different users, and call both methods for each user.

**Advanced**: Add an attribute called `login_attempts` to your User class. 
- Write a method called `increment_ login_attempts()` that increments the value of login_attempts by 1. 
- Write another method called `reset_login_attempts()` that resets the value of `login_attempts` to 0. 
- Make an instance of the User class and call `increment_login_attempts()` several times. Print the value of login_attempts to make sure it was incremented properly, and then call `reset_login_attempts()`. Print `login_attempts` again to make sure it was reset to 0.
**Consider**: Although the full implementation would be very complex, consider how this functionality might be incorporated into a real user-management app.

```py
class User:
    def __init__(self, first_name, last_name, email, age):
        self.first_name = first_name
        self.last_name = last_name
        self.email = email
        self.age = age
        self.login_attempts = 0

    def describe_user(self):
        print(f"First Name: {self.first_name}")
        print(f"Last Name: {self.last_name}")
        print(f"Email: {self.email}")
        print(f"Age: {self.age}")

    def greet_user(self):
        print(f"Hello, {self.first_name} {self.last_name}!")

    def increment_login_attempts(self):
        self.login_attempts += 1

    def reset_login_attempts(self):
        self.login_attempts = 0

# Creating instances of User
user1 = User("John", "Doe", "john@example.com", 30)
user2 = User("Alice", "Smith", "alice@example.com", 25)

# Calling methods
user1.describe_user()
user1.greet_user()

user2.describe_user()
user2.greet_user()

# Stretch and Challenge
user3 = User("Bob", "Johnson", "bob@example.com", 35)
user3.increment_login_attempts()
user3.increment_login_attempts()
user3.increment_login_attempts()
print("Login Attempts:", user3.login_attempts)

user3.reset_login_attempts()
print("Login Attempts Reset:", user3.login_attempts)
```

### 3.
Create a class called "Car" with attributes for make, model, and year. Implement a method called get_info() to print out the details of the car. Create instances representing different cars and call the get_info() method for each instance.
- Stretch and Challenge: Add an attribute called "mileage" to the Car class and implement methods to set and update the mileage of the car.

```py
class Car:
    def __init__(self, make, model, year):
        self.make = make
        self.model = model
        self.year = year
        self.mileage = 0


    def get_info(self):
        print(f"Car Details:")
        print(f"Make: {self.make}")
        print(f"Model: {self.model}")
        print(f"Year: {self.year}")
        print(f"Mileage: {self.mileage} miles")


    def update_mileage(self, mileage):
        self.mileage = mileage


# Creating instances of Car
car1 = Car("Toyota", "Camry", 2019)
car2 = Car("Honda", "Accord", 2020)


# Calling methods
car1.get_info()
car2.get_info()


# Stretch and Challenge
car1.update_mileage(15000)
car1.get_info()
```


### 4.
Define a class called "Book" with attributes for title, author, and genre. Implement a method called display_info() to print out the details of the book. Create instances representing different books and call the display_info() method for each instance.

**Advanced**: Add an attribute called "pages" to the Book class and implement methods to set and update the number of pages in the book.

```py
class Car:
    def __init__(self, make, model, year):
        self.make = make
        self.model = model
        self.year = year
        self.mileage = 0


    def get_info(self):
        print(f"Car Details:")
        print(f"Make: {self.make}")
        print(f"Model: {self.model}")
        print(f"Year: {self.year}")
        print(f"Mileage: {self.mileage} miles")


    def update_mileage(self, mileage):
        self.mileage = mileage


# Creating instances of Car
car1 = Car("Toyota", "Camry", 2019)
car2 = Car("Honda", "Accord", 2020)


# Calling methods
car1.get_info()
car2.get_info()


# Stretch and Challenge
car1.update_mileage(15000)
car1.get_info()
```

### 5.
Create a class called "BankAccount" with attributes for account number, account holder, and balance. Implement methods for depositing and withdrawing money from the account, as well as checking the balance. Create instances representing different bank accounts and perform transactions on them.

**Advanced**: Add an attribute called "interest_rate" to the BankAccount class and implement methods to calculate and apply interest to the account balance.

```py
class BankAccount:
    def __init__(self, account_number, account_holder, balance):
        self.account_number = account_number
        self.account_holder = account_holder
        self.balance = balance
        self.interest_rate = 0.05

    def deposit(self, amount):
        self.balance += amount

    def withdraw(self, amount):
        if amount <= self.balance:
            self.balance -= amount
        else:
            print("Insufficient funds")

    def check_balance(self):
        print(f"Account Balance: ${self.balance}")

    def apply_interest(self):
        interest_amount = self.balance * self.interest_rate
        self.balance += interest_amount

# Creating instances of BankAccount
account1 = BankAccount("123456789", "John Doe", 1000)
account2 = BankAccount("987654321", "Alice Smith", 2000)

# Performing transactions
account1.deposit(500)
account1.withdraw(200)
account1.check_balance()

# Stretch and Challenge
account1.apply_interest()
account1.check_balance()
```
