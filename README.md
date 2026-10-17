# Natnael Amsalu

**DevOps / SRE | Linux · Kubernetes/RKE2 · Kafka · GitOps · Observability**

I work on Linux infrastructure and the services around it: Kubernetes clusters, application deployments, messaging, databases, reverse proxies, and monitoring. Most of my hands-on experience comes from supporting banking and public-health systems, where troubleshooting often crosses several layers.

I'm based in Addis Ababa, Ethiopia, and interested in DevOps, SRE, platform and infrastructure engineering roles. I'm an AWS Certified Solutions Architect – Associate and Cloud Practitioner; my cloud practice is mostly certification and labs, while my day-to-day infrastructure experience is primarily on-premises.

## Work worth looking at

| Repository | Why I built or documented it |
| --- | --- |
| [Banking digital platform infrastructure](https://github.com/natnaela-devops/banking-digital-platform-infrastructure) | Sanitized notes from operating RKE2, messaging, storage, identity, edge routing and observability across UAT and production. Includes a [GitOps delivery failure map](https://github.com/natnaela-devops/banking-digital-platform-infrastructure/blob/main/docs/delivery-failure-boundaries.md). |
| [Observability stack](https://github.com/natnaela-devops/observability-stack) | OpenSearch, OpenTelemetry, Data Prepper, Prometheus and Alertmanager configuration with reproducible validation. Public configuration is generic; environment-specific deployment details are kept private. |
| [Troubleshooting runbooks](https://github.com/natnaela-devops/devops-troubleshooting-runbooks) | Problems I've encountered or investigated, with commands, causes, fixes, verification steps and notes on what the evidence did *not* establish. |
| [RKE2 HA reference](https://github.com/natnaela-devops/kubernetes-rke2-cluster-setup) | Three-server etcd quorum, separate workers, Longhorn and Kubernetes security settings. Includes [CI validation](https://github.com/natnaela-devops/kubernetes-rke2-cluster-setup/actions). |
| [Spring Boot CI/CD lab](https://github.com/natnaela-devops/springboot-ci-cd-demo) | Maven tests, Docker build and health check, Kustomize validation, image publishing and a reviewable Argo CD promotion path. [Workflow runs](https://github.com/natnaela-devops/springboot-ci-cd-demo/actions). |
| [Ansible host preparation](https://github.com/natnaela-devops/ansible-playbooks-collection) | Roles for common Linux setup, Docker and RKE2 prerequisites. CI covers lint, syntax and an idempotency check for the common role. [Workflow runs](https://github.com/natnaela-devops/ansible-playbooks-collection/actions). |

## Three problems that shaped how I work

**RKE2/Rancher outage and disk I/O errors.** When the API stopped responding, I checked RKE2 restarts, etcd, containerd, kernel messages and Longhorn state instead of assuming it was just a Rancher problem. The kernel and filesystem errors established an I/O failure mechanism; they did not establish whether storage hardware, the hypervisor or contention started it. [Investigation notes](https://github.com/natnaela-devops/devops-troubleshooting-runbooks/blob/main/runbooks/kubernetes/rke2-control-plane-resource-io-degradation.md).

**Kafka listener migration.** I worked through a staged move from plaintext application access to certificate-based mTLS. Keeping the old path during validation meant checking broker readiness, certificate identities, client keystores, consumer groups and application-level message delivery before retiring the previous listener. [Migration runbook](https://github.com/natnaela-devops/devops-troubleshooting-runbooks/blob/main/runbooks/kafka/kraft-rolling-mtls-listener-rollout.md).

**Redis Cluster routing.** An application could connect to Redis and still fail after receiving a `MOVED` redirect to an address or port it couldn't reach. I used cluster and proxy tests to separate Redis health from the route exposed to the application. [Runbook](https://github.com/natnaela-devops/devops-troubleshooting-runbooks/blob/main/runbooks/kubernetes/redis-cluster-moved-service-exposure.md).

## Tools I use

- **Infrastructure:** Linux, RKE2/Kubernetes, Rancher, Longhorn, Docker, containerd, Nginx, systemd
- **Automation and delivery:** Ansible, Bash, Helm, GitHub Actions, GitOps/Argo CD, Harbor, Kustomize
- **Middleware and data:** Kafka/KRaft, Redis Cluster/Predixy, Keycloak, PostgreSQL, TimescaleDB, YugabyteDB, MySQL, Oracle client tooling
- **Observability:** OpenSearch, OpenTelemetry, Prometheus, Alertmanager
- **AWS:** Solutions Architect – Associate and Cloud Practitioner certifications; architecture exercises and labs, not claimed production AWS administration

## A note about the public repos

The banking diagrams and incident notes are adapted from work I did, not exports of an employer's environment. Hostnames, addresses, credentials, internal topology and customer details are omitted. The standalone labs are labeled as labs. Where an investigation left a root cause open, the runbook says so.

**[LinkedIn](https://www.linkedin.com/in/natnaela-devops) · [Email](mailto:natnaela.devops@gmail.com)**
