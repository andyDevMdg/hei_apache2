# Create server Web automatically on Apache2 from a list of domain name using Ansible

The list of domain name should be provide as a text in this form:

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
