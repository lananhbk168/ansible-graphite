Ansible - Graphite
------------------
This Ansible playbook will install graphite via pip in its default location '/opt/graphite'


To run this playbook.

1. clone the repo
2. modify `hosts` file with the IP or hostname of the server you want to setup
3. ignore ssh's known hosts file
  * `export ANSIBLE_HOST_KEY_CHECKING=False`
4. run `ansible-playbook -i hosts playbook.yml`
5. In ~4 minutes you should have a running Graphite server!



Graphite
--------

### Secrets
Change `graphite_secret_key` under `roles/graphite/defaults/main.yml` to something unique for your graphite instance!


Testing
--------

### Vagrant
Simply clone this repo and make sure you have Vagrant + Virtual Box installed and...
  1. vagrant up
  2. visit http://192.168.111.222/
  3. :-) 

Vagrant is using Ubuntu 13.04 Raring Ringtail for it's OS.


### Digital Ocean
I've tested this playbook with Digital Ocean VM's with a few different flavor of OS's.

  * CentOS 6.5  
  * Ubuntu 12.04.3 Precise Pangolin
  * Ubuntu 13.04 Raring Ringtail



TODO
----
* Add Django superuser creation `python manage.py createsuperuser`.



Resources
---------
* http://graphite.wikidot.com/quickstart-guide
