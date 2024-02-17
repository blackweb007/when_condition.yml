# when_condition.yml
- name: condition
  hosts: all
  tasks:
    - name: Pls print centos, when condition met
      debug:
        msg: "this is centos"
      when: ansible_os_family== "RedHat" and ansible_distribution_version == "6.1"
    - name: Pls print ubuntu, when condition met
      debug:
        msg: "this is ubuntu"
      when: ansible_os_family== "Debian"
