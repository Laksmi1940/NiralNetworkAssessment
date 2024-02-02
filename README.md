# NiralNetworkAssesment

```
Lakshmikanta Nath
Cell - +91-7008096463
Email - lakshmikanta050@gmail.com
```
## Requirement

Technical Requirements

    Q1. Build a REST API server that generates response using a HashMap.

    Q2. Build a Employee Management system and create respective API endpoints to perform CRUD operations on employee details.
    
    Q3. Call a external API Server and make a GET request and store all the recived details in DB ( Website: https://developer.themoviedb.org/reference/intro/getting-started ) ( Write proper documentation for all API Endpoints with Token )
    
    Q4. Build a backend service class that uses mutli-threading (CompletableFuture) and also write test cases for the same.


## Run Locally

Clone the project using - ```https://github.com/Laksmi1940/NiralNetworkAssessment.git```

The swagger endpoint to test the APIs

```http://localhost:8080/swagger-ui/index.html```

## Usage

1. Create a REST API server that generates a response using a HashMap.

   Getmapping 
   ```
    curl -X 'GET' \
    'http://localhost:8080/response' \
    -H 'accept: */*'
   ```
   Response
   ```
   {
        "key-1": "value-1",
        "key-2": "value-2"
    }
   ```
2. Post an Employee
   Request
   ```
   {
    "name": "Lakshmikanta",
    "jobTitle": "SDE",
    "salary": 500000,
    "managerName": "Oliver"
   }
   ```
   Response
   ```
       {
          
            "id": 1,
            "name": "Lakshmikanta",
            "jobTitle": "SDE",
            "salary": 50000,
            "manager_name": "Oliver"
         }
   ```

3. Get all Employees

      Response
      ```
   [
       {
       "id": 1,
       "name": "Lakshmikanta",
       "jobTitle": "SDE",
       "salary": 50000,
       "manager_name": "Oliver"
       },
       {
       "id": 2,
       "name": "Peter",
       "jobTitle": "SDE",
       "salary": 60000,
       "manager_name": "Oliver"
       }
   ]
            ```
4. Get an Employee based on empl Id
     Path Variable - ```emplyoyeeId = 1```

     Response
     ```
        {
            "id": 1,
            "name": "Lakshmikanta",
            "jobTitle": "SDE",
            "salary": 50000,
            "manager_name": "Oliver"
        }
    ```

5. Update an emplyee details

   Path Parameter - ``` emplyoyeeId = 1```

   Request Body -
      ```
      {
         "name": "John",
         "jobTitle": "SW",
         "salary": 70000,
         "managerName": "Jonathan"
      }
      ```

      Response
      ```
      {
         "id": 1,
         "name": "John",
         "jobTitle": "SW",
         "salary": 70000,
         "managerName": "Jonathan"
      }
      ```
6. Delete Employee by given employee_id
    
        Request Parameter - ``` employee_id = "2"```

        Response
          ```
            {
                "Deleted"
            }
            ```
            
7. Call a external API Server and make a GET request and store all the recived details in DB

   GET /company/{id}
  
   RequestParameters : apiKey = String, company_id = Integer
   
   Request URL :
   curl -X 'GET' \
  'http://localhost:8080/company/{id}?apiKey=token&company_id=1' \
  -H 'accept: */*'
  
  Response:
  ```
    {
        "local_id": 3,
        "description": "",
        "headquarters": "San Francisco, California",
        "homepage": "https://www.lucasfilm.com",
        "id": 1,
        "logo_path": "/tlVSws0RvvtPBwViUyOFAO0vcQS.png",
        "name": "Lucasfilm Ltd.",
        "origin_country": "US",
        "parent_company": null
    }
  ```
  
8. Build a backend service class that uses mutli-threading (CompletableFuture) and also write test cases for the same
  
     Request :
     ```
       {
            "name": "string",
            "age": 0,
            "city": "string"
        }
     ```
     Response :
     ```
        {
            "id": 0,
            "name": "string",
            "age": 0,
            "city": "string"
        }
     ```
     
In Terminal : ```StudentController : 32 -> http-nio-8080-exec-6
StudentService : 38 -> pool-2-thread-1```
