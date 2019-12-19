In this unit you will learn how to store your first secret in Conjur.

**Log in as Dave**
Log in as Dave, the human user. When prompted for a password, copy  and paste Dave's API key stored in the *my_app_data* file:

`cat my_app_data`{{execute}}

`docker-compose exec client conjur authn login -u Dave@BotApp`{{execute}}

Verification:
To verify that you logged in successfully, run:

`docker-compose exec client conjur authn whoami`

**Generate a Secret**
Generate a value for your application's secret:

`secretVal=$(openssl rand -hex 12 | tr -d '\r\n')`{{execute}}

This generates a 12-hex-character value.

**Store the Secret**
Store the generated value in Conjur:

`docker-compose exec client conjur variable values add BotApp/secretVar ${secretVal}`{{execute}}

A policy predefined variable named *BotApp/secretVar* is set with a random generated secret.

Verification:
The terminal returns a message:

Value added.
