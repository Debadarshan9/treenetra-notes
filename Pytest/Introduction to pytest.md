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

# Date: 5-Nov-2026

**`pytest -k "matching_name"`** &rarr; The `k` options is used to select test cases based on a keyword expression that matched their names.

### **Folder Structure**

pages/

|

reports/

|

test_data/

|

tests/

|

utils/

|

screenshots/

|

logs/

|

conftest.py

|

pytest.ini

|

requirements.txt

|

.gitignore

#### **pages/**

&rarr; The pages folder contains all the page classes, locators and reusable methods related to individual application pages.

&rarr; This folder is used when implementing Page Object Model (POM) design pattern.

#### **tests/**

&rarr; The tests folder contains automated test scripts that verifies different functionalities of the application.

#### **test-data/**

&rarr; This folder stores input data required for executing test cases.

#### **utils/**

&rarr; The utils folder contains reusable helper functions and common methods used across different test cases.

#### **reports/**

&rarr; This folder stores the test execution reports generated after running the automated test cases.

#### **screenshots/**

&rarr; This folder stores images captured during automated test execution.

#### **logs/**

&rarr; This folder stores execution logs that provides information about the activity performed during the test execution.

#### **conftest.py**

&rarr; It is a special pytest configuration file used to define fixtures, hooks and shared test setup functionality.

#### **pytest.ini**

&rarr; This is a configuration file used to customize pytest execution settings.

#### **requirements.txt**

&rarr; This file contains the python packages and dependencies required to execute the automation project.

#### **.gitignore**

&rarr; This configuration file that specifies files and folders that git should ignore when tracking changes.

# Date: 6-Nov-2026

## **POM (Page Object Model)**

&rarr; POM is a design pattern used in test automation to organize web application pages into separate classes.

&rarr; Each page class contains the locator and methods required to interact with that particular page.

### **Why we use POM**

&rarr; Code reusability

&rarr; Code maintainability

&rarr; Code organization

&rarr; Reduces code duplication

&rarr; Code readability

&rarr; Scalability

### **Pytest Fixtures**

&rarr; A fixture in pytest is a function used to provide a fixed and prepared state, resources or dependency required by test case.

&rarr; Fixtures are commonly used in browser launching, database connection, API authentication, test data creation, login setup, operating and closing files, setup and teardown operation.

### **Why we use fixtures**

&rarr; Code reusability

&rarr; Setup management

&rarr; Teardown management

&rarr; Maintainability

&rarr; Dependency injection

&rarr; Scope management

```python
@pytest.fixture
def setup():
    print("Setup code executed before the test case")

def test_example(setup):
    print("Test case executed")
```

### **Fixture with setup and teardown**

&rarr; Setup means preparing the required resources before test execution.

&rarr; Teardown means cleaning up or releasing those resources after test execution.

#### **Example:**

setup - Launch browser, test perform login

teardown - Close browser

### **How does yield works in fixture**

`yield` divides the fixture into two parts,

1. The code before yield is executed before the test case runs (setup).

2. The code after yield is executed after the test case finishes (teardown) including when the test case fails.

### **Scope of fixture**

&rarr; fixture scope determines how frequently a fixture is executed and how long its resources are shared.

&rarr; By default the fixture scope is function.

&rarr; Python provided 5 commonly used scopes for fixtures:

**`1. function`** &rarr; The fixture executes once per every test function that requests it.

```python
@pytest.fixture(scope="function")
```

**`2. class`** &rarr; The fixture executes once per test class and is shared by the test method in that class that requests it.

```python
@pytest.fixture(scope="class")
```

# Date: 9-Nov-2026

**`3. module`** &rarr; A module scope fixture executes once per the python test module and is shared by the test in that module that requests it.

```python
@pytest.fixture(scope="module")
```

**`4. package`** &rarr; A package score fixture executes once per a test package and is shared among test in that package that requests it.

```python
@pytest.fixture(scope="package")
```

**`5. session`** &rarr; A session scope fixture executes once per the pytest session and is shared among tests requesting it through this session.

```python
@pytest.fixture(scope="session")
```

### **What is `yield` in fixture ?**

`yield` is used to provide a resource to a test and then resume fixture execution for teardown.

### **What is `autouse` in fixture ?**

An autouse fixture is automatically executes for applicable tests without explicitly requesting it.

```python
@pytest.fixture(scope="function",autouse=True)
```

&rarr; `autouse=True` does not mean session.

&rarr; `autouse` controls whether a fixture is automatically used by tests, while scope controls how often it runs.
