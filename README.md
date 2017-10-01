# kazoo-ansible
Ansible Playbooks to orchestrate the various components of [2600hz Kazoo](https://github.com/2600hz/kazoo).

## Pre-release Notice
kazoo-ansible is currently in a pre-release state and may introduce backward 
incompatible changes until 1.0.0 is released and this notice is removed. 
This is to provide an opportunity to greatly improve kazoo-ansible without 
needing to wait for a major release. Once we are happy with kazoo-ansible, 
it will be released as 1.0.0 and subject to backward compatibility 
guarantees.

## Features
- Automatically clusters CouchDB, Freeswitch, Kamailio, and Kazoo
- Let's Encrypt TLS certificate generation for Monster UI, including 
support for multiple Monster UI hosts
- Uses CouchDB instead of BigCouch
- Uses specific versions of Freeswitch, Kamailio, Kazoo, and Monster UI 
by default
- Splits up roles for CouchDB, Freeswitch, Kamailio, Kazoo, Monster UI, 
and RabbitMQ to allow lots of cluster custimization
- Publishes roles to Ansible Galaxy to allow easy integration into 
custom playbooks
- Manages Kazoo, Monster UI, Kamailio, and Freeswitch component versions 
by default to prevent untested versions from making it into production

## Desired Future Improvements
- Support for multiple zones
- CouchDB backup roles

## License
MIT License

## Installation Instructions
- Install CentOS 7 on all of the hosts that will be managed by kazoo-ansible
- Enable password-less SSH for the user that will run kazoo-ansible on all of 
the hosts that will be managed by kazoo-ansible
- Enable password-less sudo on all of the hosts that will be managed by 
kazoo ansible
- Install all of the roles from [kazoo-ansible at Ansible Galaxy](https://galaxy.ansible.com/kazoo-ansible/)
- Clone this GitHub repository
- Edit `group_vars/all` and `site.yml` to your liking
- Add hosts for each role in `site.yml` in `/etc/ansible/hosts`
- Run `ansible-playbook site.yml`

## Using kazoo-ansible with Existing Playbooks
If you want to use kazoo-ansible with existing playbooks, simply

## Contributions
There are many ways to contribute:
- Suggestions
- Bug Reports
- Pull Requests
- Donations

## Versioning Strategy
This project uses [Semantic Versioning](http://semver.org). In 
practical terms, this means:
- Version numbers include MAJOR.MINOR.PATC
- Major versions include backward-incompatible changes. This includes 
updating to major Kazoo versions, CentOS upgrades, or any other 
breaking changes.
- Minor versions include backward-compatible changes, such as new 
features. This includes updating to minor Kazoo versions, or any 
other backward-compatible changes.
- Patch versions include backward-compatible bug fixes. This includes 
updating to patch Kazoo versions, or any other backward-compatible 
bug fixes.

