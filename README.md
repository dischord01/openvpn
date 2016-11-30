OpenVPN
=======

This role installs the OpenVPN service.

Requirements
------------

This role requires some certificates to be generated and placed as variables as
described below.

Role Variables
--------------

    openvpn_dns1: 8.8.8.8
    openvpn_dns2: 8.8.4.4
    openvpn_server_name: server

    openvpn_ca: ""
    openvpn_server_key: ""
    openvpn_server_crt: ""
    openvpn_dh2048: ""

- `openvpn_ca:`: Certificate authority.
- `openvpn_server_key`: Server's key.
- `openvpn_server_crt`: Server's certificate
- `openvpn_dh2048`: Diffie-Hellman key exchange file.

You can check how to generate these files in the step 3 of
[this tutorial](https://www.digitalocean.com/community/tutorials/how-to-setup-and-configure-an-openvpn-server-on-centos-7).

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: inkatze.openvpn }

License
-------

BSD
