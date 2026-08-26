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

# Date: 25-August-2026

### **HTTP Methods - CRUD**

**GET**

GET method works like read. It will read specific data and all data and it fetchs data from API.

**POST**

Post method creates the data to a specific resource, often causing a change in server state for creating a new resource.

**PUT (Update or replace)**

&rarr; If the resource is present it will replace all current representations of the target resource with the uploaded request content.

&rarr; If the resource is not present then it will create a new resource.

**PATCH**

Applies partial modification to a resource instead of replacing it entirely.

**DELETE**

Permanetly remove the specified resource from the server.

### **Status Code**

100 - continue

102 - processing

200 - ok

201 - created

202 - accepted

204 - no content

#### **Client Side Error (4xx)**

&rarr; Problem with the request credential or permissions.

#### **400 - Bad Request**

&rarr; The server can't process the request because it is malformed or invalid.

**Main cause of bad request**

Malfromed json, missing mandatory field, wrong datatype, invalid query parameter.

### **Authentication**

&rarr; Authentication means verifies user identity.

&rarr; It asks are you, who you claimed to be ?

&rarr; It used credential like password, pin or biometrics.

&rarr; It happens first in the security process.

### **Authorization**

&rarr; Determines access rights on permission.

&rarr; It ask what resources can you access ?

&rarr; Uses rules like user role or action levels.

&rarr; It happens after successfull authentication.

#### **401 - Unauthorized (Authentication)**

The request doesn't contain valid authentication credentials, It means the user is not authenticated.

**Cause for unauthorized**

Missing token, invalid token, Expired token, invalid username or password.

#### **403 - Forbidden (Authorization)**

The client may be authenticated but they don't have permission to perform the requested action.

**404 - Not Found**

&rarr; The requested resource or endpoint was not found or unavailable.

&rarr; The API may intensionaly return 404 to a protected resource existance.

**Causes for not found**

Resource id doesn't exist, incorrect endpoint path, resource was already deleted.

**409 - Conflict**

&rarr; The request conflicts with the resources current state or a uniqueness rule.

**429 - Too many requests**

&rarr; The client has exceed the server's request rate

**cause for too many requests**

An API permits 100 requests per minute but client sends 150

# Date: 26-August-2026

### **Server Side Error (5xx)**

#### **500 - Internal Server Error**

The server encounters an unexpected condition while processing the request.

#### **501 - Not Implemented**

The server doesn't support the functionality required to process the request.

#### **502 - Bad Gateway**

A gateway or proxy receieved an invalid response from an offstream server.

#### **503 - Service Unavailability**

The server is temporarily unavailable to process the request.

### **504 - Gateway Timeout**

A gateway or proxy didn't receive a request from an offstream server within the allowed time.
