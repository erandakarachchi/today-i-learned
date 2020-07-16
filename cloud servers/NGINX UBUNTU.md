# Configure NGINX on Ubuntu (AWS EC2 Instance)

#### Log in to the server using following command.

`ssh -i <<your_pem_file.pem>>  <<user>>@<<server_id>>`

#### Update the server (Optional)

`sudo apt-get update`

#### Install NGINX 

`sudo apt-get install nginx`

#### Check if the installation is successful

`systemctl status service nginx` 

the above command must return something like

``` shell
 nginx.service - A high performance web server and a reverse proxy serv
   Loaded: loaded (/lib/systemd/system/nginx.service; enabled; vendor pr
   Active: active (running) since Thu 2020-07-16 21:54:45 UTC; 28s ago
     Docs: man:nginx(8)
 Main PID: 2477 (nginx)
    Tasks: 2 (limit: 1121)
   CGroup: /system.slice/nginx.service
           ├─2477 nginx: master process /usr/sbin/nginx -g daemon on; ma
           └─2480 nginx: worker process

```

