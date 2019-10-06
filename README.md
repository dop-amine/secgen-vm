# Overview

Ansible Playbook to provision SecGen dependencies on Ubuntu 18.04 Server.

# Setup

## Playbook Prep

* Create and enter ssh_keys in `vars/ssh_keys/authorized_keys.yml`
* Enter username and timezone in `vars/vars.yml`
* Enter host in `hosts`: `<username>@<ip_address>`

## Before Provision

SSH to host:

```
ssh <username>@<ip_address>
```

Setup sudo permissions:

```
sudo visudo
```

Paste lines below with <username>:

```
<username> ALL=(ALL:ALL) ALL
<username> ALL=NOPASSWD: ALL
```

Setup ssh key pair and authorized keys:

```
ssh-keygen
sudo vim ~/.ssh/authorized_keys
```

Enter public key of local machine.

## After Provision

Git Clone SecGen & bundle install:

```
cd /home/amine/SecGen
git clone
bundle install
```
