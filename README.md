Ansible Role: Docker Environment
=========

Setup docker daemon environment variables on Linux.

Requirements
------------

Docker installed.

Role Variables
--------------

`docker_envs`: Environments dict(map) for docker daemon.

Dependencies
------------

None.

Example Playbook
----------------

```yml
- hosts: servers
  vars:
    docker_envs:
      http_proxy: http://example.com:8080
      https_proxy: http://example.com:8081
      no_proxy: localhost,127.0.0.1,example.com,.example.com
  roles:
    - { role: djx339.docker-env }
```

License
-------

BSD

Author Information
------------------

This role was created by [Daniel D](https://github.com/djx339).
