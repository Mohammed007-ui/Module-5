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
# Parent class Details
class Details:
    def __init__(self, id, name, gender):
        self.id = id
        self.name = name
        self.gender = gender

    def display_details(self):
        print(f"ID: {self.id}")
        print(f"Name: {self.name}")
        print(f"Gender: {self.gender}")

# Child class Employee inheriting from Details
class Employee(Details):
    def __init__(self, id, name, gender, company, department):
        super().__init__(id, name, gender)
        self.company = company
        self.department = department

    def display_details(self):
        super().display_details()
        print(f"Company: {self.company}")
        print(f"Department: {self.department}")

# Child class Doctor inheriting from Details
class Doctor(Details):
    def __init__(self, id, name, gender, hospital, specialization):
        super().__init__(id, name, gender)
        self.hospital = hospital
        self.specialization = specialization

    def display_details(self):
        super().display_details()
        print(f"Hospital: {self.hospital}")
        print(f"Specialization: {self.specialization}")

# Main program
# Accept input for Employee
print("Enter Employee Details:")
emp_id = input("ID: ")
emp_name = input("Name: ")
emp_gender = input("Gender: ")
emp_company = input("Company: ")
emp_department = input("Department: ")

# Create Employee object
employee = Employee(emp_id, emp_name, emp_gender, emp_company, emp_department)
print("\nEmployee Details:")
employee.display_details()

# Accept input for Doctor
print("\nEnter Doctor Details:")
doc_id = input("ID: ")
doc_name = input("Name: ")
doc_gender = input("Gender: ")
doc_hospital = input("Hospital: ")
doc_specialization = input("Specialization: ")

# Create Doctor object
doctor = Doctor(doc_id, doc_name, doc_gender, doc_hospital, doc_specialization)
print("\nDoctor Details:")
doctor.display_details()


```

### OUTPUT  
![image](https://github.com/user-attachments/assets/d753e319-71af-4622-bbd5-3e5d58db56cf)
### RESULT
Thus, the Python program demonstrating Hierarchical Inheritance with Details, Employee, and Doctor classes was successfully written and executed.


