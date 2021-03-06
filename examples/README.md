# camunda-bpm-dropwizard-examples

## Log - what happened so far

### mysql instead of h2

Since I had trouble running multiple instances against a h2-server db, the example setup now uses mysql. To set up
the local instance, you can use the [EasyMysql](https://github.com/nkratzke/EasyMySQL) docker setup. On OSX and Windows, 
follow the installation directions of boot2docker, see EasyMysql/README.md.

Afterwards, before running the examples, start the mysql-db using

    ./examples/docker_mysql.sh

To admin the database without installing any additional software use [Adminer](http://www.adminer.org/de/), just
start a local php server running:

    php -S localhost:8000 adminer-4.1.0.php 

and open the page in your browser. Connect with your `boot2docker ip` address and `user=camunda, password=camunda, db=camunda`.

See also: [Easy MySQL setup with docker](http://jangalinski.github.io/2014/12/29/easy-mysql-setup-with-docker/)
 
### connect JBoss to DB

As long as there is no fully working dropwizard-admin/tasklist tool, use the default JBoss installation to startup 
the admin environment. You will have to add a mysql-driver module to the JBoss. (TODO: document setting up mysql on jboss).

Run JBoss and login with demo/demo as usual.

