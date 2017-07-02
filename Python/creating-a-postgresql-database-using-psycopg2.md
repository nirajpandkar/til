# Creating a postgresql database using psycopg2

```
from psycopg2 import connect
from psycopg2.extensions import ISOLATION_LEVEL_AUTOCOMMIT

try:
    con = connect(dbname='DBNAME',
                  user='DBUSER',
                  host='localhost',
                  password='MYPASS')
except:
    print "Unable to connect to the database."

con.set_isolation_level(ISOLATION_LEVEL_AUTOCOMMIT)

cur = con.cursor()

try:
    cur.execute("CREATE DATABASE DBNAME")
except:
    print "Unable to create database."

cur.close()
con.close()
```
### References

* [StackOverflow](https://stackoverflow.com/a/19426770/4411757)
* [Wiki](https://wiki.postgresql.org/wiki/Psycopg2_Tutorial)
* [set_isolation_level](http://initd.org/psycopg/docs/connection.html#connection.set_isolation_level)