## Client-Server Model 💻
- is a distributed application framework dividing tasks between servers and clients
- The client relies on sending a request to server in order to access a service made available by a server
- The server runs one or more programs that share resources with and distribute work among clients
- The client server relation ship communicates in arequest-response messaging pattern

## HTTP (Hypertext Transfer Protocol)
 - is a protocol which allows the fetching of resourses, such as HTML documents
 - It is the foundation of any [data exchange] on the web and it it a client server protocol, which means requests are initiated by the recipient,usually the Web browser.

## Implementing HTTP Services in NodeJS: 
- One of the most important aspects of NodeJS is the ability to quickly implements 
  HTTP and HTTPS servers and services.
- NodeJS provides the http and https modules to do most everything you need from an HTTP and HTTPS
- it is not difficult to implement a full webserver using just the http module
  
  #### Note:
  -Why use Express module if we can use HTTP module?? ( interview question)
  This is because the http module is pretty low level0 It doesn't provide calls to handle routing, 
   cookies,caching
  
## Processing URL:
   - Act as an address label for the HTTP server to handle requests from the client
   - It provides all the information needed to get the request to the correct server on a specific port 
     and access the proper data.

## Understanding Request and Response Objects in HTTP :

  #### HTTP Moudle 
  consists of two objects:
  
  1- Request 
  
  2- Response
  
  ##### Request:
  
  - is created internally when you call http.request(options, callback).
  - Use Request object to initiate, monitor, and handle the response from the server.
  - It implements a writable stream, so it provides all the functionality of a writable stream object.




## Understanding HTTP server in NodeJS :
 - It provides an underlying socket that listens on a port and handels receiving requests and then sends responses 
   out to client connection.
 - The server object implement EventEmitter and emits the events
 - To stat the HTTP server, you need to first create a Server Object using the `createServer()`.
 - Once you havve created the server object ,you can begin listening on it by calling the listen() method on the 
   Server object.
   #### Steps to create a HTTP Server:
   
   1- import the module by requiring it.
   
   2- use  `createServer()` function.
   
   3- listen on it.
   **EX:**
   ##### to run this code :
   1- node (file name)
   2- on your browser write `localhost:protnumber`  ///write your port 
   ```javascript
   const http =require('http')

   const server = http.createServer((req,res)=>{
    res.end("Hello!!");
    })

    server.on(('clientError'),(err, socket)=>{
    socket.end('HTTP/1.1 400 Bad Request\r\n\n\n');

   });
   
   server.listen(3000);
   ```
   
## Handeling Date I/O in NodeJS:

- Most active web applications and services have a lot of data flowing through them
- The data comes in the form of **text**, **JSON strings**, **binary buffers**, and **data streams**.
- For that reason, NodeJS has many mechanisms built in to support handling the data from system to system
- One of the most common data types that you work with when implementing NodeJs web applications and services is JSON (JavaScript Object Notation)
`JSON` : is a light weight method to convert JavaScript objects into a string form (which is Known as `Serializing` ) then back again (which is Known as `Serializing` )

  ### Advantages of JSON over XML:
  
  1- JSON is much more efficient and takes up fewer characters.
  
  2- Serializing/deSerializing JSON is faster than XML because it is simplier syntax.
  
  3- JSON is easier to read from a developer's perspective because it is similar to JavaScript syntax.
  `node`: The only reasons you might wanna to use XML over JSON are for complex objects.
  
     | Convert JSON to JS Object  | Convert JS object to JSON  |
     |:---------------------------|:---------------------------|
     | JSON.parse(string)         | JSON.stringify(text)       |

* the first to convert a string that is properly formatted with JSON into a javaScript object.
  
* the second to convert a javaScript object into a properly formatted JSON string.
  
#### Some questitions:

- What are advantages of JSON over XML.
- What is `Serializing` the and the `deSerializing`, how to applicate them

## Routing in NodeJS:
  #### There are two parts when defining the route
  1) HTTP request moethod (**get**, **put**, **head**, **post**, **delete**)
  2) The path specified in the URL.

 #### The **four** parameters Types in Rouring:
   1) **Query string**  (uses the standard ?key=value&key=value ...HTTP query string after tha path in the URL)                                
      - most common method for implementing parameters
      - The simplest method to add parameters to a route
      - The URLs can be come long and convoluted
      - Not secured
      - `EX:` /find?author=Brad&title=Node
  
 3) **Params** (when implementing a web for or other POST request,you can pass parameters in the body of the request)
    - Secured
    - Used with forms [Login, Save, Updata]
     
 3) **Regex***
    - Use a regex expression to match patterns as the path portion for tha route
    - Doesn't follow Standared/formatting for the path
    - Rarly used
    - `EX:` /book/:<chapter>:<page>== (/^\/book\/(\w+)?s/
     
 4) **Defined parameter (path variable)**
    - allows you define your parameters by name using `<param_name>` within the route path portion for tha route
    - better methode to use than regex
    - EX:`: /user/:useld  
## Implementing HTTP Services in NodeJSWhat is controller in NodeJS:
  **Routes**
   -to forword the supported reqest(and any information encoded in request URLs) to teh appropriate controller functions
   **Controller**
   -functions to get the requested data from the modules, create an HTML page displaying the data, and return it to the user to view in the browser.
   **Views**
   -used by the controllers to render the data.
   
