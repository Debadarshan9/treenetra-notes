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
3. Test exection
4. Feture execution
5. Parallel execution
6. Retrive management
7. Time out management
8. Assertion handling
9. Test result collection
10. Report generation

### **Playwright With Node.js Achitecture**

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
| Waits implicit, explicit, fluet           | Auto-wait                            |
| Slower                                    | Faster                               |
| Api test not possible                     | Api test possible (APICONTEXT)       |
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

&rarr; Each context has separate cookies, localstorage, session storage, authentication state, cache, permissions, geolocations, local timezone.

### **Page**

&rarr; A page represents one browser tab or pop window.

&rarr; A page is used to open urls, find elements, enter data, handling the browser actions(click, scroll, dropdown(selective and autoselective), alert popup, window handle, iframe, shadow DOM, screenshot, monitoring network calls, validate application behaviour).

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
