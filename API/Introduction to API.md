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

6. WebSocket API (Hardware communication)

# Date:23-August-2026

### **REST API**

&rarr; Rest API is an architect style define through concentrate such as client server separation, status communication, catching a uniform interface.

&rarr; Client exchange the representaion commonly on `JSON`, HTTP methods: `GET`, `POST`, `PUT`, `PATCH` and `DELETE`.

&rarr; Status means each request carries the information into process it.

**_NOTE: The server doesn't depend on hidden conventional context from the previous request._**

### **SOAP API**

&rarr; SOAP is a protocol for exchange in structured message, SOAP message using `XML` and for security it uses `WSGI` or `WSDL`.

&rarr; SOAP is secure than rest API but slower than it.

# Date: 24-August-2026

### **HTTP**

&rarr; HTTPS stands for Hyper Text Transfer Protocol and it is an application layer, request and response protocol.

&rarr; A client sends a request message and server sends a response message.

&rarr; HTTP is stateless at the protocol interaction level, each request is interrupted at the information available in that request and relavant server side resoource state.

## **HTTPS**

&rarr; HTTPS is http carried over a `TLS` and `SSL` protected connection.

&rarr; TLS provides encryption intrangit, integrrative protection and server authentication through certificates.

&rarr; It helps prevent external dropping and tampering between client and server.

| http       | https                                     |
| ---------- | ----------------------------------------- |
| http://    | https://                                  |
| 80         | 443                                       |
| Plain Text | Message are encrypted after TLS handshake |

### **Request and Response Life Cycle**

1. The client constructs a URL, method, headers and optional body

2. DNNS resolves the host name to an IP address.

3. A network connection is established, For https a TLS handshake authenticates the server

4. The request passes through components, such as CDN, loader balancer, reverse proxy or API gateway.

5. The application authenticates, authorizes and validates the request.

6. Basd on the business logic call the database, caches, queues, frontend and downstream API.

7. The server builds the status code, headers and response body.

8. The response returns through the network to the client

9. The client parses the response and updates UI.

**_NOTE: When an API fails locate the stages, DNS, TLS, gateway, auhentication, validation, databases, dependencies, serialization, status code all are the root cause._**
