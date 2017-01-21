Provisioning a new site
-----------------------

## Required packages

* nginx
* Python 3
* Git
* pip
* virtualenv

eg, on Ubuntu

sudo apt-get install nginx git python3 python3-pip
sudo pip3 install virtualenv

## Nginx Virtual Host config

* see nginx.template.conf
* replace SITENAME with, eg, staging.my-domain.com

## systemd job

* see gunicorn-upstart.template.conf
* replace SITENAME with, eg, staging.my-domain.com

## Folder structure
Assume we have an account at /home/username

/home/username
|_____sites
      |_____SITENAME
             |______database
             |______source
             |______static
             |______virtualenv
