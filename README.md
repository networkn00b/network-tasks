# network-tasks

This ansible playbook 'shutdown-trunk-ports' has been created to audit and disable all unused/inactive trunk ports on Cisco network access switches within a network.

It gathers interface facts and verifies all interfaces with the status 'down'

It also matches on interfaces that have been configured with a description 'uplink', this can be removed or changed to something else.

There are many more interface values that can be matched on the conditional 'when' rule within the playbook.
