# gitops-appmesh-eks

A progressive delivery GitOps pipeline powered by Weave Cloud

![GitOps overview diagram](https://raw.githubusercontent.com/weaveworks-experiments/gitops-appmesh-eks/master/docs/diagrams/weave-cloud-appmesh-eks.png)

Weave Cloud progressive delivery components:

* Flux: GitOps Operator
    * syncs YAMLs and Helm charts between git and clusters 
    * scans container registries and deploys new images 
* Flagger: Progressive Delivery Operator
    * automates the promotion of canary deployments using App Mesh routing for traffic shifting and Prometheus metrics for canary analysis
* Cortex: Prometheus-as-a-service
    * multi-tenant, horizontally scalable Prometheus that powers Weave Cloud observability features 

![Weave Cloud Canary UI](https://raw.githubusercontent.com/weaveworks-experiments/gitops-appmesh-eks/master/docs/screens/weave-cloud-canary-ui.png)

