# The-OpenROAD-Project-OpenLane
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0) [![Documentation Status](https://readthedocs.org/projects/openlane/badge/?version=latest)](https://openlane.readthedocs.io/) [![CI](https://github.com/The-OpenROAD-Project/OpenLane/workflows/CI/badge.svg?branch=master)](#) [![Slack Invite](https://img.shields.io/badge/Community-Skywater%20PDK%20Slack-ff69b4?logo=slack)](https://invite.skywater.tools) [![Python code style: black](https://img.shields.io/badge/python%20code%20style-black-000000.svg)](https://github.com/psf/black)
The OpenRoad Openlane is a automated RTL to GDSII flow build around open source tool. The flow perform the auto place and route of an ASIC design -in 24 hours with no human in the loop.

The documentation also available here[Readthedoc](https://the-openroad-project-openlane.readthedocs.io/en/latest/)

- [Prerequisites](#prerequisites)
- [Docker Installtion Steps](#docker_Installation)
- [Setting Up Magic](#setting-up-Magic)
- [Setting Up OpenLane](#setting-up-OpenLane)

# Prerequisites

install Python 3.6+ and create virtual environment.
# On Ubuntu
```bash 
sudo apt install -y build-essential python3 python3-venv python3-pip
```
# Docker Installation
- [Docker Installation Steps](https://docs.docker.com/engine/install/ubuntu/)

After installing the docker restart your Machine. 
```bash
check Docker install
run groups
user_name adm cdrom sudo dip plugdev lpadmin lxd sambashare docker 
#dockerinstalled 
Check docker version
run docker --version
sudo apt install klayout #for klayout
```
# Setting Up OpenLane
Clone the respository and run the below to set up the Sky130 PDK and OpenLane 
```bash git clone https://github.com/The-OpenROAD-Project/OpenLane.git 
cd OpenLane/ 
make openlane # This will pull Openlane docker image. 
make pdk # Default PDK_ROOT is $(pwd)/pdks. If you want to install the PDK at a differnt location, uncomment the next line. #export PDK_ROOT=<absolute path to where skywater-pdk and open_pdks will reside>
make test # This is to test that the flow and the pdk were properly inst #This test run the design spm. Check the final generated layout at this path ../designs/spm/runs/openlane_test/results/magic/spm.gds.
```
