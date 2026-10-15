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

## How to Run
1. Install Node.js.
2. Install Newman:
   ```bash
   npm install -g newman
   ```
3. Run the collection:
   ```bash
   newman run IdeaCenter.postman_collection.json
   ```

## Security Note
Credentials and access tokens have been removed from the published report. Use your own authorized test environment and credentials when running the collection.