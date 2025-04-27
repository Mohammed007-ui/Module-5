# Exp.No:22  
## Destructor

---

### AIM  
To create a Python class `Student` with a destructor.

---

### ALGORITHM

1. Begin the program.  
2. Define the `student` class.  
3. Inside the `student` class, define the `__init__` method (constructor) and the `__del__` method (destructor).  
4. Create an object `s2` of the `student` class. When the object `s2` is created, the `__init__` method is called, and its print statements are executed.  
5. Use the `del` statement to delete the object `s2`. This triggers the `__del__` method (destructor), and the respective print statements are executed.  
6. Terminate the program.

---

### PROGRAM

```
# Reg.No:
# Name:

# Define the class
class student:
    def __init__(self):
        print("Student object is created.")

    def __del__(self):
        print("Student object is destroyed.")

# Main program
s2 = student()

# Deleting the object
del s2

```

### OUTPUT
![image](https://github.com/user-attachments/assets/77f4db58-796f-4d16-baf3-2b40aa6c815a)


### RESULT
Thus, the Python program to create a Student class with a destructor was successfully written and executed.
