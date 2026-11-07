# url-shortener

A lightweight URL shortening service built with Python, Django REST Framework and PostgreSQL.

## Overview

LinkLite is a URL shortening platform that converts long URLs into short, shareable links.

When a visitor accesses a shortened URL, the application retrieves the original destination and redirects the visitor to it.

The primary objective of Phase 1 is to deliver a reliable URL shortening service with persistent storage and fast redirection.

## Core Features

- URL shortening
- Unique short-code generation
- URL redirection
- Duplicate URL detection
- URL validation
- Persistent URL storage
- RESTful API

## Technology Stack

| Component | Technology |
|---|---|
| Programming Language | Python |
| Backend Framework | Django |
| API Framework | Django REST Framework |
| Database | PostgreSQL |
| Version Control | Git |
| API Version | v1 |

## Project Architecture

LinkLite follows a modular monolithic architecture.

The application separates:
- API handling
- Business logic
- Data persistence

## Project Structure

```text
linklite/
├── docs/
├── config/
├── shortener/
├── manage.py
├── requirements.txt
├── README.md
├── CHANGELOG.md
├── VERSION
└── .env.example
```

## Current Version

0.1.0

See [CHANGELOG.md](CHANGELOG.md) for release history.

## Getting Started

Installation and configuration instructions will be added as the application is implemented.

## Documentation

Technical documentation is maintained in the `docs/` directory.

## Project Phases

### Phase 1 — MVP
- URL shortening
- Short-code generation
- URL redirection
- PostgreSQL integration
- Input validation
- Automated testing

### Future Phases
Potential enhancements include:
- User authentication
- URL analytics
- Custom short URLs
- QR code generation
- Rate limiting
- Caching

## Versioning

LinkLite follows Semantic Versioning:

`MAJOR.MINOR.PATCH`

All notable changes are recorded in CHANGELOG.md.

## License

To be determined.
