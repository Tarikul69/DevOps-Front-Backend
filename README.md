## `Architecture`
![alt text](image.png)

## `Ansible`
1.Write the necessary configuration on ansible playbook.
2.then mentin remote server IP on inventory.ini folder and mention the Ip address group name on the playbookfile host section.
## `Frontend`
1. Create a docker file inside the project
2. Then build the docker file ### ` docker build -t "image_name"`
3. Then run the image ### ` docker run "image_name"`

## `Backend`
1. Create a docker file inside the project
2. Then build the docker file ### ` docker build -t "image_name"`
3. Then run the image ### ` docker run "image_name"`

## `Database`
1. Import docker image from dockerhub using this command ` docker pull "image_name_version"`

## `Nginx` 
1. Install Nginx `sudo apt install nginx`
2. After that configure nginx.conf file:

events {}

http { 
 	server {
    listen 80 default_server;
    listen [::]:80 default_server;

    server_name 127.0.0.1;
    location / {
        proxy_pass http://172.17.0.3:3000/;
    }

    location /backend/ {
        proxy_pass http://172.17.0.2:3000/;
    }

}
}


 
