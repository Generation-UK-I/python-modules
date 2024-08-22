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

### 3.
Create a class called "Car" with attributes for make, model, and year. Implement a method called get_info() to print out the details of the car. Create instances representing different cars and call the get_info() method for each instance.
- Stretch and Challenge: Add an attribute called "mileage" to the Car class and implement methods to set and update the mileage of the car.

### 4.
Define a class called "Book" with attributes for title, author, and genre. Implement a method called display_info() to print out the details of the book. Create instances representing different books and call the display_info() method for each instance.

**Advanced**: Add an attribute called "pages" to the Book class and implement methods to set and update the number of pages in the book.

### 5.
Create a class called "BankAccount" with attributes for account number, account holder, and balance. Implement methods for depositing and withdrawing money from the account, as well as checking the balance. Create instances representing different bank accounts and perform transactions on them.

**Advanced**: Add an attribute called "interest_rate" to the BankAccount class and implement methods to calculate and apply interest to the account balance.