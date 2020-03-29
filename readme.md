# ansible-docker-webserver

This ansible setup prepares a fresh Ubuntu server for use as a webserver with docker.

- It hardens the server (ssh settings and firewall).
- It adds an 'ansible' user for later use.
- It adds an 'web' user for later use.
- It installs docker and docker-compose.
- It reboots the machine

## Usage

To use this setup run the following command:

`
ansible-playbook -i HOST, docker-webserver.yml --private-key ~/.ssh/PRIVATE-KEY
`