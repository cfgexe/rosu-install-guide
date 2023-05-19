# Setting Up
## First, create a folder, name it anything you want. We will be using "rosu" for this example.
```sh
mkdir rosu
cd rosu
```
## Cloning repositories
```sh
# clone pep.py
git clone https://github.com/RealistikOsu/pep.py
# clone USSR
git clone https://github.com/RealistikOsu/USSR
# clone perf-service
git clone https://github.com/RealistikOsu/performance-service
# clone avatar-server
git clone https://github.com/osuDebian/avatar-server
# clone helpers
git clone https://github.com/cfgexe/rosu-helpers
```
## Messy stuff..
### I am VERY bad at setting up stuff with go, so take these scripts i've given you.
```sh
cd rosu-helpers && ./setup_api.sh
./setup_hanayo.sh
```
