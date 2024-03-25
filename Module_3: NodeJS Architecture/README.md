## How NodeJS work?
- NodeJS uses Event-driven model
- NodeJS applications are run in a single threaded event-driven model.
  #### Note:
  - Although nodeJS implemnts a thread pool in the background to do work, the application itself doesn't have any 
   concept of multiple threads.
 ### Event-driven model:
  - instead of excuting all the work for each request on individual threads, work is added to an event queue and then 
    picked up by a single thread runnign an event loop.
 ### Thread Model:
 
  ![DataBase Design(1)](https://github.com/Eng-YasminKotb/NodeJS_Level1/assets/122429943/bd616967-5530-4882-9f63-658dc6ac2c25)


## Figure that show nodeJS architecture
 
  ![NWAGFGdrawio](https://github.com/Eng-YasminKotb/NodeJS_Level1/assets/122429943/f7455b07-67e0-45b5-ba1b-77a19e753686)

##What is NodeJS Blocking I/O:
 - this blocking process stops the excution of the current thread and waits for a response before continuing
 - NodeJS using the event callbacks until you run into the problem of functions that block waiting for I/O.
   #### Examples of blocking I/o:
   - Reading a file
   - Quering a database
   - Socket request
   - Accessing a remote service
   #### Note:
   The reason NodeJS uses event callbacks is-->  not to have to wait for blocking I/O.
   Therefore, any requests that performed on a diffferent thread in the backgroung

## The difference between blocking and non-blocking:

    - Blocking->is when the excution of additional javaScript in the NodeJS process must wait until a non 
     JavaScript operation completes
     
     EX:
     -Synchronous methods

     - Non-Blocking->is when the excution of additional javaScript in the NodeJS process dosen't wait and continue 
       processing. 
               
     EX:
     ASynchronous methods

     
  ## What is nodeJS event-Emmiter:
  
     - NodeJS allows us to create and handle custom events easily by using events module
     - These Event Module includes EventEmitter class which can be used to raise and handle custom events

     
   ### How can we do that ?
   
   1- Adding custom events to objects
   
   2- Adding Event Listeners to objects 

   
   ### Usage:
   - Logging
   - Handle Errors

  #### Functions exists in evenEmitter class:
    - .emit()             --->to emit an event in module
    - .on()               --->to listen to data on registered event in nodeJS
    - .once()             --->listen to data on registered event only once
    - .addListener()      --->it checks if the listener is registeed for an event
    - .removeListener()   --->it removes the listener for an event
    
 ####Steps of emitter:
 
 1- import events module
 
 2- create an object of it
 
 3- listen
 
 4- emit your event
 
```
var evnts= require('events');
var eventEmitter= new events.EventEmitter();

eventEmitter.on('print', function(data){
console.log("printing..................."+ data)})

eventEmitter.emit('print');
```

## Important interview questions on the last 3 modules?

 - What is NodeJS? make a discussion of event driven module

 - What NodeJS used For?

 - What is package JSON?

- What is Node Package manager?

- How the node  working?  make a discussion of [event driven module-Event loop-thread pool]

- different between threaded model  and  event driven model

- deffernt between blocking and non blocking
