Start the Conjur OSS environment:
`docker-compose up -d --build`{{execute}}

When Conjur OSS starts, the terminal returns the following:

Creating postgres_database ... done

Creating bot_app ... done

Creating openssl ... done

Creating conjur_server ... done

Creating nginx_proxy ... done

Creating conjur_client ... done

Verification

Run the following command to see a list of running containers:

`docker ps`{{execute}}
