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
| Supports by java, pytho, c#, js, ruby     | ts, js, java, python, .net           |
| Waits implicit, explicit, fluet           | Auto-wait                            |
| Slower                                    | Faster                               |
| Api test not possible                     | Api test possible (APICONTEXT)       |
| Network injection possible, request setup | Directly possible                    |
| No parallel testing                       | Built-in parallel testing            |
| echo system                               | no echo system                       |
