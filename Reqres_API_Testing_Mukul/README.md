
# Reqres API Testing - Mukul Kumar

## 🔍 Overview:
This project contains test cases and automation using Postman for the public [Reqres API](https://reqres.in/). It covers major endpoints and scenarios such as successful/failed login, user creation, updates, deletions, and invalid requests.

---

## 📄 Test Cases Summary

| Test Case | Endpoint | Method | Expected Result |
|-----------|----------|--------|------------------|
| TC_01 | /api/users?page=2 | GET | List of users (Page 2) with 200 OK |
| TC_02 | /api/users/2 | GET | Single user details with 200 OK |
| TC_03 | /api/users/23 | GET | 404 Not Found |
| TC_04 | /api/users | POST | Creates a new user with 201 Created |
| TC_05 | /api/users/2 | PUT | Updates user with 200 OK |
| TC_06 | /api/users/2 | DELETE | Deletes user with 204 No Content |
| TC_07 | /api/register | POST | Register user with 200 OK |
| TC_08 | /api/register | POST | Failed registration with 400 Bad Request |
| TC_09 | /api/login | POST | Successful login with token |
| TC_10 | /api/login | POST | Failed login with 400 Bad Request |

---

## ⚙️ Environment Setup

1. Import the Postman collection: `Reqres_API_Testing_Mukul.postman_collection.json`
2. Use Postman Runner to execute all requests.
3. Optional: Run via CLI using Newman to generate reports.

---

## 🧪 Sample Mock Data (for POST/PUT):

```
POST /api/users
{
    "name": "Mukul",
    "job": "QA Engineer"
}

PUT /api/users/2
{
    "name": "Mukul Updated",
    "job": "Senior QA Engineer"
}
```

---

## ✅ Additional Notes:
- Public API, no authentication needed.
- Edge cases like invalid user ID or missing fields are included.
- Can be extended for contract testing using schema validation.
