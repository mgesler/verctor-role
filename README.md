vector-role
=========

Install Vector

Requirements
------------

—

Role Variables
--------------

- `vector_version`
- `vector_url_rpm`
- `vector_url_deb`
- `vector_config`

The value of variables can be changed/viewed in the file [defaults/main.yml](./defaults/main.yml).

Dependencies
------------

—

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:
```yaml
- name: Vector requirements
  src: git@github.com:mgesler/vector-role.git
  scm: git
  version: "1.2.1"
  name: vector

- name: Install Vector
  roles:
    - vector
```

License
-------

MIT

------------------

