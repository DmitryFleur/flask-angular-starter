# Flask-Angular-Starter
Start your next hackathon or side project with the initial cruft out of the way. This project gets you an AngularJS with a reactive Material Design SPA frontend and a configured Python Flask REST API backend. No more will you have to suffer the monotony of implementing yet another user authentication system for your new projects, as repo sets you up with both registration and login using JSON Web Tokens. Forget about the annoying and verbose web service code and expand the applications capabilities easily and succinctly with Python and Flask.

## Application stack and tools
Framework/tool | Description
----------------- | -----------------
[Flask](http://flask.pocoo.org/) | Backend micro-framework. Parses and handles HTTP requests.
[Flask-SQLAlchemy](http://flask-sqlalchemy.pocoo.org/2.1/) | Data layer abstraction to help you with your CRUD operations.
[Flask-Restful](http://flask-restful-cn.readthedocs.org/en/0.3.4/) | Flask extension to support REST API construction.
[Flask-Jwt](https://pythonhosted.org/Flask-JWT/) | JSON Web Token library to handle stateless authentication. 
[Flask-Bcrypt](https://flask-bcrypt.readthedocs.org/en/latest/) | Encryption library for generating password hashes, keep your users safe. 
[Flask-Migrate](https://flask-migrate.readthedocs.org/en/latest/) | Library to handle SQLAlchemy database migrations.
[Flask-Assets](https://flask-assets.readthedocs.org/en/latest/) | Build and minify your frontend assets.
[Angular1.5](https://angularjs.org/) | Frontend framework for a rich, dynamic user interfaces.
[Angular-Material](https://material.angularjs.org/latest/) | Angular library implementing Material Design.
[SQLite](https://www.sqlite.org/) | Store your data in a serverless database (should not be used for production).
[Vagrant](https://www.vagrantup.com/) | Run and develop your application within a lightweight virtual environment.
[NPM](https://www.npmjs.com/) | Manage Nodejs packages.
[Bower](http://bower.io/) | Manage frontend packages.

## Setup
* Download and install both [git](https://git-scm.com/downloads) and [Vagrant](https://www.vagrantup.com/downloads.html).
* Run the following commands in a shell of your choosing.
```sh
git clone git@github.com:lwalter/flask-angular-starter.git
cd vagrant
vagrant up
vagrant ssh
cd /app
env/bin/python3.4 run.py
```
* Open a browser and navigate to localhost:5000

## Things to know
* Guest port 5000 and host port 5000 are forwarded to access the application residing on the Vagrant VM.
* The repository on the host will be shared to `/app` of the guest environment.
* A Python virtualenv will be created in the `/app` directory called `env`.
* Python packages can be installed by running `/app/env/bin/pip install <package name>`.
* Node packages can be installed by running `npm install <package name>`.
* Bower packages can be installed by running `node_modules/bower/bin/bower install <package name>`.
* After modifying any database entities, run `env/bin/python3.4 manage.py db migrate`. This will add a new migration entry to `migrations/versions`.

## TODO
* Move from Flask-assets to Gulp for frontend dependency management.
* Write backend and frontend tests.
* Modify NPM, Bower and build scripts to accommodate both development and production contexts.
* ReactJS option for frontend library.
* Move from SQLite -> PostgreSQL.

## License

[MIT](LICENSE) Luke Walter