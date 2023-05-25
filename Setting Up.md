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
## mysql setup
```sh
sudo service mysql start
sudo mysql

CREATE DATABASE YOUR_DB_NAME;

# create a user to use the bancho.py database
CREATE USER 'YOUR_DB_USER'@'localhost' IDENTIFIED BY 'YOUR_DB_PASSWORD';

# grant the user full access to all tables in the bancho.py database
GRANT ALL PRIVILEGES ON YOUR_DB_NAME.* TO 'YOUR_DB_USER'@'localhost';
FLUSH PRIVILEGES;
quit
# prepare db
mysql -u YOUR_DB_USER -p YOUR_DB_NAME < USSSR/extras/db.sql
```
## All done!
[Next: USSR setup](https://github.com/cfgexe/rosu-install-guide/blob/main/USSR.md)
