YC CLI role for Ansible
=========

Ansible role for Yandex.Cloud command-line interface (CLI)

Requirements
------------

-   Ubuntu 12.04+;
-   Ansible 2.4+

Role Variables
--------------
| Name                        | Default Value |  Description    |
|-----------------------------|-----|---------------------------|
| yc_config_user              | deplo | User for which config is generated |
| yc_token                    | - | Yandex.Cloud Token |
| yc_cloud_id                 | - | ID of the cloud to use when executing the command |
| yc_folder_id                | - | ID of the folder to use when executing the command |
| yc_compute_default_zone     | ru-central1-a | Default availability zone for the Yandex Compute Cloud service |


```yml
yc_config_user: deplo
yc_token: AAABBBCCCDDDEEEFFF
yc_cloud_id: aaabbbcccdddeeefff
yc_folder_id: aaabbbcccdddeeefff
yc_compute_default_zone: ru-central1-a

```
Installation
--------------
```
$ ansible-galaxy install teachbase-ansible.yc_cli
```

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: teachbase-ansible.yc_cli }

License
-------

MIT
