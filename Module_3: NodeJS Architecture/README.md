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
  ![DataBase Design(1)](https://github.com/Eng-YasminKotb/NodeJS_Level1/assets/122429943/bd616967-5530-4882-9f63-658dc6ac2c25)

 ### figure that show nodeJS architecture
  ![NWAGFGdrawio](https://github.com/Eng-YasminKotb/NodeJS_Level1/assets/122429943/f7455b07-67e0-45b5-ba1b-77a19e753686)
