## Client-Server Model 💻
- is a distributed application framework dividing tasks between servers and clients
- The client relies on sending a request to server in order to access a service made available by a server
- The server runs one or more programs that share resources with and distribute work among clients
- The client server relation ship communicates in arequest-response messaging pattern

## HTTP (Hypertext Transfer Protocol)
 - is a protocol which allows the fetching of resourses, such as HTML documents
 - It is the foundation of any [data exchange] on the web and it it a client server protocol, which means requests are initiated by the recipient,usually the Web browser.

## Implementing HTTP Services in NodeJS"
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
