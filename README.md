# Django React Template

Full-stack Django REST API with React frontend, PostgreSQL database, and CORS support.

## Features

- ✅ Django REST framework
- ✅ React frontend integration
- ✅ PostgreSQL database
- ✅ CORS enabled
- ✅ Static file serving
- ✅ Production ready

## Project Structure

```
django-react-template/
├── requirements.txt     # Python dependencies
├── settings.py         # Django configuration
├── core/              # Django project settings
├── api/               # Django REST API
└── frontend/          # React build output
```

## Installation

```bash
# Install Python dependencies
pip install -r requirements.txt

# Install Node.js dependencies for frontend
cd frontend
npm install
npm run build

# Go back to root
cd ..
```

## Configuration

Create `.env` file:

```bash
SECRET_KEY=your-secret-key-here
DEBUG=True
DB_NAME=mydb
DB_USER=myuser
DB_PASSWORD=mypassword
DB_HOST=localhost
DB_PORT=5432
ALLOWED_HOSTS=localhost,127.0.0.1
```

## Database Setup

```bash
# Create database
createdb mydb

# Run migrations
python manage.py migrate

# Create superuser
python manage.py createsuperuser
```

## Development

```bash
# Run Django server
python manage.py runserver

# Run with custom port
python manage.py runserver 0.0.0.0:8000

# Run with live reload
pip install django-livereload
python manage.py livereload
```

## Production

```bash
# Collect static files
python manage.py collectstatic

# Run with production settings
DJANGO_SETTINGS_MODULE=core.settings.production python manage.py runserver

# Use Gunicorn
gunicorn core.wsgi:application
```

## API Endpoints

- `GET /api/` - API root
- `GET /admin/` - Django admin
- `POST /api/users/` - Create user
- `GET /api/users/` - List users

## License

MIT
