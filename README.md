# QA Automation API Tests (Postman) — Valentyr Maryna

This repository contains a complete Postman-based API testing project.  
It includes a structured test collection, Dev/Prod environments, and fully implemented Data-Driven Tests (DDT) using JSON data files.

The project was created as part of an API testing automation assignment and is suitable for portfolio use.

---

## Overview

The collection tests core functionality of a demo vehicle-management API, including:

- User registration (signup)  
- User login and session creation  
- Profile retrieval and update  
- Validation of incorrect input  
- Cars and expenses endpoints  
- Cleanup (user deletion)  
- Data-Driven Tests for signup and profile

All tests are implemented using Postman's built-in JavaScript testing framework (`pm.*`).

---

## Project Structure

The repository contains three main folders:

- **collection/** — Postman collection with all requests and automated tests  
- **environments/** — Dev and Prod environment files used to switch API base URLs  
- **data/** — JSON files for Data-Driven Testing (signup and profile flows)

Environment file names used in this project:

- `QA Auto-Dev.Valentyr_Maryna3`  
- `QA Auto-Prod.Valentyr_Maryna3`  

These should be imported directly into Postman.

---

## Data-Driven Testing (DDT)

Two separate DDT modules are implemented:

### **Signup DDT**
JSON file: `signup_test_data_valentyr_maryna.json`  
Covers:
- Empty fields  
- Invalid emails  
- Valid signup  
- Expected responses (201 or 400)

### **Profile DDT**
JSON file: `profile_test_data_valentyr_maryna.json`  
Covers:
- Invalid names  
- Invalid date formats  
- Valid profile update  
- Expected responses (200 or 500)

Postman tests read expected values using `pm.iterationData.get()`.

---

## How to Run the Tests

### 1. Import project files
In Postman:
1. Import the collection from `/collection`
2. Import both environments from `/environments`
3. Import data files only when running DDT

---

### 2. Run the main test flow (no DDT)
1. Select environment:
   - `QA Auto-Dev.Valentyr_Maryna3` or  
   - `QA Auto-Prod.Valentyr_Maryna3`
2. Run the entire collection in Runner **without** selecting a data file  
This performs:
- Setup  
- Signup  
- Login  
- Profile tests  
- Car/expense tests  
- Cleanup  

---

### 3. Run Signup DDT
1. Open Runner  
2. Select data file: `signup_test_data_valentyr_maryna.json`  
3. Enable folder **7 – Signup DDT**  
4. Disable folder **8 – Profile DDT**  
5. Run  

---

### 4. Run Profile DDT
1. Open Runner  
2. Select data file: `profile_test_data_valentyr_maryna.json`  
3. Enable folder **8 – Profile DDT**  
4. Disable folder **7 – Signup DDT**  
5. Run  

---

## What the Tests Validate

- Correct status codes (200, 201, 400, 500)  
- Error messages for invalid data  
- Successful profile updates (name, lastName, dateOfBirth)  
- Response structure (`status`, `message`, `data`)  
- Session cookie handling  
- Full happy-path API flow  
- Cleanup ensures repeatable, isolated test runs  

---

## Tools & Skills Demonstrated

- Postman API testing  
- Environments (Dev/Prod separation)  
- Data-Driven Testing (DDT)  
- JavaScript test scripts (`pm.*`)  
- Iteration data validation  
- Request organization & folder structure  
- API negative + positive testing  

---

## Author

**Valentyr Maryna**  
QA Manual & API Testing  
Postman · JSON · DDT · Assertions · Test Design · Dev/Prod Environments

