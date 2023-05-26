# USSR setup

## Configuring
```sh
cd USSR
sudo service redis-server start

sudo python3.9 -m pip install -r requirements.txt
# revert back to last commit before oppai got removed
git checkout b982d01
# running ussr for the first time auto generates a config file
python3.9 main.py
# now, we edit the config file
nano config.json
# start a screen session
screen -S ussr
# when configured, run again and you should have USSR running!
python3.9 main.py
# detach
^A-D
