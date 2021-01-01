To run the ansible playbook
Edit the hosts file to point to your local machine (Ansible server), and remote
machine the tools are to be deployed to by the ansible-playbook.

#Local Host
[myansible]
192.168.0.xx

#Server the tools are to be deployed to
[toolpkgserver]
toolserver@192.168.0.xx


Command to run the playbook

~/AnsibleDeployment$ ansible-playbook DeploytoolsToRemoteServer.yaml 
 
How I Configured the remote machine to enable  ansible host to access the
toolserver@192.168.0.xx in the sudoers file
devops002 ALL=(ALL) NOPASSWD:ALL
devops002 ALL=(root) NOPASSWD:ALL


