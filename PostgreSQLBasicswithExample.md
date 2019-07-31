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
## PostgreSQL with an Example
The following is a walk-through tutorial for creating a new database using PSQL tool and loading a sample database from terminal in an Ubuntu system. 

### Creating a New Database
Launch the Linux terminal and connect to postgres server using user _postgres_:
```sh
$ sudo su - postgres 
```
Launch the psql tool:
```sh
$ psql
```
Create a new database called dvdrental:
```sh
postgres-# CREATE DATABASE dvdrental;
```
The postgreSQL will create a new database named ```dvdrental``` 

### Loading sample Database from Terminal using pg_restore Command

Download DVD Rental Sample Database from [here](http://www.postgresqltutorial.com/postgresql-sample-database/) and extract the zip file to _dvdrental.tar_ keeping the _.tar_ file.

In a seperate Linux terminal, copy the _.tar_ file to ```/opt/``` directory:

```sh
$ sudo cp /Downloads/dvdrental.tar /opt/
```

Restore the sample database into the database created earlier by using [pg_restore](http://manpages.ubuntu.com/manpages/bionic/en/man1/pg_restore.1.html) command:

>Please note to replace the ```database hostname```, ```username```, ```database_name``` and```database_file.tar``` with your details. This command assumes that the respective database is created earlier.  
>

```sh
$ sudo pg_restore -h localhost -U username -W -F t -d database_name database_file.tar
```
where 
```-h localhost``` : database hostname specifying the host name of the machine on which the server is running
``` -U username``` : connects to the database as user username
```-W :``` force pg_restore to prompot for a password before connecting to the database
```-F t``` : specifies the format of the file
```-d database_name``` : name of database to which we are restoring the sample database
```database_file.tar``` : name of the input file

