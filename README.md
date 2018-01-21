# mattermostServer-pushNotification

An attempt is made to integrate mattermost server app and push notification plugin for android.

## How to build and deploy
make sure docker, kubernetes and helm are configured.

Replace the value of "android-api-key" and "apple-push-cert-password" in secret.yaml. Update "mattermost_production_priv.pem" then build and push docker image. Execute below commands to deploy.

```bash
cd $PWD/kubernetes/charts/mattermost-deployment
helm package mattermost-deployment
helm install mattermost-deployment-0.0.1.tgz
```
