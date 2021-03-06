#Dockerized Piwik

A fully working dockerized piwik installation built on top of a php:7.1.0-apache official docker image.

This builds a working piwik image which includes the GeoLiteCity database and adds some security settings for apache included in `docker_resources`.

Docker has to have the following environment variables present and a accessible database for piwik.

The environment variables can be found in:
`entrypoint.sh`

```
DB_HOST
DB_USER
DB_PASSWORD
DB_NAME
DB_TABLES_PREFIX
SITE_FQDN
PROXY_CLIENT_HEADERS
SALT
```

While building the docker image we should specify the piwik version as a build argument e.g.
```
docker build . --build-arg PIWIK_VERSION=3.0.3
```
