# How to install nginx to Ubuntu
## Simple steps to install nginx also some useful commands

Update system packages and then install nginx

    sudo apt update
    sudo apt install nginx


# Useful commands

Following commands helps to see status of nginx, stop, start, restart or reload nginx

    systemctl status nginx
    sudo systemctl stop nginx
    sudo systemctl start nginx
    sudo systemctl restart nginx
    sudo systemctl reload nginx


When nginx have access problem to file or folder you can use following code:

    chmod 777 /home/foldername/

this gives all users to all rights for this and subfolders so use it carefully


# References 

[ref 1](https://www.digitalocean.com/community/tutorials/how-to-install-nginx-on-ubuntu-22-04)

