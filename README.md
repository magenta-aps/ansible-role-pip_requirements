Pip Requirements
================

Setups a virtualenv and install dependencies into it.

Usage
-----

To utilize this role, add it to the `requirements.yml` file inside the ansible folder:

    - src: git+https://github.com/magenta-aps/ansible-role-pip_requirements.git
      version: master
      name: pip_requirements

Requirements
------------

Must be run against a `apt` capable system.

Role Variables
--------------

| Variable          | Default value         | Purpose                               |
| ----------------- | --------------------- | ------------------------------------- |
| `pip_req_path`    | `/vagrant/src`        | The path to the pip requirements file |
| `pip_req_file`    | `requirements.txt`    | The name of the pip requirements file |
| `virtualenv_path` | `/home/vagrant/venv/` | The path to setup our virtualenv to   |

Dependencies
------------

Depends on:
* [ansible-role-python](https://github.com/magenta-aps/ansible-role-python)

Example Playbook
----------------

    - hosts: all
      roles:
         - pip_requirements
      vars:
        pip_req_path: /vagrant/src/code/

License
-------

MPLv2

Author Information
------------------

skeen - Emil Madsen
