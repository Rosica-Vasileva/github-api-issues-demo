# GitHub API Issues Project

## Project Overview
This project aims to demonstrate the usage of GitHub Issues API endpoints. Below, you will find a list of available endpoints along with their descriptions.

## GitHub API Endpoints

### 1. GET Endpoints
- **GET /repos/{user}/{repo}/issues**
  - Returns the issues in the given GitHub repo.
 
 {
   
    "id": 5,
    "title": "Example Issue 5",
    "body": "This is the body of the issue.",
    "created_at": "2023-01-01T00:00:00Z",
    "updated_at": "2023-01-02T12:34:56Z"

 }


 {
   
    "id": 4,
    "title": "Example Issue 4",
    "body": "This is the body of the issue.",
    "created_at": "2023-01-01T00:00:00Z",
    "updated_at": "2023-01-02T12:34:56Z"

 }


 {
   
    "id": 2,
    "title": "Example Issue 2",
    "body": "This is the body of the issue.",
    "created_at": "2023-01-01T00:00:00Z",
    "updated_at": "2023-01-02T12:34:56Z"

 }



 - **GET /repos/{user}/{repo}/issues/{num}**
  - Returns the specified issue.
 
{

    "id": 2,
    "title": "Test Issue 2",
    "body": "This is a test issue.",
    "created_at": "2023-11-24T07:21:07Z",
    "updated_at": "2023-11-24T11:56:40Z",

}


- **GET /repos/{user}/{repo}/issues/{num}/comments**
  - Returns the comments for a specific issue.
 
{


    "id": 150438254,
    "user": "Rosica-Vasileva",
    "body": "DELETE request via Postman:\r\n\r\nOpen Postman and create a new request.\r\nEnter the URL to which you want to make the DELETE request.\r\nSelect HTTP method \"DELETE\".\r\nPress the \"Send\" 
    button to send the DELETE request.",,
    "created_at": "2023-11-24T10:12:04Z",
    "updated_at": "2023-11-24T10:12:04Z",
    // ... other fields


}
    

- **GET /repos/{user}/{repo}/issues/comments/{id}**
  - Returns the specified comment.


{
 
     "url": "https://api.github.com/repos/{user}/{repo}/issues/comments/{id}",
     "html_url": "https://github.com/{user}/{repo}/issues/{issue_number}#issuecomment-{id}",
     "issue_url": "https://api.github.com/repos/{user}/{repo}/issues/{issue_number}",
     "id": 1825436828,
     "node_id": "IC_kwDOKxZOe85szfj9",
     "user": {
      "login": "Rosica-Vasileva",
      "id": 1825436828,
      // ... other user fields
    
}
  
{  
  
  
      "created_at": "2023-11-24T10:11:11Z",
      "updated_at": "2023-11-24T10:11:11Z",
      "author_association": "OWNER",
     "body":  "3. PATCH Request:\r\nOpen Postman and create a new request.\r\nEnter the URL to which you want to make the PATCH request.\r\nSelect HTTP method \"PATCH\".\r\nIn the \"Body\" tab, select \"raw\" format and enter the JSON body of the request with the changes you want to make.\r\nPress the \"Send\" button to send the PATCH request.",
      // ... other fields


}

[Вижте коментарите на Issue 4](https://github.com/Rosica-Vasileva/github-api-issues-demo/issues/4)

 
  - 

### 2. POST / PATCH / DELETE Endpoints (Authentication Required)
- **POST /repos/{user}/{repo}/issues**
  - Creates a new issue.
 
{
 
     "url": "https://api.github.com/repos/{user}/{repo}/issues/{issue_number}",
     "html_url": "https://github.com/{user}/{repo}/issues/{issue_number}",
     "number": 7,
     "title": "Create new issues from Postman",
     "user": {
     "login": "Rosica-Vasileva",
     "id": 150438254,
     // ... other user fields
  
  
  }

 
  
  {
    
     
     "state": "open",
     "created_at": "2023-11-24T12:00:00Z",
     "updated_at": "2023-11-24T12:00:00Z",
     // ... other fields


 }


- **PATCH /repos/{user}/{repo}/issues/{num}**
  - Modifies the specified issue.
 
{
     
     "url": "https://api.github.com/repos/Rosica-Vasileva/github-api-issues-demo/issues/6",
     "html_url": "https://github.com/Rosica-Vasileva/github-api-issues-demo/issues/6",
     "number": 6,
     "title": "New Title",
     "user": {
     "login": "Rosica-Vasileva",
     "id": 150438254,
     // ... other user fields
  
  
},
  

{  
  
  
    "state": "open",
    "created_at": "2023-11-24T12:00:00Z",
    "updated_at": "2023-11-24T12:30:00Z",
    // ... other fields


}


 
  [PATCH /repos/Rosica-Vasileva/github-api-issues-demo/issues/6](https://developer.github.com/v3/issues/#update-an-issue)

- **POST /repos/{user}/{repo}/issues/{num}/comments**
  - Creates a new comment for a certain issue.
 
    curl -X POST \
  -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
  -H "Content-Type: application/json" \

 {


     "body": ""Creating a new comment in problem 2 with a POST request via POSTMAN"."
  

  }


  https://api.github.com/repos/Rosica-Vasileva/github-api-issues-demo/issues/6/comments


- **PATCH /repos/{user}/{repo}/issues/comments/{id}**
  - Modifies an existing comment.
 
{
    
     "url": "https://api.github.com/repos/Rosica-Vasileva/github-api-issues-demo/issues/comments/{comment_id}",
     "html_url": "https://github.com/Rosica-Vasileva/github-api-issues-demo/issues/{issue_number}#issuecomment-{comment_id}",
     "id": 1825436828,
     "body": "Modify an existing comment with a POST request.",
      // ... other fields

}

https://api.github.com/repos/Rosica-Vasileva/github-api-issues-demo/issues/comments/1825436828

- **DELETE /repos/{user}/{repo}/issues/comments/{id}**
  - Deletes an existing comment.
 
  curl -X DELETE \
  -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
  "https://api.github.com/repos/Rosica-Vasileva/github-api-issues-demo/issues/comments/1825436828

## How to Use
To interact with these endpoints, you can use any HTTP client such as [Postman](https://www.postman.com/). Make requests to the following base URL:

`https://api.github.com`

## Authentication
Authentication is required for POST, PATCH, and DELETE endpoints. Ensure that you have the necessary credentials.

## Examples
Here are some examples of how to use these endpoints:

### Example 1: GET Issues

### Example 2: POST New Issue
