# ZRE Dashboard 2024
This is a C++ application for the dashboard of an FSAE vehicle.
## Overview
### Dependencies
qt-library  

make  

gcc
### Install and Usage
```shell
# Install
sudo apt-get update && sudo apt-get upgrade

sudo apt-get -y install build-essential openssl libssl-dev libssl1.0 libgl1-mesa-dev libqt5x11extras5 qt5-qmake

make all 

make -B create-vcan

# Usage
cd bin

./dash-qt vcan0 ../dbc/main_2023.dbc

sudo ip link set can0 type can bitrate 1000000
```

### Network Library
Used for interfacing with the operating system's network devices. CAN functionality is implemented here.
### QT
The dashboard application, implemented using QT. This program reads and displays data from a CAN bus in a interactive GUI.
### CAN CLI
A debugging tool used to monitor a CAN bus, parse DBC files, and send CAN messages.
### TUI
A debugging tool used to monitor a CAN database in real-time.