zabbix\_agent
=========

Install zabbix agent on RHEL based and Windows systems.

Requirements
------------

The Windows section assumes you have your agent executable in an accessible fileshare on the network.

Role Variables
--------------

Most important variables to set are related to Windows install which would be the directory you wish to install zabbix in and where the zabbix zip is located on the network. 

Zabbix server address and ip also should be supplied.

Dependencies
------------

None

Example Playbook
----------------


    - hosts: servers
      roles:
         - role: zabbix_agent 
           zabbix_win_zip_src: \\path\to\zip 
           zabbix_win_dir: C:\zabbix
           zabbix_win_src_zip: \\path\to\exe
           zabbix_server_ip: 10.0.0.100
           zabbix_server: zabbix.company.com
           zabbix_port: 10050
           zabbix_host_metadata: system.uname

License
-------

GPLv3
