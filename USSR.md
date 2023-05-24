# USSR setup

## Configuring
```sh
sudo service mysql start
sudo service redis-server start

sudo python3.9 -m pip install -r requirements.txt

# running ussr for the first time auto generates a config file
python3.9 main.py
# now, we edit the config file
nano config.json
