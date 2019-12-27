In this unit you will learn how to program an application to fetch a secret from Conjur using the REST API.

At the the end of this section:
You will know how to leverage Conjur's ability to store your application's secrets securely.

**Copy the sample policy to the Conjur Client** *work around step*

`docker cp ./program.sh bot_app:/tmp`{{execute}}

**Start a bash session**
Enter the BotApp container.

`docker exec -it bot_app bash`{{execute}}

**Export BotApp API Key**
Export the API Key of the BotApp to be used in the secret retrieval script.

`export BOT_APP_API_KEY=<api key>`{{copy}}


**Fetch the Secret**
Run program to fetch the secret:

`./program.sh`{{execute}}

The secret is displayed.

TIP: If the secret is not displayed, try generating the token again.  You have eight minutes between generating the conjur token and fetching the secret with BotApp.
