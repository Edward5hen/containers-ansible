# containers-ansible
* using ansible to test container images: rsyslog, support-tools, sadc, rhel-tools, net-snmp, ubi-init/rhel-init, etcd, flannel, ubi base and ubi minimal base images.
* podman needs to be installed
* no inventory file included

# requirements:
- ansible: 2.6

# Usage:
`ansible-playbook -i $inventory $container.yml -e image_fullname=$img_fn`
