**Description**

forked from mykolq/zabbix_lsi_template

**Main changes:**
1. Raid monitoring in ESXI
2. Connecting to ESXI via a key (ssh)
3. Getting metrics via ssh.


This template is for discovering and monitoring LSI based 
(Avago, Broadcom, Perc, Lenovo) storage controllers by
using json outputs of storcli tool 
Now it works only with zabbix => 6.2

**Main features**
Discovery of controllers, logical discs, physical discs, batteries (bbu and cv) without scripts on agent side (it uses parsing of json and javascript preprocessing on zabbix server side)
Monitoring controllers, logical, physical discs, batteries
Useful with OS, where storcli64 works
Overrides for reducing non supported items
Comfortable changing of time intervals by macroses.

**FAQ**
1. Install StorCli to ESXI host, like this
   esxcli software vib install -v /vmfs/volumes/datastore/storcli.vib --no-sig-check
2. Setup to access from you zabbix-proxy or zabbix-server to ESXI server, like this
   cat /home/zabbix/.ssh/id_rsa.pub | ssh root@esxi_ip 'cat >> /etc/ssh/keys-root/authorized_keys'
3. Restart ssh service on ESXI server