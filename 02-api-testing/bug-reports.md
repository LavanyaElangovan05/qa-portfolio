# Bug Reports - Restful-Booker API

Tested using Postman against https://restful-booker.herokuapp.com (public practice API).

## Bug 1: POST /booking returns 500 when lastname is missing

**Steps to reproduce**
1. Send POST to /booking with headers Content-Type: application/json and Accept: application/json.
2. Use a valid body with the lastname field removed.
3. Observe the response.

**Expected result:** 400 Bad Request with a message saying lastname is required.

**Actual result:** 500 Internal Server Error, with the plain-text body "Internal Server Error" and no field-level message.

**Severity:** Medium | **Priority:** Medium

## Bug 2: POST /booking accepts non-numeric totalprice and saves it as null

**Steps to reproduce**
1. Send POST to /booking with the same headers.
2. Use a valid body but set totalprice to "abc".
3. Observe the response.

**Expected result:** 400 Bad Request with a message that totalprice must be a number, and no booking created.

**Actual result:** 200 OK. A booking was created (id 4304) with totalprice null. No error or warning was returned.

**Severity:** High (invalid input silently becomes missing data) | **Priority:** Medium