---
description: 'A collection of various Flask, and Flask Extension documentations'
---

# Docs

The information below mainly came from the following repo.  [https://github.com/mjhea0/awesome-flask](https://github.com/mjhea0/awesome-flask)

## Official Docs:

Flask - [https://flask.palletsprojects.com/en/1.1.x/](https://flask.palletsprojects.com/en/1.1.x/)

## Third-Party Extensions

* [Admin](docs.md#admin)
* [APIs](docs.md#apis)
* [Auth](docs.md#auth)
* [Cache](docs.md#cache)
* [Data Validation and Serialization](docs.md#data-validation-and-serialization)
* [Databases](docs.md#databases)
* [Developer Tools](docs.md#developer-tools)
* [Email](docs.md#email)
* [Forms](docs.md#forms)
* [Full-text Search](docs.md#full-text-search)
* [Security](docs.md#security)
* [Task Queues](docs.md#task-queues)
* [Utils](docs.md#utils)



## Admin

* [Flask-Admin](https://github.com/flask-admin/flask-admin) - Functional admin panel that provides a user interface for managing data based on your models.

## APIs

**RESTful API Support**

* [Eve](https://docs.python-eve.org/) - RESTful API framework designed for human beings.
* [Flask-Classful](https://flask-classful.teracy.org/) - Adds support for class-based views for setting up RESTful API route endpoints.
* [Flask-MongoRest](https://github.com/closeio/flask-mongorest) - RESTful API framework wrapped around [MongoEngine](http://mongoengine.org/).
* [Flask-RESTful](https://flask-restful.readthedocs.io/) - Quickly build RESTful APIs.

**RESTful API + Swagger/OpenAPI Documentation Support**

* [Connexion](https://connexion.readthedocs.io/) - Open source, OpenAPI-based, REST framework built on top of Flask.
* [Flask-Rebar](https://github.com/plangrid/flask-rebar) - Combines Flask, [marshmallow](https://marshmallow.readthedocs.io/), and [OpenAPI](https://www.openapis.org/) for robust REST services.
* [Flask-RESTX](https://flask-restx.readthedocs.io/) - Community-driven fork of [Flask-RESTPlus](https://flask-restplus.readthedocs.io/) that makes it easy to build and document RESTful APIs with Flask.

**Swagger/OpenAPI Documentation Support**

* [Flask-APISpec](https://flask-apispec.readthedocs.io/) - Auto-documenting REST APIs.
* [SAFRS: Python OpenAPI & JSON:API Framework](https://github.com/thomaxxl/safrs) - SAFRS, which is an acronym for _S_ql_A_lchemy _F_lask-_R_estful _S_wagger, is meant to help developers create self-documenting JSON APIs for SQLAlchemy database objects and relationships.

## Auth

**Basic Auth and Session-based \(for HTML Endpoints\)**

* [Flask-HTTPAuth](https://flask-httpauth.readthedocs.io/) - Authentication.
* [Flask-Login](https://flask-login.readthedocs.io/) - Account management and authentication.
* [Flask Principal](https://pythonhosted.org/Flask-Principal/) - Authorization.
* [Flask-Security-Too](https://flask-security-too.readthedocs.io/en/stable/) - Account management, authentication, authorization.
* [Flask-SimpleLogin](https://github.com/flask-extensions/flask_simplelogin) - Authentication.
* [Flask-User](https://flask-user.readthedocs.io/) - Account management, authentication, authorization.

> Curious about the differences differences between Flask-User and Flask-Security? Review the Flask-User [FAQ](https://flask-user.readthedocs.io/en/latest/faq.html).

**JWT-based \(for JSON Endpoints\)**

* [Flask-JWT](https://pythonhosted.org/Flask-JWT/) - Basic support for working with JWTs.
* [Flask-JWT-Extended](https://flask-jwt-extended.readthedocs.io/) - Advanced support for working with JWTs.
* [Flask-JWT-Router](https://github.com/joegasewicz/flask-jwt-router) - Adds authorized routes to a Flask app.
* [Flask-Praetorian](https://flask-praetorian.readthedocs.io/) - Authentication and authorization for Flask APIs.

**OAuth**

* [Authlib](https://authlib.org/) - Library for building OAuth and OpenID clients and servers.
* [Authomatic](https://github.com/authomatic/authomatic) - Framework agnostic library for Python web applications that simplifies authentication and authorization of users via OAuth and OpenID.
* [Flask-Dance](https://github.com/singingwolfboy/flask-dance) - OAuth support via [OAuthLib](https://oauthlib.readthedocs.io/).

## Cache

* [Flask-Caching](https://flask-caching.readthedocs.io/) - Caching support.

## Data Validation and Serialization

* [Flask-Marshmallow](https://flask-marshmallow.readthedocs.io/) - Thin integration layer for Flask and marshmallow \(an object serialization /deserialization library\) that adds additional features to marshmallow.
* [Flask-Pydantic](https://github.com/bauerji/flask_pydantic) - [Pydantic](https://github.com/samuelcolvin/pydantic) support.

## Databases

**ORMs**

* [Flask-Peewee](https://flask-peewee.readthedocs.io/) - Support for Peewee, an ORM and database migration tool.
* [Flask-Pony](https://pypi.org/project/Flask-Pony/) - Support for Pony ORM.
* [Flask-SQLAlchemy](https://flask-sqlalchemy.palletsprojects.com/) - Support for SQLAlchemy, a SQL toolkit and ORM.

**ODMs**

* [Flask-MongoEngine](https://flask-mongoengine.readthedocs.io/) - Bridges Flask and MongoEngine for working with MongoDB.
* [Flask-PyMongo](https://flask-pymongo.readthedocs.io/) - Bridges Flask and PyMongo for working with MongoDB.

**Migrations**

* [Flask-Alembic](https://flask-alembic.readthedocs.io/) - Configurable [Alembic](https://alembic.sqlalchemy.org/) migration environment around a Flask-SQLAlchemy database for handling database migrations.
* [Flask-DB](https://github.com/nickjj/flask-db) - Flask CLI extension that helps you migrate, drop, create and seed your SQL database.
* [Flask-Migrate](https://flask-migrate.readthedocs.io/) - Handles SQLAlchemy database migrations via Alembic.

> Curious about the differences between Alembic, Flask-Alembic, Flask-Migrate, and Flask-DB? Review [this item](https://github.com/nickjj/flask-db#differences-between-alembic-flask-migrate-flask-alembic-and-flask-db) from Flask-DB's FAQ.

**Other Tools**

* [Flask-Excel](https://github.com/pyexcel-webwares/Flask-Excel) - Uses [pyexcel](https://github.com/pyexcel/pyexcel) to read, manipulate, and write data in different Excel formats: csv, ods, xls, xlsx and xlsm.

## Developer Tools

**Debugging**

* [Flask-DebugToolbar](https://flask-debugtoolbar.readthedocs.io/) - Port of Django's debug toolbar for Flask.
* [Flask-Profiler](https://github.com/muatik/flask-profiler) - Endpoint analyzer/profiler.

**Fixtures**

* [Flask-Fixtures](https://github.com/croach/Flask-Fixtures) - Create database fixtures from JSON or YAML.
* [Mixer](https://mixer.readthedocs.io/) - Object generation tool.

**Logging**

* [Rollbar](https://rollbar.com/error-tracking/flask/) - Flask error logging with Rollbar.

**Monitoring**

* [Airbrake](https://airbrake.io/docs/installing-airbrake/installing-airbrake-in-a-flask-app/) - Airbrake Flask integration.
* [Elastic APM Agent](https://www.elastic.co/guide/en/apm/agent/python/current/flask-support.html) - Elastic APM Flask integration.
* [Flask Monitoring Dashboard](https://flask-monitoringdashboard.readthedocs.io/) - Dashboard for automatic monitoring of Flask web-services.
* [Sentry Python SDK](https://sentry.io/for/flask/) - Sentry SDK Flask integration.

**Tracing**

* [Flask-OpenTracing](https://github.com/opentracing-contrib/python-flask) - OpenTracing instrumentation.

**Testing**

* [Flask-Testing](https://pythonhosted.org/Flask-Testing/) - Unittest extensions.
* [Pytest-Flask](https://github.com/pytest-dev/pytest-flask) - Pytest support for testing Flask applications.

## Email

* [Flask-Mail](https://pythonhosted.org/Flask-Mail/) - Provides simple email sending capabilities.

## Forms

* [Flask-WTF](https://flask-wtf.readthedocs.io/) - Integrates Flask with WTForms \(provides CSRF protection as well\).

## Full-text Search

* [flask-msearch](https://github.com/honmaple/flask-msearch) - Full-text search.
* [Flask-WhooshAlchemy3](https://github.com/blakev/Flask-WhooshAlchemy3) - Full-text search + Whoosh indexing capabilities for Flask-SQLAlchemy.
* [SQLAlchemy-Searchable](https://sqlalchemy-searchable.readthedocs.io/) - Provides full-text search capabilities for SQLAlchemy models.

## Security

* [Flask-Bcrypt](https://flask-bcrypt.readthedocs.io/) - Provides bcrypt hashing utilities.
* [Flask-CORS](https://flask-cors.readthedocs.io/) - Cross Origin Resource Sharing \(CORS\) handling.
* [Flask-SeaSurf](https://github.com/maxcountryman/flask-seasurf/) - Cross-site request forgery \(CSRF\) prevention.
* [Flask-Talisman](https://github.com/GoogleCloudPlatform/flask-talisman) - HTTPS and security headers.

## Task Queues

* [Celery](https://docs.celeryproject.org/) - The most commonly used Python library for handling asynchronous tasks and scheduling.
* [Dramatiq](https://flask-dramatiq.rtfd.io/) - Fast and reliable alternative to Celery.
* [Flask-RQ](https://github.com/mattupstate/flask-rq) - [RQ](https://python-rq.org/) \(Redis Queue\) integration.
* [Huey](https://huey.readthedocs.io/) - [Redis](https://redis.io/)-based task queue that aims to provide a simple, yet flexible framework for executing tasks.

## Utils

* [Flask-Babel](https://github.com/python-babel/flask-babel) - Support for internationalization \(i18n\) and localization \(l10n\).
* [Flask-File-Upload](https://github.com/joegasewicz/flask-file-upload) - Easy file uploads.
* [Flask-FlatPages](https://pythonhosted.org/Flask-FlatPages/) - Provides flat static pages based on text files.
* [Frozen-Flask](https://github.com/Frozen-Flask/Frozen-Flask) - Freezes a Flask application into a set of static files.
* [Flask-GraphQL](https://github.com/graphql-python/flask-graphql) - GraphQL support.
* [Flask-Injector](https://github.com/alecthomas/flask_injector) - Adds support for dependency injection.
* [Flask-Limiter](https://flask-limiter.readthedocs.io/) - Rate limiting features to Flask routes.
* [Flask-Moment](https://github.com/miguelgrinberg/Flask-Moment) - Moment.js date and time formatting helpers for Jinja2 templates.
* [Flask-Paginate](https://pythonhosted.org/Flask-paginate/) - Pagination support.
* [Flask-Shell2HTTP](https://github.com/Eshaan7/Flask-Shell2HTTP) - RESTful/HTTP wrapper for Python's subprocess API, so you can convert any command-line tool into a RESTful API service.
* [Flask-Sitemap](https://flask-sitemap.readthedocs.io/) - Sitemap generation.
* [Flask-SocketIO](https://flask-socketio.readthedocs.io/) - Socket.IO integration.

