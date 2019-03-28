# Render Jinja2 Template via Ansible

Simple example on how to render a jinja2 template using Ansible\
***Template is rendered locally so no network communication occurs***

`ansible-playbook -i hosts render-jinja.pb.yml`

```
PLAY [device1] ************************************************************************************************************************************

TASK [Build config from template] *****************************************************************************************************************
changed: [device1]

PLAY RECAP ****************************************************************************************************************************************
device1                    : ok=1    changed=1    unreachable=0    failed=0

$ ls
host_vars		hosts			output.conf		render-jinja.pb.yml	template.j2
$ more output.conf
data vlan is 100
voice vlan is 200
data vlan is 101
voice vlan is 201

value of a.b.c is 1
```
