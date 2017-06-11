# ans
My ansible playbooks

This is where I'm storing some of my ansible playbooks.
I'm pretty new at ansible, so my playbooks should reflect
that.  Please let me know if I'm doing anything horrible. :)

---
Meanwhile, a few notes about where I started:

* I'm using Chunkhost (https://chunkhost.com/r/46352)
* I've created the Chunkhost chunk
* My Ansible user is "mitnick"
```
# useradd -s /bin/bash -d /home/mitnick mitnick
# mkdir /home/mitnick
# chown mitnick.mitnick /home/mitnick
# mkdir /home/mitnick/.ssh
# chown mitnick.mitnick /home/mitnick/.ssh
# passwd mitnick  (and then assign the password)
```
* I've remoted in to my host as root, added mitnick username/password
changed shell to /bin/bash, created ~/.ssh, and then copied my ssh key (jkb@chinook) to his authorized_keys
* I've added mitnick to the /etc/sudoers
  * mitnick	ALL=NOPASSWD: ALL  # for general ansible goodness
  * mitnick	ALL=(solr) NOPASSWD: ALL  # for executing the geerlingguy.solr
* Replaced Debian's default ansible 1.7 to ansible 2.2 using pip install.

So with those changes above (I'll list any more that I find)
I should be able to use ansible and ansible-playbooks
to set up whatever else I need without using to manually
do it.

---
Example of executing playbook:
```
$ ansible-playbook -u mitnick -s playbook.yml
```
----

Next Steps:

* ~~Do an nginx tutorial to see how ansible works~~
* ~~Maybe customize nginx a little?~~
* Do a few tweaks and updates on stuff that I like on
my linux servers just to explore some of the options
  * Bash for solr user?
* What's the difference between a role and a play?
* ~~Install SOLR and Java from Ansible-galaxy.~~
* Profit.
* NTP and Pacific Time Zone
* ~~Organize the directories per the Ansible best practices~~
* Load and start a DurkaDurka service?
* Nuke the whole thing and build it from zero! :)


----

Useful links:

* Ansible nginx tutorial here: https://serversforhackers.com/an-ansible-tutorial
* Ansible Best Practices: http://docs.ansible.com/ansible/playbooks_best_practices.html

