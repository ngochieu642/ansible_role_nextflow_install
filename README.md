Role Name: Nextflow install
=========

An Ansible run that install SDKMan & Nextflow + nftest

Requirements
------------

- None

Role Variables
--------------
- `nextflow_install_sdkman_path`: "/opt/sdkman"
  - Path for SDKMan install

- `nextflow_install_nextflow_version`: "v25.04.4"
  - Version of nextflow to install

- `nextflow_install_java_version`: "17.0.6-amzn"
  - Version of Java to install

- `nextflow_install_nf_test_version`: "0.8.4"
  - Version of nf-test to install

Dependencies
------------

None

Example Playbook
----------------

```yaml
- name: Install Nextflow & nf-test
  hosts: my_vm
  become: yes
  vars:
    users:
      - name: "{{ ansible_user }}"
  roles:
    - role: nextflow_install
      nextflow_install_users: "{{ users }}"
      nextflow_install_nextflow_version: "v25.04.4"
```

License
-------

MIT

Author Information
------------------

Created in 2024 by ngochieu642
