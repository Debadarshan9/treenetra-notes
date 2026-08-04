# Date: 30-May-2026

### **Introduction of Python**

&rarr; Python is a general purpose high level programming language

&rarr; Python was developed by Guido van Rossam in 1989

&rarr; But officially python was developed in public 1991

&rarr; The official date of birth of python is 28th February, 1991

### **Where we can use python**

&rarr; For developing desktop applications

&rarr; For developing web application

&rarr; For developing database application

&rarr; For network programming

&rarr; For developing games

&rarr; For data analysis application

&rarr; For machine learning

&rarr; For AI

### **Features of python**

&rarr; Simple and easy to learn

&rarr; Freeware and open source

&rarr; High level programming language

&rarr; Platform Independent

&rarr; Portability

&rarr; Dynamically typed

&rarr; Interpreted language

&rarr; Extensive library

&rarr; Case sensitive language

---

# Date: 30-May-2026

### **Python Versions**

1\. 1.0v - 1994

2\. 2.0v - 2000

3\. 3.0v - 2008

### **Identifier**

&rarr; A name in python program is called identifier

&rarr; It can be class name or function name or module name or variable name

### **Rules to define an identifier**

&rarr; The only allowed character in python are alphabet symbols (either lower case or upper case), digits (0 to 9), underscore symbol (\_)

&rarr; Identifier should not start with digit

&rarr; Idenrifiers are case sensitive

&rarr; We can't use reserved keyword as identifier

### **Reserved Keyword**

In python some words are resorved to represent some meaning or functionality, such type of words are called reserved words.

```python
False, None, True, and, as, assert, async, await, break, class, continue, def, del, elif, else, except, finally, for, from, global, in, if, import, in, is, lambda, nonlocal, not, or, pass, raise, return, try, with, yield
```

### **Datatypes**

&rarr; Datatype represents the type of data present in as a variable

&rarr; In python we are not required to specify the type explicitily

### **Types of datatype**

1\. Text type - string

2\. Numeric type - int,float and complex

3\. Sequence type - list, tuple, range

4\. Mapping type - dict

5\. Set type - set, frozenset

6\. Boolean type - bool

7\. Binary type - bytes, bytearray, memoryview

8\. None type - None

### **Interger datatype**

&rarr; We can use int datatype to represent whole numbers

&rarr; type(identifier) function is used to know which datatype is this

### **Float datatype**

&rarr; A float is used to store decimal value in python

### **Complex datatype**

&rarr; Complex number is a number that contains real part and imaginary part

&rarr; The imaginary part is represented by j in python

#### **Where we use**

&rarr; In electrical engg.

&rarr; In signal processing

# Date: 30-May-2026

### **Variable**

&rarr; Varibles are containers for storing data values

&rarr; Variables are 3 types

    camelCase: Each word except the first starts with a capital letter. ex: myVariableName="test"

    PascalCase: Each word starts with capital letter.
    ex: MyVariableName="test"

    snake_case: Each word separated by an underscore.
    ex: my_variable_name="test"

### **String Datatype**

&rarr; A string is a sequence of characters enclosed within single quote (' '), double quote (" ") and triple quote (''' ''' - especially used for commenting more than one line)

&rarr; Strings are immutable

```python
s1="python developer"
print(s1.replace("develper","tester")) #python tester
print(s1) #python developer
```

&rarr; String supports indexing

&rarr; Python supports both forward and backward indexing

&rarr; Forward indexing starts with 0 and backward indexing starts with -1

&rarr; Python supprts slicing

# Date: 5-June-2026

```python
s1 = "Python is Easy and Simple"
```

### **Capitalize()**

It converts the 1st character of 1st word to uppercase and rest to lowercase

```python
print(s1.capitalize()) # Python is easy and simple
```

### **title()**

It converts the 1st character of every word to uppercase

```python
print(s1.title()) # Python Is Easy And Simple
```

### **islower()**

It returns true if all characters are in lowercase

```python
print(s1.islower()) # False
```

### **isupper()**

