<img width="750" src="https://raw.githubusercontent.com/lemonsaurus/lemonsaurus/main/django-starter.png" alt="This man is baking a Django.">

This project provides a useful starter dough that you can use to bake a delicious Django cake! It's extremely opinionated, just like Django, and is mostly just something I'll use for my own projects -- Although, you're welcome to use it if you want!

# What's included?

- A basic `Pipfile` with some useful packages and scripts.
- A `docker-compose` file that allows hot-seat reloading and includes a PostgreSQL database that will automatically hook up to your Django app.
- `gunicorn` for launching your webapp with several workers and threads. Makes it more scalable, basically. 
- `nginx` for serving your static files. All static files must be within `static/` folder. In order to get static files in django admin section working please run `python manage.py collectstatic --noinput` in your project's directory. It will copy necessary static files from Django app installed in virtual environment.
- A `.gitignore` with some common ignores in it.
- One Django app with nothing in it.

# Okay, now how do I do this?
Make sure `docker` and `docker-compose` are installed, then just run `docker-compose up` in the root folder. This will launch your app, and the files will all be hot-reloadable, so you can just write code and refresh the browser.

This will set up a database too, but the database will not persist any data.


# Docker is scary, do I have to use it?
Well, no. Here's how you would use it without Docker.

First, you'll need PostgreSQL running somewhere. You'll also need to make sure `pipenv` is installed. Then create a new file called `.env` in the root folder, and fill it with something like this:
```dotenv
DEBUG=1
SECRET_KEY=yellowpolkadotbikini
POSTGRES_USER=lemon
POSTGRES_PASSWORD=coolpassworddude
POSTGRES_HOST=localhost
POSTGRES_PORT=5432
```

Now to start your app, just run `pipenv install` to set everything up, and then `pipenv run start` to run the app.


