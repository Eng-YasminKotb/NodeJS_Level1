## Implementing Express in NodeJS:

`Express`: is a lightweight module that:
 - wraps the functionality of the NodeJS http modulr in a simple to use interface.
 - extends the fuctionality of the http module to make it easy for you to handle server routes, **responses**, **cookies**, and **statues of HTTP requests**.

  #### To install Express run the following command:
  ```javascript
 npm install express
```
once you have installed the express, you need to create an instance of the express class

```javascript
var express= require('express')
var app =express()
```
## Advantages of Express Middlewar HTTP Module: 
- support serving static files
- implement cookies
- support sessions

## Express Middlewar Components:
  - **Logger** : implements a formatted request logger to track requests to the server
  - **Static** : Allows the express server to stream static file get requests
  - **Favicon** : Support sending the favicon to the browser
  - **BasicAuth**: Support for basic HTTP authentication
  - **CookieParser**: allows you to read cookies from the request and set cookies in the response
  - **Session**: provides a robust session implementation
  - **BodyParser**: parses the body data of POST requests into the req.body property
  - **Query**: converts the query string to a JavaScript object and stores it as req.query
  - **Compress**: provides Gzip compress support for large responses to the client
