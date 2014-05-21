ansible-transmission-common
========

Ansible role which installs [Transmission](http://www.transmissionbt.com), a cross-platform BitTorrent client.

By default the following components are installed:

 - transmission-cli: lightweight BitTorrent client (command line programs)
 - transmission-common: lightweight BitTorrent client (common files)
 - transmission-daemon: lightweight BitTorrent client (daemon)

Role Variables
--------------

Additional components can be specified by means of the variable `transmission_optional_components`:

	transmission_optional_components: 
	  - transmission-gtk    # lightweight BitTorrent client (GTK+ interface)
	  - transmission-qt     # lightweight BitTorrent client (Qt interface)

Example Playbook
-------------------------

1) Install transmission with default components

    - hosts: all
      roles:
      - ansible-transmission-common


2) Install transmission with GUI components as well

    - hosts: all
      roles:
      - {role:                             'ansible-transmission-common',
         transmission_optional_components: ['transmission-gtk']}

Dependencies
------------

None

License
-------

BSD

Author Information
------------------

Parv Mihai