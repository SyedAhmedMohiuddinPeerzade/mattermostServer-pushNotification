# mattermostServer-pushNotification

An attempt is made to integrate mattermost server app and push notification plugin for android.

## How to deploy
make sure docker, kubernetes and helm are configured
replace the value of AndroidApiKey in secret.yaml

```bash
cd $PWD/kubernetes/charts/mattermost-deployment
helm package mattermost-deployment
helm install mattermost-deployment-0.0.1.tgz
```
