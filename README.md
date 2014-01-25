devops-classday
===============

devops-classday documentation &amp; presentation

----------------------------------------------

# Pre-Requisites

## Github Account
* https://www.github.com
* Fork this Repo!

## VirtualBox
* v4.3.6
* https://www.virtualbox.org/wiki/Downloads
* Required

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
git clone git://github.com/{YOURGITHUBACCOUNT}/devops-classday.git
cd devops-classday
vagrant up {centos6|saucy}
vagrant ssh {centos6|saucy}
```

----------------------------------------------

# Session Two - Environment Automation with Chef
## Chef-Zero
* It's chef-lite!
* Makes working with encrypted data bags a breeze
* No need to install chef-solo-search on everything

```bash
apt-get install ruby-dev
vagrant plugin install vagrant-berkshelf
vagrant plugin install vagrant-omnibus
vagrant plugin install vagrant-chef-zero
meez -l apachev2 -C "Alex Corley" -m acorley@anthroprose.com -o ./ devopsclassday
mv devopsclassday/* ./
rmdir devopsclassday
```

----------------------------------------------

# Session Three - Modern Web App
## Nginx
* http://nginx.org/en/download.html
* https://github.com/opscode-cookbooks/nginx

## uWSGI
* https://uwsgi-docs.readthedocs.org/en/latest/
* https://github.com/50onRed/uwsgi - but this one sucks, so we're going to hack our own depending on ubuntu or centos