# Consuming Trusted Content from Tanzu Application Catalog (VMworld 2020)

This is a quick info with additional resources for the VMworld 2020 session about Tanzu Application Catalog.

## Demos
Some useful commands used during my session.

### Consume TAC Demo content from the command line
```
$ gcloud container images list-tags gcr.io/sys-2b0109it/demo/bitnami/redis
$ docker image pull gcr.io/sys-2b0109it/demo/bitnami/redis-sentinel@sha256:1dca243cbc088c4f89dba4cad203d2277702c626b14463b08d23ec525837701e
$ curl https://charts.trials.tac.bitnami.com/demo/index.yaml
$ helm repo add tac https://charts.trials.tac.bitnami.com/demo
$ helm repo list
$ helm search repo tac
$ helm fetch tac/redis
$ shasum -a 256 redis-10.8.1.tgz
$ helm install jenkins tac/jenkins -n your-namespace
```

### TAC cli

```
tac login
tac config
tac get apps --asset-type chart| less
tac metadata fetch --asset-id 8cebcee0ce35ca9d85f8bffd4a4c705cc770f15a # kafka
tac metadata fetch --digest sha256:a33c4044cdc574ad6f93dc8123ca672f392177eed75d951ba2cc086271faf55f > a.json
tac metadata artifacts a.json
tac metadata verify a.json
```

## TAC Documentation
- [Tanzu Application Catalog Documantation](https://docs.bitnami.com/tanzu-application-catalog/)
- [How To Use And Consume Trusted Content In Your Organization With VMware Tanzu Application Catalog](https://docs.bitnami.com/tanzu-application-catalog/get-started-tanzu-application-catalog/)
  - in your Local Machine
  - through Kubeapps
  - through Google Container Registry
  - through a private repository: Harbor
  
 ## Kubeapps
 - [2.0beta released](https://github.com/kubeapps/kubeapps/releases/tag/v2.0.0-beta.2)
 - [What is Kubeapps](https://liveandletlearn.net/post/what-is-kubeapps/) - great post and demo video from Michael.
 - [Kubeapps on a TKG Management Cluster](https://liveandletlearn.net/post/kubeapps-on-tkg-management-cluster/)
 - [VMware Tanzu Kubernetes Grid (TKG) with OpenID Connect - First Experience](https://liveandletlearn.net/post/tanzu-kubernetes-grid-tkg-first-experience/)
 
 
  
