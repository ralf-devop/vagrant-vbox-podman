# Vagrant-Vbox-Podman

My vagrant vbox environment to play around with podman containers.

## Required Software

 * [Vagrant](https://developer.hashicorp.com/vagrant/install)
 * [VirtualBox](https://www.virtualbox.org/wiki/Downloads)

## Provison with Ansible

The configuration is defined as an ansible playbook.
Changes in a running environment can be applied as follows:
`ansible-playbook --connection=local --inventory 127.0.0.1, /vagrant/ansible/playbook.yml`

## Using Podman-Compose

`cd /vagrant/podman/<project>`

### Start
`podman compose up -d`

### Stop
`podman-compose down`
