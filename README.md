# mattermostServer-pushNotification

An attempt is made to integrate mattermost server app and push notification plugin for android.

## How to deploy
make sure docker, kubernetes and helm are configured.

Replace the value of "android-api-key" in secret.yaml, then execute below commands.

```bash
cd $PWD/kubernetes/charts/mattermost-deployment
helm package mattermost-deployment
helm install mattermost-deployment-0.0.1.tgz
```
