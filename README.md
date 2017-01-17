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
* I've remoted in to my host as root, added mitnick username/password
changed shell to /bin/bash, created ~/.ssh, and then copied my ssh key to his authorized_keys
* I've added his name to the /etc/sudoers

So with those changes above (I'll list any more that I find)
I should be able to use ansible and ansible-playbooks
to set up whatever else I need without using to manually
do it.

----

Next Steps:

* ~~Do an nginx tutorial to see how ansible works~~
* ~~Maybe customize nginx a little?~~
* Do a few tweaks and updates on stuff that I like on
my linux servers just to explore some of the options
* What's the difference between a role and a play?
* Install SOLR and Java from Ansible-galaxy.
* Profit.
* NTP and Pacific Time Zone
* Organize the directories per the Ansible best practices


----

Useful links:

* Ansible nginx tutorial here: https://serversforhackers.com/an-ansible-tutorial
* Ansible Best Practices: http://docs.ansible.com/ansible/playbooks_best_practices.html

