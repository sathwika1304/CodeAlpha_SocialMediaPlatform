# Connectly — Social Media Platform

A beginner-friendly social media web application built with Django, Python, SQLite, HTML, and CSS. Users can create accounts, share posts, add images, like posts, comment, and customize their profile.

## Features
- User registration, login, and logout
- Community home feed with newest posts first
- Create, edit, and delete your own posts
- Optional image upload on posts
- Like/unlike posts (one like per user per post)
- Add comments to posts
- Public user profiles with bio, profile photo, and posts
- Django admin for managing profiles, posts, likes, and comments
- Responsive layout for desktop and mobile
- SQLite database for local development

## Requirements
- Python 3.10 or newer
- pip

## Run on Ubuntu/Linux

```bash
# Go to the project folder
cd ~/Downloads/CodeAlpha_SocialMediaPlatform

# Create and activate a virtual environment (skip creation if you already made it)
python3 -m venv venv
source venv/bin/activate

# Install packages
pip install -r requirements.txt

# Create database tables
python manage.py makemigrations social
python manage.py migrate

# Optional: create an admin login
python manage.py createsuperuser

# Start the local development server
python manage.py runserver
```

Open http://127.0.0.1:8000/ in your browser. Admin page: http://127.0.0.1:8000/admin/.

## Main project structure

```text
CodeAlpha_SocialMediaPlatform/
├── config/                 # Django project settings and URLs
├── social/                 # Models, forms, views, and admin
│   ├── migrations/
│   ├── static/social/      # CSS
│   └── templates/social/   # HTML pages
├── manage.py
├── requirements.txt
└── README.md
```

## Security note
This project is configured for local development (`DEBUG = True`) and includes a development-only secret key. Before deploying it publicly, set `DEBUG = False`, use a private environment-based secret key, configure `ALLOWED_HOSTS`, and configure secure file uploads and HTTPS.

## Internship task
Created as a learning project for the CodeAlpha Social Media Platform task.
