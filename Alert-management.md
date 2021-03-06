# :horse: Alert Manager

## Alert event flow overview      
<p align="center" >
<img width=700 src="https://github.com/moreal70/IBM-Cloud-Private-useful-infomation/blob/master/images/alert-process.jpg">
</p>

- alert manager pod is located on Management node
<p align="center" >
<img width=700 src="https://github.com/moreal70/IBM-Cloud-Private-useful-infomation/blob/master/images/alert-manager-pod.jpg">
</p>

- list of configmap which should be updated
<p align="center" >
<img width=700 src="https://github.com/moreal70/IBM-Cloud-Private-useful-infomation/blob/master/images/alert-manager-configmap.jpg">
</p>

- check the current settings
<p align="center" >
<img width=700 src="https://github.com/moreal70/IBM-Cloud-Private-useful-infomation/blob/master/images/alert-manager-portal.jpg">
</p>

- how to set up alert	https://developer.ibm.com/recipes/tutorials/setting-up-system-alerts-in-an-ibm-cloud-private-environment/
- config map	https://www.ibm.com/support/knowledgecenter/SSBS6K_3.1.0/manage_metrics/monitoring_service.html
- alert rule	https://github.com/ibm-cloud-architecture/CSMO-ICP/tree/master/prometheus/alerts_prometheus2.x

## example yaml
- alert manager https://github.com/moreal70/IBM-Cloud-Private-useful-infomation/blob/master/files/alert-manager.yaml    
- alert rule https://github.com/moreal70/IBM-Cloud-Private-useful-infomation/blob/master/files/alert-rule.yaml

## Webhook for snmp trapper
- snmp	https://github.com/chrusty/prometheus_webhook_snmptrapper
- snmp trapper 	https://github.com/ibm-cloud-architecture/CSMO-ICP/tree/master/prometheus/alertmanager_to_snmp

## CEM
- CEM dashboard	https://devcluster.icp/cemui/administration
- icp set up	https://medium.com/@niklaushirt/ibm-cloud-private-alerting-with-prometheus-bc01e2f9b518
- icp set up	https://github.com/niklaushirt/alertmanager_configuration
- CEM manual	https://www.ibm.com/support/knowledgecenter/en/SSURRN/com.ibm.cem.doc/em_prometheus.html

## Remarks
- parameter	https://www.robustperception.io/whats-the-difference-between-group_interval-group_wait-and-repeat_interval  
~~~
In this blogpost we try and clear up some confusion by outlining the key differences between commonly confused
alerting configuration options: group_interval, group_wait, and repeat_interval.

Before digging into these 3 Alertmanager configuration options, let's recap on some Prometheus alerting basics.
Prometheus itself has two global clocks: scrape_interval and evaluation_interval.
~~~
- need to change the parameter for alert catch up time settings  
<p align="center" >
<img width=700 src="https://github.com/moreal70/IBM-Cloud-Private-useful-infomation/blob/master/images/alert-manager-config.jpg">
</p>

- amtool	https://github.com/prometheus/alertmanager/blob/master/README.md
