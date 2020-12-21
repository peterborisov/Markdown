## API
---
A - Aplication - Software that does s task<br/>
P - Programming - Program that does the task in the Aplication<br/>
I - Interface - Place to tell the program to run<br/>

> Interface that run program, owned by aplication. <br/>
Example:<br/>
Viber message using cell phone.<br/>
A - Viber<br/>
P - messaging<br/>
I - cell phone<br/>

## Web Service
---
> Web services include any software, application, that provides web protocols (HTTP or HTTPS) to communicate, and exchange data messaging – usually XML (Extensible Markup Language) – throughout the internet.<br/>
API over internet - web service.

https://www.tutorialspoint.com/webservices/what_are_web_services.htm<br/>

web = internet<br/>
service = API<br/>
Web service = API that uses the internet<br/>

Web service use:<br/>
 - XML or JSON to format data over the internet
 - REST, SOAP or XML/RPC to transfer that data

## HTTP
Hypertext Transfer Protocol

---
HTTP request:
1. Start line - 
    - version(1.1), 
    - methods(get, post, put, delete), 
    - API program folder location(/search), 
    - parameters(?q=tuna),
    - format
2. Headers - 
    - host, 
    - token,
    - https://en.wikipedia.org/wiki/List_of_HTTP_header_fields 
3. Blank line - separate header from body
4. Body - username/pass
 
HTTP response: same parts
1. Start line - +status code(200 ok)
2. Headers - cookie
3. Blank line
4. Body - html

## XML
eXtensible Markup Language

---
HTTP header - content-type: application/xml<br/>
HTTP body: XML<br/>

## JSON
Javascript object notation

---
HTTP header - content-type: application/json<br/>
HTTP body: JSON<br/>

## SOAP
Simple Object Access Protocol - rules to form HTTP req/res<br/>

---
Uses s WSDL(web services description language)<br/>

1. Start line - POST WSDL HTTP version
2. Headers - content-type: text/xml
3. Blank line
4. Body - xml envelope formed using WSDL

## REST
Representational State transfer

---
- Cache
- Stateless

1. Start line - All methods
2. Headers - All
3. Blank line
4. Body - JSON, XML, images, html web page, ets.

## Apps
---
- Native
- Web
- Hybrid
