# API Testing – JSONPlaceholder  
Manual test execution using Postman (GET + POST requests)  
Project for entry-level QA portfolio

## ✅ Tested Endpoint  
**Base URL:** `https://jsonplaceholder.typicode.com/posts`  
**API Type:** Public REST API (Mock)

---

## 📂 Folder Structure

postman-api-testing/  
├── README.md  
├── postman-request-screenshots/  
│   ├── TC01_valid_get_post_1_response.png  
│   ├── TC02_invalid_get_post_9999.png  
│   ├── TC03_create_new_post_response.png  
│   ├── TC04_get_all_posts.png  
│   └── TC05_post_missing_title_field.png  

---

## 🧪 Test Cases Overview

| TC ID | Method | Endpoint   | Test Type      | Description                             |
|-------|--------|------------|----------------|-----------------------------------------|
| TC01  | GET    | /posts/1   | Positive Test  | Valid post retrieval by ID              |
| TC02  | GET    | /posts/9999| Negative Test  | Invalid post ID returns empty/404       |
| TC03  | POST   | /posts     | Positive Test  | Create new post with valid data         |
| TC04  | GET    | /posts     | List Test      | Retrieve list of all posts (100+)       |
| TC05  | POST   | /posts     | Negative Test  | Missing required field: `title`         |

---

## 📸 Screenshots

All responses were verified and saved inside `/postman-request-screenshots/` for each test case.  
Each screenshot includes request method, URL, status code, and response body.

---

## 💡 What I Learned

### Understanding `"userId"` Field  
In TC03 and TC05, we used a field like `"userId": 99` or `"userId": 42`. In a real system, this links the post to a valid authenticated user.  
In this mock API, it's just a placeholder that accepts any number.

### Why `"userId": 42` in Negative Test (TC05)?  
To isolate the test to **missing title only** — not an invalid user. Keeping `userId` valid ensures the error is caused by the missing `"title"` field.

### Fake API Behavior  
JSONPlaceholder accepts even invalid input. For example, TC05 returns `201 Created` even though `"title"` is missing. This shows mock APIs don’t enforce validation — another reason real testing environments matter.

---

## 📌 Tools Used
- Postman (desktop)
- Windows 11
- JSONPlaceholder test API

---

## 📘 Notes  
This project simulates real-world API testing manually, with no automation. Ideal for entry-level QA portfolio development.
