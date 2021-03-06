<img width="200" alt="profbit logo" src="https://raw.githubusercontent.com/joshblum/profbit/master/profbit/static/img/logo.png">

[![Circle CI](https://circleci.com/gh/joshblum/profbit.svg?maxAge=2592000&style=shield)](https://circleci.com/gh/joshblum/profbit)
[![codecov](https://codecov.io/gh/joshblum/profbit/branch/master/graph/badge.svg)](https://codecov.io/gh/joshblum/profbit)
[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)

Track your bitcoin, bitcoin cash, ethereum, and litecoin gains and losses in
one place.  ![profbit
preview](https://github.com/joshblum/profbit/blob/master/profbit/static/img/preview.gif)

## Development Setup

### Requirements
We use [Pipenv](http://docs.python-guide.org/en/latest/dev/virtualenvs/) to
manage requirements.

```bash
pip install pipenv
pipenv install
pipenv shell
npm install --dev
```

### Server Config
You will first have [register an application on
Coinbase](https://coinbase.com/oauth/applications/new). When registering your app
be sure to add the redirect url i.e.
https://app-name.herokuapp.com/complete/coinbase/. Then `export` the following
configuration variables and create the database:

```bash
cd profbit

export SECRET_KEY="super-secret-key"
export SOCIAL_AUTH_COINBASE_KEY="coinbase-key"
export SOCIAL_AUTH_COINBASE_SECRET="coinbase-secret"
export FLASK_APP=app.py
export FLASK_DEBUG=1

flask syncdb
npm build
```


## Donate

Profbit is an open source side project. To support development and keep
our server running, you can donate using:

- Bitcoin: `19UsnMKjhm22mFEYKKNHjxdFCfnShTcbPM`
- Bitcoin Cash: `1L7qfnMFdgfrE5qTLDYvQskn3TiubUUpJP`
- Ethereum: `0x97A3D535391A5a87f8362935B26f252E68C25Aca`
- Litecoin: `LWk4TL8n866gmLmEvQWSs9V7tBBdyoWjgQ`


## Attribution
The heart icon was created by Jivan from the Noun Project.
