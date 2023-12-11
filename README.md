# ansible-roles

Various Ansible roles.

## GoAccess

Limitation: the role currently only supports Debian/Ubuntu systems.

## OAuth2 Proxy

https://oauth2-proxy.github.io/oauth2-proxy/

The OAuth2 Proxy role is written to install/support multiple instances of
OAuth2 Proxy. It can be used as follows:

```
# playbook.yml
---
- hosts: ...
  roles:
    - ...
    - role: oauth-proxy
      oauthproxy_name: example-one
      oauthproxy_config: "{{ playbook_dir }}/files/www.example.com/oauth2-proxy-example-one.cfg"
    - role: oauth-proxy
      oauthproxy_name: example-two
      oauthproxy_config: "{{ playbook_dir }}/files/www.example.com/oauth2-proxy-example-two.cfg"
  vars:
    ...
```
