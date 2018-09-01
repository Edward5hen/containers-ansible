# containers-ansible
* using ansible to test container images
* no inventory file included, target must be Atomic Host.

# status:
*Being developed*

# requirements:
- ansible: 2.6
- python: 2.7

# Usage:
`ansible-playbook -i $inventory $container.yml -e image_version=$version`
