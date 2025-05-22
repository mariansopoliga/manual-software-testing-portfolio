# Login Functionality – Manual Test Project

This folder documents the manual testing of the **login functionality** on [the-internet.herokuapp.com](https://the-internet.herokuapp.com/login). The goal was to validate expected behavior under various login scenarios and capture any security or usability defects.

---

## ✅ Scope

- Positive login with valid credentials
- Negative login with empty or invalid inputs
- Edge cases (emoji in password, long inputs, spaces, etc.)
- Session behavior after logout and browser back navigation

---

## 📋 Included Files

- `Login_Functionality_Manual_Test_Report_C1-C15_Marian_Sopoliga.pdf` – structured test case report
- `Login_Functionality_Manual_Test_Summary_Report_C1-C15_Marian_Sopoliga.pdf` – execution summary
- `BugReport_Login_BackButton_AccessAfterLogout_MarianSopoliga.pdf` – Jira export of security flaw
- `C14_Back_Button_Access_After_Logout.png` – screenshot proving session leak

---

## 🐞 Key Finding

A high-risk bug was discovered (see bug report) where the user can access the secure page after logging out by simply clicking the **Back** button in the browser, indicating improper session invalidation.

---

## ⚙️ Tools Used

- **TestRail** for test case management and report generation
- **Jira** for detailed bug documentation with reproduction steps and visual evidence
