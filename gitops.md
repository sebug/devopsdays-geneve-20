# GitOps as a way to manage enterprise K8s and virtual machines: feedback!
Yann Albou, Sébastien Féré

## What is GitOps

### Declarative
The entire system is described declaratively.

### Git as Single Source of Truth
Declarative changes let you think of changes as *transactions*.

Changes by pull requests (more precise than a ticket, isn't it?)

### Kubernetes Operator
Approved changes to the desired state are automatically applied to the system.

### Continuous Observability
Software agents ensure correctness and alert on divergence.

## Pull and Push-based approach
Pull - Kubernetes fetches updates and applies them

Push - at the end of our build pipeline, launch continuous deployment by triggering the changes on the cluster.

## Experience Report
They decided against Helm Tiller to be safer (Tiller-less).

Multi-tenant makes Helm even harder.

Since they had other components to manage than just Kubernetes, they decided upon Ansible.

Trade-off between masking all implementation details to developers and letting them write the YAML themselves.

## Conclusions
Works in the Enterprise, had to stay with the push model because of the wish to control who updates when.

Had to adapt tooling to work with existing infrastructure.

White-listing images for the Docker registry, but don't forbid the devs to experiment (get any image onto the dev cluster, push to registry from your own machine).


