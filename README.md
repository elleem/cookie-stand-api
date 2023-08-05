## Project: Putting it All Together: A Restful API with a user facing site

Author: Lauren Main

Version 2.0

### Links and Resources

Thank you to Code Fellows for the Quick Start API

### Feature Tasks and Requirements

Version 1.0 Feature Tasks

- [x] install from requirements.txt
- [x] export requirements.txt
- [x] update template for cookie_stands
- [x] deploy with ElephantSQL and Vercel

Version 2.0 Feature Tasks

- [x] if user not logged in `<CreateNewUser>` renders
- [x] users cannot see other users' entries
- [x] updates API end points to allow new user registration in project\urls.py
- [x] updates models.py
- [x] adds serializer in cooke_stands\views.py
- [x] adds serializers.py in accounts
- [x] updates readme with [preview link](https://cookie-stand-api-git-dev5-elleem.vercel.app/)
- [x] updates readme with [deployed link](https://cookie-stand-api-omega.vercel.app/)

# api-quick-start

Template Project for starting up CRUD API with Django Rest Framework

## Customization Steps

- DO NOT migrate yet
- add additional dependencies as needed
  - Re-export requirements.txt as needed
- change `things` folder to the app name of your choice
- Search through entire code base for `Thing`,`Things` and `things` to modify code to use your resource
  - `project/settings.py`
  - `project/urls.py`
  - App's files
    - `views.py`
    - `urls.py`
    - `admin.py`
    - `serializers.py`
    - `permissions.py`
  - "Front" files
    - if including a customer facing portion of the site then update/recreate:
      - `urls_front.py`
      - `views_front.py`
      - template files
      - Make sure to update project `urls.py` to add routes to the "front".
- Update ThingModel with fields you need
  - Make sure to update other modules that would be affected by Model customizations. E.g. serializers, tests, etc.
- Rename `project/.env.sample` to `.env` and update as needed
  - To generate secret key use `python3 -c "import secrets; print(secrets.token_urlsafe())"`
- Run makemigrations and migrate commands when ready.
- Run `python manage.py collectstatic`
  - This repository includes static assets in repository. If you are using a Content Delivery Network then remove `staticfiles` from repository.
- Optional: Update `api_tester.py`

## Database

**NOTE:** If you are using Postgres instead of SQLite then make sure to install `psycopg2-binary` and include in `requirements.txt`

### Set up environment -

    python3.11 -m venv .venv
    source .venv/bin/activate

### Setup -

    pip install -r requirements.txt
    python manage.py makemigrations
    python manage.py migrate
    python manage.py createsuperuser
    python manage.py runserver
