# VMA
Ansible code to use the VMA to manage virtual environments. Why would we want to use the VMware VMA 6 appliance?
Understand that ESXi by default does not enable SSH and for a good reason, security. Yes you can use Ansible and direct connect to ESXi via SSH. 
But you do not need to. VMware provides the tools to do what you need to do and securley. Using their tools gets you support and you do not modify the core ESXi like installing perl. Any new features for ESXi will be supported in the VMA no need to wait for someone to create a module in Ansible for it.

Example: Had a issue with a EMC array that needed VAAI disabled before patch is applied. There is no Ansible module for it. But using the VMA and the credstore.yml to setup all the ESXi hosts (they have different root passwords FYI). Then using vma-vaai-DISABLE.yml to disable VAAI on the hosts to allow the EMC patch to be installed. Then run the vma-vaai-ENABLE.yml to turn it back on. Simple and easy with Ansible and the VMA.


