# Prometheus_ansible_role
## Description

[![Ansible Galaxy](https://img.shields.io/badge/galaxy-sbouii.prometheus_ansible-blue.svg)](https://galaxy.ansible.com/sbouii/prometheus_ansible/) 

[![Build Status](https://travis-ci.org/sbouii/prometheus_ansible.svg?branch=master)](https://travis-ci.org/sbouii/prometheus_ansible)

**[Prometheus](https://prometheus.io/)** is an open-source systems monitoring and alerting toolkit.
This is an ansible role for installing Prometheus on Debian and RedHat distributions. It doesn't handle the configuration aspect of Prometheus. As always I prefer to separe the installation and the configuration/monitoring aspect of a software for organizing purposes.It uses the infrastructure testing tool **[KitchenCi](http://kitchen.ci/)** to verify if the infrastructure is well setup and configured as expected.


