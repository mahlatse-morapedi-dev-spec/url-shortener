# Component Architecture — LinkLite

## 1. Django Project

The `config` package contains global application configuration.

Responsibilities:
- Django settings.
- Root URL configuration.
- ASGI configuration.
- WSGI configuration.

## 2. Shortener Application

The `shortener` Django application contains the URL shortening functionality.

### models.py

Defines database models and their constraints.

### serializers.py

Validates incoming API data and controls API response representation.

### views.py

Handles HTTP requests and returns HTTP responses.

### services.py

Contains business logic, including short-code generation and URL creation.

### urls.py

Defines URL routes belonging to the shortener application.

### tests.py

Contains automated tests for application functionality.

## 3. Component Interaction

Views receive requests and invoke business logic.

Services coordinate operations and interact with models.

Models represent persistent database records.

Serializers validate and represent API data.

## 4. Architectural Principle

Business logic should not be unnecessarily duplicated across API views.

Database operations should use Django ORM.
