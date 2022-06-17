The OpenROAD-Project OpenLane
=============================
 The OpenRoad Openlane is a automated RTL to GDSII flow build around open source tool. The flow perform the auto place and route of an ASIC design -in 24 hours with no human in the loop.

Prerequisites
-------------
``install Python 3.6+ and create virtual environment``

On Ubuntu
---------
``sudo apt install -y build-essential python3 python3-venv python3-pip``

Docker Installation
-------------------
Docker Installation Steps
(https://docs.docker.com/engine/install/ubuntu/)

| After installing the docker restart your Machine.
| check Docker install
  run groups
user_name adm cdrom sudo dip plugdev lpadmin lxd sambashare docker::
| #dockerinstalled
| Check docker version::
| run docker --version::
``sudo apt install klayout #for klayout``

Setting Up Magic 
----------------
| #Prerequisites of magic
| ``sudo apt install m4``
| ``sudo apt install csh``
| ``sudo apt install libx11-dev``
| ``sudo apt install libncurses-dev``
| ``sudo apt install tcl-dev tk-dev``
| ``sudo apt install blt-dev``
| ``sudo apt install freeglut3``
| ``sudo apt install libgl1-mesa-dev``
| ``sudo apt install libglu1-mesa-devash``

| Clone the respository to install magic

git clone https://github.com/RTimothyEdwards/magic.git
| ``cd magic``
| ``./configure``
| ``sudo make``
| ``sudo make install``
| ``magic --version``
``cd ../``

Setting Up OpenLane
-------------------
| Clone the respository and run the below to set up the Sky130 PDK and OpenLane
| git clone https://github.com/The-OpenROAD-Project/OpenLane.git
| ``cd OpenLane/``
| ``make openlane``# This will pull  Openlane docker image.
| ``make pdk`` # Default PDK_ROOT is $(pwd)/pdks. If you want to install the PDK at a differnt location, uncomment the next line.
| #export PDK_ROOT=<absolute path to where skywater-pdk and open_pdks will reside>
| ``make test`` # This is to test that the flow and the pdk were properly inst
#This test run the design spm. Check the final generated layout at this path ../designs/spm/runs/openlane_test/results/magic/spm.gds.
```
#





  




