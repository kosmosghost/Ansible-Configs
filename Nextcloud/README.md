# Nextcloud Ansible script

This Ansible Script will install Nextcloud with an encrypted data directory, and an admin user.

# Description

This is a Nextcloud Ansible Script with optimized settings for a Raspberry PI 4 running Debian.

To use place the Community Zip file provided by Nextcloud, usually named latest.zip in the files directory. Add SSL keys into the keys directory. SSL keys must have the same name, minus the extension. IE: `server.crt` and `server.key`

Add a new host file with the appropriate IP address for the server you are configuring, and then run:

`ansible-playbook -i host nextcloud.yaml -K -k -u <SSH_USER>`

Replace <SSH_USER> with the username on the remote machine you will be connecting to.

# It is advisable to run mysql_secure_installation after running this script.