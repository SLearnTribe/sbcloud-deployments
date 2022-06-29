# Pre-Requisite

- Install latest version of [Docker](https://docs.docker.com/desktop/windows/install/)

## Steps to Deploy in Local

- Open git bash & `git clone https://github.com/SLearnTribe/sbcloud-deployments`
- Change dir to `cd sbcloud-deployments/sbdev22`
- Run `docker-compose -f sbdev22.yml up -d`
- Validate to see if all the containers are up and running `docker container ps`
- Navigate to http://localhost:5050 for Pgadmin
```
Add Server with the below details
# name : postgres
# hostname/ip : localhost
# port : 5432
# maintenance database : keycloak
# username : keycloak
# password : password
```
- Navigate to http://localhost:8085 for Keycloak
- Use `docker logs 'container-id' -f` to follow the logs of a container