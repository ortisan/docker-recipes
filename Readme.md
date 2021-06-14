# Recipes for Docker and Docker Compose

Commands:

```
Build images before starting containers.
docker-compose up --build  <service-name>

# Recreate containers even if their configuration does not changed
docker-compose up --force-recreate  <service-name>

# Recreate dependent containers.
docker-compose up --always-recreate-deps  <service-name>
```
