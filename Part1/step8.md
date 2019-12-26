In this unit you will learn how to program an application to fetch a secret from Conjur using the REST API.

At the the end of this section:
You will know how to leverage Conjur's ability to store your application's secrets securely.

**Start a bash session**
Enter the BotApp container.

`docker exec -it bot_app bash`{{execute}}

**Generate a Conjur Token**
Generate a Conjur token to the *conjur_token* file, using the BotApp API key:

`curl -d "<BotApp API Key>" -k https://proxy/authn/myConjurAccount/host%2FBotApp%2FmyDemoApp/authenticate > /tmp/conjur_token`{{execute}}

The Conjur token is stored in the *conjur_token* file.

Copy the sample policy to the Conjur Client

`docker cp ./conf/policy/BotApp.yml conjur_client:/BotApp.yml`{{execute}}

**Fetch the Secret**
Run program to fetch the secret:

`/tmp/program.sh`{{execute}}

The secret is displayed.

TIP: If the secret is not displaued, try generating the token again.  You have eight minutes between generating the conjur token and fetching the secret with BotApp.