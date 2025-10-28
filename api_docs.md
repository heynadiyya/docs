# Eiger Adventure Land - User API Documentation

## Base URL
https://api.eigeradventureland.com/v1

## Overview
This API allows clients to retrieve, create, and manage user profiles within the Eiger Adventure Land platform.  
All requests must be made over HTTPS and require an API key for authentication.

## Endpoints
### 1. Get All Users
Retrieve a list of all registered users.

**Endpoint:**
GET /Users

**Response:**
[
  {
    "id": 1,
    "name": "Nadiyya",
    "email": "nadiyya@example.com"
  },
  {
    "id": 2,
    "name": "Raka",
    "email": "raka@example.com"
  }
]

**Response Code:**
| Code | Meaning      |
| ---- | ------------ |
| 200  | OK           |
| 401  | Unauthorized |
| 500  | Server Error |


### 2. Create New User [POST]
Create a new user record.

**Endpoint:**
POST /Users

**Request:**
{
  "name": "Dina",
  "email": "dina@example.com",
  "password": "strongpassword123"
}

**Response:**
{
  "message": "User created successfully",
  "id": 5
}

**Response Code:**
| Code | Meaning              |
| ---- | -------------------- |
| 201  | Created              |
| 400  | Bad Request          |
| 409  | Email Already Exists |

**Error Format:**
All errors follow this format:
{
  "error": "Invalid Request",
  "message": "Missing authentication token"
}

### Version
API Version: 1.0
Last Updated: October 2025
Maintainer: Nadiyya






