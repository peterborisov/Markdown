1. HTTP - Hypertext Transfer Protocol
2. API - Application Programming Interface
3. REST - Representational State Transfer
4. XML - eXtensible Markup Language
5. JSON - Javascript object notation
6. SOAP - Simple Object Access Protocol
7. Apps

## HTTP - Hypertext Transfer Protocol

> The HTTP is an application layer protocol, for sending and receiving messages over a network(client <-> server communication).<br/>
The HTTp is the messenger of the web.<br/>
It is a TCP/IP based protocol.<br/>
It is used to deliver contents(images, videos, audios, documents, etc.)

> Every time you type URL in the browser, we use HTTP/ HTTPS
<img src="./assets/url.png" width="500">


#### Important things about HHTP

1. HTTP is **connectionless**: after request, the client disconnect from server,
when response is ready, server re-establish the connection.
2. HTTP is **media independent**:HTTP can deliver any data, as long as two computers can read it. 
3. HTTP is **stateless**: client and server know about each other, just during the current request. If it closes and want to connect again, the connection is handled as first one.

<img src="./assets/how-http-works.png" width="500">
<img src="./assets/http-messages.png" width="500">
<img src="./assets/http-req-res.png" width="500">

#### HTTP request:
1. Start line - 
    - version(1.1), 
    - methods(get, post, put, delete), 
    - API program folder location(URI/search), 
    - parameters(?q=tuna),
    - format
2. Headers - 
    - host, 
    - token,
    - https://en.wikipedia.org/wiki/List_of_HTTP_header_fields 
3. Blank line - separate header from body
4. Body - username/pass
 
#### HTTP response: same parts
1. Start line - +status code(200 ok)
2. Headers - cookie
3. Blank line
4. Body - html

## API Aplication Programming Interface

> An API is the way to let software components to talk to each other. Give us access to additional functionality. 

<img src="./assets/api.png" width="500">

## REST - REpresentational State Transfer
> REST API is an API that follows the rules of REST specification.<br/>
REST is a specification that dictates, how systems on the web should comunicate.<br/>
REST is a way to implement and use HTTP.<br/>
<img src="./assets/rest-api.png" width="500">

1. **Client-Server**. SystemA makes an HTTP request to a URL hosted by SystemB, which returns a response.
2. **Stateless**. The client request should contain all the information necessary to respond to a request. In other words, it should be possible to make two or more HTTP requests in any order and the same responses will be received.
3. **Cacheable**. A response should be defined as cacheable or not.
4. **Layered**. The requesting client need not know whether it’s communicating with the actual server, a proxy, or any other intermediary.
## Web Service
> Web services are set of rules and technologies that enable two or more components **on the web** to talk to each other<br/>
API over internet - web service.<br/>
Not every API is a web service

https://www.tutorialspoint.com/webservices/what_are_web_services.htm<br/>

web = internet<br/>
service = API<br/>
Web service = API that uses the internet<br/>

Web service use:<br/>
 - XML or JSON to format data over the internet
 - REST, SOAP or XML/RPC to transfer that data

## XML - eXtensible Markup Language

HTTP header - content-type: application/xml<br/>
HTTP body: XML<br/>

## JSON - Javascript object notation
> Data representation format.<br/>
Keys must be strings, and values must be a valid JSON data type (string, number, object, array, boolean or null).

HTTP header - content-type: application/json<br/>
HTTP body: JSON<br/>

## SOAP - Simple Object Access Protocol
>Rules to form HTTP req/res

Uses s WSDL(web services description language)<br/>

1. Start line - POST WSDL HTTP version
2. Headers - content-type: text/xml
3. Blank line
4. Body - xml envelope formed using WSDL

## Apps

- Native
- Web
- Hybrid

## Web Worker

- Web workers provide a mechanism to spawn a separate script in the background
- Basic communication happens between UI and web worker using following API
  - postmessage() - to send message
  - onmessage() - to receive message
  - myWorker.terminate() - to terminate the worker thread

#### Web workers use cases

- Data and web page caching
- Image encoding - base64 conversion
- Canvas drawing
- Network polling and websockets
- Background I/O operations
- Video/audio bu

## Server-side rendering SSR vs Client-side rendering CSR

### Client-side rendering

- When the browser makes a request to the server
  - HTML is returned as response
  - But no content yet
  - Browsers gets almost empty document
  - User sees a blank page until other resources such as JavaScript, styles, etc are fetched
  - Browser compiles everything then renders the content
- Steps involved
  - Download HTML
  - Download styles
  - Download JS
  - Browser renders page
  - Browser compiles and executes JavaScript
  - The page is then viewable and interact-able

#### Advantages of Client-Side Rendering

- Lower server load since the browser does most of the rendering
- Once loaded pages don't have to be re-rendered so navigating between pages is quick

#### Disadvantages of Client-Side Rendering

- Initial page load is slow
- SEO (Search Engine Optimization) may be low if not implemented correctly

### Server-side rendering

- When the browser makes a request to the server
  - Server generates the HTML as response plus the content
  - Server sends everything - HTML, JS to render page
  - So, the page is viewable but not interact-able
- Steps involved
  - Server sends ready to be rendered HTML, JS, and all the content
  - Browser renders page - the page is now viewable
  - Browser downloads JavaScript

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
