# Restful-booker API Testing 
API test suite for the [Restful-booker](https://restful-booker.herokuapp.com) playground API, built  with Postman. Covers functional, workflow and basic security testing across 8 endpoints. 
## Scope
|Area | Coverage |
|---|---|
| Endpoints | Auth, Booking CRUD (6), Ping |
| Test types | Functional, response schema, negative/validation, E2E workflow, security |
## Structure 
- `postman/` — collection + environment (import into Postman to run)
- `docs/` — test plan, test cases, findings
 
## How to run 
1. Import both files in 'postman/' into Postman 
2. Select the 'booker-prod' environment 
3. Run the collection with Collection Runner 
## Findings (spec vs actual)
- Missing required field returns **500** instead of 400 (POST /booking)
- Invalid credentials return **200 + "Bad credentials"** instead of 401 (POST /auth)
-see the full findings log (5 findings) in `docsTestcases_RestfulBooker.xlsx`, sheet *Findings_DevLog*
## Roadmap 
- [x] P1 happy path with assertions 
- [x] Self-written test cases for Ping and Auth (executed, with findings)
- [ ] Test cases for all endpoints 
- [ ] Auth-protected PUT/PATCH/DELETE
- [ ] Full CRUD workflow suite 
- [ ] Newman CLI + GitHub Actions CI
