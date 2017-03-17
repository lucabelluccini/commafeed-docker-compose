# Commafeed with Nginx, Redis and Postgres

## To improve

- Enforce best practices for logs:
  - Unify all logs per directory
  - Force errors to errors and output to output
- Make at least public hostname and port configurable for commafeed
- Nginx must implement https with letsencrypt
- Nginx must daemonize to wait for commafeed to be up?
- Add password to redis
- Update password/user for postgres (make parameter?)
- Make data persistent (db, logs)

## Architecture

Nginx 80 ->
  Commafeed 8082:8082 ->
    Redis 6379:6379
    Postgres 5432:5432
