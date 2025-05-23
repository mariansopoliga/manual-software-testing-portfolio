postman-api-testing/ 
Manual test execution using Postman (GET + POST requests)  
Project for entry-level QA portfolio  

## ✅ Tested Endpoint
Base URL: `https://jsonplaceholder.typicode.com/posts`  
API Type: Public REST API (Mock)

---

## 📂 Folder Structure

api-testing-jsonplaceholder/
├── README.md
└── postman-request-screenshots/
├── TC01_valid_get_post_1_response.png
├── TC02_invalid_get_post_9999.png
├── TC03_create_new_post_response.png
├── TC04_get_all_posts.png
└── TC05_post_missing_title_field.png


---

## 🧪 Test Cases Overview

| TC ID | Method | Endpoint           | Test Type        | Description                                |
|-------|--------|--------------------|------------------|--------------------------------------------|
| TC01  | GET    | /posts/1           | Positive Test    | Valid post retrieval by ID                 |
| TC02  | GET    | /posts/9999        | Negative Test    | Invalid post ID returns empty/404          |
| TC03  | POST   | /posts             | Positive Test    | Create new post with valid data            |
| TC04  | GET    | /posts             | List Test        | Retrieve list of all posts (100+)          |
| TC05  | POST   | /posts             | Negative Test    | Missing required field: `title`            |

---

## 📸 Screenshots

All responses were verified and saved inside `/postman-request-screenshots` for each test case.  
They include request method, URL, status code, and response body.

---

## 💡 What I Learned

### Understanding `"userId"` Field:
In test cases TC03 and TC05, we use a field like `"userId": 99` or `"userId": 42`. This represents which user is creating the post. In a real system, this would link the post to a valid authenticated user. In this mock API, it's a placeholder that accepts any numeric value.

### Why `"userId": 42` in Negative Test (TC05)?
To isolate the test to **missing title only**, not an invalid user. We kept `userId` valid so the response failure (or success) relates purely to the missing `"title"` field — this ensures proper test isolation and clarity.

### Fake API Behavior:
JSONPlaceholder accepts even incomplete or invalid input (e.g. TC05 returns `201 Created` despite the missing title). This taught me that mock APIs don’t always enforce validation — and why real testing environments are critical.

---

## 📌 Tools Used
- Postman (desktop)
- Windows 11 (folder structure)
- JSONPlaceholder public test API

---

## 📘 Notes
This project is designed to simulate real-world API testing scenarios using manual steps only. No automation tools were used to keep it aligned with beginner QA expectations.

