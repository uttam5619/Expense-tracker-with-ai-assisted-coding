# Coding Standards

## 1. General Principles

- Write clean, readable, and maintainable code.
- Follow the Single Responsibility Principle.
- Avoid unnecessary complexity.
- Prefer simple and explicit implementations over clever code.
- Do not duplicate logic.
- Reuse existing utilities, services, and components where appropriate.
- Do not introduce new dependencies unless required.
- Do not modify unrelated files while implementing a feature.

---

### Naming Conventions for variables files and functions

## Naming conventions for Variables

- Use descriptive names.
- Use camelCase.

## Naming conventions for Files
- Use descriptive names.
- Follow the naming convention already established by the project.
- Do not introduce multiple naming conventions.

## Naming convention for Functions
- Use descriptive names.
- Use camelCase.

### Functions
- Functions should follow the single responsibility principle.
- Extract reusable logic into separate functions.
- Avoid deeply nested conditional logic.

### Error Handling
- Never silently ignore errors.
- Handle errors at the appropriate layer.
- Return meaningful error messages.
- Do not expose sensitive internal information to clients.
- Use appropriate HTTP status codes.

### Validation
- Validate all external input.
- Never trust client-provided data.
- Validate request body, query parameters, and route parameters.
- Validate data before sending it to the database.
- Keep validation logic separate from business logic where possible.

### Database
- Database operations should be isolated from controllers.
- Do not place database queries directly inside route definitions.
- Use appropriate indexes for frequently queried fields.
- Use foreign keys where relationships require referential integrity.
- Use transactions when multiple database operations must succeed or fail together.
- Avoid unnecessary database queries.
- Never store sensitive data in plain text.

### API Standards
The api needs tostrictly follow the REST conventions. The standerd REST conventions are mentioned below under the HTTP Methods and status code.

## HTTP Methods
Use HTTP methods according to their intended purpose:
- GET → Retrieve data
- POST → Create data
- PUT → Replace/update data
- PATCH → Partially update data
- DELETE → Delete data

## Status Codes
Use appropriate HTTP status codes:
- 200 -> OK
- 201 -> Created
- 204 -> No Content
- 400 -> Bad Request
- 401 -> Unauthorized
- 403 -> Forbidden
- 404 -> Not Found
- 409 -> Conflict
- 422 -> Unprocessable Entity
- 500 -> Internal Server Error

### Response Format
The response format will need to include following attributes
- success : true/false
- message
- data

Ex- If an action results in success then it should result in success:true, followed by a one liner descriptive message and the data. If the action is of POST,PUT,PATCH type then it should include the new data. If the action is of GET,DELETE type then it should include the existing data.


### Authentication and Authorization
- Authentication and authorization must be handled separately.
- Never store passwords in plain text.
- Passwords must be hashed using a secure password-hashing algorithm.
- Never expose passwords or sensitive authentication data in API responses.
- Protected resources must verify authentication.
- Authorization must be checked before performing protected operations.


### Security
- Never hardcode secrets, API keys, passwords, or tokens.
- Store secrets in environment variables.
- Validate and sanitize external input.
- Prevent SQL injection through parameterized queries/ORM mechanisms.
- Do not expose stack traces or internal errors to clients.
- Do not log passwords, tokens, or other sensitive information.


### Comments
- Write comments only when they provide useful context.
- Do not comment obvious code.
- Prefer self-explanatory code over excessive comments.
- Comments should explain why, not simply what.


### Logging
- Use structured and meaningful logs.
- Do not log sensitive information.
- Avoid excessive logging.
- Log important application events and errors.
- Use appropriate log levels such as: INFO, WARN, ERROR, DEBUG.


### Environment Configuration
- Environment-specific configuration must be stored in environment variables.
- Never commit .env files containing secrets.
- Provide .env.example when environment variables are required.
- Use descriptive environment variable names.


### Dependency Management
- Do not install a package when the existing project functionality can solve the problem.
- Use stable and maintained dependencies.
- Avoid duplicate libraries providing the same functionality.
- Keep dependencies updated when appropriate.
- Do not modify dependency versions unnecessarily.


### Code Formatting
- Use consistent indentation.
- Use the project's formatter if one exists.
- Avoid unnecessarily long lines.
- Use consistent spacing and brackets.
- Do not mix formatting styles within the project.


### Testing
- New functionality should include appropriate tests.
- Test business logic independently.
- Test important edge cases.
- Test validation and error conditions.
- Do not consider a feature complete if critical functionality is untested.


### Changes to Existing Code
Before modifying existing code:
- Understand the existing implementation.
- Identify dependencies.
- Check whether reusable functionality already exists.
- Make the smallest change necessary.
- Avoid unrelated refactoring.
- Verify that existing functionality still works.



### AI Coding Agent Rules
When an AI coding agent works on this project:
- Read AGENTS.md before making changes.
- Read the relevant project context before implementing a feature.
- Read the applicable specification before writing code.
- Follow the architecture and coding standards defined by the project.
- Do not invent requirements.
- Do not change requirements without explicit approval.
- Do not modify unrelated files.
- Reuse existing project patterns.
- Validate the implementation after making changes.
- Report any ambiguity instead of making assumptions.