OpenVpn client for Ubuntu 16
=========

Installs OpenVpn client on Ubuntu xenial.

Requirements
------------

Ubuntu 16.04 tested only.
It is supposed to use SSH Public Key Authentication on client.
Variables such as ansible_user and ansible_ssh_private_key_file must be defined in the inventory file.
Keys for open VPN client (ca.crt, tls-auth etc) must be specified in templates/client.conf

Role Variables:         Default:        Description
-------------------------------------------------------------------------------------
 - openvpn_server_ip       8.8.8.8         VPN server ip address
 - openvpn_port            2195            VPN server port
 - openvpn_proto           udp             The protocol which you want to use (tcp/udp)
 - openvpn_reneg_sec       259200          Renegotiate data channel key after X seconds. When using dual-factor authent$

Dependencies
------------
None

Example Playbook
----------------
    ---
    - hosts: your_host
      roles:
      - role: openvpn_client


License
-------

MIT

Author Information
------------------

This role was created by Ilnar
