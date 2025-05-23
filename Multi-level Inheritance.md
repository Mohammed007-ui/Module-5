# Exp.No:24  
## Multi-level Inheritance

---

### AIM  
To write a Python program to get the name, age, and ID of a person and display them using multilevel inheritance.

---

### ALGORITHM

1. Define the `Person` class:
   - Inside the `Person` class, define the `__init__` method (constructor) with two parameters: `name` and `age`.
   - Inside the `__init__` method, assign the `name` to `self.name` and `age` to `self.age`.

2. Define the `PersonDetails` class that inherits from the `Person` class:
   - Inside the `PersonDetails` class, define the `__init__` method (constructor) with three parameters: `name`, `age`, and `person_id`.
   - Inside the `__init__` method, call the `__init__` method of the `Person` class using `super()` to initialize `name` and `age`.
   - Assign `person_id` to `self.person_id`.

3. Define the `DisplayDetails` class that inherits from the `PersonDetails` class:
   - Inside the `DisplayDetails` class, define the `__init__` method (constructor) with three parameters: `name`, `age`, and `person_id`.
   - Inside the `__init__` method, call the `__init__` method of the `PersonDetails` class using `super()` to initialize `name`, `age`, and `person_id`.

4. Inside the `DisplayDetails` class, define the `show_details` method:
   - Inside the `show_details` method, return a formatted string with `self.name`, `self.age`, and `self.person_id`.

5. Prompt the user to enter `name` (string), `age` (integer), and `person_id` (integer).

6. Create an instance `person` of the `DisplayDetails` class, passing `name`, `age`, and `person_id` to the constructor.

7. Call the `show_details` method on the `person` object and print the result.

8. Terminate the program.

---

### PROGRAM

```
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

class PersonDetails(Person):
    def __init__(self, name, age, person_id):
        super().__init__(name, age)
        self.person_id = person_id

class DisplayDetails(PersonDetails):
    def __init__(self, name, age, person_id):
        super().__init__(name, age, person_id)

    def show_details(self):
        return f"\nName: {self.name}\nAge: {self.age}\nPerson ID: {self.person_id}"

# Input from user
name = input("Enter Name: ")
age = int(input("Enter Age: "))
person_id = int(input("Enter Person ID: "))

# Create object
person = DisplayDetails(name, age, person_id)

# Display details
print(person.show_details())


```

### OUTPUT
![image](https://github.com/user-attachments/assets/63a70321-a9d7-491f-bb90-41b6122e504d)

### RESULT
Thus, the Python program demonstrating multi-level inheritance using the classes Person, PersonDetails, and DisplayDetails was successfully implemented and executed.
