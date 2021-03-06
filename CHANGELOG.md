# Change Log
All notable changes to this project will be documented in this file.

## v3.7.0-37xx



## v3.7.0-3701

### Added

- Amazon Linux deployments are now supported ([#71](https://github.com/wazuh/wazuh-ansible/pull/71)) and for the old repository structure ([#67](https://github.com/wazuh/wazuh-ansible/pull/67))
- Added the option to add rule files and decoders directly over the local rule and decoder directories in /var/ossec/etc ([#81](https://github.com/wazuh/wazuh-ansible/pull/81)).
- Added the necessary variables to configure a new configuration template for the Wazuh API ([#80](https://github.com/wazuh/wazuh-ansible/pull/80)).
- Added the option to verify the shared configuration for agents set in the manager ([#76](https://github.com/wazuh/wazuh-ansible/pull/76)).
- Added the option to configure the active response ([#75](https://github.com/wazuh/wazuh-ansible/pull/75)).

### Changed

- Repository restructure.
- Extended conditions to register a Wazuh agent. Now will register the agent in cases where there is no client.keys or the file exists but this empty ([#79](https://github.com/wazuh/wazuh-ansible/pull/79)).
- Grouping of tasks in a block under the same condition to improve the efficiency of the code ([#74](https://github.com/wazuh/wazuh-ansible/pull/74)).
- Improved efficiency of the Java repository ([#73](https://github.com/wazuh/wazuh-ansible/pull/73)).

### Fixed

- Fix oracle java cookie ([#71](https://github.com/wazuh/wazuh-ansible/pull/71)).
- include the logall_json label in ossec.conf template. This was causing an error when recreating the cdb_lists ([#84](https://github.com/wazuh/wazuh-ansible/pull/84)).

## v3.6.0

Ansible starting point.

Roles:
 - Elastic Stack:
   - ansible-elasticsearch: This role is prepared to install elasticsearch on the host that runs it.
   - ansible-logstash: This role involves the installation of logstash on the host that runs it.
   - ansible-kibana: Using this role we will install Kibana on the host that runs it.
 - Wazuh:
   - ansible-filebeat: This role is prepared to install filebeat on the host that runs it.
   - ansible-wazuh-manager: With this role we will install Wazuh manager and Wazuh API on the host that runs it.
   - ansible-wazuh-agent: Using this role we will install Wazuh agent on the host that runs it and is able to register it.

