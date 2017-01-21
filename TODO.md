## Todo:

Todo Tasks in the Roles:

* update-alternatives --config java  (and pick Java8)


http://solr.kr47.net:8983/solr/admin/cores
http://solr.kr47.net:8983/solr/#/
http://solr.kr47.net:8983/solr/#/~cores/turkey


TODO: Ask Keegan where to put the todo information about how you customize the ansible-galaxy configurations.
TODO: Ask Keegan how ansible-galaxy updates get plugged back in

* webinar: https://programs.lucidworks.com/Webinar-Solr-example-files.html?utm_source=hp <https://programs.lucidworks.com/Webinar-Solr-example-files.html?utm_source=hp> and blog post series that will have the final in that series published soon too: https://lucidworks.com/blog/2015/12/08/browse-new-improved-solr-5/ <https://lucidworks.com/blog/2015/12/08/browse-new-improved-solr-5/>


## Customizations to external roles:

### geerlingguy.java
https://galaxy.ansible.com/geerlingguy/java/
Add the Apt repository to get the openjdk-8-jdk from the system role.
Change vars/Debian.yml to use openjdk-8-jdk instead of 7.

### geerlingguy.solr
https://galaxy.ansible.com/geerlingguy/solr/
Need Java8 to run SOLR
Specify the names of the solr_cores in defaults/main.yml



## Ansible-Galaxy Commands:
Show all Ansible-Galaxy packages:
$ ansible-galaxy list -p roles

Install a new package with Ansible-Galaxy:
$ ansible-galaxy install -p roles geerlingguy.solr

Remove an Ansible-Galaxy package:
$ ansible-galaxy remove -p roles geerlingguy.solr

# ansible-galaxy install -p roles geerlingguy.java