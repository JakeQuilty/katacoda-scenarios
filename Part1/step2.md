The master data key will be used later to encrypt the database.
In the working directory, generate the key and store it to a file:
* Tip: Although not mandatory, we prefer to store sensitive data to a file and not to display it directly on console screen.

`docker-compose run --no-deps --rm conjur data-key generate > data_key`{{execute}}

The data key is generated in the working directory and is stored in a file called data_key.

Load data_key file content (the master data key) as an environment variable:

`export CONJUR_DATA_KEY="$(< data_key)"`{{execute}}