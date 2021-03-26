# About
Ansible playbook to create a HA pair of proxy servers to simply forward traffic from defined floating VIPS to backends. Created specifically to proxy armor services, but could be used for any service.

# Specifics
The Playbook is designed specifically to run on 2 severs to configure them as a HA pair.

Proxy forwarding software used is HAproxy, VIP and HA management with keepalived.

This playbook is designed and tested on centos7, but may work on other operating systems.

# Usage / configuration
The inventory hostgroup "proxy_pair" must contain 2 hosts that are desired to become the HA pair.

The playbook defined variable "proxy" must contain a list of items with the following elements:
* name
* vip
* vip_port
* destination

Current configuration is for Armor hosting services, VIPs should be set as desired for the implementation.
