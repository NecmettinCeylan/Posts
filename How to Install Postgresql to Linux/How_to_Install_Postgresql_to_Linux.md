# How to Install Postgresql to Linux
## Simple steps to get you postgres up and running and accesible to all ip addresses

# 1. Update Linux Packages
  
    sudo apt update
    sudo apt -y upgrade

# 2. Install Postgresql
    
    sudo apt install postgresql postgresql-contrib

# 3. Start Postgresql
    
    sudo systemctl start postgresql.service

# 4. Add postgres to sudo
    
    sudo usermod -aG sudo postgres

# 5. Switch to postgres user
    sudo -i -u postgres

# 6. List Databases
    psql
    SELECT datname FROM pg_database;
    \q

# 7. Create a DB
    createdb django
    sudo -u postgres createdb django

# 8. Create Postgres User
 
    createuser --interactive

or

    sudo -u postgres createuser --interactive

you need to create linux user with same username created for Postgresql
    
    sudo adduser django
    sudo -i -u django
    psql

print connection information via:

    \conninfo

# 9. Get Location of hba_file and config_file
    psql
    SHOW hba_file; 

/etc/postgresql/14/main/pg_hba.conf

    SHOW config_file;

/etc/postgresql/14/main/postgresql.conf


# 10. Open Postgresql to All Connections

    sudo vim /etc/postgresql/14/main/pg_hba.conf

change to:
- host    all             all             0.0.0.0/0            md5
- host    all             all             ::0/0       md5

    sudo vim /etc/postgresql/14/main/postgresql.conf

change to:

listen_addresses = '*'


    SELECT pg_reload_conf();

restart the server


# some useful commands

Create user and give permissions of a db to that user:

    CREATE DATABASE db;
    CREATE USER user WITH PASSWORD 'pass';
    GRANT ALL PRIVILEGES ON DATABASE db TO user;

    ALTER USER user SET search_path = public;


list all users on postgres:

    \du

list all databases on postgres:

     \l

or

     \l+


# References

[https://www.digitalocean.com/community/tutorials/how-to-install-and-use-postgresql-on-ubuntu-20-04](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-postgresql-on-ubuntu-20-04)


[https://stackoverflow.com/questions/3278379/how-to-configure-postgresql-to-accept-all-incoming-connections](https://stackoverflow.com/questions/3278379/how-to-configure-postgresql-to-accept-all-incoming-connections)

    
    