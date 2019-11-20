Create a Conjur account and initialize the built-in admin user.

`docker-compose exec conjur conjurctl account create myConjurAccount > admin_data`{{execute}}

An account named myConjurAccount is created and the admin user is initialized, following keys are created and stored at admin_data file:

* admin user API key. Later on, we will use this key to log in to Conjur.
* myConjurAccount Conjur account public key.

This is a one-time action. For the duration of the container’s life or until additional initcommand is issued, the Conjur client and the Conjur server remain connected.
Use the account name that you created in the last step:

`docker-compose exec client conjur init -u conjur -a myConjurAccount`{{execute}}