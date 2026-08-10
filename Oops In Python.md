# Date: 31-July-2026

### **_OOPs_**

### **What is class**

&rarr; In python everything is an object. To create object we requires some model or plan or buleprint which is nothing but `class`

&rarr; We can write a class to represent `properties (atribute)` and `actions (behaviour)` of object

&rarr; Properties can be represented by `variables` and action can be represented by `methods`

### **How to define a class**

We define a class by using `class` keyword

**Syntax**

```python
class ClassName:
    pass
```

### **What is object**

&rarr;Physical existance of a class is nothing but object

&rarr;We can create any number of object for a class

**Syntax**

```python
class ClassName:
    pass
variable = ClassName() # This is the object
```

There are 3 types of variables in python (oops)

1. Instance variable (Obect level variable)
2. Static variable (Class level variable)
3. Local variable (Method level variable)

&rarr; Within the python class we can represent operations by using methods

There are 3 types of method

1. Instance method
2. Class Mmethod
3. Static method

# Date: 3-August-2026

### **self variable**

&rarr; Self is the default variable which is always pointing to the `current object`

&rarr; By using self we can access `instance variable` and `instance method` of object

&rarr; Self should be `1st parameter` inside the constructer

**Syntax**

```python
def __init__(self):
    pass
```

**Example**

```python
class Student:
    def __init__(self,rollno,name,dept):
        self.rollno = rollno

s1 = Student(111,"Debadarshan","CSE")
s1 = Student(48,"Kuna","ECE")
```

### **Constructor**

&rarr; Constructor is a special method in python

&rarr; The name of the constructor should be `__init__(self)`

&rarr; Constructor will be executed automatically at the time of object creation

&rarr; The main purpose of constructor is to `declare` and `initialise instance variable`

&rarr; Per object constructor will be executed only once

&rarr; Constructor can take at leat one parameter or argument i.e `self`

&rarr; Construcotr is optional and if we are not providing any constructor then python will provide default constructor

### **Method vs constructor**

| Method                                         | Constructor                                                               |
| ---------------------------------------------- | ------------------------------------------------------------------------- |
| Name of Method can be any name                 | Constructor name should be always `__init__(self)`                        |
| Method will be executed if we call that method | Constructor will be executed automatically at the time of object creation |
| Per object method can be called n no. of times | Per object constructor will be executed only once                         |
| Inside method we can awrite business logic     | Inside constructor we have to declare and initialise instance variables   |

**Example**

```python
class Student:
    def __init__(self, rollno, name, dept):
        self.rollno = rollno # Instance variable
        self.name = name
        self.dept = dept

    def display(self): # Instance method (if the 1st parameter is self)
        print(f"Name: {self.name}")
        print(f"Roll No: {self.rollno}")
        print(f"Department: {self.dept}")


s1 = Student(111, "Debadarshan", "CSE")
s2 = Student(48, "Kuna", "ECE")
s1.display()
print("-----------------")
s2.display()
```

# Date: 4-August-2026

### **Instance Variable**

&rarr; If the value of a variable is varied from object to object then such type of variables are called instance variable.

&rarr; For every object a separate copy of instance variable will be created.

### **Where we can declare instance variable ?**

&rarr; Inside constructor by using `self` variable

```python
def __init__(self,name,age):
    self.name = name
    self.age = age
```

&rarr; Inside instance method by using `self` variable

```python
def display(self):
    self.college = "GIET"
    self.dept = "CSE"
```

&rarr; Outside of the class by using `object reference` variable

```python
s1 = Student("Deba",24)
s1.city = "Puri"
```

### **How to access instance variable ?**

&rarr; We can access instance variables within the class and within the `instance method` by using `self` varibale and outside of the class by using `object reference`.

```python
def __init__(self,name,age):
    self.name = name
    self.age = age

# Accessing the instance variable inside instance method
def display(self):
    print(self.name)
    print(self.age)

# Accessing the instance variable outside of the class using object reference
s1 = Student("Deba",24)
print(s1.name)
```

### **How to delete instance variable from the object ?**

&rarr; Within a class we can delete instance variable by using `del` keyword.

```python
del self.variable_name
```

&rarr; From outside of class we can delete instance variable by using `del` keyword.

```python
del object_reference.variable_name
```

# Date: 5-August-2026

### **Static Variable or Class Variable**

&rarr; If the value of a variable is not varied from object to object, these variables are declared within the class directly but outside of methods. Such type of variables are called static variable or class variable.

&rarr; For total class only one copy of static variable will be created and shared by all object of that class.

&rarr; We can access static variable either by `class name` or by `object reference` but recommended to use `class name`

```python
class Test:
    x = 10 # Static Variable
    def __init__(self,y):
        self.y = y

t1 = Test(20)
print(t1.x) # 10, we can access static variable by using object referenece
print(Test.x) # 10, we can access static variable by using class name
t2 = Test(30)
print(t2.x) # 10, we can access static variable by using object referenece
print(Test.x) # 10, we can access static variable by using class name
```

