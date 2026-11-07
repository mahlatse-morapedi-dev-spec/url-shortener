# Acceptance Criteria — LinkLite

## AC-01: Successful URL Creation

Given a valid HTTP or HTTPS URL,

When the client submits the URL,

Then the application must generate and return a shortened URL.

## AC-02: Successful Redirection

Given an existing short code,

When a visitor accesses it,

Then the application must return HTTP 302 and redirect to the original URL.

## AC-03: Invalid URL

Given an invalid URL,

When submitted,

Then the API must return HTTP 400.

## AC-04: Unknown Short Code

Given a short code that does not exist,

When accessed,

Then the application must return HTTP 404.

## AC-05: Duplicate URL

Given a previously shortened URL,

When submitted again,

Then the application must return the existing short URL.

## AC-06: Unique Short Codes

Given multiple URL creation requests,

When short codes are generated,

Then no existing short-code mapping may be overwritten.

## AC-07: Data Persistence

Given previously created URLs,

When the application restarts,

Then previously created mappings must remain available.

## AC-08: URL Length

Given a URL exceeding 2,048 characters,

When submitted,

Then the application must reject it with HTTP 400.

## Completion Definition

All acceptance criteria must pass their corresponding automated tests before Phase 1 is considered complete.
