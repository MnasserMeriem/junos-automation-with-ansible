Module: junos_command  
Executes commands (cli or rpc) on Junos devices and return the results to the Ansible playbook.     
In addition, it can specify a set of conditionals to be evaluated against the returned output, only returning control to the playbook once the entire set of conditionals has been met. So you can check if you bgp neighbors are established as example.  
Documentation: http://docs.ansible.com/ansible/junos_command_module.html  
source code: https://github.com/ansible/ansible-modules-core/tree/devel/network/junos 
Installation: this is a core module. It ships with ansible itself      
Requirements on Ansible: Ansible 2.1 and junos-eznc   
Requirements on  Junos devices: netconf  

Playbooks:  
- pb.check_lldp.yml: check if the lldp neighbors are the ones we expect (so check if there is no cabling error)  
- pb.check.bgp.yml: check if the state of your bgp neighbors are established.  
- pb.check.bgp_2.yml: check if the state of your bgp neighbors are established.   
- pb.check.vlans.yml: check from devices operationnal state if desirated vlans are presents  
- pb.yml: pass various commands on Junos devices. Parse the commands output. Save the output on the Ansible server.   
- pb.rpc.yml: pass rpc to Junos devices. And print the result in JSON and XML format.  

Usage:  
```
ansible-playbook junos_command/pb.check_lldp.yml  
ansible-playbook junos_command/pb.check.bgp.yml
ansible-playbook junos_command/pb.check.bgp_2.yml
ansible-playbook junos_command/pb.check.vlans.yml
ansible-playbook junos_command/pb.yml
ansible-playbook junos_command/pb.rpc.yml
```