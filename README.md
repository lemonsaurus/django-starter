# Django-starter
<img width="550" src="https://cdn.pixabay.com/photo/2020/11/28/12/25/bread-5784572_960_720.jpg" alt="Django starter, baby!">

This project provides a useful starter dough that you can use to bake a delicious Django cake! It's extremely opinionated, just like Django, and is mostly just something I'll use for my own project -- Although, you're welcome to use it if you want!

# What's included?

- A basic `Pipfile` with some useful packages and scripts.
- A `docker-compose` file that allows hot-seat reloading and includes a PostgreSQL database that will automatically hook up to your Django app.
- `gunicorn` for launching your webapp with several workers and threads. Makes it more scalable, basically.
- `whitenoise` which is super convenient for serving static files straight out of your webapp. Greatly simplifies things.
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



