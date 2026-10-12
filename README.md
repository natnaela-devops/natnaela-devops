# Natnael Amsalu

**DevOps & Site Reliability Engineer | AWS Certified Solutions Architect | Kubernetes & Cloud Infrastructure**

DevOps and Site Reliability Engineer with hands-on experience supporting Linux platforms, Kubernetes/RKE2 environments, and distributed services across banking and public-health systems. My work centers on reliable service delivery, incident troubleshooting, observability, infrastructure automation, networking, identity, data platforms, and clear operational documentation.

My strongest practical experience is in **Linux, on-premises infrastructure, Kubernetes/RKE2, middleware, databases, networking, and production-support troubleshooting**. My AWS knowledge is certification-backed and reinforced through labs and architecture exercises; I do not present it as production AWS operating experience.

Based in Addis Ababa, Ethiopia, and open to international **DevOps, Site Reliability Engineering, Platform Engineering, Infrastructure, and Junior Cloud Engineering** opportunities.

## Start here — production infrastructure evidence

**[Banking Digital Platform Infrastructure](https://github.com/natnaela-devops/banking-digital-platform-infrastructure)**

This is the closest public representation of the platform work behind my banking DevOps/SRE experience: a sanitized case study of hands-on **UAT and production** work across:

**RKE2 / Rancher · Longhorn · Harbor · Kafka/KRaft · Redis Cluster / Predixy · YugabyteDB · TimescaleDB · Keycloak · Nginx / TLS · SeaweedFS · PM2 · OpenSearch · Prometheus / Alertmanager**

It documents platform setup and operations, service integration, secure routing, cluster readiness, storage, observability, authentication and certificate hardening, incident troubleshooting, UAT validation, production rollout, and rollback-aware change execution.

```text
Users / mobile / web
        |
        v
   Nginx / TLS edge
        |
   APIs / gateways / identity / web
        |
        v
     RKE2 / Rancher
        |
   +----+-----+-----------+-----------+
   |          |           |           |
 Kafka      Redis      YugabyteDB   TimescaleDB
 /KRaft    /Predixy
   |
   +--> Longhorn / Harbor / SeaweedFS
   +--> OpenSearch / Prometheus / Alertmanager
```

The case study intentionally excludes customer names, real IPs/domains, credentials, certificates, private keys, production data, and unverified performance claims.

## Engineering focus

- **Kubernetes and platform operations:** RKE2, Rancher, Kubernetes, Helm, Longhorn, Harbor, containerd, Docker, workload troubleshooting, upgrades, storage, and cluster operations
- **Linux and service reliability:** systemd, networking, DNS, TLS, filesystem/resource troubleshooting, Java service operations, process diagnostics, and recovery runbooks
- **Distributed services and data platforms:** Kafka/KRaft, Redis Cluster, Predixy, PostgreSQL, TimescaleDB, MySQL, YugabyteDB, Oracle client operations, ActiveMQ, Keycloak, Nginx, and SeaweedFS
- **Delivery automation:** GitHub Actions, GitOps, Argo CD, Kustomize, Ansible, Bash, container pipelines, validation gates, and repeatable deployment workflows
- **Observability and incident response:** Prometheus, Alertmanager, OpenSearch, OpenTelemetry, log/metric/trace correlation, alert validation, capacity awareness, and evidence-driven troubleshooting
- **Cloud foundation:** AWS Solutions Architect certification plus structured VPC, IAM, EC2, S3, RDS, Route 53, CloudWatch, architecture, and Terraform labs

## Recent operational focus

- setup and operation of a multi-service banking digital platform across UAT and production
- rolling a three-node Kafka/KRaft cluster from legacy PLAINTEXT application access to a parallel **mTLS listener** without restarting the whole cluster
- issuing and validating per-broker and per-application certificate identities using PKCS12 and JKS stores
- separating Kafka quorum health from Java/WildFly/Spring client configuration failures
- validating runtime Kafka properties, consumer-group joins, partition assignments, and multi-broker communication
- troubleshooting Rancher/Kubernetes binary Secret encoding, keystore password failures, and certificate-store integrity
- validating **Redis Cluster + Predixy** routing, authentication, `MOVED` behavior, and application access paths

## Selected engineering evidence

| Project | What it demonstrates | Evidence |
| --- | --- | --- |
| [Banking Digital Platform Infrastructure](https://github.com/natnaela-devops/banking-digital-platform-infrastructure) | Sanitized UAT and production platform work across RKE2/Rancher, Kafka/KRaft mTLS, Redis Cluster/Predixy, YugabyteDB, TimescaleDB, Keycloak, Nginx, SeaweedFS, Harbor, Longhorn, OpenSearch, Prometheus, and supporting services | Architecture, operational scope, migration patterns, security hardening, UAT-to-production workflow, troubleshooting and recovery |
| [DevOps Troubleshooting Runbooks](https://github.com/natnaela-devops/devops-troubleshooting-runbooks) | Sanitized troubleshooting patterns drawn from real DevOps/SRE work across RKE2, Linux, Kafka/KRaft mTLS, Redis/Predixy, databases, Java services, networking, storage, authentication, containers, and observability | Root-cause-oriented runbooks, rolling-change procedures, runtime verification, safety notes, and explicit evidence boundaries |
| [RKE2 High-Availability Platform Reference](https://github.com/natnaela-devops/kubernetes-rke2-cluster-setup) | Three-server etcd quorum, dedicated workers, Longhorn, security controls, Helm examples, HA design, and cluster operations | Configuration, shell, Helm, and Kubernetes manifest validation in GitHub Actions |
| [Spring Boot CI/CD and GitOps Lab](https://github.com/natnaela-devops/springboot-ci-cd-demo) | Maven, Docker, Kubernetes/Kustomize, Argo CD, GitHub Actions, GHCR/Harbor patterns, probes, resource controls, and container hardening | Tests, image build, health smoke test, linting, and Kubernetes schema validation |
| [Ansible Infrastructure Automation Lab](https://github.com/natnaela-devops/ansible-playbooks-collection) | Reusable Linux baseline, Docker, and RKE2 host-preparation roles with safe defaults and idempotent automation | YAML lint, Ansible lint, syntax validation, and repeat-run idempotency checks |

> Public repositories use sanitized or disposable configurations. They demonstrate engineering decisions, troubleshooting methods, and repeatable evidence without exposing employer, customer, network, credential, or production data.

## How I troubleshoot

I separate symptoms from root causes and validate each layer independently. A reachable port does not prove an application is healthy; a Kubernetes manifest existing does not prove the pod is running; and a healthy Kafka quorum does not prove the producer is configured correctly.

The [DevOps Troubleshooting Runbooks](https://github.com/natnaela-devops/devops-troubleshooting-runbooks) repository captures this approach using a consistent structure:

**Problem → Symptoms → Investigation → Root cause or evidence boundary → Recovery → Verification → Safety notes → Lessons learned**

## Core technologies

| Area | Technologies |
| --- | --- |
| Platforms | Linux, Kubernetes, RKE2, Rancher, Docker, containerd, Helm, Longhorn, Harbor, Argo CD |
| Automation and delivery | Ansible, Git, GitHub Actions, CI/CD, GitOps, Kustomize, Bash, Terraform labs |
| Reliability and observability | Prometheus, Alertmanager, OpenSearch, OpenTelemetry, Grafana, incident response, runbooks |
| Networking, identity, and edge | TCP/IP, DNS, TLS, Nginx, load balancing, VPN troubleshooting, Kubernetes RBAC, Keycloak, AWS IAM |
| Data, messaging, and storage | PostgreSQL, TimescaleDB, MySQL, YugabyteDB, Redis, Predixy, Kafka/KRaft, ActiveMQ, Oracle client tooling, SeaweedFS, MinIO |
| AWS knowledge and labs | VPC, EC2, IAM, S3, RDS, Route 53, CloudWatch, architecture and Terraform exercises |

## Certifications

- **AWS Certified Solutions Architect – Associate**
- **AWS Certified Cloud Practitioner**

## Portfolio principles

- No fabricated uptime, performance, or production-scale claims
- Production work is generalized and sanitized before publication
- Lab projects are clearly labeled as labs or references
- CI and validation output are preferred over claims that cannot be reproduced
- Recovery procedures include verification and safety boundaries, not just commands
- Secrets, internal IPs, customer identifiers, private certificates, and environment-specific data stay out of public repositories

## Connect

- [LinkedIn](https://www.linkedin.com/in/natnaela-devops)
- [Email](mailto:natnaela.devops@gmail.com)
