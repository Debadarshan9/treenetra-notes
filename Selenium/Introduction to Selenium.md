# Date: 7-Sept-2026

### **What is HTML**

&rarr; HTML stands for Hyper Text Markup Language.

&rarr; HTML is used to create the structure and content of web page.

**`Docktype html`** &rarr; It defines the document as html file.

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

A locator is a way to identiy a specific web element on a web page, So that an automation tool can interact with it.

### **Types of Locator**

id, name, classname, tagname, link text, partial text

# Date: 9-Sept-206

### **What is Selenium**

&rarr; Selenium is an open source automation testing framework used to automate web application in different browser.

&rarr; It allows us to automate actions that a real user performs on a website such as open a browser, open a URL, enter username, enter passwork, click a button, etc.

### **Why we use Selenium**

&rarr; Manual testing becomes repeatative when we need to execute the same test cases again and again.

### **Advantages**

&rarr; It is open source

&rarr; It supports multiple browser

&rarr; It supports multiple programming language

&rarr; It supports windows, linux and mac os

&rarr; It supports parallel execution through `selenium grid`

&rarr; It can integgrate with pytest, jenkins and ci/cd

### **What can selenium automate **

Selenium is primarily design for web application

It can automate browser based application

**_NOTE: Selenium can't directly automate desktop application and for mobile application we use `Appiom`_**

### **Components in Selenium**

There are 4 components in selenium

### **1. Selenium IDE**

&rarr; It is a browser extension used for record and playback style automation.

&rarr; It is usefull for beginers and quick prototypes.

### **2. Selnium RC**

&rarr; RC stands for Remote Control.

&rarr; It was the older selenium automation approach.

### **3. Selenium WebDriver**

&rarr; This is the main component we use for morden selenium automation.

&rarr; It directly communicate with the browser through browser specific drivers.

### **4. Selenium Grid**

It is used when we want to execute test in parallel, on different browser, on different OS, on different machine.

# **Date: 10-Sept-2026**

### **What is Selenium WebDriver**

It is an automation API that allow us to programatically control and interact with web browser.

### **WebDriver Architecture**

Selenium webdriver architecture is the communtication flow through which our automation scripts sends command to the browser and the browser performs those actions on the web apllication.

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

**`back()`** &rarr; It navgates the browser to the previous page in its history

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
5. link test
6. partial link test
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
