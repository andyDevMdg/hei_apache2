# Create server Web automatically on Apache2 from a list of domain name using Ansible

## Prerequisite
- should be root user or have root privilege
- ssh should be installed on your server

## List of domain names
The list of domain names should be provide as a text in this form:

```sh
- www.hei.school
- back.hei.school
- front.hei.school
- api.hei.school
```

## Example
The "domains" variable should only be changed in the playbook

```sh
---
  - name: Installation de serveurs Web
    hosts: web
    remote_user: root
    vars:
      domains:
        - www.hei.school
        - back.hei.school
        - front.hei.school
        - api.hei.school
  
  roles:
    - apache2
...
```
