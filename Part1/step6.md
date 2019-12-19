**Load the Sample Policy**

Load the provided sample policy into Conjur built-in *root* policy to create resources for the BotApp:

`docker-compose exec client conjur policy load root BotApp.yml > my_app_data`{{execute}}

Conjur generates the following API keys and stores them in a file, my_app_data:
* An API key for Dave, the human user. This key is used to authenticate user Dave to Conjur.
* An API key for BotApp, the non-human identity. This key is used to authenticate BotApp application to Conjur.

Those API keys is correlated with the number of Users & Hosts defined in a policy.

Verification:
The termial returns:

Loaded policy 'root'

**Log out of Conjur**

Log out of Conjur:
`docker-compose exec client conjur authn logout`{{execute}}

Verification:
When you successfully log out, the terminal returns:

Logged out