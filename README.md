Vector
=========

Роль предназначена для установки и настройки ПО Vector для сбора и отправки логов.


Role Variables
--------------

| variables | description |
|--------|-----------|
| vector_version | версия устанавляемого ПО |


Example Playbook
----------------
```
- name: Install Vector
  hosts: all
  roles:
    - vector-role
```

Author Information
------------------

Midzaru2011
