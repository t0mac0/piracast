Copyright 2013

Welcome to the Piracast project. 
=========

### Limitation: 
    1. Only works with TP-Link dongle.
    2. No HDCP support (cannot remote Netflix or Google Music). 

### Environment Setup: 
1. Install driver: 
	sudo cp env/8188eu.ko /lib/modules/`uname -r`/kernel/drivers/net/wireless
   	sudo depmod -a
   	sudo modprobe 8188eu

2. Install DHCP server
	sudo apt-get install isc-dhcp-server
	cp env/isc-dhcp-server /etc/default
	cp dhcpd.conf /etc/dhcp/

### Compile the project: 
    1. cd target
    2. make core

### To run Piracast:
    1. cd scripts
    2. sudo python piracast.py