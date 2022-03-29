# Restful API Signatures

REST stands for representational state transfer. Let's see how.

For Example, User is you resource. What operation you can perform over your user object. You can `create` a user, you can `read` that user, you can `update` the user and you can `delete` the users. You can perform `CRUD` over you object. 

How will you write the API? Your API should be writen in such a way that anyone can tell, what the basic operation API is doing just by looking at you signatures or contracts. 

Let's start CRUD. Let's assume we are working with JSON data here.

### 1. Create
  `API URL: [POST] {{domain_name}}/<resource_name>`  
  `Content Type: application/json`  
  Request Body:
  ```json
  {
    "json_body": "json_body"
    ...
  }
  ```
  Response
  Http Response Code: 201
  Response Body: 
  ```json
  {
    "json_body_id": "json_body_id",
    "json_body": "json_body"
    ...
  }
  ```

### 2. Read All Data
  `API URL: [GET] {{domain_name}}/<resource_name>`  
  `Content Type: application/json`  
  
  Response
  Http Response Code: 200
  Response Body: 
  ```json
  [
    {
      "json_body_id": "json_body_id",
      "json_body": "json_body"
      ...
    },
    {
      "json_body_id": "json_body_id",
      "json_body": "json_body"
      ...
    }
    ....
  ]
  ```

### 3. Read Single Data
  `API URL: [GET] {{domain_name}}/<resource_name>/{{resource_id}}`  
  `Content Type: application/json`  
  
  Response
  Http Response Code: 200
  Response Body: 
  ```json
  {
    "json_body_id": "json_body_id",
    "json_body": "json_body"
    ...
  }
  ```

### 4. Update Single Data
  `API URL: [GET] {{domain_name}}/<resource_name>/{{resource_id}}`  
  `Content Type: application/json`  
  Request Body:
  ```json
  {
    "json_body_id": "json_body_id",
    "updated_json_body": "updated_json_body"
    ...
  }
  ```
  Response
  Http Response Code: 200
  Response Body: 
  ```json
  {
    "json_body_id": "json_body_id",
    "json_body": "json_body"
    ...
  }
  ```

