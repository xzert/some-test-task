Common OS
=========

Common role for bootsrtaping new working server

Requirements
------------

nothing special

Role Variables
--------------

* `common_os_allow_reboot`: `boolean`, allow reboot during tasks execution
* `common_os_cpu_optimize_cstates`: `boolean`, enable or disable cstates optimizing (sanitaized)
* `common_os_cpu_max_cstate`: maximum allowed cstate level. 0 for disable
* `common_os_cpu_optimize_performance_level`: `boolean` enable or disable cpu power performance policy optimization (sanitaized)
* `common_os_cpu_performance_level`: `string` name of policy that's would be applied to cpu cores
* `common_os_cpu_performance_levels_list`: `list` - whitelist of policies available
* `common_os_primary_network_interface_name`: `string` target name for primary interface
* `common_os_packages`: `list` - list of packages will be installed to system
* `common_os_ecrypt_changes`: `boolean` enable or disable part with disk encryption (sanitized)
* `common_os_encrypt_disk_key`: `rsa4096` key for partions(disks) encryption with luks2, should be encrypted. May be generated with `openssl genrsa 4096` command
* `common_os_encrypt_disks`: `list of dicts` - list with names and params of partitions for encryption. `name` and `device` minimum required, other options passed for ansible `community.crypto.luks_device` module

Sanitized values can be changed during vars sanity check for fail prevention.

Dependencies
------------

nothing special

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

  vars:
    common_os_allow_reboot: true
    common_os_primary_network_interface_name: "net0"
    common_os_encrypt_disks:
      - name: firstencrypt
        device: "/dev/xvdf"
      - name: scndpartencrypt
        device: "/dev/xvda14"

    - hosts: servers
      roles:
         - common_os_role
      vars:
        common_os_allow_reboot: true
        common_os_encrypt_disks:
          - name: encdisk
            device: "/dev/sdb"

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
