# Date: 21-Sept-2026

### **Playwright**

&rarr; It is an open source browser automation framework developed by microsoft.

&rarr; It is mainly used to automate and test modern web application.

```text
Selenium
    ↓
   URL
    ↓
w3cprotocol
    ↓
Webdriver (API Request)
    ↓
Browser
```

### **Playwright Architecture**

```text
Test Runner
    ↓
Test Script
    ↓
Playwright API
    ↓
Playwright WebDriver
    ↓
Browser
    ↓
Browser Context
    ↓
Page (Tab)
    ↓
Web Application
    ↓
Backend API
    ↓
Template & Database
    ↓
Response
```

### **Test Runner Layer**

Test runner manages the complete test life cycle

Test runner perform

1. Test Discovery
2. Test collection
3. Test execution
4. Feature execution
5. Parallel execution
6. Retrieve management
7. Time out management
8. Assertion handling
9. Test result collection
10. Report generation

### **Playwright With Node.js Architecture**

```text
Test Script
    ↓
Playwright test runner
    ↓
Node.js worker process
    ↓
Playwright core API
    ↓
Browser
    ↓
Response
```

### **Selenium VS Playwright**

| Selenium                                  | Playwright                           |
| ----------------------------------------- | ------------------------------------ |
| Developed by open-sources community       | Developed by microsoft               |
| W3C architecture                          | Browser specific automation protocol |
| Chrome, Edge, Firefox, Safari, IO         | Chromium, Firefox and webkit         |
| Supports by java, python, c#, js, ruby    | ts, js, java, python, .net           |
| Waits implicit, explicit, fluent          | Auto-wait                            |
| Slower                                    | Faster                               |
| Api test not possible                     | Api test possible (API CONTEXT)      |
| Network injection possible, request setup | Directly possible                    |
| No parallel testing                       | Built-in parallel testing            |
| echo system                               | no echo system                       |

# Date: 22-Sept-2026

create venv - `python -m venv venv`
activate venv - `. venv/Scripts/activate`
upgrade pip - `python -m pip install --upgrade pip`
install package - `python -m pip install package_name`

for playwright:
download playwright - `python -m pip install playwright`
install playwright - `python -m playwright install`

# Date: 22-Sept-2026

### **Browser**

A browser represents a running browser process connect by `playwrightContextManager` through playwright core API.

`browser = p.chromium.launch()`

### **Browser Context**

&rarr; Browser context is an independent isolated browser session.

&rarr; It behaves similarly to an incognito window.

&rarr; Each context has separate cookies, localstorage, session storage, authentication state, cache, permissions, geo-locations, local timezone.

### **Page**

&rarr; A page represents one browser tab or pop window.

&rarr; A page is used to open urls, find elements, enter data, handling the browser actions(click, scroll, dropdown(selective and auto-selective), alert popup, window handle, iframe, shadow DOM, screenshot, monitoring network calls, validate application behavior).

### **page.goto()**

&rarr; It opens the browser with the help of url.

&rarr; We have to close the browser after finish the task with `browser.close()`

### **Locator**

&rarr; Locator is a absolute value of web browser location and they have a specific address and path

Playwright has 8 type of locators

1. getByRole()
2. getByLabel()
3. getByPlaceholder()
4. getByText()
5. getByTestId()
6. CSS Selector
7. XPath Selector
8. ID Selector

# Date: 25-Sept-2026

| Locator                  | Selector                     |
| ------------------------ | ---------------------------- |
| Who have actual location | Who provides way of location |

```python
# id
page.locator("#username").fill("Debadarshan")

# classname
page.locator(".login-btn").click()
```

```python
tagname[attribute = "value"] -- css

//tagname[@attribute = "value"] -- x-path

```

| CSS    | X-Path |
| ------ | ------ |
| Faster | Slower |

css --> input[name = "email"]

x-path --> //input[@name = "email"]

### **Types of x-path**

There are 2 type of x-path

#### **absolute**

&rarr; The absolute x-path gives the complete path from the root of the html document to element.

// - node

/ - follows

```
(//main/section/div[2]/input)[2]
```

#### **relative**

&rarr; Relative x-path finds an element from anywhere in the DOM using attributes, text or relationships.

```
//tagname[@attribute = "value"]
```

### **X-Path Functionality**

**`text()`**

```
//button[text() = "Search"]
```

**`contains()`**

```
//div[contains(@class, "product-card")]
```

**`starts-with()`**

```
//div[starts-with(@id,"product_202")]
```

**`normalize-space`**

```
//p[normalize-space() = "Selenium Webdriver"]
```

**_Used when there is extra space in the text_**

# Date: 28-Sept-2026

**`parent`**

Parent tag hit the above parent

```
//span[text() = "Ravi Kumar"]/parent::li/parent::ul
```

**`following-sibling`**

It is used to find the next sibling element

```
//span[text() = "Ravi Kumar"]/following-sibling::span
```

**`preceding-sibling`**

It is used to select the previous tag

```
//div[@data-source="playwright"]/preceding-sibling::div
```

ancestor works like a grand parent

```
//p[text()=""]/ancestor::section/preceding-sibling::section
```

# Date: 09-Oct-2026

### **Assertion**

It is a validation check point used to automation test to compare the actual result with expected result

There are 2 types of assertion

#### **1. Hard Assertion**

&rarr; It immediately raise an exception when validation fails.

&rarr; The remaining statement in the current test function will not execute unless the exception is handled.

#### **2. Soft Assertion**

&rarr; It records assertion failure but allows the remaining validation to execute.

&rarr; At the end the collected failure are reported together.

```python
# URL Validation
expect(page).to_have_url(url)

# Title validation
expect(page).to_have_title(title)

# Text validation
expect(page).to_have_text(text)

# Visibility Validation
expect(page.locator("#id")).to_be_visible()

# Enable Validation
expect(page.locator("#id")).to_be_enabled()

# Enable Validation
expect(page.locator("#id")).to_be_disabled()
```
