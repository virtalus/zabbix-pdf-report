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

API for Cluster Report:
curl 'http://IP/zabbix-pdf-report/createpdf.php?ReportType=host&HostID=10281&GraphsOn=yes&ReportRange=last&timePeriod=Month' \
  -H 'Connection: keep-alive' \
  -H 'Upgrade-Insecure-Requests: 1' \
  -H 'User-Agent: Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/85.0.4181.8 Safari/537.36' \
  -H 'Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9' \
  -H 'Referer: http://172.17.52.5/zabbix-pdf-report/chooser.php' \
  -H 'Accept-Language: es-US,es;q=0.9,en-US;q=0.8,en;q=0.7,es-419;q=0.6' \
  -H 'Cookie: zbx_sessionid=ef2698535a1f481a33cc511fbe5e319b; PHPSESSID=9tb18j9lhvdl3nf4fldj0cud5s; tab=0' \
  --compressed \
  --insecure
