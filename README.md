## Overview

Project `containers-ansible` is designed for internal layered image Errata Test.
Currently, project includes rsyslog, support-tools, sadc, rhel-tools, net-snmp, ubi-init/rhel-init, etcd, flannel, ubi base and ubi minimal base images.

## Requirement

- Ansible / ansible-core is necessary in your main (local) node.
- Podman is necessary in your worker (beaker) node(s).
 - If your worker (beaker) nodes are RHEL-7, please use subscription-manager to book related repos based on different platforms.
- Add above worker nodes hostname / ip to `inventory` file.

## Known Issue

- Unsecurity repo task failure
- Container size failure
- Parts of task ignore

## Usage

Run in your main (local) node `ansible-playbook -i $inventory $container.yml -e image_fullname=$img_fn -e correct_version=$rhelVR -v`

$container.yml should be replaced to related playbooks under containers-ansible folder.
$img_fn should be replaced to internal brew page.
$rhelVR should be replated to version.release.

|**Playbook Name**|**Platform**|**Errata Task**|
|---|---|---|
|rhel_tools.yml|(RHEL-7 / 8 / 9)|Red Hat Enterprise Linux x.x.x rhel-tools Container Image|
|sadc.yml|(RHEL-7 / 8 / 9)|Red Hat Enterprise Linux x.x.x sadc Container Image|
|ubi_init.yml|(RHEL-7 / 8 / 9)|Red Hat Universal Base Image x Init Container Image |
|rhel_init.yml|(RHEL-7)|Red Hat Enterprise Linux 7.x rhel7-init Container Image|
|ubi7-minimal.yml|(RHEL-7) |WIP|
|ubi8.yml| (RHEL-8) | WIP|
|rhel7-atomic.yml| (RHEL-7) |WIP|
|etcd.yml|(RHEL-7 / 8 / 9)|WIP |
|net_snmp.yml|(RHEL-7 / 8 / 9)|WIP|
|rhel7.yml| (RHEL-7)| WIP|
|support_tools.yml|(RHEL-7 / 8 / 9)|WIP |
|ubi7.yml| (RHEL-7)| WIP|
|flannel.yml|(RHEL-7 / 8 / 9)|WIP|
|podman-in-podman.yml|(RHEL-7 / 8 / 9)|WIP |
|rsyslog.yml|(RHEL-7 / 8 / 9)|WIP |
|ubi8-minimal.yml| (RHEL-8)| WIP|