It returns true if all characters are in uppercase

```python
print(s1.isupper()) # False
```

### **lower()**

It converts all chacters into lowercase

```python
print(s1.lower()) # python is easy and simple
```

### **upper()**

It converts all chacters into uppercase

```python
print(s1.upper()) # PYTHON IS EASY AND SIMPLE
```

### **len()**

It returns the total number character in the string

```python
print(len(s1)) # 25
```

### **count()**

It returns how many times a substring occures

```python
print(s1.count("s")) # 3
```

### **find()**

&rarr; It finds the index position of the specific character or substring in the given string

```python
print(s1.find("i")) # 7
```

&rarr; it returns -1 if the substring not found

```python
print(s1.find("z")) # -1
```

### **split()**

It splits the string into a list of multiple string

```python
print(s1.split())

# ["Python", "is", "easy", "and" "simple"]
```

### **strip()**

It removes spaces from both sides of a string

```python
s1 = "#python##"

print(s1.strip("#")) # Python
```

### **swapcase()**

It converts the uppercase to lowercase and vice versa

### **replace()**

it replace a substring to another substring

```python
print(s1.replace("easy","hard"))

# Python is hard and simple
```

### **isnumeric()**

It returns true if all characters are numeric

Everything isdigit() accepts plus other numeric Unicode characters (e.g., fractions ½, Roman numerals Ⅷ)

```python
s1 = "VII"

print(s1.isnumeric()) # True
```

### **isdigit()**

It retutns true if all characters are digit

Digits and digit-like characters (e.g., 0-9, ²)

```python
s1="1234"

print(s1.isdigit()) # True
```

# Date: 6-June-2026

### **What is slicing?**

Slicing is the technique used to extract a portion of string, list, tuple using

### **Syntax:**

variable[start:end:step]

start - starting index position

end - ending index position

step - no. of position to move

# Date: 24-June-2026

### **Logical Operator**

#### **and**

&rarr; It returns true if both conditions are true

&rarr; If any condition is false then it returns false

#### **or**

&rarr; It returns true if any one of the condition is true

&rarr; It returns false only if both the conditions are false

#### **not**

&rarr; Reverse the boolean value

### **Membership Operator**

&rarr; Python has two membership operators

**1. In**

It checks if the value is exist in a sequence like string, list, tuple, dictionary

**2. not in**

It checks if the value doesn't exist in a sequence

### **Identiry operator**

Python has 2 identity operators

**1. is**

It checks if two variables point to the same object in memory

**is vs ==**

**2. is not**

it checks if two variable don't point to the same object

### **Typecasting**

&rarr; Typecasting is converting one datatype into another datatype

### **Types of typecasting**

**1. Implicity typecasting**

Python converts the datatype automatically

```python
a = 10
b = 20.5
c = a + b
print(c) # 30.5
print(type(c)) # float
```

**2. Explicity typecasting**

The programmer converts the datatype

```python
a = "560"
b = int(a)
print(b) # 560
print(type(b)) # int
```

### **Input and output statement**

#### **input()**

```python
name = input("Enter your name:")
age = int(input("Enter your age:"))
salary = float("Enter your salary:")
```

#### **eval()**

```python
var = eval(input("Enter your name:"))
print(type(var))

# 23 --> int
# 23.6 --> float
# "python" --> str
```

# Date: 25-June-2026

### **What is conditional statement?**

A conditional statement is used to execute a block of code only when a specific condition becomes true.

### **Why we use conditional statement?**

&rarr; Make decision

&rarr; Execute code based on decision

&rarr; Validate the data

&rarr; Compare values

&rarr; Implement business logic

### **Types of conditional statement**

#### **1. if**

The if statement executes code only when the condition becomes true

**syntax:**

```python
if condition:
    statements
```

**Example**

```python
marks = 45
if marks >= 40: #True
    print("You will pass.") # You will pass.
```

#### **2. if else**

If the condition is true, the if block executes otherwise else block executes

**syntax:**

```python
if condition:
    statements

else:
    statements
```

