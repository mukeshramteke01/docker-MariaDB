### docker-MariaDB

This repo contains a recipe for making Docker container for MariaDB on Red Hat Enterprise Linux.

Check your Docker version

    # docker version

pull the image

    # docker pull <yourname>/mariadb .

Check the image out.

    # docker images

Run it:

    # docker run -it -d -p 3306:3306 <yourname>/mariadb /bin/bash

Get container ID:

    # docker ps

Get the IP address for the container:

    # docker inspect --format "{{ .NetworkSettings.IPAddress }}" <container_id>

For MySQL:

    # mysql -h 172.17.0.x -u root -p redhat

Create a table:

```
\> show databases;

\> use test;

\> CREATE TABLE test (name VARCHAR(10), owner VARCHAR(10),
    -> species VARCHAR(10), birth DATE, death DATE);

\> show tables;
```
