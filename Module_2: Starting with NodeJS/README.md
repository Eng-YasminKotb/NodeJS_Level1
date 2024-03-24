## Setps to Create NodeJS project:

1- create a directory for your new application and navigate into it: mkdir my app cd my app.

2- Use the nmp init command to create a package.josn file for your application.

3-  install the required libarary like : Express in the myapp directory and save it in the dependencies list of your pakage.json file 


#### use the following command to install Express :

- nmp install express

## What is package.json?

- package.json file is a simple JSON text dile that defines the module including dependencies.
- can contain a number of different directives to tell the Node Package Manager how to hadle the module.
##### Wait!! what is Node Package manager??!
- it is a command-line utility allows yo to find, install, remove, publish modules

  
## What is NodeJS modules?

  #### Types:
1- Core module [built-in module]

2- Local modules

3- Third-Party modules

#### Keyword to use the module is--> 'require':

## Dealing with fileSystem?
##### The following code will return all files existing in the folder

```
const fs=require('fs');

const folderPath=" ";
                                       //write your folder path
fs.readdir(folderPath,(err,files)=>{

console.log("files : ",files);
                                      //it will return all files existing in the folder
})
```
##### The following code will return the content of a specific file int the folder
```
const fs=require('fs');

const filePath=" ";          //write your file path
                                       
fs.readFile(filerPath,'utf-8',(err,content)=>{       //you can remove 'utf-8' as it the default

console.log("Content : ",content);

## Setps to Create NodeJS project:                                   
})
```
###### Note: Asynchronous // callback function   'logic!'


## Create and exports your owned modules:
- create a module--->simply require to create a file 
- exports a funs inside the module--> exports.[fun_Name]=[fun_Name]
- imports as we discussed:
  
       1- just use the key word 'require' and assign it to a variable
  
       2- then write the modulename. and you will get a list of fund that exsits oready in the module.
    