**Example**

```python
num1 = 40
num2 = 50

if num1 > num2: #False
    print("num1 is greater than num2")

else:
    print("num2 is greater that num1")
    # num2 is greater that num1
```

# Date: 26-June-2026

#### **3. if elif else**

&rarr; The if elif else statement is used to check multiple condition one after another.

&rarr; As soon as one condition becomes true, python executes that block and skip the remaining conditions

#### **Why we use if-elif-else**

&rarr; Multiple condition need to be checked

&rarr; Only one block of code should be executed

&rarr; Decision depends on different range or value

**syntax:**

```python
if condition1:
    statements

elif condition2:
    statements

elif condition3:
    statements

else:
    statements
```

**Example**

```python
marks = int(input("Enter yours marks: "))

if(marks >= 90):
    print("Grade O")

elif(marks >= 75):
    print("Grade A")

elif(marks >= 60):
    print("Grade B")

elif(marks >= 40):
    print("Grade C")

else:
    print("Fail")
```

#### **4. Nested if**

## A nested if is an if statement inside another if statement

#### **Why we use nested if**

&rarr; When multiple conditions depends on each other

&rarr; The condition should be checked only if the 1st condition is true

&rarr; We need multiple level of decision making

**Syntax**

```python
if condition1:
    statement1
    if condition2:
        statement2
```

**Example**

```python
marks = int(input("Enter your marks: "))
attendance = int(input("Enter your attendace: "))

if attendance >= 60:
    if marks >= 30:
        print("PASS")
    else:
        print("FAIL")
else:
    print("FAIL because of insuffiecient attendance")
```

# Date: 29-June-2026

### **Loop**

&rarr; A loop is used to execute a block of code repeatedly until a condition becomes false or unit all items in a sequence are processed

### **Why we use loops?**

&rarr; Avoid writing the same code repeatedly

&rarr; execute a block of code multiple times

&rarr; Iterate through strings, list, tuple

&rarr; Solve repeatative task efficiently

### **Types of loop**

#### **1. For loop**

&rarr; A for loop is used to iterate over a sequence such as string, list, tuple, set, dictionary or range

**Syntax**

```python
for variable in sequence:
    statements
```

**Example**

```python
l1 = [10,23,34,51,40,94,5,8]

even = []
odd = []

for i in l1:
    if i % 2 == 0:
        even.append(i)
    else:
        odd.append(i)

print("Even numbers are ",even) # [10,34,40,94,8]
print("Odd numbers are ",odd) # [23,51,5]
```

# Date: 2-July-2026

### **While Loop**

&rarr; A while loop is used to execute a block of code repeatedly as long as if the given condition is true

**Syntax**

```python
while condition:
    statement
```

### **Why we use while loop**

&rarr; We don't know how many times the loop will be executed

&rarr; The loop depends on a condition

&rarr; We want to repeat a task until a condition is false

**Example**

```python
s1 = "python"
i = 0

while i < len(s1):
    print(s1[i], end=" ") # p y t h o n
    i += 1
```

# Date: 3-July-2026

### **Transfer Statement**

&rarr; Transfer statement are statement that changes the normal flow of execution in a loop or program.

&rarr; They are used to stop a loop, skip an iteration and do nothing temporarily

### **Types of transfer statement**

Python has 3 transfer statement

1. break
2. continue
3. pass

### **What is break statement**

The break statement is used to immediately terminate(stop) the loop even a the loop conditon is still true

**Example**

```python
for i in range(10):
    if i == 6:
        break
    print(i, end=" ") # 0 1 2 3 4 5
```

### **What is continue statement**

The continue statement skips the current iteration and moves to the next iteration of the loop

**Example**

```python
for i in range(10):
    if i == 6:
        continue
    print(i, end=" ") # 0 1 2 3 4 5 7 8 9
```

### **What is pass statement**

&rarr; The pass statement is a placeholder.

&rarr; It does nothing when executed

&rarr; We use it when we want to write code later

**Example**

