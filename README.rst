pmsproject
==========

Just one more CMS


Project has two branches on gitlab:
 - master(for deploy to prod) - never commit to master branch.
 - dev - (for tests, etc) where you have to commit.



This project can be run in 4 ways:

 - **production-remote-docker**: these are settings to run it in docker on prod server(heroku, or any other server)

 - **production-local-docker**: these are settings to run it locally in docker with settings as close as possible to real production-remote-docker settings. Run this to see how all goes if not possible to run it on remote server.

 - **dev-local-docker-complete**: these are settings to run it locally for dev totally with docker, these are ok if internet connection is good. Try to keep these settings also as similar as possible with production settings.

 - **dev-local-docker-partly**: these are settings to run it for dev locally - django runs just inside conda environment, and postgres and redis runs in docker containers. These are for easy development when no internet connection is provided. Because postgres and redis we have already loaded and configured, and conda_env also might be already installed and configured for the project. Locally this uses **env38_cookiecutter**.


.. image:: https://img.shields.io/badge/built%20with-Cookiecutter%20Django-ff69b4.svg?logo=cookiecutter
     :target: https://github.com/pydanny/cookiecutter-django/
     :alt: Built with Cookiecutter Django
.. image:: https://img.shields.io/badge/code%20style-black-000000.svg
     :target: https://github.com/ambv/black
     :alt: Black code style

:License: MIT

Settings
--------

Moved to settings_.

.. _settings: http://cookiecutter-django.readthedocs.io/en/latest/settings.html

Basic Commands
--------------

Setting Up Your Users
^^^^^^^^^^^^^^^^^^^^^

* To create a **normal user account**, just go to Sign Up and fill out the form. Once you submit it, you'll see a "Verify Your E-mail Address" page. Go to your console to see a simulated email verification message. Copy the link into your browser. Now the user's email should be verified and ready to go.

* To create an **superuser account**, use this command::

    $ python manage.py createsuperuser

For convenience, you can keep your normal user logged in on Chrome and your superuser logged in on Firefox (or similar), so that you can see how the site behaves for both kinds of users.

Type checks
^^^^^^^^^^^

Running type checks with mypy:

::

  $ mypy pmsproject

Test coverage
^^^^^^^^^^^^^

To run the tests, check your test coverage, and generate an HTML coverage report::

    $ coverage run -m pytest
    $ coverage html
    $ open htmlcov/index.html

Running tests with py.test
~~~~~~~~~~~~~~~~~~~~~~~~~~

::

  $ pytest

Live reloading and Sass CSS compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Moved to `Live reloading and SASS compilation`_.

.. _`Live reloading and SASS compilation`: http://cookiecutter-django.readthedocs.io/en/latest/live-reloading-and-sass-compilation.html

Deployment
----------

The following details how to deploy this application.
