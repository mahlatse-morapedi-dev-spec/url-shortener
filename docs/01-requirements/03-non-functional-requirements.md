# Non-Functional Requirements — LinkLite

## 1. Performance

- URL creation should normally complete within 500 milliseconds under light MVP load.
- Redirect operations should normally complete within 200 milliseconds under light MVP load, excluding destination website response time.

## 2. Reliability

- URL records must persist across application restarts.
- Invalid requests must not crash the application.
- Database constraints must protect short-code uniqueness.

## 3. Security

- Validate all submitted URLs.
- Accept HTTP and HTTPS schemes only.
- Use Django ORM to avoid unsafe SQL construction.
- Protect sensitive environment variables.
- Return controlled error responses.
- Do not expose internal database errors.

## 4. Maintainability

- Separate API handling from business logic.
- Separate business logic from data persistence.
- Maintain automated tests.
- Maintain technical documentation.

## 5. Scalability

The initial system will use a modular monolithic architecture.

Future scalability improvements may include:
- Redis caching.
- Rate limiting.
- Horizontal scaling.
- Load balancing.

These are not mandatory Phase 1 implementations.
