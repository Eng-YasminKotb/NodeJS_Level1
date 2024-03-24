## How NodeJS work?
- NodeJS uses Event-driven model
- NodeJS applications are run in a single threaded event-driven model.
  #### Note:
  - Although nodeJS implemnts a thread pool in the background to do work, the application itself doesn't have any 
   concept of multiple threads.
 ### What is Event-driven model:
  - instead of excuting all the work for each request on individual threads, work is added to an event queue and then 
    picked up by a single thread runnign an event loop.
 ### Thread Model:

