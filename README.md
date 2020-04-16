# containers-ansible
* This branch is for CVP only. Stable tests are moved from master branch.
* For rhel7 containers, docker and atomic should be installed in the system, since the scan feature is wanted.
* No inventory file included

# requirements:
- ansible: 2.6

# Usage:
`ansible-playbook -i $inventory $container.yml -e image_fullname=$img_fn`
