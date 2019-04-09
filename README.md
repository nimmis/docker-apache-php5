## Apache2 with php5 on Ubuntu 14.04 LTS

This is docker images of Ubuntu 14.04 LTS with apache2 and php5/composer

To access site contents from outside the container you should map /var/www/html

Includes composer for easy download of php libraries

For php7 please se the Ubuntu 16.04 LTS and php7 container [nimmis/apache-php7](https://hub.docker.com/r/nimmis/apache-php7/)

### Examples

- plain, accessable on port 8080 `docker run -d -p 8080:80 nimmis/apache-php5`
- with external contents in /home/nimmis/html `docker run -d -p 8080:80 -v /home/nimmis/html:/var/www/html nimmis/apache-php5`

The docker container is started with the -d flag so it will run inte the background. To run commands or edit settings inside
the container run `docker exec -ti <container id> /bin/bash'
 
