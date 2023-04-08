# PHP, MariaDB and Nginx

* This example provides containers for:
    * PHP 8.1 (FPM)
    * MariaDB 10.9
    * Nginx (latest)
* Code in this directory will be mapped into the PHP container at `/var/www/html`
* Nginx will serve code from the `web` directory (i.e. `web` is the document root)
    * By default, `web/index.php` will provide you a `phpinfo()` report 
* You can access the website via **http://127.0.0.1:8080**
* If you want to use this example, it is suggested you copy the configuration into your own project and customise it accordingly


## Security warning

* There is a default password for MariaDB's root user specified in `docker/docker-compose.yml`
* You are strongly recommended to edit this line to replace `YOURPASSWORDHERE` with a value known to you:

    
```
    MYSQL_ROOT_PASSWORD: YOURPASSWORDHERE
```

* This docker configuration has not been security hardened.  Expose it to public networks at your own risk!


## Usage (command line)

* `cd` into `docker`
* Run `docker-compose up`
* Docker will pull down the relevant images and start the containers 
