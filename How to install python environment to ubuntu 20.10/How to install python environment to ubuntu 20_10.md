# How to install python environment to ubuntu 20.10
## Simple steps to create install python virtual environment to ubuntu 20.10 using console

# Step 1 - Update Ubuntu packages

    sudo apt update
    sudo apt upgrade -y

# Step 2 - Install python3-venv package

    sudo apt install python3-venv

# Step 3 - Create virtual environment

    python3 -m venv new_virtual_env

# Step 4 - Activate virtual environment

    source new_virtual_env/bin/activate

# Step 5 - Install packages using pip with or without requirements.txt

    pip3 install django

Alternatively using requirements.txt

    pip3 install -r requirements.txt

# All steps in a code block 

    sudo apt update
    sudo apt upgrade -y
    sudo apt install python3-venv
    python3 -m venv new_virtual_env
    source new_virtual_env/bin/activate
    pip3 install django
    pip3 install -r requirements.txt

# Extra - Deactivating current virtual environment

Simply write deactivate to active console

    deactivate
