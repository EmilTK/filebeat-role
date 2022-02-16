Filebeat-role
=========

Данная роль предназначена для установки Filebeat и сбора системных метрик о хосте в учебных целях.

Requirements
------------

  * Ansible > 2.9
  * Elasticsearch instance
  * Kibana instance

Role Variables
--------------

  variable | Description | Default
 --- | --- | ---
 filebeat_version | Устанавливаемая версия Filebeat | 7.14.0
 filebeat_install_type | Тип установки | remove
 elastic_instance | Адрес инстанса Elasticsearch | IPv4 хоста `el-instance` при наличии такого в инвентари, в случае его отсутствия - `0.0.0.0`
 kibana_instance | Адрес инстанса Kibana | IPv4 хоста `k-instance` при наличии такого в инвентари, в случае его отсутствия - `0.0.0.0`


Example Playbook
----------------

``` yml
- name: Install Filebeat
  hosts: filebeat
  roles:
    - filebeat
```

License
-------

MIT

Author Information
------------------

Emil Temerbulatov - студент курса DevOps Netology