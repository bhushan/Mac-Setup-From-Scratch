run

```bash
brew install mysql
```

and run to start mysql server

```bash
brew services start mysql
```

now run `mysql_secure_installation` select No for validate_plugin install (first question) and then yes for all
  
now run `mysql -uroot -p` and fire `SELECT user,authentication_string,plugin,host FROM mysql.user;` this query to see users.

now alter root user 

```bash
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY '';
```

and

```bash
FLUSH PRIVILEGES;
```

now again check users with `SELECT user,authentication_string,plugin,host FROM mysql.user;` query. 

```
+------------------+-------------------------------------------+-----------------------+-----------+
| user             | authentication_string                     | plugin                | host      |
+------------------+-------------------------------------------+-----------------------+-----------+
| root             |                                           | mysql_native_password | localhost |
+------------------+-------------------------------------------+-----------------------+-----------+
```

Now you can access mysql by `mysql -u root` notice we have remove root password now. 

create `test` database for handy temporary database. `create database test;` to check `show databases;`. 

NOTE: I always have test database created so for any project i can quickly migrate and flush things when needed.
