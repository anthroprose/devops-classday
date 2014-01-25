devops-classday
===============

devops-classday documentation &amp; presentation

----------------------------------------------

# Pre-Requisites

## VirtualBox
* v4.3.6
* https://www.virtualbox.org/wiki/Downloads
* Required
* 
## Vagrant
* v1.4.3
* http://www.vagrantup.com/downloads.html
* Required

## Meez
* [meez](https://github.com/paulczar/meez)
* Not Required, but good for bootstrapping chef cookbooks

----------------------------------------------

# Session One - Local Development Environment
## Vagrant Setup
```bash
apt-get install ruby-dev
vagrant plugin install vagrant-berkshelf
vagrant plugin install vagrant-omnibus
vagrant plugin install vagrant-chef-zero
git clone git://github.com/anthroprose/devops-classday.git
cd devops-classday
vagrant up
```

----------------------------------------------
