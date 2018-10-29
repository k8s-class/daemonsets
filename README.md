```
$ kubectl create secret generic papertrail-destination --from-literal=papertrail-destination=syslog+tls://logsN.papertrailapp.com:XXXXX
$ kubectl create -f https://help.papertrailapp.com/assets/files/papertrail-logspout-daemonset.yml
```
