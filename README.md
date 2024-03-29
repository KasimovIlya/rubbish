# ADV/Authenticator/Documentation #

## Creating virtual environment ##

First install python's `virtualenv` package via pip :
`
pip3.7 install virtualenv
`

Then create your environment by following command:

`
virtualenv VIRTUAL_ENV_NAME -p PATCH_PYTHON3.7
`

Activate :

`
source VIRTUAL_ENV_NAME/bin/activate
`

## Installing requirements ##

`
pip install -e .
`

## Configuration ##

Create `.env`-file in your folder or manually by

`
export "var"=path/to/smth
`

it is used for creating variable environments

1. create environment variable `ADV_APP_SETTING` by this command :

`
export 'ADV_APP_SETTINGS'=path/to/config.yml
`

or writing

`
ADV_APP_SETTINGS=path/to/config.yml
`

in `.env`-file

create JWK using  https://mkjwk.org;

`
key_use=signing; algorithm=RS256; key_id=client_auth@key(in our case);
`

2. write JWK in `.env`-file:

`
CLIENT_AUTH_SERVICE_JWK={"kty": "RSA", "d": ...
`

`
AUTH_LONG_JWK={"kty": "RSA", "d": ...
`

`
AUTH_SHORT_JWK={"kty": "RSA", "d": ...
`

3. change redis/revoke/host in `config.yml` from `"REDIS_HOST, host"` to `"REDIS_HOST, localhost"`

or

write it in `.env`-file ` REDIS_HOST = localhost `
