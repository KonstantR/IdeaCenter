# IdeaCenter API Testing

## Overview
This project contains API tests for the IdeaCenter application using Postman and Newman.

## Tools Used
- Postman
- Newman
- Newman HTML Extra Reporter
- Node.js

## Test Scenarios
The collection contains 5 API requests:

1. **Login** – authenticate a user and obtain an access token.
2. **Create New Idea** – create a new idea.
3. **List All Ideas** – retrieve ideas.
4. **Edit Idea** – update an existing idea.
5. **Delete Idea** – delete an idea.

## Test Results
- Total requests: 5
- Total assertions: 15
- Failed assertions: 0
- Skipped tests: 0

All 15 assertions passed in the recorded test run.

## Project Files
- `IdeaCenter.postman_collection.json` – exported Postman collection.
- `IdeaCenter-Report-SANITIZED.html` – sanitized Newman HTML report.

## User Setup

The collection uses an existing IdeaCenter user account.

If you don't have an account yet, register manually by sending a `POST` request to `/api/User/Create`.

Set the request body to `raw` → `JSON` in Postman:

```json
{
  "userName": "your_username",
  "email": "your_email@example.com",
  "password": "your_password",
  "rePassword": "your_password",
  "acceptedAgreement": true
}
```

Next, open the `Login` request and enter your own email and password. After a successful login, the collection script automatically saves the returned access token in the `token` collection variable.

The remaining idea requests use this token for authorization.

**Note:** Use your own credentials.

## How to Run

### Prerequisites
- Install [Node.js](https://nodejs.org/).
- Install Newman and the HTML Extra reporter:

```bash
npm install -g newman newman-reporter-htmlextra
```

### Run the API tests

Open a terminal in the project directory and run:

```bash
newman run IdeaCenter.postman_collection.json
```

### Generate an HTML report

Run the following command to execute the collection and generate an HTML report:

```bash
newman run IdeaCenter.postman_collection.json -r htmlextra --reporter-htmlextra-export IdeaCenter-Report.html
```

The report is generated locally in the project directory.
