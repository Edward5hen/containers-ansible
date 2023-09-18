# Documentation

- [**Overview**](#overview)
- [**Requirement**](#requirement)
- [**Known Issue**](#known-issue)
- [**Usage**](#usage)

## Overview

Project `containers-ansible` is designed for internal (Red Hat) layered image Errata Test.

## Requirement

- Ansible / ansible-core is necessary in your host (local) node.
  - Recommand Ansible 6 (ansible-core 2.13) +.
- Package net-snmp-utils installation in your host (local) node.
- Podman installations are necessary in your client (beaker) nodes.

## Known Issue

- Configuration of unsecurity repo in client nodes. TBD.
- Installations failures of podman in RHEL-7 client nodes. TBD.

## Usage

In your host (local) node, `ansible-playbook -i $inventory $target.yml -e image_fullname=$img_fn -e correct_version=$rhelVR -v`
$target.yml should be replaced to related playbooks.
$img_fn and $rhelVR should be found in internal (Red Hat) brew page.

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
