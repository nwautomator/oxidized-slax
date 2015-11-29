Oxidized Commit Script
========================
This is a commit script for Juniper devices that kicks off an Oxidized run. It basically makes a HTTP request to the Oxidized REST API to place your device in the front of the queue to have its configuration pulled.

Requirements
============
- Juniper routers/switches running at least version 10 of the JunOS operating system
- A working Oxidized installation on an NMS
- Permissions to install the script on your Juniper gear

Installation
============
0. Clone this repository (```git clone https://github.com/nwautomator/oxidized-slax.git```)
1. Change the `$OXIDIZED-SERVER` URL in the script to the appropriate NMS system for your environment
2. Use SCP (or WinSCP) to copy the script to `/var/db/scripts/commit` on your Juniper devices
3. Use `set system scripts commit oxidized.slax` in configuration mode to activate the script
4. Do a few changes and commits to make sure it's working

TODO
====
1. Send requests to multiple NMS systems (for the paranoid)
2. ???
