# Ansible Role: ansible-apps_nutanix_exporter

## Description

[![Build Status](https://travis-ci.com/lotusnoir/ansible-apps_nutanix_exporter.svg?branch=master)](https://travis-ci.com/lotusnoir/ansible-apps_nutanix_exporter)[![License](https://img.shields.io/badge/license-MIT%20License-brightgreen.svg)](https://opensource.org/licenses/MIT)[![Ansible Role](https://img.shields.io/badge/ansible%20role-apps__nutanix_exporter-blue)](https://galaxy.ansible.com/lotusnoir/ansible-apps_nutanix_exporter/)[![GitHub tag](https://img.shields.io/badge/version-latest-blue)](https://github.com/lotusnoir/ansible-apps_nutanix_exporter/tags)

Deploy [nutanix_exporter](https://github.com/JacobCalmes/nutanix-exporter) to expose nutanix metrics to prometheus.

## Role variables

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| `nutanix_exporter_version` | 0.3.2 | nutanix_exporter version |
| `nutanix_exporter_listen_port` | :9110 | port to expose prometheus metrics |
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

This project is licensed under MIT License. See [LICENSE](/LICENSE) for more details.
