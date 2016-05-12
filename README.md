# Ansible Role: Elasticsearch ELK stack

[![Build Status](https://travis-ci.org/bakhti/ansible-elk.svg?branch=master)](https://travis-ci.org/bakhti/ansible-elk) [![Ansible Galaxy](http://img.shields.io/badge/galaxy-bakhti.elk-660198.svg)](https://galaxy.ansible.com/list#/roles/1243)

Setup [Elasticsearch ELK Stack](http://www.elasticsearch.org/overview/) on Debian/Ubuntu linux servers.
New [Kibana (v4)](https://github.com/elasticsearch/kibana) is installed by this role. Please check [kibana3](https://github.com/bakhti/ansible-elk/tree/kibana3) branch if you need to setup ELK with [previous](https://github.com/elasticsearch/kibana/tree/kibana3) version of Kibana.

## Changelog

### 12/05/2016
 * Upgrade elasticsearch, logstash, and kibana versions.
 * Add support for beats input.
 * Ability to specify multiple configs via a variable.
 
### 26/10/2015
 * Upgrade elasticsearch and logstash versions
 * Change config variables in dicts to independent to make overriding simple.
 * Ability to supply TLS information.
 * Add support for log-courier input.
 * Add support for s3 output.

## Prerequisites
 * Requires `monit` to monitor processes.
 * Required `supervisord` to be installed (for Kibana). i.e.: [zenomaro.supervisord](https://galaxy.ansible.com/detail#/role/373/) 

## Required Variables
 * `elk_logstash_ssl_certificate` : SSL certificate used by input plugins.
 * `elk_logstash_ssl_key` : SSL key used by input plugins.

For other customizable variables, inspect `defaults/main.yml`

## License

MIT

## Author Information

This role was created in 2014 by [Bakhti Aripov](http://bakhti.github.io/).
This role was updated by [Rajitha Perera](http://git.io/rajiteh).
