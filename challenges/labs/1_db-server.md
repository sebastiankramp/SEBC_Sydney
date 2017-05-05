# DB-Server

##Hostname
```
MariaDB [(none)]> select @@hostname;
+------------------------------------------------+
| @@hostname                                     |
+------------------------------------------------+
| ip-172-31-15-167.eu-central-1.compute.internal |
+------------------------------------------------+
1 row in set (0.00 sec)
```

##Version
```bash
MariaDB [(none)]> select @@version;
+----------------+
| @@version      |
+----------------+
| 5.5.56-MariaDB |
+----------------+
1 row in set (0.00 sec)
```

##Database-listing
```bash
MariaDB [(none)]> SHOW DATABASES;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| hive               |
| hue                |
| mysql              |
| oozie              |
| performance_schema |
| rman               |
| scm                |
| sentry             |
+--------------------+
9 rows in set (0.00 sec)
```