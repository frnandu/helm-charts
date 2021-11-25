# Flitz Technologies [Helm](https://helm.sh) Charts

This respoitory contains [Helm](https://helm.sh) charts for the following projects:

* [LNDHub](charts/lndhub)
* [LND](charts/lnd) (copy of [Fold's chart](https://github.com/fold-team/helm-charts/tree/master/charts/lnd))
* [C-Lightning](charts/c-lightning)


The workflow will package all these charts on push, and upload them to S3.

To fetch and install the charts, install the Helm S3 plugin:

```
helm plugin install https://github.com/hypnoglow/helm-s3.git
helm repo add flitz-helm-charts s3://flitz-helm-charts/charts
helm install lnd flitz-helm-charts/lnd
```