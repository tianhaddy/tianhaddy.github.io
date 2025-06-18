# tianhaddy.github.io
api-testing-postman-portfolio/
├── README.md
├── collections/
│   └── DummyAPI_Reqres.postman_collection.json
├── environments/
│   └── ReqresEnvironment.postman_environment.json
├── reports/ (optional)
│   └── sample-newman-report.html
# 🧪 API Testing Portfolio with Postman

This project contains my sample API test cases built using **Postman** and executed on a public dummy API service: [reqres.in](https://reqres.in). It showcases my knowledge and experience in API testing, scripting, collection management, and environment handling as a Software QA Engineer.

---

## 🔧 Tools Used
- Postman
- Postman Environment Variables
- Test Scripts (JavaScript)
- Newman (CLI for Postman)
- Reqres Dummy API

---

## 📁 Project Structure


---

## ✅ Collection Overview

| # | API Scenario               | Method | Endpoint                 | Expected |
|---|----------------------------|--------|--------------------------|----------|
| 1 | Login (Success)            | POST   | `/api/login`             | 200 OK + Token |
| 2 | Login (Missing Password)   | POST   | `/api/login`             | 400 Error |
| 3 | Get Single User            | GET    | `/api/users/2`           | 200 OK + User Data |
| 4 | Create User                | POST   | `/api/users`             | 201 Created |

---

## 📜 Sample Test Script

```javascript
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});

pm.test("Token is returned", function () {
    const jsonData = pm.response.json();
    pm.expect(jsonData.token).to.not.be.undefined;
});
