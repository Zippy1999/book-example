Provisioning a new site
-----------------------

## Required packages

* nginx
* Python 3
* Git
* pip
* virtualenv

eg, on Ubuntu

sudo apt-get install nginx git python3 python3-pip python-pip
# sudo apt-get install build-essential autoconf libtool pkg-config python-opengl python-imaging python-pyrex python-pyside.qtopengl idle-python2.7 qt4-dev-tools qt4-designer libqtgui4 libqtcore4 libqt4-xml libqt4-test libqt4-script libqt4-network libqt4-dbus python-qt4 python-qt4-gl libgle3 python-dev
sudo easy_install greenlet
sudo apt-get install build-essential libssl-dev libffi-dev python-dev
sudo easy_install gevent
sudo pip3 install virtualenv

on Windows, make sure latest version of pip2 is installed (pip install --upgrade pip)

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
