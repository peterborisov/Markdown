## What is HTTP

- Hyper Text Transfer Protocol
- It defines set of rules for sending and receiving (transfer) web pages (hypertext)
- It is a simple request -> response cycle between a local machine called as client and a
  remote machine called as server
- When a request is made it has 3 main pieces

```
Start-line(Method, target, version => ex: GET /image.jpg HTTP/2.0)
Headers
Body
```

- When a response is send back it also has 3 main pieces

```
Start-line(Version, status code, status text => ex: HTTP/2.0 404 Not Found)
Headers
Body
```

#### HTTP is a stateless protocol

- It treats each pair of request and response independent
- It does not require to store session information

#### HTTP Headers

- Information about client and server systems are transmitted through HTTP headers
- For ex: timestamps, IP addresses, server capabilities, browser information, cookies

- **General headers**
  - Request URL: https://www.ngninja.com
  - Request Method: GET
  - Status Code: 200 OK
- **Request Headers**
  - Accept: text/html
  - Accept-Language: en-US,en
  - Connection: keep-alive
  - Host: ngninja.com
  - User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10_13_6
  - Cookie: key=value; key2=value2; key3=value3
- **Response Headers**
  - Connection: keep-alive
  - Content-Encoding: gzip
  - Content-Type: application/json
  - Server: nginx
  - X-Content-Type-Options: nosniff

## Web Services

- They are reusable application components => Ex: currency conversion app, weather app
- These applications are mainly based on open standards like XML, HTTP, SOAP,etc.
- They are self-contained, modular, distributed, dynamic applications
- They use standardized XML messaging system

- Web services work using the following components
- SOAP
  - Simple Object Access Protocol
  - It is a communication protocol
  - Used to transfer messages
  - It uses the internet to communicate
  - XML based messaging protocol
- WSDL
  - Web Services Description Language
  - Used describe the availability of service
  - This is written in XML
  - It is used to describe operations and locate web services

## RESTful web services - REST API

- REST is an architectural style
- REpresentational State Transfer (REST)
- It is a stateless client-server architecture
- Web services are viewed as resources and they are identified by the URLs
- Web clients can access or modify these REST resources
- It is often used in mobile applications, social networking sites
- REST lets us use HTTP for all four CRUD (Create/Read/Update/Delete) operations

## GraphQL

- It is an open-source server-side technology
- It is an execution engine and a data query language
- GraphQL is used to interact with server data source
- There are two types of operations you can perform
  - Queries => read the data
  - Mutations => create, update or delete the data