```python
for i in range(10):
    pass
```

### **What is function?**

&rarr; A function is a named block of reusable code that performs a specific task

&rarr; Instead of writing the same code again and again we write it once inside a function and call it whenever needed

# Date: 4-July-2026

### **Types of function**

Python supports 2 types of function

1. Built in function
2. User defined function

### **What is built in function**

The function which are coming along with python software automatically are called built in function or predefined function

**Example**

```python
print(), type(), id(), eval(), input(), etc.
```

### **What is user defined function**

The functions which are developed by programmer explicitily according to business requirement are called user defined function

**Syntax**

```python
def function_name():
    statement
```

**Example**

```python
def wish():
    print("Good Morning")

wish()
```

### **Parameters**

&rarr; Parameters are the inputs to the function

&rarr; If a function contains parameters, then at the time of calling compulsory we should have provide values otherwise we will get error

# Date: 6-July-2026

### **What is return statement?**

&rarr; Function can take input value as parameter and execute business logic and returns output to the caller with return statement

### **Types of parameter or argument**

There are 4 types of argument in python

1. Positional Argument
2. Keyword Argument (\*\*kwargs)
3. Default Argument
4. Variable length Argument (\*args)

### **Positional Argument**

&rarr; These are the arguments passed to function in correct positional order

&rarr; The number of arguments and position of arguments must be matched

&rarr; If we change the order then result may be changed

&rarr; If we change the number of arguments then we will get error

**Example**

```python
def add(a,b):
    return a+b

add(20,30)
```

### **Keyword Argument (\*\*kwargs)**

&rarr; We can pass argument value by keyward that is why parameter name

&rarr; Here the order of the argument is not important but the number of argument must be matched

**Example**

```python
def wish(name,msg):
    return f"Helo {name} {msg}"

wish(msg="Good Morning",name="Debadarshan")
```

### **Default Argument**

&rarr; Sometimes we can provide default value as for our positional argument

&rarr; If we are not passing any argument then only default value will be considered

**Example**

```python
def wish(msg:"Good Morning"):
    return msg

print(wish()) # Good Morning
print(wish("Good Night")) # Good Night
```

### **Variable length Argument (\*args)**

&rarr; Sometimes we can pass variable number of arguments to our function. Sucg type of arguments are called variable length argument

&rarr; We can declare a variable length argument with \* symbol

**Example**

```python
def sum(*n):
    total = 0
    for i in n:
        total += i
    return total

print(sum(10,20,30,40)) # 100
```

# Date: 8-July-2026

### **Types of variablea**

&rarr; Python supports 2 types of variable

1. Local varibale
2. Global variable

### **Local Variable**

&rarr; The variable which are declare inside a function are called local variables

&rarr; Local variables are available only for the function in which we declare

&rarr; If the variable is outside of the function, then we can't access this inside the function

**Example**

```python
def func1():
    a = 10
    b = 20
    print(a,b)

func1()

def func2():
    print(a) # It will give error because a is delcared in func1
```

### **Global variable**

&rarr; The variable which are declared outside of a function are called global variable

&rarr; These varibales can be accessed in all functions of that module

**Example**

```python
a = 10
def func1():
    print(a) # we can access this variable because a is global variable

func1()
```

### **Global Keyword**

&rarr; We can use global keyword for two purposes

1. To decalare global variable inside a function
2. To make global variable available to the function so that we can perform required modification

**Example**

```python
a = 5

def func1():
    global a
    a = 10
    print(a) # 10

func1()

def func2():
    print(a) # 10

func2()
```

### **Note**

&rarr; If the global variable and local variable having same name then we can access the local variable

### **Anonymous Function**

&rarr; Sometimes we can declare a function without any name, such type of nameless function is called anonymous function or lambda function

&rarr; The main purpose of anonymous function or lambda function is just for instant use (that means for one time usage)

**Syntax**

```python
lambda argument_list:expression
```

**Example**

