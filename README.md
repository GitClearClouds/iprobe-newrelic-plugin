NewRelic ClearClouds Plugin
The New Relic ClearClouds Plugin is published and supported by ClearClouds team. This plugin provides real-time network visibility from wire data that is typically unavailable from APM solutions. Currently the following metrics are recorded:

 

TCP

·       Throughput: Total, Inbound and Outbound

·       Latency：Client side, Server side

·       Close Status: FIN, TIMEOUT, RESET

·       New/Close connections : Requests per second

·       Retransmission Rate

·       Attack (count per second):SYN, Scan

HTTP

·       Traffic

·       Latency

·       Status Codes Count

·       Error Rate

·       Apdex: users' satisfaction rate on URL

Alerts

New Relic allows you to setup at most 5 metrics. For each of the metrics, you can set a caution threshold and a critical threshold signaled by different colors. Alert policies can be configured against those metrics. When an alert is trigged, New relic platform will not only display it on the GUI, but also inform you via an email or other ways based on your configuration. The alert frequency is once per 30 minutes. Below are the metrics:

·         Latency

·         Bytes

·         Error Rate

·         Apdex

·         Attack

 

 

Requirements

==============================================

The NewRelic ClearClouds Plugin need to be installed on the same appliance as the iProbe.

OS : CentOS6.2 64Bits or later

Software : Python 2.6 or later

 

Running and Installation

=====================================================

1.       Install plugin

a)          Download iprobe_newrelic_plugin.zip from https://github.com/GitClearClouds/iprobe_newrelic_plugin

b)          Enter the download directory

c)          Unzip iprobe_newrelic_plugin.zip

d)          cd iprobe_newrelic_plugin

e)          chmod -R 777 ./*

f)           sudo python setup.py install

 

2.       Configuration

Run the plugin only once:

iprobe_ plugin -d <datadir> -n <pluginid> -k <newrelickey>

<datadir> : your data directory

<pluginid> : your plugin name, generally server name

<newrelickey> : your license key from your New Relic account.

e.g :

iprobe_plugin -d /home/juyun/datafile -n ClearClouds -k 19e5cb7a2ec9c43a7a90cec3360fb7b5868d08d6

 

3.         Execute the plugin

iprobe_plugin -r

 

 

About Us : http://www.clearclouds.com/

Surport: https://github.com/gitclearclouds/iprobe-newrelic-plugin/issues

plugin Download: https://github.com/gitclearclouds/iprobe-newrelic-plugin
