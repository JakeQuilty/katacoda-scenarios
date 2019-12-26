In this unit you will learn how to load your first policy.
Formatted in YAML, policy defines Conjur entities and the relationships between them.  An entity can be a policy, a host, a user, a layer, a group, or a variable.

A sample application policy named BotApp.yml is provided in the client container under policy directory.

At the end of this section:
As a privileged user, you will load a policy that defines a human user, a non-human user that represents your application, and a variable.

**Copy the Sampke Policy**

Copy the sample policy to the Conjur Client *work around step*

`docker cp ./conf/policy/BotApp.yml conjur_client:/BotApp.yml`{{execute}}

**Login to Conjur as admin**

Log in to Conjur as admin. When prompted for a password, insert the API key stored in the *admin_data* file:

`cat admin_data`{{execute}}

`docker-compose exec client conjur authn login -u admin`{{execute}}

Verification:

When you successully log in, the terminal returns:
Logged in