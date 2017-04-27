# chamaeleon

Wordpress REST API v2 Stack

# requirements

* docker
* docker-compose
* yarn/npm (optional, just to use package.json scripts)

# how-to

## first-run

```bash
$ yarn build:db && yarn build:api
```
## startup

Just use `yarn`. To quickly mount the stack with (your mariadb is immutable unless explicit unmount):

```bash
$ yarn start+
```

OR

```bash
$ yarn build && WORDPRESS_DB_PASSWORD=some-password MYSQL_ROOT_PASSWORD=some-password yarn start
```

Now can navigate to `localhost:10000/` to set up your wordpress instance `username` and `password`. Then use endpoint `localhost:10000/?rest-route=/` to consume the JSON REST API.

For quick dismount the stack:

```bash
$ yarn st0p
```
