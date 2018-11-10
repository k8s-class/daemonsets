# Go to papertrailapp.com and sign up for the free tier


```
$ kubectl create secret generic papertrail-destination --from-literal=papertrail-destination=syslog+tls://logsN.papertrailapp.com:XXXXX
$ kubectl create -f https://help.papertrailapp.com/assets/files/papertrail-logspout-daemonset.yml
```
