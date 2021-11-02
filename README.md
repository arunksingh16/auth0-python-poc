# auth0-python-poc
An Application for Auth0 demo based on https://github.com/auth0-samples/auth0-python-web-app


## Auth0 Concepts

- Callback URL
A callback URL is a URL in your application where Auth0 redirects the user after they have authenticated.

A logout URL is a URL in your application that Auth0 can return to after the user has been logged out of the authorization server.

- Auth0 Organizations
The Organizations feature represents a broad update to the Auth0 platform that allows our business-to-business (B2B) customers to better manage their partners and customers, and to customize the ways that end-users access their applications. Auth0 customers can use Organizations to:

Represent their business customers and partners in Auth0 and manage their membership.

Configure branded, federated login flows for each business.

Build administration capabilities into their products, using Organizations APIs, so that those businesses can manage their own organizations.


### How to Use this repository

#### Running Codebase in Local
- Pipenv
```
# install
pip3 install pipenv
# initialise
pipenv
# activate
pipenv shell
# install
pipenv install 
# Install a local setup.py into your virtual environment/Pipfile:
pipenv install -e .
# generate lock file
pipenv lock
# execute in prd
pipenv install --ignore-pipfile
# generate requirements.txt
pipenv run pip freeze > requirements.txt
# records the new requirements to the Pipfile.lock file and installs the missing dependencies on the Python interpreter.
pipenv update
```

#### cleanup
Remove project virtualenv (inferred from current directory):
```
$ pipenv --rm
```
Purge all package(s) from virtualenv
```
pipenv uninstall --all
```

#### Running Using Docker

```
docker build -t auth0-python-poc .
docker run --env-file .env -p 3000:3000 -it auth0-python-poc
```
