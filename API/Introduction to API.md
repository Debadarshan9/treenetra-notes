# Date: 21-August-2026

### **What is API?**

&rarr; API stands for Application Programming Interface.

&rarr; An API is a defined way for one software component to request data or an action from another software component.

&rarr; The requester does not know the internal code database designed or implementation details of the provider.

**1. Customer** &rarr; Client

**2. Menu** &rarr; API documentation

**3. Waiter** &rarr; API endpoint / communication layer

**4. Order** &rarr; API Request

**5. Kitchen** &rarr; Backend / Business Logic

**6. Ingedients** &rarr; Database or External services

**7. Prepared Food** &rarr; API responses

### **Endpoint**

```
http://www.domain.ext
```

&rarr; The address of resuource or operation through path parameter and query parameter.

### **Method**

&rarr; API does the CRUD operation

&rarr; Ex: GET, POST, PUT, PATCH, DELETE

### **Header**

Metadata such as `content-type`, `accept` and `authorization`

**1. Content-type** (JSON, XML, YML>)

**2. Authorization** (OTP, Token, Captcha)

### **Parameter**

1. Path Parameter

2. Query Parameter (For Specific resource)

### **Body**

Structure input and output data (commonly used JSON in API)

### **Response**

`Status code`, `header` and `optional body` return by the server

### **Types of API**

There are 6 types of API

1. Composite API

2. REST API (JSON, Fast)

3. SOAP API (XML, Slow)

4. GraphQL API

5. GRDC API

6. WebSocket API Hardware communication

# Date:23-August-2026

### **REST API**

&rarr; Rest API is an architect style define through concentrate such as client server separation, status communication, catching a uniform interface.

&rarr; Client exchange the representaion commonly on `JSON`, HTTP methods: `GET`, `POST`, `PUT`, `PATCH` and `DELETE`.

&rarr; Status means each request carries the information into process it.

**_NOTE: The server doesn't depend on hidden conventional context from the previous request._**

### **SOAP API**

&rarr; SOAP is a protocol for exchange in structured message, SOAP message using XML and for security it uses WSGI.

&rarr; SOAP is secure than rest API but slower than it.

### **HTTP**

&rarr; HTTPS stands for Hyper Text Transfer Protocol and it is an application layer.
