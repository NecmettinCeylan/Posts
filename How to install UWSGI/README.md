# How to install UWSGI
## Steps to install UWSGI to a python 3.8 virtual environment and starting django server using UWSGI


# 1. Install python 3.8

First get updates for os, install python 3.8 and python 3.8 venv 

    sudo apt update && sudo apt upgrade
    sudo apt install software-properties-common -y
    sudo add-apt-repository ppa:deadsnakes/ppa -y
    sudo apt update
    sudo apt install python3.8 -y
    sudo apt install python3.8-venv -y

# 2. Create python3.8 virtual environment

Using following code, create a python 3.8 venv and then activate it

    python3.8 -m venv django_env_38
    source django_env_38/bin/activate


# 3. Install uwsgi

Using pip install uwsgi    

    pip install uwsgi

# 4. Test the uwsgi with django:

    uwsgi --module=mysite.wsgi:application \
    --http=0.0.0.0:8000 \
    --virtualenv=/home/myuser/django_env_38/


# 5. Start django using uwsgi.ini file

    uwsgi --ini /home/myuser/mysite/config/uwsgi.ini

# 6. Start django using uwsgi.ini file in background mode and save log file

    uwsgi --ini /home/myuser/mysite/config/uwsgi.ini --daemonize /home/myuser/logs/uwsgi.log


# References

[https://www.linuxcapable.com/how-to-install-python-3-8-on-ubuntu-22-04-lts/](https://www.linuxcapable.com/how-to-install-python-3-8-on-ubuntu-22-04-lts/)
