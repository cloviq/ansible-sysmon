sysmon
=========

This role is intended to be used for all Windows hosts that should be capturing sysmon data for security purposes.

Requirements
------------

This requires that each windows host have PSCX to unzip the sysmon package.

Role Variables
--------------

These variables can be set:
     
    sysmon_dir: C:\Windows
    sysmon_zip: Sysmon.zip
    sysmon_state: present
    sysmon_config_dir: /tmp
    sysmon_config: sysmonconfig.xml

Dependencies
------------

N/A

Example Playbook
----------------

Example playbook that also calls the compile-sysmon role:

     - name: Compile sysmon
       hosts: sysmon_compile
       roles:
         - compile-sysmon

     - name: Install sysmon
       hosts: windows
       roles:
         - sysmon

License
-------

GPL

Author Information
------------------

Reach out to Splunk Professional Services.
