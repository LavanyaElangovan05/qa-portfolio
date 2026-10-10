# QA Portfolio - Lavanya Elangovan

Senior QA Engineer with 7+ years of experience in US healthcare payer systems (FACETS, EDI 834, eligibility and enrollment). This portfolio shows my manual testing, API testing, and automation work, all using synthetic data.

## Projects
1. Healthcare Enrollment Testing
2. API Testing
3. UI Automation Framework
4. QA Metrics Dashboard

## Automated checks (Day 3)
- Assertions on status code, response time and body fields
- Environment variable (`baseUrl`) instead of a hard-coded address
- Request chaining: the booking ID from the POST is saved and reused in the GET
- Collection Runner: 3 requests, 8 tests, all passing

## How to run
1. In Postman, import `Restful Booker.postman_collection.json` and `Restful Booker Env.postman_environment.json`.
2. Select **Restful Booker Env** in the top-right dropdown.
3. Open the collection's Runner, untick "Create booking - negative tests", and click Start run.