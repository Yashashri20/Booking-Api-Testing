
# Booking API Automation Testing

This repository presents an **automated API testing project** built around the Booking API. The test suite focuses on validating complete booking workflows using **Postman** for test design and **Newman** for command-line execution and report generation.

The project demonstrates practical knowledge of API testing, environment handling, assertions, and professional reporting.

---

##  Overview

The purpose of this project is to verify that the Booking API performs reliably across its core endpoints. Multiple scenarios are tested to ensure correct API behavior during booking creation, data retrieval, updates, and deletion operations.

Both **functional correctness** and **performance aspects** are validated to ensure the API responds accurately and within acceptable response times.

---

##  Highlights of the Test Suite

* **Core API Coverage**
  End-to-end validation of booking-related endpoints including create, read, update, and delete operations.

* **Environment-Based Execution**
  Uses Postman environments to manage base URLs, authentication tokens, and dynamic values efficiently.

* **CLI Automation with Newman**
  Enables collection execution from the command line with support for multiple report formats.

* **Rich Test Reports**
  Generates JSON, standard HTML, and **HTML Extra** reports for detailed execution analysis.

---

##  Repository Contents

| File                                                 | Description                                               |
| ---------------------------------------------------- | --------------------------------------------------------- |
| `Booking_ApiTesting.json`                            | Postman collection containing automated API test cases    |
| `Environment_BookingAPI.json`                        | Environment configuration with required variables         |
| `Booking Api Testing.postman_test_run.json`          | JSON output of test execution with logs                   |
| `newman-run-report-2024-09-22-12-51-08-091-0.html`   | Standard Newman HTML execution report                     |
| `Booking Api Testing-2024-09-22-13-21-31-213-0.html` | Detailed HTML Extra report with request and response data |

---

##  Prerequisites & Setup

### Required Software

* **Node.js** (version 14 or higher)
* **Postman**
* **Newman**

Install Newman globally:

```bash
npm install -g newman
```

### Install HTML Extra Reporter

```bash
npm install -g newman-reporter-htmlextra
```

---

##  Executing the Tests

### Running via Postman

1. Open Postman
2. Import the collection and environment files
3. Select the configured environment
4. Run the collection using the Collection Runner

---

### Running via Newman (Command Line)

#### Standard Execution

```bash
newman run Booking_ApiTesting.json -e Environment_BookingAPI.json
```

#### Execution with HTML Extra Report

```bash
newman run Booking_ApiTesting.json -e Environment_BookingAPI.json -r htmlextra \
--reporter-htmlextra-export newman-run-report.html
```

The generated HTML report can be viewed in any web browser.

---

## 🧪 Tested API Endpoints

* **Create Booking (POST)**
  Validates booking creation with both valid and invalid request payloads.

* **Retrieve Booking (GET)**
  Confirms booking details retrieval using booking ID, including negative scenarios.

* **Update Booking (PUT)**
  Ensures existing booking records can be updated correctly.

* **Delete Booking (DELETE)**
  Verifies deletion behavior and error handling for non-existent bookings.

---

##  Assertions & Validations

The following checks are implemented across test cases:

* HTTP status code verification (200, 201, 400, 401, 404, etc.)
* API response time validation
* JSON schema compliance
* Data accuracy validation (IDs, dates, and fields)
* Error and negative scenario handling
* Authentication and authorization validation

---

## Test Reports

The **HTML Extra reports** provide:

* Summary of executed and failed tests
* Detailed request and response payloads
* Assertion results with failure explanations
* Performance metrics such as response time
* Error logs for failed scenarios

Included example reports:

* `newman-run-report-2024-09-22-12-51-08-091-0.html`
* `Booking Api Testing-2024-09-22-13-21-31-213-0.html`

---

 Planned Improvements

* CI/CD integration using Jenkins or GitHub Actions
* Performance and load testing extensions
* Expanded negative and edge-case coverage
* Security-focused test scenarios
* Data-driven testing using external data files

---
Contributions

Contributions are welcome. Feel free to raise issues or submit pull requests that enhance test coverage or improve automation quality.





