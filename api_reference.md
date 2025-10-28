# API Reference - Eiger Adventure Land

This document provides a structured overview of all available API endpoints for the Eiger Adventure Land platform.

## Endpoint Summary

| No | Endpoint | Method | Description | Auth Required | Response Codes |
|----|-----------|---------|--------------|----------------|----------------|
| 1 | `/users` | GET | Retrieve all registered users | ✅ | 200, 401, 500 |
| 2 | `/users` | POST | Create a new user | ✅ | 201, 400, 409 |

## Request and Response Details

### GET `/users`
**Description:** Returns all registered users.  
**Parameters:** None  
**Example Response:**
{
  "id": 1,
  "name": "Nadiyya",
  "email": "nadiyya@example.com"
}

### POST `/users`
**Description:** Create a new user. 

**Request Body:**
| Field      | Type   | Required | Description           |
| ---------- | ------ | -------- | --------------------- |
| `name`     | string | Yes      | Full name of the user |
| `email`    | string | Yes      | User email address    |
| `password` | string | Yes      | Secure password       |

**Example Request:**
{
  "name": "Dina",
  "email": "dina@example.com",
  "password": "strongpassword123"
}
**Example Response:**
{
  "message": "User deleted successfully"
}

### Version
Version: 1.0
Last Updated: October 2025
Maintainer: Nadiyya
Contact: nnba.nadiyya@gmail.com