```python
s1 = lambda x:x*x
print(s1(4))

s2 = lambda a,b,c,d:a+b+c+d
print(s2(1,2,3,4))

s3 = lambda a,b:a if a>b else b
print(s3(10,20))
```

# Date: 9-July-2026

### **map()**

Map function is used to apply the same operation to every element in an iterable like list, tuple, set, etc.

### **Why we use map()**

Instead of writing a for loop to modify each element, map() performs the operation on all element and returns the result।

**Syntax**

```python
map(function or lambda,iterable)
```

**Example**

```python
numbers = [10,20,30]
result = list(map(lambda x : x**2, numbers))
print(result) # [100,400,900]
```

### **filter()**

filter() is used to select only those elements that satisfied a condition

### **Why we use filter()**

Instead of checking each element using a for loop and if statement, filter() returns only those elements that match the condition

**Syntax**

```python
filter(function,iterable)
```

**Example**

```python
numbers = range(10)
result = list(filter(lambda x: x % 2 == 0, numbers))
print(result) #[0,2,4,6,8]
```

# Date: 10-July-2026

### **Reduce**

&rarr; reduce() is used to reduce multiple values in a list to a single value by repeatedly apply a function

&rarr; It is available in the functools

**_What is difference between map(), filter() and reduce_**

**Syntax**

```python
reduce(function,iterable)
```

**Example**

```python
from functools import reduce

l1 = [20, 10, 4, 70, 8, 10, 45]

largest = reduce(lambda x, y: x if x > y else y, l1)

print(largest)

20 > 10 = 20
20 > 4 = 20
20 > 70 = 70
8 > 70 = 70
10 > 70 = 70
45 > 70 = 70
```

# Date: 14-July-2026

### **Decorator**

**Syntax**

```python

```

**Example**

```python
def func1(func):
    def wrapper():
        print("Good Morning")
    func()
    retrun wrapper

@func1
def hello():
    print("Hello Students")

hello()
```

# Date: 17-July-2026

### **Generator**

A generator is a special type of function that uses the yield keyword to return value one at a time instead of returning all value at once

### **yield**

yield is a keyword that causes the execution of a generator function and returns one value at a time

### **next()**

next() is a builtin function used to get the next value from a generator

### **return vs yield**

| return                        | yield                            |
| ----------------------------- | -------------------------------- |
| Ends the function             | Pauses the function              |
| Returns only one value        | Returns value one by one         |
| It is used in normal function | It is used in generator function |

### **Why we use generator**

&rarr; To save memory

&rarr; To handle large dataset

&rarr; To improve performance

&rarr; To iterate efficiently

&rarr; To work with data streams

**Example**

```python
def square():
    for i in range(1, 5):
        yield i*i

var = square()
for num in var:
    print(num) #1, 4, 9, 16
```

# Date: 21-July-2026

### **Recursive function**

&rarr; A recursive function is a function that calls itself until a stoping condition (best case) is met

### **Component of recursion**

Every recursive function has 2 parts

**1. Base case**

&rarr; It stops the recursion

&rarr; Without a base case the function will keep caling itself forever and eventuallly raise a recursion error

**2. Recursive call:**

It calls the function again with a smaller problem

### **Usage of recursion**

&rarr; To solve repeatative problem

&rarr; To solve problem that can be divided into smaller sub problem

&rarr; Used in fibbonacci, factorial, traversal, DFS

# Date: 22-July-2026

### **Types of module**

&rarr; Modules are 3 types

1. Standard module
2. Userdefined module
3. Third party module

### **Standard Module**

&rarr; These modules are already defined and kept in python software

&rarr; So when we install python, then automatically these standard modules will be installed in our machine

### **Userdefined Module**

&rarr; These modules are defined by users as per there requirement, so here user defined modules is nothing but the .py file, which contains methods, functions, variables and also classes

### **Third Party Module**

&rarr; These modules are already defined by some other people and kept in internet, so we can download and install in our machine by using `pip`

### **What is pip**

pip is a package management system used to install and manage software packages written in python like mysql, oracle

&rarr; In python modules are accesed by using import statement

