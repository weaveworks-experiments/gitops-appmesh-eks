# gitops-appmesh-eks

A progressive delivery GitOps pipeline powered by [Weave Cloud](https://weave.works) and [AWS App Mesh](https://aws.amazon.com/app-mesh/)

![GitOps overview diagram](https://raw.githubusercontent.com/weaveworks-experiments/gitops-appmesh-eks/master/docs/diagrams/weave-cloud-appmesh-eks.png)

Weave Cloud progressive delivery components:

* [Flux](https://github.com/weaveworks/flux): GitOps Kubernetes Operator
    * syncs YAMLs and Helm charts between git and clusters 
    * scans container registries and deploys new images 
* [Flagger](https://github.com/weaveworks/flagger): Progressive Delivery Kubernetes Operator
    * automates the promotion of canary deployments 
    * uses App Mesh routing for traffic shifting and Prometheus metrics for canary analysis
* [Cortex](https://github.com/cortexproject/cortex): Prometheus-as-a-service CNCF project
    * multi-tenant, horizontally scalable Prometheus
    * powers Weave Cloud observability features 

![Weave Cloud Canary UI](https://raw.githubusercontent.com/weaveworks-experiments/gitops-appmesh-eks/master/docs/screens/weave-cloud-canary-ui.png)

