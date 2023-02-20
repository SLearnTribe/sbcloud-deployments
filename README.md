# Pre-Requisite

- Install latest version of [Docker](https://docs.docker.com/desktop/windows/install/).

## Steps to Deploy in Local

- Open git bash & `git clone https://github.com/SLearnTribe/sbcloud-deployments`
- Change dir to `cd sbcloud-deployments/sbdev22`.
- Run `docker-compose -f sbdev22.yml up -d`.
- Validate to see if all the containers are up and running `docker container ps`.
- Navigate to http://localhost:5050 for Pgadmin.
```
Add Server with the below details
# name : postgres
# hostname/ip : localhost (validate the ip before deploy)
# port : 5432
# maintenance database : keycloak
# username : keycloak
# password : password
```
- Navigate to http://localhost:8085 for Keycloak
- Use `docker logs 'container-id' -f` to follow the logs of a container.

## Steps to Deploy in Development Server

### Ensure all the code is deployed to git and docker.
### Login into the dev server.

1. Run `cd sbcloud-deployments/sbstag23`
2. Run `docker ps` and ensure if all services are listed.
3. Check your container name or id with `docker ps`
4. Run `docker stop 'container_name'` or `docker stop container_id`
5. Run `docker rm 'container_name'` or `docker rm container_id`
6. Run `docker images`
7. Check the image is to be removed.
8. Run `docker image rm image_id`
9. Run `docker-compose -f sb-inquisitve.yml up -d`
10. Run `docker ps` ensure all services are up and running.



