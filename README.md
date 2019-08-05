# ADV/Authenticator/Documentation #

## Creating virtual environment ##

First install python's 'virtualenv' package via pip :

'pip3.7 install virtualenv'

Then create your environment by following command:

'virtualenv VIRTUAL_ENV_NAME'

Activate :

'source VIRTUAL_ENV_NAME/bin/activate'

## Installing requirements ##

'pip3.7 install -r path/to/requires.txt'

or by hand via :

'pip3.7 install ...'

## Configuration ##

Create '.env' file in your folder or manually by 'export "var"=path/to/smth', it is used for creating variable environments

1. create environment variable "ADV_APP_SETTING" by this command 'export 'ADV_APP_SETTINGS'=path/to/config.yml'

create JWK, use https://mkjwk.org; key_use=signing; algorithm=RS256; key_id=client_auth@key;

2. write JWK in '.env': 

### CLIENT_AUTH_SERVICE_JWK={"kty": "RSA", "d": ...###

### AUTH_LONG_JWK={"kty": "RSA", "d": ... ###

### AUTH_SHORT_JWK={"kty": "RSA", "d": ... ###

3. change redis/revoke/host in 'config.yml' from "REDIS_HOST, host" to "REDIS_HOST, localhost"


