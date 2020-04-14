# Keepalived VRRP POC

This POC contains 3 CentOS/8 VM Boxes - 1 client and 2 routers.  The configuration is basic, but is an attempt to deploy a virtual MAC address on the virtual IP.

The boxes are called:
1. router1
2. router2
3. client

The private network between them is 192.168.254.0/24

## Requirements

1. Virtualbox - https://virtualbox.org
2. Vagrant - https://vagrantup.com
3. Ansible - https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html

## Instructions

1. Start up the POC `vagrant up`.
2. Access the client with `vagrant ssh client`
3. Test the router - `$ ping 192.168.254.1`
4. Determine the MAC of the router - `$ arp 192.168.254.1`
5. Determine which router is the master - `vagrant ssh router1` and execute `ip a` to determine if 192.168.10.1 is present.
