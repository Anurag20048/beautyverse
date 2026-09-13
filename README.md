# BeautyVerse

AI-assisted beauty discovery, personalization, salon services, consultations, and booking in one full-stack web platform.

[![CI](https://github.com/Anurag20048/beautyverse/actions/workflows/ci.yml/badge.svg)](https://github.com/Anurag20048/beautyverse/actions/workflows/ci.yml)

## 🚀 Overview

BeautyVerse is a full-stack BeautyTech platform designed to bring beauty discovery, personalized recommendations, salon services, consultations, and booking workflows into one experience. It is built for customers looking for convenient beauty and wellness services, as well as salons and professionals who need dedicated workflows to manage services and bookings.

The platform combines a Django backend with responsive web interfaces, role-based portals, AI-assisted features, service discovery, booking workflows, notifications, payments, and analytics.

## 📸 Demo / Screenshot

The repository contains the complete application source and deployment configuration.

**Local application:** `http://127.0.0.1:8000/`

## ✨ Features

- Customer registration, authentication, dashboard, profile, and Beauty Passport
- AI-assisted skin scan workflow using camera/image input
- AI beauty assistant for personalized guidance
- Salon and beauty-service discovery
- Service availability and booking workflows
- Doctor discovery and consultation workflow
- Role-based portals for customers, salons, doctors, and administrators
- Provider service and booking management
- Notifications and follow-up workflows
- Payment domain and transaction handling
- Analytics and reporting components
- Automated tests and GitHub Actions CI
- Docker and Render deployment configuration

## 🛠️ Tech Stack

- **Backend:** Python, Django, Django REST Framework
- **Frontend:** HTML, CSS, JavaScript, Django Templates
- **Database:** PostgreSQL
- **Caching / infrastructure:** Redis
- **AI:** OpenAI API integration
- **Testing:** pytest, Django test framework
- **DevOps:** Docker, Docker Compose, GitHub Actions
- **Deployment:** Render

## 📦 Installation

### Windows

```powershell
git clone https://github.com/Anurag20048/beautyverse.git
cd beautyverse\src\backend
python -m venv venv
venv\Scripts\activate
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
python manage.py check
python manage.py migrate --noinput
```

For the project setup scripts:

```powershell
setup_windows.bat
```

Create your local environment file from the provided example configuration before enabling integrations that require credentials.

## ▶️ Usage

Start the Django development server:

```powershell
cd src\backend
python manage.py runserver
```

Open:

```text
http://127.0.0.1:8000/
```

Useful application routes include:

```text
/                     Home
/login/               Authentication
/dashboard/           Customer dashboard
/scan/                AI skin scan
/assistant/           AI beauty assistant
/passport/            Beauty Passport
/services/            Service discovery
/bookings/            Booking management
/profile/             Profile management
/salon-portal/        Salon portal
/doctor-portal/       Doctor portal
/admin-portal/        Admin portal
```

## 📁 Project Structure

```text
beautyverse/
├── src/
│   ├── backend/
│   │   ├── apps/              # Business-domain Django applications
│   │   ├── config/            # Settings, URLs, ASGI and WSGI
│   │   ├── templates/         # Application UI
│   │   ├── static/            # CSS, JavaScript and static assets
│   │   ├── requirements/      # Split dependency requirements
│   │   ├── manage.py
│   │   ├── requirements.txt
│   │   ├── setup_windows.bat
│   │   └── verify_local.bat
│   ├── frontend/
│   ├── docs/
│   └── infra/
├── .github/
│   └── workflows/             # CI automation
├── docker-compose.yml
├── render.yaml
├── build.sh
└── README.md
```

## 🧩 Architecture

```text
Browser
   |
   v
Django Templates + Static UI
   |
   +--> Customer Portal
   +--> Salon Portal
   +--> Doctor Portal
   +--> Admin Portal
   |
   v
Django Application Layer
   |
   +--> Users
   +--> Salons & Services
   +--> Bookings
   +--> Doctors & Consultations
   +--> AI Features
   +--> Beauty Passport
   +--> Payments
   +--> Notifications
   +--> Analytics
   |
   +--> PostgreSQL
   +--> Redis
   +--> External AI Services
```

## 🔧 Configuration

Create the local environment configuration from the included example file and add only the credentials required for the services you enable.

```text
DJANGO_SECRET_KEY=your_secret_key
DJANGO_DEBUG=True
DATABASE_URL=your_database_url
REDIS_URL=your_redis_url
OPENAI_API_KEY=your_api_key
```

Production credentials should be supplied through the deployment environment rather than committed to the repository.

## 🧪 Running Tests

Run Django validation and the automated test suite from the backend directory:

```powershell
cd src\backend
python manage.py check
python manage.py makemigrations --check
python manage.py migrate --check
python -m pytest -q
```

The repository also includes release and validation documentation under `docs/` and the backend verification files.

## 🗺️ Roadmap

- [ ] Expand AI-assisted personalization and recommendation capabilities
- [ ] Extend provider-side service management and analytics
- [ ] Add deeper notification and appointment automation
- [ ] Expand production integrations and deployment environments

## 🤝 Contributing

Pull requests and focused improvements are welcome. For larger changes, open an issue first to discuss the proposed direction.

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## 👤 Author

**Anurag Pareek**

- GitHub: [@Anurag20048](https://github.com/Anurag20048)
- Repository: [BeautyVerse](https://github.com/Anurag20048/beautyverse)
