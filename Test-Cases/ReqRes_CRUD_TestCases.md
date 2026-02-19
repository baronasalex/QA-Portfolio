# Test Cases — ReqRes User API

---

## TC-001 Get Existing User

**Preconditions**
- API available
- Valid API key added

**Steps**
1. Send GET request `/api/users/2`

**Expected Result**
- Status code = 200
- Response contains user data object
- User id = 2

---

## TC-002 Get Non-existing User

**Steps**
1. Send GET request `/api/users/23`

**Expected Result**
- Status code = 404
- Response body empty or error message returned

---

## TC-003 Create User

**Steps**
1. Send POST request `/api/users`
2. Provide name and job in body

**Expected Result**
- Status code = 201
- Response contains id
- Response contains createdAt timestamp

---

## TC-004 Update User

**Steps**
1. Send PUT request `/api/users/{id}`
2. Update job field

**Expected Result**
- Status code = 200
- Updated fields returned
- updatedAt present

---

## TC-005 Delete User

**Steps**
1. Send DELETE request `/api/users/{id}`

**Expected Result**
- Status code = 204
- Empty response body
