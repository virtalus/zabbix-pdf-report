# Zabbix PDF Report

This plugin allows to generate reports of the physical infrastructure of each cluster, and through the Zabbix API to be able to generate reports in PDF format.

## Installation

Install project
```
cd /usr/share/zabbix/
git clone https://github.com/virtalus/zabbix-pdf-report.git
```

Create working dir
```
cd /usr/share/zabbix/zabbix-pdf-report
sh fixrights.sh
```

If you are using different credentials than user: Admin, password: zabbix, then set the right credentials
```
edit /usr/share/zabbix/zabbix-pdf-report/config.inc.php
```

Use url http://IP/zabbix-pdf-report
