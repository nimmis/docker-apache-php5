## Apache2 with php5 on Ubuntu 14.04 LTS

This is docker images of Ubuntu 14.04 LTS with apache2 and php5

To access site contents from utside the container you should map /var/www

### Examples

- plain, accessable on port 8080 `docker run -d -p 8080:80 nimmis/apache`
- with external contents in /home/nimmis/html `docker run -d -p 8080:80 -v /home/nimmis/html:/var/www/html nimmis/apache`

The docker container is started with the -d flag so it will run inte the background. To run commands or edit settings inside
the container run `docker exec -ti <container id> /bin/bash'
 
