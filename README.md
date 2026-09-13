# BeautyVerse

> A full-stack BeautyTech platform for personalized beauty discovery, salon services, wellness consultations, bookings, and provider operations.

[![CI](https://github.com/Anurag20048/beautyverse/actions/workflows/ci.yml/badge.svg)](https://github.com/Anurag20048/beautyverse/actions/workflows/ci.yml)

## Overview

**BeautyVerse** is a web application designed to bring beauty and wellness journeys into one platform. It connects customers with beauty service providers and consultation workflows while adding AI-assisted personalization features.

The project is built as a practical full-stack application rather than a static UI demo. It includes a Django backend, domain-based applications, role-aware portals, booking and payment models, notifications, analytics, automated tests, CI configuration, environment-based settings, and deployment support.

## Key features

- Customer authentication, dashboard, profile and Beauty Passport
- Camera/image-based AI skin scan workflow
- AI assistant with deterministic local fallback
- Salon discovery, services, availability and booking flow
- Verified doctor discovery and consultation workflow
- Role-based customer, salon, doctor and admin portals
- Django tests, migration validation and GitHub Actions CI
- Docker and Render deployment configuration

## Run locally on Windows

```powershell
git clone https://github.com/Anurag20048/beautyverse.git
cd beautyverse\src\backend
python -m venv venv
venv\Scripts\activate
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
python manage.py check
python manage.py makemigrations --noinput
python manage.py makemigrations --check
python manage.py migrate --noinput
python -m pytest -q
python manage.py seed_demo_data
python manage.py runserver
```

Open **http://127.0.0.1:8000/**

### One-command setup

From `src/backend`:

```powershell
setup_windows.bat
verify_local.bat
```

> Install from `backend/requirements.txt`. The `backend/requirements/` folder contains dependency splits and should not be passed directly to `pip -r`.

## Project structure

```text
src/
├── backend/                 # Django application
│   ├── apps/                # Domain applications
│   ├── config/              # Settings, URLs, ASGI/WSGI
│   ├── templates/           # Web UI
│   ├── static/              # CSS, JS, service worker, favicon
│   ├── requirements/        # Split dependency files
│   ├── requirements.txt
│   ├── manage.py
│   ├── setup_windows.bat
│   └── verify_local.bat
├── frontend/
├── docs/
├── infra/docker/
├── .github/workflows/
├── docker-compose.yml
├── render.yaml
└── build.sh
```

## Architecture

```text
Browser
  |
  v
Django templates + static UI
  |
  +-- Customer portal
  +-- Salon portal
  +-- Doctor portal
  +-- Admin portal
  |
  v
Django application layer
  |
  +-- users
  +-- salons
  +-- doctors
  +-- bookings
  +-- AI scan
  +-- Beauty Passport
  |
  +-- PostgreSQL
  +-- Redis / cache
  +-- Optional AI provider
```

## Important routes

`/` · `/login/` · `/dashboard/` · `/scan/` · `/assistant/` · `/passport/` · `/services/` · `/bookings/` · `/profile/` · `/doctor-portal/` · `/salon-portal/` · `/admin-portal/`

## Deployment

Included: `render.yaml`, Dockerfiles, `docker-compose.yml`, `build.sh`, production requirements, CI and release validation documentation.

A public production deployment still requires environment-specific credentials and managed services such as PostgreSQL, Redis, SMS/email and an AI provider.

## Verification

See `docs/FINAL_VALIDATION.md`, `docs/TESTING_AND_RELEASE.md`, `docs/RELEASE_GATES.md` and `backend/VERIFY_RELEASE.md`.

Full execution of the release checks requires package/network access and any external services needed by the chosen configuration.

## Security note

No real third-party credentials are stored in the repository. Production secrets are expected through environment variables. The AI scan workflow is intended for consumer-level visible observations, not clinical diagnosis.

## Professional project description

**BeautyVerse is a full-stack BeautyTech platform built with Django that combines beauty-service discovery, personalized customer experiences, AI-assisted skin analysis, salon booking, doctor consultation workflows, provider portals, notifications, payments, and analytics. The project uses a domain-oriented backend structure with role-based access control, service-layer business logic, automated testing, CI validation, environment-based configuration, and Docker/Render deployment support.**

## Resume project entry

**BeautyVerse | Full-Stack BeautyTech Platform**

Developed a Django-based BeautyTech platform integrating beauty-service discovery, personalized customer workflows, AI-assisted skin analysis, salon booking, consultation workflows, provider portals, notifications, payments, and analytics. Implemented role-based access control, domain-oriented business logic, automated testing, CI validation, environment-based configuration, and container/cloud deployment support.

**Tech:** Python, Django, Django REST Framework, PostgreSQL, Redis, JavaScript, HTML/CSS, Docker, GitHub Actions, Render, pytest, OpenAI API

## Author

**Anurag20048**  
https://github.com/Anurag20048
