# Go to papertrailapp.com and sign up for the free tier

### This captures all logs from stdout 
```
$ kubectl create secret generic papertrail-destination --from-literal=papertrail-destination=syslog+tls://logsN.papertrailapp.com:XXXXX
$ kubectl create -f https://help.papertrailapp.com/assets/files/papertrail-logspout-daemonset.yml
```
### If you want to capture systems and docker logs

- edit the file fluentd-daemonset-papertrail.yaml
- kubectl create -f fluentd-daemonset-papertrail.yaml


### If you want to capture logs on the master servers add this to the spec.template.spec section.

```
tolerations:
- key: node-role.kubernetes.io/master
  effect: NoSchedule
```

### Setup papertrail cli

```
sudo apt-get install ruby
sudo gem install papertrail
export PAPERTRAIL_API_TOKEN='asdfasdfasdfasdf'
papertrail
```