We can import modules in 3 different ways:

1. `import <module_name>`

2. `from <module_name> import <method>`

3. `from <module_name> import *`

### **Iterator**

&rarr; An iterator is an object that returns one element at a time using `next()` and `iter()`

&rarr; Iterator in python is used with a for loop

&rarr; String, list, tuple, set are the examples

```python
l1 = [10,20,30,40]
it = iter(l1)

print(it) # It will return list_iterator object
print(next(it)) # only 10
print(next(it)) # only 20
```

### **Iterator vs Iterable**

| Iterator                      | Iterable                            |
| ----------------------------- | ----------------------------------- |
| It returns one time at a time | It can be looped over               |
| Used `next()` to get values   | Used `iter()` to create an iterator |
|                               | String, list, tuple, set            |

### **List comprehension**

&rarr; It is a short and simple way to create a list using a single line of code
**Syntax**

```python
new_list = [expression for item in iterable]
```

**Example**

```python
l1 = [i for i in range(1,9)]
print(l1) # [1, 2, 3, 4, 5, 6, 7, 8]

l1 = [2, 5, 7, 10, 24, 53, 75, 80, 45]
even = [i for i in l1 if i % 3 == 0 and i % 5 == 0]
print(even) # [2, 10, 24, 80]


name = ['hari', 'chiku', 'arman', 'sri']
upper_case = [i.upper() for i in name]
title_case = [i.title() for i in name]

print(upper_case) # ["HARI", "CHIKU", "ARMAN", "SRI"]
print(title_case) # ["Hari", "Chiku", "Arman", "Sri"]


number = [1, 2, 3, 4, 5, 6, 8, 10]

result = ["even" if i % 2 == 0 else "odd" for i in number]

print(result) # ["odd", "even", "odd", "even", "odd", "even", "even", "even"]
```

# Date: 23-July-2026

### **Dictionary comprehension**

It is a shortest way to create a dictionary in a single line of code

**Syntax**

```python
new_dict = {key:value for item in iterable}
```

**Example**

```python
square = {item: item*item for item in range(1, 6)}
print(square) # {1: 1, 2: 4, 3: 9, 4: 16, 5: 25}
```

## **Exception Handling**

&rarr; An exception is a runtime error that happens during the execution of the program

&rarr; Python raises an exception whenever it tries to execute invalid code

&rarr; Error handling is generally reduced by saving the state of execution at the moment the error occured and interpreting the normal flow of the programming

### **How we handle exception**

There are 4 blocks in python. By using these we can handle exception

**1. try**

&rarr; The try block contents the code that may generate an exception

**2. except**

&rarr; except block execute if an exception occures

**3. else**

&rarr; else executed when no exception occures

**4. finally**

&rarr; finally always executes whether an exception occures or not

**Example**

```python
num1 = int(input("Enter a number: "))
num2 = int(input("Enter 2nd number: "))

try:
    result = num1/num2
    print(result)
except:
    print("Division with 0 is not possible")
else:
    print("Code executed successfully")
finally:
    print("Very Good")
```

# Date: 28-July-2026

### **Error**

In any programming language there are 2 types of error

### **1. Syntax Error**

The error which occures because of invalid syntax is called syntax error

### **2. Runtime Error**

While executing one program if something goes wrong because of end user input can programming broken or memory problem happens that is called runtime error

### **Default Exception Handling**

Default exception handling is the mechanism where python automatically handles an exception by displaying an error message and terminating the program

### **Userdefined Exception Handling**

A user defined exception is a custom exception created by the programer by inheriting from the built-in exception class

```python
class MyException:
    pass

age = int(input("Enter your age: "))
if age < 18:
    raise MyException("Age must be 18 or above")
print("Eligible for voting")
```

### **raise**

The raise keyword is used to explicitily raise an exception when a specific condition occures

### **Why do we use userdefined exception**

&rarr; To create meaningfull error message

&rarr; To make debug easier

&rarr; To improve code readability

