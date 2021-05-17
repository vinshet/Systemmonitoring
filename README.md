# Systemmonitoring

The services relevant to the node(s) that will host the zabbix server are
mysql-server
zabbix-server-mysql
zabbix-web-nginx-mysql

The services relevant to the node(s) that will send metrics to the server are
zabbix-agent

The node(s) that are intended to be zabbix server(s) are assigned node labels via
docker node update --label-add <key>=<value> NODE
  
Changes are to be made under the relevant services to change the key value pair
deploy:
  placement:
    constraints:
      - node.labels.<key> == <value>


