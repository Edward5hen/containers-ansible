# containers-ansible
* using ansible to test container images: rsyslog, support-tools, sadc, rhel-tools, net-snmp, ubi-init/rhel-init, etcd and flannel
* no inventory file included

# status:
*Being developed*

# requirements:
- ansible: 2.6
- python: 2.7

# Usage:
`ansible-playbook -i $inventory $container.yml -e image_fullname=$img_fn`
