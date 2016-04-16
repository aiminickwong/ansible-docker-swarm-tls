# ansible-docker-swarm-tls
Ansible Playbooks to Deploy Docker Swarm with TLS (including certificate creation)

Specify the server you would like to use to generate certificates. These will be downloaded to the Ansible hosts in a playbook subdirectory named client-certs that will be created at runtime.

The current playbook setup will use FQDNs for the Swarm consul, managers, and nodes. If your servers do not have a resolvable FQDN, the playbook can be updated to use host IPv4 by editing the references in the swarm-discovery and swarm-nodes tasks.

cd swarm-playbook
ansible-playbook -i hosts -k site.yml