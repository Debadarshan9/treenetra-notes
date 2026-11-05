# Date: 7-Sept-2026

### **What is HTML**

&rarr; HTML stands for Hyper Text Markup Language.

&rarr; HTML is used to create the structure and content of web page.

**`DOCTYPE html`** &rarr; It defines the document as html file.

**`html`** &rarr; It is the root element of html file.

**`head`** &rarr; It contains the information about the web page.

**`title`** &rarr; It defines the browser tab title.

**`body`** &rarr; It contains the visible web page for text

**`h1`** &rarr; Main heading

**`p`** &rarr; Paragraph

# Date: 8-Sept-2026

### **DOM**

&rarr; DOM stands for `Document Object Model`.

&rarr; It represents and HTML document as a tree like structure of object or element.

### **Locator**

A locator is a way to identify a specific web element on a web page, So that an automation tool can interact with it.

### **Types of Locator**

id, name, classname, tag name, link text, partial text

# Date: 9-Sept-206

### **What is Selenium**

&rarr; Selenium is an open source automation testing framework used to automate web application in different browser.

&rarr; It allows us to automate actions that a real user performs on a website such as open a browser, open a URL, enter username, enter password, click a button, etc.

### **Why we use Selenium**

&rarr; Manual testing becomes repetitive when we need to execute the same test cases again and again.

### **Advantages**

&rarr; It is open source

&rarr; It supports multiple browser

&rarr; It supports multiple programming language

&rarr; It supports windows, linux and mac os

&rarr; It supports parallel execution through `selenium grid`

&rarr; It can integrate with pytest, jenkins and ci/cd

### **What can selenium automate **

Selenium is primarily design for web application

It can automate browser based application

**_NOTE: Selenium can't directly automate desktop application and for mobile application we use `Appium`_**

### **Components in Selenium**

There are 4 components in selenium

### **1. Selenium IDE**

&rarr; It is a browser extension used for record and playback style automation.

&rarr; It is useful for beginners and quick prototypes.

### **2. Selenium RC**

&rarr; RC stands for Remote Control.

&rarr; It was the older selenium automation approach.

### **3. Selenium WebDriver**

&rarr; This is the main component we use for modern selenium automation.

&rarr; It directly communicate with the browser through browser specific drivers.

### **4. Selenium Grid**

It is used when we want to execute test in parallel, on different browser, on different OS, on different machine.

# **Date: 10-Sept-2026**

### **What is Selenium WebDriver**

It is an automation API that allow us to programmatically control and interact with web browser.

### **WebDriver Architecture**

Selenium webdriver architecture is the communication flow through which our automation scripts sends command to the browser and the browser performs those actions on the web application.

```
Test Script ----> Selenium webdriver ---> Browser Driver / webdriver Implement --> Browser --- > Application
```

**Test Script**

This is the code we write using python.

**Selenium webDriver**

Webdriver provides the API methods that we use to automate the browser.

**Browser Webdriver**

The browser specific web driver implementation handles communication with the corresponding browser.

**Web Browser**

The browser receives the command and performs the required action.

**Web Application**

Finally the browser interacts with the web application.

# Date: 13-Sept-2026

### **What is navigation method**

Navigation method is used to navigate between webpage and interact with the browser navigation history

```
get()
back()
forward()
refresh
```

**`get()`** &rarr; Used to open a specific URL in browser

```python
from selenium import webdriver
driver.webdriver.chrome()
driver.get("url")
```

**`back()`** &rarr; It navigates the browser to the previous page in its history

```
driver.back()
```

**`forward()`** &rarr; It navigates the browser to the next page in its history

```
driver.forward()
```

**`refresh`** &rarr; It rewrote the current web page

### **What is web element**

&rarr; A web element is an individual component of a web page that selenium can locate and interact with it

&rarr; Ex: Text box, button, link, checkbox, radio button, drop down and image

### **What is locator**

A locator is a mechanism used to identify a specific web element on a web page

### **Types of locator**

1. id
2. name
3. class name
4. tag name
5. link text
6. partial link text
7. css selector
8. x-path

# Date: 16-Sept-2026

### **ID Locator**

&rarr; It should be unique

&rarr; Always prefer id locator if available

&rarr; ID locator always fast and stable

### **Name Locator**

&rarr; We use name locator when id is not available

&rarr; Name should be unique

### **class name locator**

&rarr; class name must be single value

&rarr; It don't use space and separated class name

# Date: 06-Oct-2026

### **xPath**

&rarr; It stands for xml path.

&rarr; It is used to locate elements in a html or xml doc.

&rarr; We used xpath when id or name is not available.

&rarr; It can handle dynamic elements and it is the most powerful locator in selenium.

### **Types of xpath**

### **1. Absolute xPath**

