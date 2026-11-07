# Functional Requirements — LinkLite

## 1. Introduction

This document defines the functional behaviour required for LinkLite Phase 1.

## 2. URL Submission

The system must accept URL submissions through an HTTP POST request.

Requirements:
- Accept HTTP and HTTPS URLs only.
- Reject empty URLs.
- Reject malformed URLs.
- Reject URLs exceeding 2,048 characters.

## 3. Short-Code Generation

The system must:
- Generate unique alphanumeric short codes.
- Generate identifiers between 6 and 8 characters.
- Prevent existing codes from being overwritten.
- Associate each code with its original URL.

## 4. URL Creation

The system must return:
- Original URL.
- Short code.
- Complete shortened URL.
- Creation timestamp.

## 5. URL Redirection

When a visitor accesses a short URL:
1. Extract the short code.
2. Find its associated database record.
3. Retrieve the original URL.
4. Return an HTTP 302 redirect.

Unknown codes must return HTTP 404.

## 6. Duplicate URL Handling

If an identical URL already exists, the system must return its existing short code.

Matching must use the exact submitted URL string.

## 7. URL Information Retrieval

The system must expose an endpoint that allows consumers to retrieve information associated with an existing short code.

## 8. Authentication

Authentication is not required in Phase 1.

All users can create shortened URLs anonymously.
