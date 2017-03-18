# Commafeed with Nginx, Redis and Postgres

The docker composition generates the following architecture:

```
Nginx 80 ->
  Commafeed 8082:8082 ->
    Redis 6379:6379
    Postgres 5432:5432
```

The Nginx config file could be eventually modified to scale up and target multiple instances of Commafeed.

## To improve

  - Enforce best practices for logs:
    - Unify all logs per directory
    - Force errors to errors and output to output
    - Try to add logging monitoring using Elastic stack?
  - Nginx must implement https with letsencrypt
  - Add password to redis
  - Somehow parametrize password/user for postgres
  - Make data persistent (db, logs)
  - Migrate to Docker compose format 3 (requires Docker engine 1.13.0+)

## Requires

  - Docker engine 1.12.0+
  - Docker compose

## How to run

Just type

```
docker-compose up
```
