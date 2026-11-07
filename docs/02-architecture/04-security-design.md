# Security Design — LinkLite

## 1. Input Validation

All submitted URLs must be validated.

Only HTTP and HTTPS schemes are accepted.

Maximum URL length is 2,048 characters.

## 2. Database Security

- Use Django ORM for database operations.
- Avoid unsafe raw SQL.
- Enforce database-level uniqueness constraints.
- Store credentials in environment variables.

## 3. Redirect Security

- Resolve short codes against stored database records.
- Never construct redirect destinations directly from user-controlled short-code input.
- Only redirect to previously validated stored URLs.
- Use the approved HTTP redirect behaviour.

## 4. Error Handling

Internal database details and stack traces must not be exposed to API consumers.

## 5. Future Security Improvements

- Rate limiting.
- Abuse detection.
- Malicious URL detection.
- Authentication.
