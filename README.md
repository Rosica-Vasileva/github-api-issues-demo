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

- **GET /repos/{user}/{repo}/issues/{num}/comments**
  - Returns the comments for a specific issue.

- **GET /repos/{user}/{repo}/issues/comments/{id}**
  - Returns the specified comment.

### 2. POST / PATCH / DELETE Endpoints (Authentication Required)
- **POST /repos/{user}/{repo}/issues**
  - Creates a new issue.

- **PATCH /repos/{user}/{repo}/issues/{num}**
  - Modifies the specified issue.

- **POST /repos/{user}/{repo}/issues/{num}/comments**
  - Creates a new comment for a certain issue.

- **PATCH /repos/{user}/{repo}/issues/comments/{id}**
  - Modifies an existing comment.

- **DELETE /repos/{user}/{repo}/issues/comments/{id}**
  - Deletes an existing comment.

## How to Use
To interact with these endpoints, you can use any HTTP client such as [Postman](https://www.postman.com/). Make requests to the following base URL:

`https://api.github.com`

## Authentication
Authentication is required for POST, PATCH, and DELETE endpoints. Ensure that you have the necessary credentials.

## Examples
Here are some examples of how to use these endpoints:

### Example 1: GET Issues

### Example 2: POST New Issue
