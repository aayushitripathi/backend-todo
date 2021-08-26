# backend-todo
Introduction
This is a todo list which has functionality of adding the task , deleting the task , editing the task and marking task as completed.The data is stored in the form on JSON data.</br>
Concepts Used :<br />
1.express <br />
2.file read/write operations <br />
3.middleware <br />
4.router <br />
5.cors</br>

Acces Postman</br>
[![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/6e68e5325da949235f09?action=collection%2Fimport)


Folder Structure</br>

├── app.js</br>
├── controller</br>
│   └── taskController.js</br>
├── data</br>
│   └── tasks.json</br>
├── models</br>
│   └── taskmodels.js</br>
├── package.json</br>
├── package-lock.json</br>
├── route</br>
│   └── taskroutes.js</br>
└── utils</br>
    └── sendResponse.js</br>

To use this project follow these steps:</br>
1.clone this repo    $ git clone https://github.com/aayushitripathi/backend-todo</br>
2. install npm       $ npm install</br>
3. Run the project using   $ npm run start</br>
4. To fetch all the task stored you need:</br>
METHOD :GET</br>
URL :/tasks</br>
EXAMPLE:http://localhost:3000/tasks</br>
OUTPUT:
```
{
    "message": "Succesful",</br>
    "data": [
        {
            "taskId": "2qqgj3p0ksaqb7uz",
            "content": "hii123",
            "createdAt": "2021-08-13T19:14:02.497Z",
            "updatedAt": "2021-08-15T10:44:54.738Z",
            "iscompleted": true</br>
        },
       
            "taskId": "2qqgj2e5ksd2ou2b",
            "content": "ayyu",
            "createdAt": "2021-08-15T10:36:05.549Z",
            "updatedAt": "2021-08-15T11:17:24.789Z",
            "iscompleted": true</br>
        }
        }
        
  ```     
5. To fetch the particular task using task id :</br>
METHOD :GET</br>
URL :/tasks/taskid</br
EXAMPLE:http://localhost:3000/tasks/2qqgj3p0ksaqb7uz</br>
OUTPUT:
```{
    "message": "successfully fetched all tasks",
    "data": {
        "taskId": "2qqgj3p0ksaqb7uz",
        "content": "hii123",
        "createdAt": "2021-08-13T19:14:02.497Z",
        "updatedAt": "2021-08-15T10:44:54.738Z",
        "iscompleted": true
    }
}
```

6.Add new todo in the list</br>
METHOD :POST</br>
URL :/tasks</br>
EXAMPLE:http://localhost:3000/tasks</br>
Body should contain :
```
{
        "content": "hii123",
        "createdAt": "2021-08-13T19:14:02.497Z",
        "updatedAt": "2021-08-15T10:44:54.738Z",
        "iscompleted": true
}
```
OUTPUT:
```
{
    "message": "successfully fetched all tasks",
    "data": {
        "taskId": "2qqgj3p0ksaqb7uz",
        "content": "hii123",
        "createdAt": "2021-08-13T19:14:02.497Z",
        "updatedAt": "2021-08-15T10:44:54.738Z",
        "iscompleted": true
    }
}
```

7.To update a particular todo:</br>
METHOD :PUT</br>
URL :/tasks/taskid</br>
EXAMPLE:http://localhost:3000/tasks/2qqgj3p0ksaqb7uz</br>
Body should contain :
```{
        "content": "hii123",
        "createdAt": "2021-08-13T19:14:02.497Z",
        "updatedAt": "2021-08-15T10:44:54.738Z",
        "iscompleted": true
}
```
OUTPUT:
```{
    "message": "successfully fetched all tasks",
    "data": {
        "taskId": "2qqgj3p0ksaqb7uz",
        "content": "hii123",
        "createdAt": "2021-08-13T19:14:02.497Z",
        "updatedAt": "2021-08-15T10:44:54.738Z",
        "iscompleted": true
    }
}
```
8.Delete a particular task</br>
METHOD :DELETE</br>
URL :/tasks/taskid</br>
EXAMPLE:http://localhost:3000/tasks/2qqgj3p0ksaqb7uz</br>
OUTPUT:NO OUTPUT COZ WE ARE USING STATUS CODE 204 WHICH RETURNS NO OUTPUT</br>

PLEASE NOTE:</br>
1.DO NOT CHANGE node_modules file</br>
2.Installation done on vscode terminal will only be used in that particular project / folder only it is not global <br />
