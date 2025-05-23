# API Testing – JSONPlaceholder

This folder contains a simple API testing project using Postman and the public JSONPlaceholder REST API.
The goal was to practice manual validation of HTTP requests, test different input scenarios, and analyze API responses.

---

## ✅ Scope

- Manual testing of public REST API endpoints using Postman
- Creating and executing both positive and negative test cases
- Validating API responses (status codes, response body, headers)
- Understanding mock API behavior and test data isolation

---

## 🧪 Covered Test Cases

| TC ID | Method | Endpoint     | Test Type      | Description                             |
|-------|--------|--------------|----------------|-----------------------------------------|
| TC01  | GET    | /posts/1     | Positive Test  | Valid post retrieval by ID              |
| TC02  | GET    | /posts/9999  | Negative Test  | Invalid post ID returns empty/404       |
| TC03  | POST   | /posts       | Positive Test  | Create new post with valid data         |
| TC04  | GET    | /posts       | List Test      | Retrieve list of all posts (100+)       |
| TC05  | POST   | /posts       | Negative Test  | Missing required field: `title`         |

---

## 📸 Screenshot Evidence

Screenshots were taken for each test case and saved in the project folder.
Each screenshot includes the request method, endpoint, status code, and returned body.

---

## 💡 What I Learned

### `"userId"` in Mock APIs
- Used placeholder values such as `"userId": 99` and `"userId": 42`
- In a real-world application, this would be tied to an authenticated user
- JSONPlaceholder accepts any numeric `userId`, no authentication required

### Testing Strategy
- TC05 intentionally omits the required field `"title"` to simulate a negative case
- This helps evaluate how the system handles incomplete payloads

### Mock API Behavior
- JSONPlaceholder is non-strict: even invalid POST data often returns a success code (`201 Created`)
- Reinforced the importance of validating APIs in real environments with real backend logic

---

## 🔧 Tools Used
- **Postman** (desktop app)
- **Windows 11**
- **JSONPlaceholder** – https://jsonplaceholder.typicode.com

---

## 📘 Notes
This is a beginner-friendly API testing exercise intended to demonstrate testing logic, scenario thinking, and manual testing skills without automation.

Created by **Marián Sopoliga**  
[GitHub Portfolio](https://github.com/mariansopoliga/manual-software-testing-portfolio)
