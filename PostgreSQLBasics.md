## PostgreSQL Basic Commands 
### Connect to PostgreSQL with psql Tool
After installing the PostgreSQL database server, a user named *postgres* is created with a role of _postgres_ by default. To connect to Postgres server, log into the system as user *postgres* and connect to the database server
```sh
$ sudo su - postgres
$ psql
```
### Check login info
```sh
postgres-# \conninfo
```
### Check PostgreSQL Version info
```sh
postgres-# select version();
```
### Change password of a postgres database role 
```sh
postgres-# \password postgres
```

### List all databases in the server
\l command can be used to list all the databases in the server:
```sh
postgres-# \l
```
A SELECT statement can also be used to query the database names from the pg_database catalog by using:

> SELECT
>   datname
> FROM
>   pg_database; 

The databases present in the server would be listed as a result.

### Listing all users in the PostgreSQL database server
```sh
postgres-# \du
```
\du+ psql command can be used to show for information about the role.

### Connect to a database in PSQL prompt
Replace the <dbname> below with the name of database you would like to connect to:
```sh
postgres-# \c <dbname>
```

### Disconnect from PostgreSQL database
```sh
postgres-# \q
```
