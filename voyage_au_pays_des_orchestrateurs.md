# Voyage au pays des orchestrateurs
Thomas Cottier

The product in question - Tuleap (PHP + JS + MySQL)

Idea - Tuleap as a service

## History
Before 2014 - physical server per client, wildcard cert

First try with Docker - tuleap-aio (all in one - one docker image - yolo!)

### myTuleap v1

Write some ansible playbooks to deploy Docker, SSL/TLS certs. Pull and run docker images.

Now, the problem is: Where do I have capacity?

### myTuleap v2

We're gonna use an orchestrator! Docker Swarm and Kubernetes exist

They bet on Docker Swarm

Write some Ansible Playbooks:

- Deploy Docker Swarm
- Mount NFS filesystem
- Pull images from private hub

Issues: Not really doing scaling as we expect it.

Small customer: Can I run Tuleap in <Country> ?

Big customer: Can I run it in my Kubernetes cluster?

### myTuleap v2.5
- Rewrite images
- Use a PaaS


### myTuleap v3
Only deal with the orchestrator, no lower layers.

[Nomad](https://nomadproject.io)

If you only need to scale, no need for Kubernetes.

