# Setting Up
## First, create a folder, name it anything you want. We will be using "rosu" for this example.
```sh
mkdir rosu
cd rosu
```
## Installing dependencies
```sh
sudo add-apt-repository -y ppa:deadsnakes
sudo apt install -y python3.9-dev python3.9-distutils \
                    build-essential \
                    mysql-server redis-server \
                    nginx golang-go screen
```
## Cloning repositories
```sh
# clone pep.py
git clone https://github.com/RealistikOsu/pep.py
# clone USSR
git clone https://github.com/RealistikOsu/USSR
# clone perf-service (optional, don't do if you want an oppai system)
git clone https://github.com/RealistikOsu/performance-service
# clone avatar-server
git clone https://github.com/osuDebian/avatar-server
# clone API
git clone https://github.com/RealistikOsu/RealistikAPI
# clone hanayo
git clone https://github.com/RealistikOsu/hanayo
```
## Nginx setup
```sh
sudo cp extras/nginx.conf /etc/nginx/sites-available/rosu.conf
sudo ln -s /etc/nginx/sites-available/rosu.conf /etc/nginx/sites-enabled/rosu.conf
# Edit this file replacing `your.domain`  with your domain and `path/to/certs` with the path to the certs generated from cloudflare
sudo nano /etc/nginx/sites-avaiable/rosu.conf
```
## All done!
[Next: USSR setup](https://github.com/cfgexe/rosu-install-guide/blob/main/USSR.md)