### **Various cases to delcare static variable**

&rarr; In general we can declare static variable `within the class` directly but `outside of any method`.

&rarr; Inside the constructor by using `class name`.

```python
def __init__(self):
    Test.z = 50
```

&rarr; Inside the instance method by using `class name`.

```python
def show(self):
    Test.z = 50
```

&rarr; Inside the class method by using either `class name` or `class variable`.

```python
@classmethod
def show(cls):
    Test.z = 50
    cls.a = 50
```

&rarr; Inside static method by using `class name`

```python
@staticmethod
def show():
    Test.b = 50
```

# Date: 6-August-2026

### **How to access Static Variable**

&rarr; Inside the constructor by using either `self` or `class name`

```python
x = 10
def __init__(self):
    print(self.x) # 10
    print(Test.x) # 10
```

&rarr; Inside the instance method by using `self` or `class name`

```python
def show(self):
    print(self.x) # 10
    print(Test.x) # 10
```

&rarr; Inside the class method by using `class variable` or `class name`

```python
@classmethod
def cm(cls):
    print(cls.x) # 10
    print(Test.x) # 10
```

&rarr; Inside the staic method by using `class name`

```python
@staticmethod
def sm():
    print(Test.x) # 10
```

&rarr; From outside of class by using `object reference` or `class name`

```python
t1 = Test()
print(t1.x) # 10
print(Test.x) # 10
```

### **Where we can modify the static variable**

&rarr; Anywhere either within the class or outside of class we can modify by using `class name`

&rarr; But inside the classmethod by using `class variable`

```python
@classmethod
def show(cls):
    cls.x = 50 # By using class variable we can modify static variable
```

**_Note: If we change the value of static variable by using either `self` or `object reference` variable then the value of static variable won't be change, just a new instance variable with that name will be added to that particular object._**

### **How to delete a static variable of a class**

&rarr; We can delete static variable from anywhere by using `del` keyword

```python
del class_name.variable_name
```

&rarr; But inside the class method we can delete by using `class variable`

```python
del cls.variable_name
```

# Date: 7-August-2026

### **Local Variable**

&rarr; Sometimes to meet temprary requirement of programer we can declare variables inside a method directly. Such type of variables are called local variable or temporary variable.

&rarr; Local variable will be created at the time of `method execution` and destroyed once method completes.

&rarr; Local variable of a method can't be accessed from outside of method.

```python
def func1(self):
    a = 10 # a is the local variable and can be accessed only inside this function
    print(a)
```

### **Instance Method**

&rarr; Inside method implementation if we are using instance variables then such type of methods are called instance method.

&rarr; Inside instance method declaration we have to pass `self` variable.

&rarr; By using self variable inside the methods we can able to access instance variable.

&rarr; Within the class we can call instance method by using `self` variable and from outside of the class we can call by using `object referenece`.

```python
class Test:
    def __init__(self,name,marks):
        self.name = name
        self.marks = marks

    def grade(self):
        if self.marks >= 40:
            return "D"
        elif self.marks >= 60:
            return "C"
        elif self.marks >= 70:
            return "B"
        elif self.marks >= 80:
            return "A"
        elif self.marks >= 90:
            return "O"
        else:
            return "Fail"

    def show(self):
        print(f"Name: {self.name}")
        print(f"Age: {self.marks}")
        print(f"Grade: {self.grade()}")
t1 = Test("Deba",60)
t1.show()
```

### **Setter & Getter Method**

We can set and get the value of instance variable by using `getter` & `setter` method.

### **Setter**

&rarr; Setter method can be used to set value to instance variables

&rarr; Setter method is also known as `mutator method`

**Syntax**

```python
def setVariable(self,variable):
    self.variable=variable
```

### **Getter**

&rarr; Getter method can be used to get value of the instace variable

&rarr; Getter method is also known as `acessor method`

**Syntax**

```python
def getVariable(self):
    return self.variable
```

**Example**

```python
class Student:
    def setName(self, name):
        self.name = name

    def getName(self):
        return self.name

    def setMarks(self, marks):
        self.marks = marks

    def getMarks(self):
        return self.marks


n = int(input("Enter the number of students: "))
for i in range(n):
    s = Student()
    name = input("Enter your name: ")
    s.setName(name)
    marks = int(input("Enter your marks: "))
    s.setMarks(marks)
    print(f"Hii, {s.getName()}")
    print(f"Your marks are: {s.getMarks()}")
```

### **Class Method**

&rarr; Inside method implementation if we are using only `class variable (static variable)`, then such type of methods we should declare as class method.

&rarr; We can declare class method explicitily by using `@classmethod` decorator.

&rarr; For class method we should provide `cls` variable at the time of declaration.

&rarr; We can call class method by using `class name` or `object referenece`

```python
class Animal:
    legs = 4

    @classmethod
    def walk(cls,name):
        print("{} walks with {} legs".format(name,cls.legs))

a1 = Animal()
a1.walk("Tiger")
Animal.walk("Tiger")
```
