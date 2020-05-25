# ansible-docker-webserver

This ansible setup prepares a fresh Ubuntu server for use as a webserver with docker.

- It hardens the server (ssh settings and firewall).
- It adds an 'ansible' (with sudo) user for later use with a random password, please write down this password (provided during playbook execution).
- It adds a user (without sudo but in the docker group) for later use (by default this user is called 'web' but this name can be overwritten by passing the `user` variable in the --extra-vars).
- It installs docker and docker-compose.
- It reboots the machine.

## Usage

To use this setup run the following command:

`
ansible-playbook -i HOST, docker-webserver.yml --private-key ~/.ssh/PRIVATE-KEY --extra-vars "authorized_key=~/.ssh/id_rsa.pub user=USER"
`