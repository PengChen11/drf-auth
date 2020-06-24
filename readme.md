# Lab: Authentication & Production Server

## Overview

Let’s move our API closer to production grade by adding Authentication and switching to a Production Server

## Feature Tasks and Requirements

### Features - Django

- Add JWT Authentication to your API.
  - Install needed libraries in project configuration and/or site settings.
- Keep existing authentication so DRF Browsable API still usable.
  -That includes keeping the styling
  -Install needed libraries in project configuration and/or site settings.

### Features - Docker

- Create a boilerplate ```Dockerfile``` and ```docker-compose.yml``` so you don’t need to start from scratch each time.
- Switch to using Gunicorn instead of Django’s built in development server.
  - mind the number of workers to avoid sluggishness
- Warning You will run into styling issues when you switch over to Gunicorn.
  - On Django side you’ll need to properly handle static files.
- Adjust ```docker-compose.yml``` so that data is persisted in a volume outside of container.

## Stretch Goals

- Research deployment options for Docker/Postgres/Django and report findings to class
- Create a ```seed``` project on Github so that you can have a running start on next DRF project.

## Implementation Notes

### User Acceptance Tests

- Use tests from demo and adjust as needed for your project.
- Ensure tests pass

## Misc

After install httPie, using the folloing bash command to requests token and use it

```bash
http POST :8000/api/token/ username=(your user name) password=(your password)
```

```bash
http :8000/api/ "Authorization: Bearer (token_here)"
```
