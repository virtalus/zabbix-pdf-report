# Zabbix PDF Report

This instruction assumes you are using default zabbix installation which points on http://127.0.0.1/zabbix/

The following solution uses zabbix API which are located at http://127.0.0.1/zabbix/api_jsonrpc.php

After you complete the installation steps you we be able to access reporting tool on http://127.0.0.1/zbxreport/

Prepare git utility on RHEL/CentOS family
```
yum -y install git
```

Prepare git utility on Debian/Ubuntu family
```
apt -y install git
```

Install project
```
cd /usr/share
git clone https://github.com/catonrug/zabbix-pdf-report.git
```

Prepare access
```
cd /usr/share/zabbix-pdf-report
cp config.inc.php.dist config.inc.php
```

Create working dir
```
cd /usr/share/zabbix-pdf-report
./fixrights.sh
```

Install httpd directive
```
cp /usr/share/zabbix-pdf-report/zabbix-pdf-report.conf /etc/httpd/conf.d
```

Restart httpd
```
systemctl restart httpd
```

Make sure SELinux is off
```
setenforce 0
```

## To create link without authorization

http://127.0.0.1/zbxreport/chooser.php

# Related
https://www.zabbix.com/forum/showthread.php?t=24998
