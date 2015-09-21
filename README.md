# Notes

* Jenkins is available on 192.168.33.10:8080. Change the address if necessary in the Vagrantfile.
* Files were included because I was having problems with builds failing due to strange network errors. This is possibly because I was running Vagrant/VirtualBox inside of VirtualBox. 
* I used a simple playbook instead of a role because I didn't use templates or conditional variables that would benefit from the role structure, and I wasn't working within a repository that was already set up to use the role structure. One of my goals is always to "right-size" effort on a task. The right size for this task was to use a single playbook, and refactoring could be done later if the playbook grew. 

# Suggested Improvements

After struggling to go from zero to development environment on my Windows gaming machine, I started to get short on time. If I had a touch more time, I'd make the following improvements. 

* I'd use the OpenStack Jenkins Job Builder (http://docs.openstack.org/infra/system-config/jjb.html) instead of the CLI. 
* I'd split the playbook into 'install Jenkins' and 'install job'. 
* I'd install and configure a proxy to put Jenkins on port 80.
* I did a simple compliation of lighttpd, and didn't do anything with it. I should instead use Ant to create an artifact. 
