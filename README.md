# ansible-role-ndi-da
Ansbile role for running Nexus Dashboard Insights - Post-Change Delta Analysis jobs 

Use the following in the collection requirements.yml file

https://galaxy.ansible.com/docs/using/installing.html

```yaml
---
roles:
  - name: ndi-da
    src: https://github.com/cisco-apjc-cloud-se/ansible-role-ndi-da
    version: main
    scm: git
```

Execute the role as a play with host/inventory and customised variables

```yaml
- name: Initiate Nexus Dashboard Insights - Post-Change Delta Analysis
  hosts: nd
  gather_facts: false
  vars:
    insights_group: MEL-SE-LAB-ACI
    job_name: ANSIBLE-CICD-POST-DA
    site_name: MEL-SE-LAB-ACI
  roles:
    - role: ndi-da
```