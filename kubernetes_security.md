# Kubernetes Security Jumpstart
Mafizur Rahman

## Parts
### Application Security
That's your problem.

### Container Security
No unknown base image.

Lock down versions

Update for vulnerability remediation (it's not just your code!)

Limited attack vector

### Image Security
Least privilege access

### Infrastructure Security
Don't expose underlying infrastructure

Metadata is more valuable than you think

Hardened nodes

Update regularly

### Network Security
Network Segmentations

Cluster Network Policies

### Runtime Kubernetes Security
RBAC - Role-Based Authentication Control

Define Quotas

Pod Resource Quotas

### Monitor and Log


### Admission Controllers


### Encrypt at Rest

## Tools

### Image Scanning and Analysis
Anchore, [Clair](https://github.com/quay/clair), Dagda, KubeXRay, Snyk, Trivy

### Runtime Security
Falco, AppArmor, Seccomp, Selinux, Sysdig OS

### Network Security
Aporeto (Commercial), Calico, Cilium, Tigera (Commercial), Trireme

### Secrets Management
Vault

### Image Distribution
Grafeas, In-toto, Portieris

### Security Audit
Kube-bench, Kube-hunter, Kubeaudit, Kubesec, Open Policy Agent

### Service Mesh
Istio - can add mutual TLS

