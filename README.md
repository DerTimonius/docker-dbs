# Docker Compose files for databases

If you think like me, you probably also don't want to clutter your local databases with unnecessary data entries, just for testing new technologies.

I much prefer to throw things in a dockerized database volume and delete it afterwards when testing a new ORM for example.

In this repo, you will find some `docker-compose.yaml` files that will help you setup a dockerized database (if you plan to use these databases in production, don't. They're intended to be used for testing purposes)

## Usage

First clone the repo locally:

```sh copy
git clone git@github.com:DerTimonius/docker-dbs.git
```

Then, decide what database you want and use the command provided in each section. You can of course change the names of the databases, the passwords, users and ports. If you change them, keep in mind that the connection strings will change accordingly.

### Postgres

```sh copy
docker-compose -f docker-postgres.yaml up -d
```

The connection string of this database will be `postgresql://user:password@localhost:5432/db`

### MySQL

```sh copy
docker-compose -f docker-mysql.yaml up -d
```

The connection string of this database will be `mysql://user:password@localhost:3306/db`

### MongoDB

```sh copy
docker-compose -f docker-mongodb.yaml up -d
```

The connection string of this database will be `mongodb://admin:adminpassword@localhost:27017/`
