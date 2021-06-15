# 2 Apps in One Container With [Supervisord](http://supervisord.org/)

Starts 2 apps into one container.

Run:

```sh
docker build -t tentativafc/all-in-one:latest .
docker run -p 8080:8080 -p 8081:8081 tentativafc/all-in-one:latest
```

Testing:

```sh
curl http://localhost:8080/hello/say-hello && \
curl http://localhost:8081/world/say-world
```