&rarr; It starts with single slash(/).

&rarr; It instruct the xpath using to search for the element with the root code

&rarr; element identification is faster compare to relative xpath.

### **2. Relative xPath**

&rarr; It starts with (//).

&rarr; It instruct the xpath using to search for the matching element anywhere in the dom.

&rarr; It is slower than absolute xpath.

#### **Syntax for multiple attribute**

```
//tagname[@atr='value' and @atr='value']
```

### **cssSelector**

In selenium a css selector is a way to locate the web element using the css syntax.

1. by id --> #id
2. by class --> .classname
3. tag+id --> tag#id
4. tag+class --> tag.class
5. attribute --> tagname[atr='value']
6. multiple attribute - tagname[atr='value'][atr='value']

### **Link Text**

It is used only for anchor tag.

### **PartialLink Text**

It is used to locate a link when you know parts of it's visible text.

# Date: 7-Oct-2026

### **Web Elements Method**

These methods are function used to interact with elements after locating to dev

**`click()`** &rarr; It is used to click button, link, radio button, checkbox

```
driver.find_element(By.ID, "value").click()
```

**`send_keys()`** &rarr; It is used to type text into input field

```
driver.find_element(By.ID, "value").send_keys()
```

**`clear()`** &rarr; It removes existing text from an input field

```
driver.find_element(By.ID, "value").clear()
```

**`submit()`** &rarr; It submits a form, usually use the forms.

**`text()`** &rarr; It gets visible text

**`get_attribute()`** &rarr; It gets HTML attribute value

**`is_displayed()`**

&rarr; It checks if the element is visible.

&rarr; It returns boolean value.

**`is_enable()`**

&rarr; It checks if the element is enable (clickable).

&rarr; It returns boolean value.

**`is_selected()`**

&rarr; It checks checkbox and radio button selected state.

&rarr; It returns boolean value.

**`size()`** &rarr; It gets element size

```
driver.get_element(By.ID,"value").size()
```

# Date: 9-Oct-2026

### **Wait Mechanism in Selenium**

Waits are used to handle synchronization problem between selenium and web application.

### **Types of wait**

In selenium mainly there are 3 types of wait.

#### **1. Implicit wait**

It is a global wait that apply to every elements.

```python
driver.implicitly_wait(5)
```

**Advantages**

&rarr; It is easy to use.

&rarr; Globally configuration.

**Disadvantages**

&rarr; It applies on every element.

&rarr; Less control.

&rarr; Not suitable for complex application

#### **2. Explicit wait**

&rarr; It waits for a specific condition

&rarr; Mostly used in real project

```python
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC

WebDriverWait(driver,10).until(condition)
```

**`Visibility_of_element_located()`** &rarr; It waits until the element is visible.

**`presence_of_element_located()`** &rarr; Element exist in the DOM.

**`element_to_be_clickable()`** &rarr; Until an element will click.

**`title_contains()`** &rarr; It checks the web application contains the title or not.

**`alert_is_present()`** &rarr; It waits until javascript alert appears.

**`url_contains()`** &rarr; It waits until the url contains the specified text.

| Implicit Wait                                        | Explicit Wait                                             |
| ---------------------------------------------------- | --------------------------------------------------------- |
| It waits for an element to be found                  | It waits for a specific condition                         |
| It applies to a global element searches              | It apply to a particular operation                        |
| Doesn't directly wait for visibility or clickability | It supports condition such as visibility and clickability |
| It is simpler but less flexible                      | More flexible for dynamic web application                 |

#### **3. Fluent Wait**

&rarr; It is the advance version of explicit wait.

&rarr; It allows polling frequency and ignore exception.

**Polling Frequency**

How often selenium checks whether the required condition as become true.

```python
WebDriverWait(driver,
            timeout=20, #It waits for a maximum 20 seconds
            polling_frequency=2, # it checks the condition in every 2 seconds
            ignore_exception=["Timeout Exception"]) # It ignores the exception while waiting

login = wait.until(EC.element_to_be_clickable(By.ID,'btn'))
login.click()
```

**_Note: if the condition is not satisfied within the timeout then selenium raises a time out exception_**

# Date: 12-Oct-2026

### **Dropdown**

&rarr; Dropdown is a web element that display a list of options in selenium.

&rarr; It is created using the HTML `select tag` and handled using the `select class`.

### **Methods of select class**

**`select_by_visible_text()`** &rarr; Select an option on the text visible to the user

```python
dropdown.select_by_visible_text("India")
```

**`select_by_index()`** &rarr; Select an option based on its text position

```python
dropdown.select_by_index(1)
```

**`select_by_value()`** &rarr; Select an option using the value attribute

```python
dropdown.select_by_value("india")
```

```python
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.support.ui import Select
import time

driver = webdriver.Chrome()
driver.maximize_window()
driver.get("https://demo.automationtesting.in/Register.html")
drop_down = Select(driver.find_element(By.ID, 'Skills'))
drop_down.select_by_value("Linux")
time.sleep(1)
drop_down.select_by_visible_text("Analytics")
time.sleep(1)
drop_down.select_by_index(14)
time.sleep(1)
driver.quit()
```

Basically dropdowns are 2 types

### **1. Static Dropdown**

This is created using select tag and handled using `Select` class

### **2. Dynamic Dropdown**

This is created using div, ul, li, js

We can handle dynamic dropdown by using `WebDriverWait(element_to_be_clickable())`

# Date: 13-Oct-2026

### **Checkbox**

It allows user to select one or multiple options.

### **Methods for checkbox**

**`1. click()`** &rarr; It select and unselect the checkbox

**`2. is_selected()`** &rarr; It is used to verify checkbox status

### **Radio Button**

It allows user to select one option from the list.

### **Methods for checkbox**

**`1. click()`** &rarr; It select and unselect the radio

**`2. is_selected()`** &rarr; It is used to verify radio status

### **Alert**

Alert is a pop up message display by the browser.

### **Types of alert**

**1. Simple alert**

It contains only `OK`

**2. Confirmation alert**

It contains `OK` and `cancel`

**3. Prompt alert**

It contains a text box, ok and cancel

### **How to handle alert**

```python
driver.switch_to.alert()
```

**`accept()`** &rarr; It click to `ok`

**`dismiss()`** &rarr; It click to `cancel`

**`send_keys()`** &rarr; It types text input prompt

# Date: 14-Oct-2026

### **iFrame**

&rarr; An `iFrame` is an HTML element that embeds another HTML document within the current web page.

&rarr; Selenium must switch into that iframe before interacting with its internal elements.

### **Methods to switch to iframe**

```python
driver.switch_to.frame()
```

1. switch by index

2. switch by id

**`driver.switch_to.default_content()`** &rarr; It switch back to the main page.

**`driver.switch_to.parent_frame()`** &rarr; It switch back to the parent frame.

| default_content()         | parent_frame()                |
| ------------------------- | ----------------------------- |
| It goes to the main page  | It goes one level up          |
| It contains root document | It contains only parent frame |

# Date: 15-Oct-2026

### **Window Handle**

Window handle is the process of switching between multiple browser. window, tabs during automation.

### **How to handle multiple windows**

```python
driver.current_window_handle # It returns the unique handle of the current browser window.

driver.window_handles # It returns a list of handles of all the open browser windows.

driver.switch_to.window(handle) # It switches selenium focus to the specified window.

driver.close() # It closes the current browser window.

driver.quit() # It closes all the browser windows and ends the WebDriver session.
```

# Date: 21-Oct-2026

### **What is web table**

A web table is used to display data in rows and columns in a web page such as employee details, student marks, product details, order history etc.

### **Tags in a web table**

**`<table>`** &rarr; It defines the table

**`<thead>`** &rarr; It defines the header section

**`<tbody>`** &rarr; It groups the data rows

**`<tr>`** &rarr; It defines a table row

**`<th>`** &rarr; It defines the header cell

**`<td>`** &rarr; It defines the data cell

**`<tfoot>`** &rarr; It groups the footer section

### **Types of table**

There are 2 types of web table

#### **1. Static Table**

The table structure and data are already present in the HTML and don't change dynamically during interaction.

#### **2. Dynamic Table**

Based on search, filter, pagination or user

# Date: 22-Oct-2026

### **How to handle web table in selenium**

&rarr; If the table uses pagination I navigate through the page until the record is found or no more pages is available.

&rarr; For asynchronous update I use explicit wait to ensure the latest data is loaded.

### **What is action class**

action class is used to perform advanced mouse and keyboard operation that can't be done using selenium methods.

| action         | method            | purpose                          |
| -------------- | ----------------- | -------------------------------- |
| mouse hover    | move_to_element() | Move the mouse over an element   |
| left click     | click()           | Click an element                 |
| right click    | context_click()   | Open the context menu            |
| double click   | double_click()    | Double click an element          |
| drag & drop    | drag_and_drop()   | Move an element to another       |
| click and hold | click_and_hold()  | Hold the left mouse button       |
| release        | release()         | Release a hold mouse button      |
| keyboard input | send_keys()       | Send keys to the focused element |
| key down       | key_down()        | Press a modifier key             |
| key up         | key_up()          | Release a modifier key           |

```python
from selenium.webdriver.common.action_chains import ActionChains

ActionChains(driver).move_to_element(element).perform()
ActionChains(driver).click(element).perform()
```

# Date: 23-Oct-2026

### **Screenshot**

&rarr; A screenshot is an image captured during test execution to record the current state of the application.

&rarr; Ex: test failure evidence, bug reporting, debugging an reporting.

```python
driver.save_screenshot("screenshot.png")
```

### **File upload in selenium**

&rarr; File upload is the process of sending a file from local machine to a web application.

&rarr; Ex: resume upload, profile picture upload, document upload.

### **How to upload a file in selenium**

Selenium uploads a file using the `send_keys()` by passing the complete file path.

```python
file_input = driver.find_element(By.XPATH, "//input[@type='file']")
file_input.send_keys("/path/to/your/file.txt")
```

### **File download in selenium**

File download means downloading a file from a web application and verifies that it exists in local machine.

```python
download_path = os.path.join(os.path.expanduser("~"),"download")
files = os.listdir(download_path)

if files:
    print("File is exist")
else:
    print("File is not exist")
```

### **Drag & Drop**

It is an action where an element is dragged from one location and dropped on another location.

```python
ActionChains(driver).drag_and_drop(source,destination).perform()
```

# Date: 26-Oct-2026

### **What is Javascript Execution**

&rarr; It is an interface provided by selenium that allow us to execute javascript code directly inside the browser through selenium webdriver to interact with web elements, modify the page property, retrieve information or perform browser side operation.

&rarr; We need to get information from DOM.

&rarr; We need to interact with certain element using JS.

&rarr; We need to inspect or modify certain browsers side properties during testing.

```python
# 1. Click using JS
driver.execute_script("arguments[0].click();",element)

# 2. Scroll down
driver.execute_script("window.scrollTo(0,500);")

# 3. Scroll up
driver.execute_script("window.scrollTo(500,0);")

# 4. Scroll right
driver.execute_script("window.scrollTo(document.body.scrollWidth,0);")

# 5. Scroll left
driver.execute_script("window.scrollTo(0,0);")

# 6. Get page title
title = driver.execute_script("return document.title")

# 7. Enter text using js
driver.execute_script("arguments[0].value='Python';",element)

# 8. Refresh the browser
driver.execute_script("history.go[0];") # Refresh the current page
driver.execute_script("location.reload();") # Reloads the current URL
```

# Date: 27-Oct-2026

## **Exception**

An Exception is an unwanted event that occurs during program execution and stop the normal flow of the program

### **Why Exception occurs**

1. Wrong locator

2. Slow page loading

3. DOM change

4. Frame not switched

5. Window not switched

## **Examples of some exception**

### **1. NoSuchElementException**

&rarr; It occurs when selenium can't find the element

&rarr; Element not loaded

&rarr; Element removed

&rarr; Element hidden

### **How to handle it**

&rarr; We used wait like `webDriverWait` mechanism.

&rarr; Correct locator

&rarr; Exact iFrame

### **2. StaleElementReferenceException**

&rarr; It occurs when the previously located element is no longer attached to the DOM.

### **How to handle it**

&rarr; Relocate the element

# Date: 28-Oct-2026

### **3. TimeOutException**

It occurs when explicit wait times out

### **How to handle it**

&rarr; Increase the wait

&rarr; Verify the locator

&rarr; Check page loading

### **4. ElementNotInteractableException**

If element exist but can't interactable with

### **How to handle it**

&rarr; Visibility of element locator

&rarr; Scroll into view

### **5. ElementClickInterceptedException**

Another element blocks the click

### **How to handle it**

&rarr; Use Explicit wait

&rarr; Use javascript click

### **6. NoSuchFrameException**

It occurs when the frame doesn't exist

### **How to handle it**

&rarr; Locate the frame

&rarr; Count the frame

### **7. NoSuchWindowException**

It occurs when selenium switch a window that doesn't exist

### **How to handle it**

&rarr; Switch to corresponding window

### **8. InvalidSelectorException**

When xpath or css selector is invalid

### **How to handle it**

&rarr; Locating correct xpath or css selector

### **9. InvalidElementStateException**

It occurs when selenium tries to perform an action on a web browser, but the element is not a state that allows the action.

### **How to handle it**

&rarr; Check element is enable

&rarr; Using js execution

### **10. WebDriverException**

It occurs when parent exception of many selenium exception (browser close sudden, no internet, invalid url etc.)

## **Important Questions**

1. What is webdriver?

2. Difference between find_element and find_elements?

3. How to handle a dropdown in selenium?

4. What is iFrame and how to handle to it?

5. What is alert and pop up? How to handle it?

6. What is the difference between implicit wait and explicit wait?

7. How we handle multiple windows in selenium?

8. Why we use playwright over selenium?

9. What is difference between is_displayed(), is_enable() and is_selected()?

10. What is difference between xpath and css selector?

11. What is difference between absolute xpath and relative xpath?
