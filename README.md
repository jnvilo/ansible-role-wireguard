ansible-role-wireguard
=========

This ansible role installs and configures a wireguard server and also create configuration for peers. 

Requirements
------------

None

Role Variables
--------------

- wg_ipaddress : The private ip address: for example 10.10.10.1/24
- wg_listen_port: Example: 3113


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: wireguarg
      roles:
         - role: wireguard
           wg_ipaddress: 10.10.10.1
           wg_listen_port: 3113
           wg_private_key: ..... 
           wg_peers: 
            - ipaddress: 10.10.10.2
              public_key: ....
            - ipaddress: 10.10.10.3
              public_key: ....
           allowed_ssh:
            - 84.233.234.123/32
            - 203.303.192.93/32
            

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
