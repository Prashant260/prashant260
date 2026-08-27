<div align="center">

# Hi 👋, I'm Prashant

### Cloud & DevOps Engineer — Terraform · AWS · Kubernetes · CI/CD

I design and automate cloud infrastructure end-to-end: provisioning with Terraform, shipping through CI/CD pipelines, and running workloads on Docker and Kubernetes — with a growing focus on security and observability.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/prashant-choudhary-392a1620b/)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white)](https://github.com/Prashant260)

</div>

---

## About Me

I build cloud infrastructure the way I'd want to hand it off to another engineer: version-controlled, reproducible, and pipeline-driven rather than clicked together in a console.

Most of my recent work centers on **AWS infrastructure provisioned with Terraform** — VPCs, EC2, ECS Fargate, and EKS — wired into **GitHub Actions and Jenkins pipelines** that build, scan, and deploy containerized applications. I've provisioned a Kubernetes cluster from raw EC2 instances rather than relying only on a managed control plane, because I wanted to understand what EKS is abstracting away.

Lately I've been pulling security and observability earlier into that same pipeline: OIDC-based cloud auth instead of static keys, Trivy/Snyk/SonarQube scanning in CI, Prometheus/Grafana/OpenTelemetry stacks for visibility into what's actually running, and a Zero Trust–style deployment as a first step into policy-based access control.

---

## Tech Stack

| Category | Technologies |
|---|---|
| ☁️ **Cloud** | AWS · EC2 · VPC · S3 · IAM (OIDC) · ECS Fargate · ECR · ALB · EKS · RDS · CloudWatch · DynamoDB |
| ⚙️ **CI/CD** | GitHub Actions · Jenkins · Docker Hub · JFrog Artifactory |
| 🏗️ **Infrastructure as Code** | Terraform · Ansible · Pulumi · OpenTofu |
| 🐳 **Containers** | Docker · Docker Compose |
| ☸️ **Kubernetes** | Kubernetes · Minikube · containerd · Calico CNI |
| 💻 **Languages** | Python · JavaScript/Node.js · Java · Bash · HCL · TypeScript |
| 🔐 **Security** | Trivy · Snyk · SonarQube · OIDC · Zero Trust / Cedar policies |
| 📊 **Monitoring** | Prometheus · Grafana · Alertmanager · OpenTelemetry · Loki · Netdata · CloudWatch |
| 🗄️ **Databases** | PostgreSQL (RDS) · MySQL |

---

## Featured Projects

### 🔐 [Two-Tier DevSecOps Deployment on AWS](https://github.com/Prashant260/2-tier-app-deployment)
End-to-end pipeline for a two-tier app on AWS: Terraform provisions the infrastructure, GitHub Actions authenticates via **OIDC (no static AWS keys)**, and the pipeline runs SonarQube, Snyk, and Trivy scans before deploying Docker containers.

**Tech:** `Terraform` `GitHub Actions` `Docker` `SonarQube` `Snyk` `Trivy` `AWS OIDC`

The security-scanning stage and keyless cloud auth are what separate this from a typical "deploy to EC2" tutorial.

### 📦 [Two-Tier DevSecOps Deployment — ECS Fargate](https://github.com/Prashant260/eECS-app-deploy)
The serverless-containers counterpart to the project above: a Flask app deployed on **ECS Fargate** behind an ALB, images pulled from ECR, logs shipped to CloudWatch, infrastructure defined as modular Terraform, and the same OIDC-secured CI/CD approach.

**Tech:** `Terraform` `ECS Fargate` `ECR` `ALB` `CloudWatch` `Flask` `GitHub Actions`

### ☸️ [CI/CD Pipeline to AWS EKS with Monitoring](https://github.com/Prashant260/devops_project-1)
A Python application taken from commit to a running EKS workload: Dockerized, deployed via a GitHub Actions pipeline, with Prometheus and Grafana dashboards tracking cluster CPU/memory, workload health, and CoreDNS metrics.

**Tech:** `Docker` `GitHub Actions` `AWS EKS` `Prometheus` `Grafana`

Demonstrates the full loop — not just "it deploys," but "here's how I know it's healthy."

### 🖥️ [Kubernetes Cluster Provisioning on AWS (Terraform)](https://github.com/Prashant260/kubernetes_on-prem)
Builds a Kubernetes cluster from scratch on two EC2 instances (one master, one worker) using Terraform for the VPC/networking and provisioning scripts for `containerd` and the **Calico CNI**, rather than starting from a managed control plane.

**Tech:** `Terraform` `EC2` `containerd` `Calico` `Kubernetes 1.30`

Shows an understanding of what EKS or other managed Kubernetes services are actually abstracting.

### 🛠️ [Self-Healing Infrastructure](https://github.com/Prashant260/self_healing-_infrastructure)
Prometheus and Alertmanager detect service failures; a Flask webhook receiver bridges the alert to **Ansible playbooks** that automatically restart the failing service — closing the loop from "detected" to "remediated" without a human in the middle.

**Tech:** `Prometheus` `Alertmanager` `Ansible` `Python (Flask)`

### 📡 [Cloud-Native Observability Platform](https://github.com/Prashant260/opentelemetry)
A self-hosted observability stack wiring together an **OpenTelemetry Collector**, Prometheus, Grafana, and Loki, deployable via Docker Compose, with a Kubernetes manifests/Helm directory for cluster deployment.

**Tech:** `OpenTelemetry` `Prometheus` `Grafana` `Loki` `Docker Compose`

### 🔄 [Blue-Green Deployment on AWS](https://github.com/Prashant260/blue-green-deployment)
Implements a Blue-Green deployment strategy across two EC2 environments behind an Application Load Balancer, with a GitHub Actions pipeline pushing new images to Docker Hub and traffic switched at the ALB rather than the instance.

**Tech:** `AWS EC2` `ALB` `Docker` `GitHub Actions`

### 🛡️ [Zero Trust Security Implementation](https://github.com/Prashant260/zero-Trust-security-implementation)
The newest project in the profile: a Terraform-provisioned AWS environment (VPC, hardened security groups, S3+DynamoDB remote state with locking) running a Flask app, paired with **Cedar policy files** as a first step into policy-based access control.

**Tech:** `Terraform` `AWS` `Cedar` `Flask`

Earlier-stage than the projects above, but the clearest signal of where the DevSecOps focus is heading next.

---

## DevOps & Cloud Journey

```
Git & Linux Basics → Jenkins CI/CD → Terraform (single resource) → Docker
    → GitHub Actions → AWS (EC2/ECS/EKS) → Kubernetes (Minikube → self-built cluster)
        → Monitoring (Netdata → Prometheus/Grafana) → DevSecOps (OIDC, Trivy, Zero Trust)
```

This progression is drawn directly from repository history — from labeled DevOps-internship tasks (Git basics, a single Terraform-provisioned Docker container, a first Jenkins pipeline, Netdata monitoring) through to the multi-service AWS/Kubernetes/security projects above, most of which were built or updated in the last few months.

---

## Engineering Focus

- **Infrastructure automation** — modular Terraform with remote state (S3 + DynamoDB locking) across multiple projects
- **CI/CD** — GitHub Actions and Jenkins pipelines covering build, test, security scan, and deploy stages
- **Containerization & Kubernetes** — Docker across nearly every project; Kubernetes via Minikube, a self-provisioned cluster, and AWS EKS
- **Cloud deployment patterns** — EC2, ECS Fargate, and EKS as three different ways of running the same kind of workload
- **Observability** — Prometheus/Grafana/CloudWatch/OpenTelemetry/Loki, used to validate deployments rather than just ship them
- **DevSecOps** — OIDC-based keyless cloud auth, integrated SAST/SCA scanning (SonarQube, Snyk, Trivy), and an early Zero Trust implementation

---

## Currently Exploring

- GitOps patterns and ArgoCD on EKS
- IaC tool comparison — Pulumi (TypeScript) vs. OpenTofu, provisioning identical AWS resources side by side
- Policy-based access control (Cedar) as an extension of the Zero Trust project
- FinOps / cloud cost visibility tooling

---

## GitHub Stats

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=Prashant260&show_icons=true&theme=dark&hide_border=true&count_private=true" alt="Prashant's GitHub stats" height="165"/>
<img src="https://github-readme-streak-stats.herokuapp.com/?user=Prashant260&theme=dark&hide_border=true" alt="Prashant's GitHub streak" height="165"/>

<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Prashant260&layout=compact&theme=dark&hide_border=true&langs_count=8" alt="Top languages" height="165"/>

</div>

---

## Connect With Me

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/prashant-choudhary-392a1620b/)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Prashant260)

</div>
