ansible-role-nginx-install
=========

NginxをNaxsi込みでインストールする

```bash
ansible-galaxy install git+https://github.com/a-tak/ansible-role-nginx-install.git -p ../roles
```

Requirements
------------

Role Variables
--------------

* naxsi_version
  * naxsiのgithubリリースページからバージョン確認して指定すること
    * https://github.com/nbs-system/naxsi/releases
* nginx_version
  * nginxのバージョンを確認して指定すること
    * https://nginx.org/en/download.html

inventory サンプル

```yaml:
all:
  hosts:
    hoge:
      ansible_host: xxx.xxx.xxx.xxx
      ansible_user: hogeuser
      naxsi_version: 0.56
      nginx_version: 1.16.1
```

Dependencies
------------

Example Playbook
----------------

```yaml
- hosts: all
  become: yes
  roles:
    - ../roles/ansible-role-nginx-install
```

License
-------

BSD

Author Information
------------------

