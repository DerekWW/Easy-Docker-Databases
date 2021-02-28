# Easy Docker Databases

This repo contains docker-compose files to setup local development databases as well as Portainer to monitor containers. These are meant for quick and easy local development. Nothing in this repo should be used for production. All usernames and passwords included are generic and should be changed, you can also set them other ways if you do not want them in your compose file(see docs [here](https://docs.docker.com/compose/environment-variables/)).

All database services come with a named volume, which compose will remount to the containers on either a `restart` or `up`. If you change the volumes to be un-named then compose will not remount them(see docs [here](https://docs.docker.com/compose/environment-variables/)).

Currently there are compose files for the following databases:
*  Mongodb
   - Includes Mongo Express as database admin tool
 - PostgreSQL
   - Includes pgAdmin4 as database admin tool


## Mongodb | Mongo Express
- Mongodb is exposed on post `27017`
- Mongo Express can be accessed from http://localhost:8081/ and the credentials set in the compose file

## PostgreSQL | pgAdmin4
- pgAdmin can be accessed from http://localhost:5050/ and the credentials set in the compose file

- When you add a server the hostname will be `postgres`

## Portainer
- Portainer can be accessed from http://localhost:9000/ and the credentials set in the compose file
- Portainer is useful if you want a GUI and are on linux since docker desktop is not avaliable