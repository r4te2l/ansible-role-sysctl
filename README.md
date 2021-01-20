sysctl
=========

Manages kernel parameters

Requirements
------------

N/A

Role Variables
--------------

:
:

| variable        | Purpose                                | Default                        |
| --------------- | -------------------------------------- | ------------------------------ |
| `sysctl_params` | Dictionary of sysctl parameters        | {}                             |
| `sysctl_file`   | Full path to sysctl configuration file | '/etc/sysctl.d/98-sysctl.conf' |

Dependencies
------------

N/A

Example Playbook
----------------

```yaml
    - hosts: servers
      roles:
         - { role: sysctl }
      vars:
        sysctl_params:
          net.ipv4.ip_forward: 1
          net.ipv6.conf.all.forwarding: 1

```

License
-------

BSD
