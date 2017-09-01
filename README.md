# Prometheus_ansible_role
## Description

[![Ansible Galaxy](https://img.shields.io/badge/galaxy-sbouii.prometheus_ansible-blue.svg)](https://galaxy.ansible.com/sbouii/prometheus_ansible/) 

[![Build Status](https://travis-ci.org/sbouii/prometheus_ansible.svg?branch=master)](https://travis-ci.org/sbouii/prometheus_ansible)

**[Prometheus](https://prometheus.io/)** is an open-source systems monitoring and alerting toolkit.
This is an ansible role for installing Prometheus on Debian and RedHat distributions. It doesn't handle the configuration aspect of Prometheus. As always I prefer to separe the installation and the configuration/monitoring aspect of a software for organizing purposes.It uses the infrastructure testing tool **[KitchenCi](http://kitchen.ci/)** to verify if the infrastructure is well setup and configured as expected.

## Requirements

### Software Requirements

- **Python 2.7** or higher

- **Ansible 2.2** or higher 

- **[Vagrant](https://www.vagrantup.com/) 1.9** or higher 

- **Virtualbox**

## Supported Systems

- Debian
- Ubuntu
- Centos

More infos in the role's metadata file.


### Dependencies

None.


## Role variables

- **`debian_prometheus_repositoy_filename`** - the filename of the kubernetes debian repository 
- **`redhat_prometheus_repositoy_name`** - a unique kubernetes redhat repository ID
- **`redhat_prometheus_repositoy_description`** - a description for the kubernetes redhat repository
- **`prometheus_port`** - grafana server port


## Available tags

- **`install-prometheus`** -  Default tag to perform grafana installation

## Usage

In order to set up a prometheus server across your plateform, start by checking out the role from Ansible galaxy:
```bash
ansible-galaxy install sbouii.prometheus_ansible
```

Finally call the role within you Ansible playbook:
```yaml
---
- hosts: localhost
  sudo: yes
  roles:
    - prometheus_ansible
```


Finally call the role within you Ansible playbook:
```yaml
---
- hosts: localhost
  sudo: yes
  roles:
    - prometheus_ansible
```


## Development and Testing
### Test with Vagrant
For quick tests, you can spin up a Debian VM using Vagrant. You maybe need to adapt the Vagrantfile to suit your environment (IP addresses, etc).

    $ vagrant up

### Run acceptance tests

For runing Acceptance/Integration tests against your role , we use the tool `test-kitchen`.All written acceptance tests are in the **./test/integration/** directory.

The `.kitchen.yml` file describes the testing configuration and the list of suite tests to run. By default, the instances will be converged with Ansible and ran in Vagrant virtual machines.

To list the instances:

    $ kitchen list

    Instance                    Driver   Provisioner      Verifier  Transport  Last Action
    default-debian-8-x64        Vagrant  AnsiblePlaybook  Busser    Ssh        <Not Created>
    ...

To run the default test suite, for instance, on a Ubuntu Trusty platform, run the following command:

    $ kitchen test default-ubuntu-1404-x64

## Author information

This role was created by [Mariem Sbouii](https://www.linkedin.com/in/mariem-sboui-76906711b) ,a DevOps enthusiast

