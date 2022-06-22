# How to Clone Private Github Repository Using Personal Token
## Simple steps to clone own private repository generating github personal token

# 1. Go to settings then to Developer settings

You can go to developer settings using following link: 

[https://github.com/settings/tokens](https://github.com/settings/tokens)

Then, click to generate new token and give preferred admin rights to token, once done copy this token somewhere safe.

# 2.1 Clone repository

Now you can clone using you username and access token for your repo

    git clone https://USERNAME:ACCESS_TOKEN@github.com/user123/whateverapp.git

# 2.2 Alternatively clone dev branch

You can also clone any other branch of the repo using -b flag and branch name

    git clone -b dev https://USERNAME:ACCESS_TOKEN@github.com/user123/whateverapp.git
