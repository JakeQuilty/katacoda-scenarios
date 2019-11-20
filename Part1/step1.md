Clone the GitHub repository to your working directory:

`git clone https://github.com/cyberark/conjur-quickstart.git`{{execute}}

Browse to the directory:
`cd conjur-quickstart`{{execute}}

Pull the Docker images defined in docker-compose.yml:
`docker-compose pull`{{execute}}


Verification:

When the required images are successfully pulled, the terminal returns the following:

Pulling openssl ... done \n
Pulling bot_app ... done \n
Pulling database ... done \n
Pulling conjur ... done \n
Pulling proxy ... done \n
Pulling client ... done \n

