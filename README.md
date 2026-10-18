# WordPress + MariaDB

A WordPress installation backed by MariaDB. Two services:

- **wordpress** — the PHP/Apache app (primary endpoint, `authenticated` access)
- **db** — MariaDB 11 with a healthcheck

## Required environment values

Set these before deploying (see `.env.example`):

- `WORDPRESS_DB_NAME`, `WORDPRESS_DB_USER`, `WORDPRESS_DB_PASSWORD`
- `MYSQL_ROOT_PASSWORD`
- `WORDPRESS_TABLE_PREFIX` (optional, defaults to `wp_`)

## Resources

App: 0.50 CPU / 512 MB · DB: 0.50 CPU / 512 MB · **Total: 1.0 CPU / 1024 MB**

Note: the total exceeds a 0.5-core workspace ceiling; assign to a team with a
1+ core limit.
