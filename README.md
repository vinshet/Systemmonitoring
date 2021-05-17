# Systemmonitoring
<pre>
The services relevant to the node(s) that will host the zabbix server are<br />
mysql-server<br />
zabbix-server-mysql<br />
zabbix-web-nginx-mysql<br />

The services relevant to the node(s) that will send metrics to the server are<br />
zabbix-agent<br />

The node(s) that are intended to be zabbix server(s) are assigned node labels via<br />
docker node update --label-add [key]=[value] NODE<br />
  
Changes are to be made under the relevant services to change the key value pair<br />
deploy:<br />
  placement:<br />
    constraints:<br />
      - node.labels.[key] == [value]<br />
</pre>
