# Date: 3-Nov-2026

### **What is pytest ?**

PyTest is a python testing framework used to write, execute and manage test case efficiently.

### **Why we use pytest**

&rarr; Easy to write and understand test case

&rarr; It supports fixtures

&rarr; It supports parameterization

&rarr; It supports markers

&rarr; It generates test report through plugin

&rarr; It supports parallel execution

&rarr; It supports selenium, playwright and API automation

### **How to install pytest**

```shell
pip install pytest
```

# Date: 4-Nov-2026

### **Naming Conversation**

&rarr; Pytest discovers files matching with `test_*.py` or `*_test.py`.

&rarr; Functions begins with `test`.

```python
def test_addition():
    a = 10
    b = 20
    assert a+b == 30

def test_subtraction():
    c = 30
    d = 10
    assert c - d == 10
```

### **assert keyword**

&rarr; `assert` is a python keyword used to check whether an expected condition is true or false.

&rarr; In pytest we use assert statement to validate the actual result against the expected result.

&rarr; If the condition is `true`, the test `passes`.

&rarr; If the condition is `false`, the test `fails`.

### **Why we use assert**

&rarr; We use assertion to verify whether our application is working as expected.

&rarr; Ex: Check whether the login is successful, verify whether the correct title is displayed, check whether an API returns the expected status code

### **Command**

**`pytest`** &rarr; This command is used to discover and execute all test cases available in current directory and its sub directory based on pytest discover rules.

**`pytest -v (verbose output)`** &rarr; The `-v` stands for verbose, it means it displays details information about each test case during execution.

**`pytest -s (Display print statement)`** &rarr; The `-s` option disables pytest output capturing, allowing print statement and other standard output to appear directly in the terminal.

**`pytest filename.py`** &rarr; This command is used to test a specific file.