```python
try:
    amount = int(input("Enter your amount: "))
    if amount < 0:
        raise ValueError("Amount can not be negative")
    print(amount)
except ValueError as e:
    print(e)
```

```python
def calculator():
    try:
        num1 = int(input("Enter 1st number: "))
        num2 = int(input("Enter 2nd number: "))
        operator = input("Enter an operand(+,-,*,/): ")
        if operator == "+":
            result = num1 + num2

        elif operator == "-":
            result = num1 - num2

        elif operator == "*":
            result = num1*num2

        elif operator == "/":
            result = num1/num2

        else:
            raise ValueError("Invalid operator")

        return f"Result: {result}"

    except ValueError as e:
        return f"Error: {e}"

    except ZeroDivisionError as e:
        return f"Error: {e}"

print(calculator())
print("Calculator closed")
```

# Date: 29-July-2026

### **File Handling**

It is the process of creating, opening, reading, writting, updating and deleting files using a programing language like python

### **Types of Files**

There are 2 types of files:

**1. Text File**

Usually we can use text files to store character data

**2. Binary File**

usually we can use binary files to store binary data like images, video, audio, etc.

### **Opening a file**

&rarr; Before performing any operation like read or write on the file 1st we have to open that file

&rarr; For this we should use python's inbuilt function `open()`

&rarr; But at the time of open we have to specify mode which represents the purpose of opening a file

**Syntax**

```python
f=open(file_name,mode)
```

### **Mode**

**r (Read)**

&rarr; open an existing file for read operation.

&rarr; The pointor position is at start of the file.

&rarr; If the specific file doesn't exist then we will get `FileNotFoundError`

**w (Write)**

&rarr; Open an existing file for write operation.

&rarr; If the file already contained some data then it will be overriden

&rarr; If the specified file is not already available then this mode will create the file

**a (update)**

&rarr; Open an existing file for append operation

&rarr; It won't override existing data

&rarr; If the specified file is not available then this mode will create a new file

**r+**

&rarr; To read and write data into the file

&rarr; The previous data in the file will not be deleted.

&rarr; The file pointer is placed at the begining of the file

**w+**

&rarr; To write and read the data

&rarr; It will override existing data

**a+**

&rarr; To append and read data from the file

&rarr; It won't override the existing data

**x**

&rarr; To open a file in exclusive creation mode for write operation

&rarr; If the file already exist then we will get `FileExistError`

**b** &rarr; B standa for binary mode, It is used to read and write binary files such as images, video, audio, etc.

**rb** &rarr; For read a binary file

**wb** &rarr; For write a binary file

**ab** &rarr; Append to binary file

**rb+** &rarr; Read and write a binary file

**wb+** &rarr; Read and write a binary file but it overrides existing file

**ab** &rarr; Read and append to a binary file

### **Closing a file**

&rarr; After completing our operation on the file it is highly recomended to close a file

&rarr; For this we have `close()`

**read**

```python
file = open(r"D:\Treenetra\Python\File Handling\file1.txt", "r")
print(file.read())
file.close()
```

**write**

```python
file = open(r"D:\Treenetra\Python\File Handling\file2.txt", "w")
file.write("This is the python class")
file.close()
```

# Date: 30-July-2026

### **read()**

This method is used to read the entire content of a file or a specific no. of character `read(size of character)` from a file

### **readline()**

This method is used to read only 1 line at a time from a file

### **readlines()**

This method is used to read all lines at a time from a file and returns them as a list

### **write()**

This method is used to write data into a file

### **writelines()**

This method is used to write multiple lines from a list into a file

### **seek()**

This method is used to move the file cursor to a specified position

### **tell()**

This method is used to return the current position of the file cursor

# Date: 31-July-2026

### **with open()**

The with statement is used to open a file and automatically close it after the block of code finishes executing

**Syntax**

```python
with open("filename","mode") as file:
    statement
```

### **Why we use with statement**

&rarr;Without with we have to close the file manually

&rarr;If we forgot `file.close()` the file remains open

&rarr;Python closes the file automatically by using `with`

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
