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

# Date: 10-August-2026

### **Static Method**

&rarr; In generally these methods are general utility methods.

&rarr; Inside these methods we won't use `instance` or `class variables`.

&rarr; Here we don't provide `self` or `cls` argument at the time of declaration.

&rarr; We can declare static method explicitily by using `@staticmethod` decorator.

&rarr; We can access static method by using `class name` or `object reference`

**Example**

```python
class Math:
    @staticmethod
    def add(x, y):
        return x + y

    @staticmethod
    def average(a, b):
        return Math.add(a, b) / 2

m1 = Math()
print(m1.average(2, 4)) # 3.0
print(Math.average(5, 6)) # 5.5
```

### **Inner classes**

&rarr; Sometimes we can declare `a class inside another class`, such type of classes are called inner classes.

&rarr; Without existing one type of object if there is no chance of existing another type of object then we should go for inner classes.

**_Note: Without existing outer class object there is no chance of existing inner class object. Hence inner class object is always associated with outer class object._**

**Example**

```python
class Outer:
    def __init__(self):
        print("Outer class constructor")

    class Inner:
        def __init__(self):
            print("Inner clas constructor")
        def m1(self):
            print("Inner class method")

o1 = Outer() # Outer class constructor
i1 = o1.Inner() # Inner class constructor
i1.m1() # Inner class method
```

In Oops concept there are 4 pillars

1. Encapsulation
2. Inheritance
3. Polymorphism
4. Abstraction

### **Encapsulation**

&rarr; Encapsulation is about protecting data inside a class.

&rarr; It means keeping data (properties) and methods together in a class, while controlling how the data can be accessed from outside the class.

### **Why we use encapsulation ?**

&rarr; **Data protection:** It prevents accidental modification of data.

&rarr; **Validation:** You can validate data before settings.

&rarr; **Flexibility:** Interal implementation can change without affecting external code.

&rarr; **Control:** You have full control over how data is accessed and modified.

&rarr; **Private:** In python you can make properties and methods privately by using `__` (double underscore)

&rarr; **Protected:** In python you can make properties and methods protected by using `_` (single underscore)

**_Note: Private property can't be accessed directly from outside of the class_**

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.__age = age


p1 = Person("Deba", 24)
print(p1.name) # Deba
print(p1.__age) # Error: Person has no attribute "__age"
```

### **Accessing private property**

&rarr; To accessing a private property we should use getter method

# Date: 11-August-2026

### **Protected**

&rarr; Protecetd may lose

&rarr; There are not strictly private but should be treated as internal

```python
class Employee:
    def __init__(self, name, age):
        self.name = name
        self._age = age

    def showAge(self):
        print("Age is:", self._age)


emp2 = Employee("Deba", 25)
emp2.showAge() # 25
```

```python
class Employee:
    def __init__(self,name,age):
        self.name = name
        self._age = age

class SubEmployee(Employee):
    def show_age(self):
        print("Age is:",self._age)


emp2 = SubEmployee("Deba",23)
emp2.show_age() # 23
```

### **Private**

&rarr; Private variables and methods that can't be access directly from outside the class.

&rarr; There are used to restrict access and protect internal data.

```python
class BankAccount:
    def __init__(self):
        self.balance = 1000

    def _show_balance(self):
        print("Balance is:", self.balance)

    def __update_balance(self, amount):
        self.balance += amount

    def deposite(self, amount):
        if amount > 0:
            self.__update_balance(amount)
            self._show_balance()
        else:
            print("Invalid Deposite Amount")


bank1 = BankAccount()
bank1.deposite(2000) # Balance is: 3000
```

### **Protected vs Private**

| Proteted                                                  | Private                                   |
| --------------------------------------------------------- | ----------------------------------------- |
| It is written by single underscore (`_`)                  | It is written by double underscore (`__`) |
| It means internal or protected member                     | It is totally provate member              |
| In the same class we can access                           | In the same class we can access           |
| In child class it can be accessible directly              | It can't be accessible directly           |
| Outside the class it technically accessible               | Outside the class it can't be accessible  |
| It indicates that member is for internal or inherited use | It prevent accidental directly access     |

### **Inheritance**

&rarr; Inheritance is a fundamental concept in oops that allows a child class to inherit attributes and methods from another class (parent class).

**syntax**

```python
class ParentClass:
    pass
class ChildClass(ParentClass):
    pass
```

**Example**

```python
class Animal:
    def __init__(self,name):
        self.name = name

    def info(self):
        print("Animal name:",self.name)


class Dog(Animal):
    def sound(self):
        print(self.name,"Bark")

d1 = Dog("Jacky")
d1.info()
d1.sound()
```

### **Advantages of Inheritance**

&rarr; Code reusability

&rarr; Real world hierachy

&rarr; Avoid code duplication

&rarr; Extend existing functionality
