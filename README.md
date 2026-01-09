

# Roots To Realities App

A Django-based web application for managing events, bookings and resources for the Roots To Realities project.

## Summary

This repository contains the backend and frontend assets for the Roots To Realities application. It exposes REST APIs, admin UI and the web frontend. The project includes a Django app under `roots_to_realities` and a Django app `myapp` with models, serializers and endpoints.

## Features

- User and admin management (Django admin)
- REST API endpoints (Django REST Framework)
- JWT authentication (SimpleJWT)
- OpenAPI docs (drf-yasg)
- Static asset handling (WhiteNoise)

## Prerequisites

- Python 3.11+ (tested with 3.13)
- Git
- PostgreSQL (recommended for production) or SQLite for local testing

## Local setup

1. Clone the repository:

```bash
git clone https://github.com/FargoSeabi/RootsToRealitiesApp.git
cd RootsToRealitiesApp
```

2. Create and activate a virtual environment:

```powershell
python -m venv .venv
. .\.venv\Scripts\Activate.ps1
# or on bash: source .venv/bin/activate
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

4. Copy environment file and configure (create `.env` from `.env.example`) and set any required values (SECRET_KEY, DATABASE_URL, etc.).

5. Run database migrations and create a superuser:

```bash
python manage.py migrate
python manage.py createsuperuser
```

6. Start the development server:

```bash
python manage.py runserver
```

The app will be available at `http://127.0.0.1:8000/`.

## Running in production

This project includes configuration for deployment (Procfile, runtime.txt, whitenoise). For production use a WSGI/ASGI server (Gunicorn or Daphne) and a managed database. See `DEPLOYMENT.md` and `RENDER_DEPLOYMENT.md` for more details.

## Tests

Run Django tests with:

```bash
python manage.py test
```

## Contributing

Contributions are welcome. Please open issues or PRs on the repository.

## License

Add a `LICENSE` file if you intend to specify reuse terms.

