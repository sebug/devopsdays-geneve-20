# A multi cloud Service Mesh deployment in action
Denis Jannot

## Istio Architecture
Service A talks to proxy A, which talks to proxy B which talks to service B (each pod has a proxy).

With Istio, Ingress proxy is handled by Istio.

## Notes Demo
AWS Multi-site deployment.

Two Kubernetes clusters set up with [Konvoy](https://d2iq.com/solutions/ksphere/konvoy).

### Step: Create Istio on the first cluster
- Use the same set of certificates.

No point in creating your own APIs if you have CRDs

helm template install/kubernetes/helm/istio

[The doc for Istio install is here](https://istio.io/docs/setup/install/multicluster/)

In Istio you have another layer of DNS - istiocoredns

DNS server - if we have something ending in .global, forward the DNS request to the Istio DNS server.

Create a new ServiceEntry object -> DNS. Just want to resolve to the entry.

Example - using [Flagger](https://flagger.app) to progressively deploy.

