# Various Ansible Playbooks
Generally these are intended to be run with the following command:
`ansible-playbook -i <INVENTORY FILE> -u <USERNAME> --ask-become-pass playbook.yml`

For basic configuration options variables are intended to be set in the inventory file using `[<inventory_item>:vars]`.

## Dependencies

The following apply to some but not all playbooks:

Ansible Galaxy Roles
- `geerlingguy.docker`
- `geerlingguy.pip`