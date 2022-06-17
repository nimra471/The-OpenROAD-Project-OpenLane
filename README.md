# The OpenROAD-Project OpenLane
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0) [![Documentation Status](https://readthedocs.org/projects/openlane/badge/?version=latest)](https://openlane.readthedocs.io/) [![CI](https://github.com/The-OpenROAD-Project/OpenLane/workflows/CI/badge.svg?branch=master)](#) [![Slack Invite](https://img.shields.io/badge/Community-Skywater%20PDK%20Slack-ff69b4?logo=slack)](https://invite.skywater.tools) [![Python code style: black](https://img.shields.io/badge/python%20code%20style-black-000000.svg)](https://github.com/psf/black)

The OpenRoad Openlane is a automated RTL to GDSII flow build around open source tool. The flow perform the auto place and route of an ASIC design -in 24 hours with no human in the loop.

- [Prerequisites](#prerequisites)
- [Docker Installtion Steps](#docker_Installation)
- [Setting Up Magic](#setting-up-Magic)
- [Setting Up OpenLane](#setting-up-OpenLane)


# Prerequisites

- install Python 3.6+ and create virtual environment.

# On Ubuntu
```bash
sudo apt install -y build-essential python3 python3-venv python3-pip
```
# Docker Installation
- [Docker Installation Steps](https://docs.docker.com/engine/install/ubuntu/)

After installing the docker restart your Machine.
```bash
  check Docker install
- run groups
  user_name adm cdrom sudo dip plugdev lpadmin lxd sambashare docker
  #dockerinstalled
  Check docker version
- run docker --version
  sudo apt install klayout #for klayout

```
# Setting Up Magic 
```bash
#Prerequisites of magic
sudo apt-get install m4
sudo apt-get install csh
sudo apt-get install libx11-dev
sudo apt-get install libncurses-dev
sudo apt-get install tcl-dev tk-dev
sudo apt-get install blt-dev
sudo apt-get install freeglut3
sudo apt-get install libgl1-mesa-dev
sudo apt-get install libglu1-mesa-devash
```
Clone the respository to install magic
```bash
git clone https://github.com/RTimothyEdwards/magic.git
cd magic
./configure
sudo make
sudo make install
magic --version
cd ../
```
# Setting Up OpenLane
Clone the respository and run the below to set up the Sky130 PDK and OpenLane
```bash
git clone https://github.com/The-OpenROAD-Project/OpenLane.git
cd OpenLane/
git checkout v0.23
make pull-openlane # This will pull updated Openlane docker image.
make pdk # Default PDK_ROOT is $(pwd)/pdks. If you want to install the PDK at a differnt location, uncomment the next line.
#export PDK_ROOT=<absolute path to where skywater-pdk and open_pdks will reside>
make test # This is to test that the flow and the pdk were properly inst
#This test run the design spm. Check the final generated layout at this path ../designs/spm/runs/openlane_test/results/magic/spm.gds.
```





  




