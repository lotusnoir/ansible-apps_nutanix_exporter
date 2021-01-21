# Ansible Role: ansible-apps_nutanix_exporter

## Description

[![Build Status](https://travis-ci.com/lotusnoir/ansible-apps_nutanix_exporter.svg?branch=master?style=flat)](https://travis-ci.com/lotusnoir/ansible-apps_nutanix_exporter)
[![License](https://img.shields.io/badge/license-Apache--2.0-brightgreen?style=flat)](https://opensource.org/licenses/Apache-2.0)
[![Ansible Role](https://img.shields.io/badge/galaxy-apps_nutanix_exporter-purple?style=flat)](https://galaxy.ansible.com/lotusnoir/apps_nutanix_exporter)
![GitHub repo size](https://img.shields.io/github/repo-size/lotusnoir/ansible-apps_nutanix_exporter?color=orange&style=flat)
![Ansible Quality Score](https://img.shields.io/ansible/quality/52300)
[![downloads](https://img.shields.io/ansible/role/d/52300)](https://galaxy.ansible.com/lotusnoir/apps_nutanix_exporter)
[![Version](https://img.shields.io/github/release/lotusnoir/ansible-apps_nutanix_exporter.svg)](https://github.com/lotusnoir/ansible-apps_nutanix_exporter/releases/)
[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_nutanix_exporter&metric=alert_status)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_nutanix_exporter)
[![Maintainability Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_nutanix_exporter&metric=sqale_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_nutanix_exporter)
[![Reliability Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_nutanix_exporter&metric=reliability_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_nutanix_exporter)
[![Security Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_nutanix_exporter&metric=security_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_nutanix_exporter)

Deploy [nutanix_exporter](https://github.com/JacobCalmes/nutanix-exporter) to expose nutanix metrics to prometheus.

## Role variables

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| `nutanix_exporter_version` | 0.3.2 | nutanix_exporter version |
| `nutanix_exporter_config_dir` | /etc/nutanix_exporter | directory to install config file |
| `nutanix_exporter_install_dir` | /usr/local/bin | directory to install binary |
| `nutanix_exporter_force_install` | false | force install variable |
| `nutanix_exporter_listen_port` | 9110 | port to expose prometheus metrics |
| `prism_user` | admin | prism user |
| `prism_password` | "" | prism password |

## Examples

	---
	- hosts: apps_nutanix_exporter
	  become: yes
	  become_method: sudo
	  gather_facts: yes
	  roles:
	    - role: ansible-apps_nutanix_exporter
	  environment: 
	    http_proxy: "{{ http_proxy }}"
	    https_proxy: "{{ https_proxy }}"
	    no_proxy: "{{ no_proxy }}

## License

This project is licensed under Apache License. See [LICENSE](/LICENSE) for more details.
