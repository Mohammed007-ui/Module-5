# Exp.No:25  
## Hierarchical Inheritance

---

### AIM  
To write a Python program to get the employee and doctor details and display them using hierarchical inheritance. Create a parent (base) class named `Details` and two child (derived) classes named `Employee` and `Doctor`.

---

### ALGORITHM

1. **Begin the program.**
2. **Create a class Details** with an `__init__` method to initialize three attributes: `id`, `name`, and `gender`.
3. **Define a method display_details()** to print the values of `id`, `name`, and `gender`.
4. **Create a class Employee** that inherits from the `Details` class. 
   - Add two additional attributes: `company` and `department`.
   - Override the `display_details()` method to print the employee-specific attributes (`company` and `department`) along with the inherited details.
5. **Create a class Doctor** that also inherits from the `Details` class. 
   - Add two additional attributes: `hospital` and `department`.
   - Override the `display_details()` method to print the doctor-specific attributes (`hospital` and `department`) along with the inherited details.
6. **Accept input** for employee and doctor details.
7. **Create objects of Employee and Doctor** using the input.
8. **Call the `display_details()` method** for both objects to print the details.
9. **Terminate the program.**

---

### PROGRAM
```
class Details:
    def __init__(self, id, name, gender):
        self.id = id
        self.name = name
        self.gender = gender

    def display_details(self):
        print(f"ID: {self.id}")
        print(f"Name: {self.name}")
        print(f"Gender: {self.gender}")

class Employee(Details):
    def __init__(self, id, name, gender, company, department):
        super().__init__(id, name, gender)
        self.company = company
        self.department = department

    def display_details(self):
        print("\n--- Employee Details ---")
        super().display_details()
        print(f"Company: {self.company}")
        print(f"Department: {self.department}")

class Doctor(Details):
    def __init__(self, id, name, gender, hospital, department):
        super().__init__(id, name, gender)
        self.hospital = hospital
        self.department = department

    def display_details(self):
        print("\n--- Doctor Details ---")
        super().display_details()
        print(f"Hospital: {self.hospital}")
        print(f"Department: {self.department}")

# Input for Employee
eid = input("Enter Employee ID: ")
ename = input("Enter Employee Name: ")
egender = input("Enter Employee Gender: ")
ecompany = input("Enter Company Name: ")
edepartment = input("Enter Employee Department: ")

# Input for Doctor
did = input("Enter Doctor ID: ")
dname = input("Enter Doctor Name: ")
dgender = input("Enter Doctor Gender: ")
dhospital = input("Enter Hospital Name: ")
ddepartment = input("Enter Doctor Department: ")

# Create objects
emp = Employee(eid, ename, egender, ecompany, edepartment)
doc = Doctor(did, dname, dgender, dhospital, ddepartment)

# Display details
emp.display_details()
doc.display_details()


```

### OUTPUT  


![image](https://github.com/user-attachments/assets/7d124ac2-9871-4a2b-bdc9-0775c2bb3497)


### RESULT
Thus, the Python program demonstrating hierarchical inheritance using a base class Details and derived classes Employee and Doctor was successfully implemented and executed.

