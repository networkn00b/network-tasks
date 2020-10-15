# Trunk Port Audit

This ansible playbook 'shutdown-trunk-ports' has been created to audit and disable all unused/inactive trunk ports on Cisco network access switches within a network.

# Objective

It gathers interface facts and verifies all interfaces with the status 'down'

It also matches on interfaces that have been configured with a description 'uplink', this can be removed or changed to something else.

There are many more interface values that can be matched on the conditional 'when' rule within the playbook.

# Requirements
To use this playbook you will need:
- Ansible 2.6+ installed on a Linux box
- SSH client
- Git installed on Linux

# Install and Setup
1. Logon to your Linux box
2. Execute the following to download playbook git clone https://github.com/networkn00b/network-tasks.git
3. cd ~/git/networkn00b
4. Move yaml files into folder containing your ansible installation
5. Update hosts file, under mysite include hostnames/IPs of devices being targetted
6. Update network_cli with credentials to access devices
7. If required, Update shutdown-trunk-ports.yml file  with description of interfaces being targetted
8. Execute playbook ansible-playbook shutdown-trunk-ports.yml -C -V to check config of playbook and expected result
9. Execute playbook without check mode to proceed to disable interfaces - ansible-playbook shutdown-trunk-ports.yml




