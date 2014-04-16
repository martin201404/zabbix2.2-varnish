zabbix2.2-varnish
=================

zabbix2.2 varnish Template

cat /etc/zabbix/zabbix_agentd.d/varnish_params.conf
UserParameter=varnish.stat[*],(test -f /usr/bin/varnishstat && varnishstat -1 -f $1 | awk '{print $$2}')
