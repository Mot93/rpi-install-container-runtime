Role Name
=========

The purpose of this ansible role is to instal a container runtime on a raspberry pi

Requirements
------------

In order to use this role you need to install the community.general.modprobe plugin
You need root privileges to run this script.

    become: yes


Role Variables
--------------

The variable runtime can either be "docker" or "containerd", the default runtime is "docker". 
Hopefully in future even cri-o will be supported.

Example Playbook
----------------

Out of the box solution:

``` YAML
---
- hosts: dramble
  become: yes
  roles:
    - rpi-install-container-runtime
      vars: 
```

Specifying the runtime:

``` YAML
---
- hosts: dramble
  become: yes
  roles:
    - rpi-install-container-runtime
      vars: 
        runtime: "containerd"
```

License
-------

MIT

Author Information
------------------

If you like my work and whant to know more, visit my website:
[www.mattiarubini.com](https://www.mattiarubini.com)
