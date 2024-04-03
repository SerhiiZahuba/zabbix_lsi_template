**Description**

forked from mykolq/zabbix_lsi_template

This template is for discovering and monitoring LSI based 
(Avago, Broadcom, Perc, Lenovo) storage controllers by
using json outputs of storcli tool. 
Now it works only with zabbix => 6.2

**Main features**
Discovery of controllers, logical discs, physical discs, batteries (bbu and cv) without scripts on agent side (it uses parsing of json and javascript preprocessing on zabbix server side)
Monitoring controllers, logical, physical discs, batteries
Useful with OS, where storcli64 works
Overrides for reducing non supported items
Comfortable changing of time intervals by macroses.