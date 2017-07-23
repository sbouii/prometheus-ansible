# Prometheus_ansible_role
## Description

[![Ansible Galaxy](https://img.shields.io/badge/galaxy-sbouii.prometheus_ansible-blue.svg)](https://galaxy.ansible.com/sbouii/prometheus_ansible/) 

[![Build Status](https://travis-ci.org/sbouii/prometheus_ansible.svg?branch=master)](https://travis-ci.org/sbouii/prometheus_ansible)

**[Prometheus](https://prometheus.io/)** is an open-source systems monitoring and alerting toolkit.
This is an ansible role for installing Prometheus on Debian and RedHat distributions. It doesn't handle the configuration aspect of Prometheus. As always I prefer to separe the installation and the configuration/monitoring aspect of a software for organizing purposes.It uses the infrastructure testing tool **[KitchenCi](http://kitchen.ci/)** to verify if the infrastructure is well setup and configured as expected.

## Requirements

### Software Requirements

- **Python 2.7** or higher

- **Ansible 2.0** or higher (can be easily installed via pip. E.g: sudo pip install ansible==2.0.0.2)

- **[Vagrant](https://www.vagrantup.com/) 1.7** or higher 

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

