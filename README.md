Role Name
=========

This installs and lightly configures the OWASP ZAP Proxy project. 

Requirements
------------

java 8 runtime


Supported Systems
-----------------

Ubuntu 14.04

Should work anywhere that has a java 8 jre and supports init scripts

Role Variables
--------------

zap_user: zap
zap_group: zap
zap_user_home: /var/zap
zap_user_shell: /sbin/nologin
zap_jar_home: /opt
zap_version: 2.7.0
zap_java_path: /opt/jre1.8.0_151/bin/java
zap_dir: "{{zap_user_home}}"
zap_javaargs: ''
zap_pid_file: /var/run/zap.pid
zap_host: 0.0.0.0
zap_allowed_network: .*

Dependencies
------------

None

Example Playbook
----------------


    - hosts: zappers
      roles:
         - { role: java }
         - { role: zap }

License
-------

BSD

