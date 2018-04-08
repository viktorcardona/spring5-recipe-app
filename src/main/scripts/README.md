Scripts Directory

This directory will contain SQL Migration Scripts

We are going to have 2 DDs:

  1. For dev : sfg_dev
         User: sfg_dev_user
  2. For prod: sfg_prod
         User: sfg_prod_user


Docker: Running MySQL in a docker container:

docker run --name mysqldb -p 3306:3306 -e MYSQL_ALLOW_EMPTY_PASSWORD=yes -d mysql



The client use for connecting to MySQL DB is:

https://sequelpro.com/

    Start sequelpro and define the parameters:
        Host: 127.0.0.1
        Username: root
        Clic Test Connection
        