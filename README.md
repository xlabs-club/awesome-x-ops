# awesome-x-ops

Awesome tools, projects, blogs, and companion technologies for AI, DataOps, DevOps, GitOps, FinOps, and Platform Engineering.

Languages: English | [简体中文](README.zh-CN.md)

## Curation Principles

- Keep entries concise, efficient, accurate, and relevant.
- Prefer GitHub links when a reliable project repository exists.
- Include only proven, reliable, and high-quality projects.
- Ignore duplicates or projects already covered by an equivalent entry.
- Add or refine categories when useful, but avoid unrelated content.

## AIOps

- [Netdata](https://github.com/netdata/netdata): Distributed real-time monitoring for infrastructure metrics, visualization, and alerting.
- [PostHog](https://github.com/PostHog/posthog): Open-source product analytics platform for user behavior tracking and product metrics.

## Agentic Workflow

- [AutoGPT](https://github.com/Significant-Gravitas/Auto-GPT): Autonomous AI agent framework that can break down and execute complex tasks.
- [LangChain](https://github.com/langchain-ai/langchain): Framework for building LLM-powered applications, including agent workflow orchestration.
- [crewAI](https://github.com/joaomdmoura/crewAI): Framework for collaborative AI agents with role definition and task orchestration.
- [Dify](https://github.com/langgenius/dify): Open-source LLM application development platform with visual agent workflows and AI app deployment.
- [Flowise](https://github.com/FlowiseAI/Flowise): Low-code LLM workflow orchestration tool for visually building AI application chains.
- [Langflow](https://github.com/langflow-ai/langflow): Graphical builder for LangChain-style LLM workflows.
- [BentoML](https://github.com/bentoml/BentoML): Open-source model serving platform for deploying models across frameworks and orchestrating AI applications.
- [Haystack](https://github.com/deepset-ai/haystack): Extensible framework for question answering and custom AI workflow development.
- [LlamaIndex](https://github.com/run-llama/llama_index): Data framework for LLM applications, supporting structured data retrieval and augmentation.

## DataOps

- [Apache NiFi](https://nifi.apache.org/): Visual dataflow orchestration for routing, transforming, and coordinating data across systems.
- [Dagster](https://dagster.io/): Data orchestration platform for modeling data assets and managing the data lifecycle.

## FinOps

- [kubecost](https://kubecost.com/): Kubernetes cost management and monitoring platform.
- [OpenCost](https://opencost.io/): Open-source tool for tracking and allocating cloud costs in Kubernetes environments.
- [Infracost](https://github.com/infracost/infracost): Cloud cost forecasting tool for Terraform and Kubernetes cost estimates.
- [KubeStellar Console](https://github.com/kubestellar/console): Multi-cluster Kubernetes dashboard with AI-powered operations, real-time observability, and CNCF project integrations across edge and cloud clusters.

## Platform Engineering

A curated technology stack and toolchain for platform engineering.

### API Management Tools

- [Bruno](https://github.com/usebruno/bruno): Fast, Git-friendly open-source API client for managing API collections and running API calls via desktop app or CLI.
- [Hoppscotch](https://github.com/hoppscotch/hoppscotch): Lightweight API development suite for REST, GraphQL, and WebSocket.

### Artifact Management

- [ORAS](https://github.com/oras-project/oras): Tool for storing arbitrary content as OCI artifacts.
- [Skopeo](https://github.com/containers/skopeo): Open-source tool for inspecting, copying, and signing container images.
- [Harbor](https://github.com/goharbor/harbor): Enterprise-grade container registry with security scanning and access control.
- [Nexus Repository](https://github.com/sonatype/nexus-public): Universal artifact repository supporting Maven, npm, Docker, and more.

### CI/CD

- [argo-workflows](https://github.com/argoproj/argo-workflows): Kubernetes-native workflow engine.
- [argo-cd](https://argo-cd.readthedocs.io/): Popular declarative GitOps CD tool for Kubernetes.
- [Flux](https://fluxcd.io/): Popular Kubernetes GitOps toolkit.
- [Apache Airflow](https://airflow.apache.org/): Open-source workflow orchestration platform for data pipelines.
- [Jenkins](https://www.jenkins.io/): Open-source CI/CD automation server with a large plugin ecosystem.
- [Tekton](https://tekton.dev/): Kubernetes-native CI/CD framework with flexible task orchestration.

### Code Service

- [OpenRewrite](https://docs.openrewrite.org): Automated large-scale code refactoring and modernization tool.
- [reviewdog](https://github.com/reviewdog): Automated code review and analysis tool for many languages and linters.
- [Dependency Track](https://dependencytrack.org/): Open-source software component analysis platform for supply-chain risk, SBOM analysis, and license checks.
- [Hyades](https://github.com/DependencyTrack/hyades): Next-generation software supply-chain security platform intended to replace Dependency-Track after stabilization.
- [SonarQube](https://github.com/SonarSource/sonarqube): Continuous code quality platform supporting 27+ programming languages.
- [Trivy](https://github.com/aquasecurity/trivy): Comprehensive scanner for containers, code, vulnerabilities, misconfigurations, and SBOMs.

### Event Mesh

- [CloudEvents](https://cloudevents.io/): Specification for interoperable event-driven systems.
- [Apache EventMesh](https://eventmesh.apache.org/): Distributed event middleware supporting multiple messaging protocols and event stream management.
- [Argo Events](https://argoproj.github.io/argo-events/): Event-driven workflow automation framework for Kubernetes.

### Infrastructure as Code (IaC)

Infrastructure as Code manages and provisions infrastructure through code instead of manual processes.

- [Pulumi](https://github.com/pulumi/pulumi): IaC tool for building infrastructure on any cloud using familiar programming languages.
- [OpenTofu](https://github.com/opentofu/opentofu): Community-driven Terraform fork governed by the Linux Foundation.
- [Crossplane](https://github.com/crossplane/crossplane): Kubernetes add-on that lets platform teams compose infrastructure from multiple vendors and expose higher-level self-service APIs.
- [helmfile](https://github.com/helmfile): Declarative tool for orchestrating and deploying Helm charts.
- [sops](https://github.com/getsops/sops): Editor for encrypted YAML, JSON, ENV, INI, and binary files using AWS KMS, GCP KMS, Azure Key Vault, age, or PGP.
- [bitnami/sealed-secrets](https://github.com/bitnami-labs/sealed-secrets): Declarative Kubernetes secret management by encrypting secrets for safe storage in Git and decrypting them in-cluster.
- [Terragrunt](https://github.com/gruntwork-io/terragrunt): Terraform wrapper for DRY configuration and remote state management.
- [Checkov](https://github.com/bridgecrewio/checkov): Static analysis tool for Infrastructure as Code security and compliance.

### Identity and Access Management (IAM)

Trusting is hard. Knowing who to trust is even harder.

- [keycloak](https://github.com/keycloak/keycloak): Open-source IAM for modern applications and services.
- [zitadel](https://github.com/zitadel/zitadel): Open-source IAM for modern applications and services, focused on simplicity.
- [dexidp/dex](https://github.com/dexidp/dex): Lightweight pluggable OpenID Connect (OIDC) and OAuth 2.0 provider.
- [oauth2-proxy](https://github.com/oauth2-proxy/oauth2-proxy): Lightweight OAuth2 reverse proxy for Google, Azure, OpenID Connect, and more, with simple authorization checks.
- [pomerium](https://github.com/pomerium/pomerium): Identity-aware proxy with richer access-control capabilities.
- [Casdoor](https://github.com/casdoor/casdoor): Open-source identity management platform supporting OAuth 2.0, OIDC, and SAML.

### Internal Developer Platform (IDP)

An internal developer platform is more than a pile of tools; it is not just another management console or dashboard.

- [backstage](https://github.com/backstage/backstage): Open platform for building developer portals that help teams build, deploy, and maintain software.

### IaaS Tools

Lightweight virtualization tools useful for local Kubernetes and container-platform debugging.

- [lima](https://github.com/lima-vm/lima): Linux virtual machines with automatic file sharing and port forwarding, including heterogeneous VM simulation.
- [multipass](https://github.com/canonical/multipass): Lightweight virtualization tool from Ubuntu.
- [Vagrant](https://github.com/hashicorp/vagrant): Cross-platform virtual machine management tool supporting multiple virtualization backends.
- [Minikube](https://github.com/kubernetes/minikube): Local Kubernetes cluster deployment tool.

### Testing Tools

Tools for testing engineers and quality-focused platform teams.

- [grafana/k6](https://github.com/grafana/k6): Modern load-testing tool using Go and JavaScript, also useful for API testing workflows.
- [googletest](https://github.com/google/googletest): Google Testing and Mocking Framework.
- [JMeter](https://github.com/apache/jmeter): Java-based performance testing tool supporting many protocols.
- [Selenium](https://github.com/SeleniumHQ/selenium): Browser automation framework for web application testing.

## License

This document is licensed under [CC BY-NC 4.0][].

[CC BY-NC 4.0]: https://creativecommons.org/licenses/by-nc/4.0/
