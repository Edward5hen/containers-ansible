# containers-ansible
* using ansible to test container images: rsyslog, support-tools, sadc, rhel-tools, net-snmp, ubi-init/rhel-init, etcd, flannel, ubi base and ubi minimal base images.
* podman needs to be installed
* prepare a local inventory file by inv_template.yml

# requirements:
- ansible: 2.6
- snmpgetnext: For the reference, it provides by net-snmp-utils in fedora 37

# Usage:
`ansible-playbook -i $inventory $container.yml -e image_fullname=$img_fn`
