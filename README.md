# QA-Automation API Tests (Postman) — Valentyr Maryna

This repository contains a complete Postman project designed for API testing.  
It includes a structured API collection, separate Dev/Prod environments, and fully implemented Data-Driven Tests (DDT) using JSON files.

---

## What’s Included

### API Collection
A full test suite covering:
- User registration (signup)
- Login and session handling
- Profile update and validation
- Car and expense management
- Negative validation scenarios
- Automated cleanup

### Environments
Two separate Postman environments:
- QA Auto-Dev
- QA Auto-Prod

Both environments contain `baseUrl` and required variables.

### Test Data (DDT)
JSON files used for data-driven tests:
- `signup_test_data_valentyr_maryna.json`  
- `profile_test_data_valentyr_maryna.json`

Each contains positive and negative scenarios.

---

## How to Run the Tests

### 1. Import the project
- Import the collection file
- Import both environment files

### 2. Run the main flow (without DDT)
1. Select environment:  
   - QA Auto-Dev **or**  
   - QA Auto-Prod  
2. Run the entire collection  
This performs the complete flow: signup → login → profile → cars → cleanup.

---

### 3. Run Signup DDT
1. Open Postman Runner  
2. Select data file: `signup_test_data_valentyr_maryna.json`  
3. Enable folder **7-Signup DDT**  
4. Disable **8-Profile DDT**  
5. Run the test — each row in the JSON becomes an iteration.

---

### 4. Run Profile DDT
1. Open Postman Runner  
2. Select data file: `profile_test_data_valentyr_maryna.json`  
3. Enable **8-Profile DDT**  
4. Disable **7-Signup DDT**  
5. Run the test — the flow validates profile fields and positive update.

---

## What the Tests Cover
- Positive and negative signup
- Session creation (signin)
- Profile validation (required fields, invalid dates, formats)
- Successful profile update
- Car and expense operations
- Cleanup (user deletion)
- Assertions on:
  - Status codes  
  - Response structure  
  - Error messages  
  - Updated fields  
- DDT using external JSON files

---

## Why This Project Works Well for a Portfolio
- Demonstrates API testing skills with Postman
- Uses environments professionally (Dev/Prod separation)
- Shows understanding of DDT with iteration data
- Contains clean structure and readable tests
- Easy for instructors and recruiters to import and run
- Reflects real testing workflow with setup and cleanup

---

## Author
**Valentyr Maryna**  
API & QA Testing  
Postman · JSON · DDT · Environments · Assertions
