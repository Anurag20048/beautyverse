# BeautyVerse: Recruiter Snapshot

## 30-second view

BeautyVerse is a portfolio-grade full-stack BeautyTech application built with Django. It models a real product rather than a static UI: users authenticate, complete an AI-assisted skin workflow, receive recommendations, discover salons and doctors, book services, and retain a Beauty Passport history.

## What a reviewer can evaluate

- Backend architecture and domain separation in Django apps
- Authentication and protected web routes
- Serializers, views, permissions and service-layer business logic
- Database models and migration handling
- AI integration with deterministic fallback behavior
- Booking, availability and consultation workflows
- Responsive browser UI with reusable static assets
- Automated validation through pytest and Django checks
- CI, Docker and Render deployment configuration

## Start here

1. Read `README.md` for the product and setup overview.
2. Open `src/backend/apps/` to inspect the domain architecture.
3. Review `src/backend/apps/salons/services.py` and `src/backend/apps/doctors/services.py` for business-logic separation.
4. Review `src/backend/apps/*/tests/` for application-level tests.
5. Review `src/.github/workflows/ci.yml`, `src/render.yaml` and `src/infra/docker/` for delivery/deployment practices.
6. Review `src/docs/` and `src/backend/VERIFY_RELEASE.md` for release engineering.

## Interview discussion points

- Why service/selector layers are used instead of putting all logic in views
- How protected routes and authentication state are handled
- How the app remains usable without an external AI provider
- How migration validation is separated from pytest's test-database setup
- How environment variables keep credentials out of source control
- What would change to productionize the AI/vision pipeline and observability stack

## Portfolio note

The repository documents both implemented capabilities and production prerequisites. External credentials and managed infrastructure are not committed to source control.
