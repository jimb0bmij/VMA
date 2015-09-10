# VMA
Ansible code to use the VMA to manage virtual environments. Why would we want to use the VMware VMA 6 appliance?
Understand that ESXi by default does not enable SSH and for a good reason, security. Yes you can use Ansible and direct connect to ESXi via SSH. 
But you do not need to. VMware provides the tools to do what you need to do and securley. Using their tools gets you support and you do not modify the core ESXi like installing perl. Any new features for ESXi will be supported in the VMA no need to wait for someone to create a module in Ansible for it.
