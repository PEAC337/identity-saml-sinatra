Sinatra-based Identity SP
=========================

[![CircleCI](https://circleci.com/gh/18F/identity-sp-sinatra.svg?style=svg)](https://circleci.com/gh/18F/identity-sp-sinatra)

Example service provide (SP) app for use with 18F's IdP.

### Setup

    $ make setup

### Testing

    $ make test

### Running (local development mode)

    $ make run

### Generating a new key + self-signed cert

    openssl req -days 3650 -newkey rsa:2048 -nodes -keyout config/demo_sp.key \
      -x509 -out config/demo_sp.crt -config config/openssl.conf

    openssl x509 -fingerprint -noout -in config/demo_sp.crt
