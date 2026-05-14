# awesome-x-ops

A curated map of modern X-Ops: AI Ops, LLM/Agent Observability, Platform Engineering, GitOps, DataOps, FinOps, DevSecOps, and production-grade open-source operations tooling.

Languages: English | [简体中文](README.zh-CN.md)

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![License: CC BY-NC 4.0](https://img.shields.io/badge/license-CC%20BY--NC%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc/4.0/)

## Why awesome-x-ops?

Operations work is no longer just infrastructure monitoring or CI/CD glue. Modern teams need a practical map across AI-native applications, LLM observability, platform engineering, software delivery, cloud cost, security, and developer experience.

This list focuses on tools that help teams build, run, observe, secure, and optimize production systems.

## Featured Maps

- [LLM and Agent Observability Stack](#llm-and-agent-observability): tracing, prompt monitoring, evaluation, feedback, and production telemetry for LLM and agent systems.
- [Platform Engineering Stack](#platform-engineering): internal developer platforms, IAM, IaC, artifacts, API tooling, CI/CD, and testing.
- [GitOps and Kubernetes Operations Stack](#kubernetes-operations): cluster networking, autoscaling, deployment, and runtime operations.
- [FinOps Stack](#finops): cloud and Kubernetes cost visibility, allocation, and forecasting.
- [DevSecOps and Supply Chain Stack](#security-and-supply-chain): policy, runtime security, SBOM, scanning, and software supply-chain risk management.
- [DataOps Stack](#dataops): dataflow, orchestration, and data asset lifecycle tooling.

## Who is this for?

- Platform engineering teams building internal developer platforms.
- DevOps, SRE, and infrastructure teams modernizing operations stacks.
- AI engineering teams operating LLM, RAG, and agent applications in production.
- Engineering leaders looking for reliable open-source options before buying or building.
- Open-source maintainers who want their production-grade operations tools to be discoverable.

## Curation Principles

- Keep entries concise, efficient, accurate, and relevant.
- Prefer GitHub links when a reliable project repository exists.
- Include only proven, reliable, and high-quality projects.
- Ignore duplicates or projects already covered by an equivalent entry.
- Add or refine categories when useful, but avoid unrelated content.
- Prefer production-grade open source over demos, abandoned experiments, or vendor-only marketing pages.

## Growth and Contribution

This project aims to become a practical open-source map for modern X-Ops. Contributions are welcome if they improve accuracy, coverage, or navigation without turning the list into a link dump.

- Suggest a missing project via [Issues](https://github.com/xlabs-club/awesome-x-ops/issues).
- Open a focused pull request using [CONTRIBUTING.md](CONTRIBUTING.md).
- Keep descriptions short and explain why the project belongs in an operations/platform context.

## LLM and Agent Observability

Tools for tracing, evaluating, debugging, and operating LLM, RAG, and agent applications in production.

- [LiteLLM](https://github.com/BerriAI/litellm): OpenAI-compatible LLM gateway with routing, budgets, logging, and provider abstraction.
- [Langfuse](https://github.com/langfuse/langfuse): Open-source LLM engineering platform for traces, prompt management, evaluations, and metrics.
- [DeepEval](https://github.com/confident-ai/deepeval): LLM evaluation framework for testing RAG, agents, and model outputs in CI or production workflows.
- [Ragas](https://github.com/explodinggradients/ragas): Evaluation framework for RAG pipelines and LLM applications.
- [Arize Phoenix](https://github.com/Arize-ai/phoenix): Open-source observability and evaluation platform for LLM, RAG, and ML systems.
- [OpenLLMetry](https://github.com/traceloop/openllmetry): OpenTelemetry-based observability for LLM applications and agent workflows.
- [Helicone](https://github.com/Helicone/helicone): Open-source observability platform for LLM usage, latency, cost, caching, and request logs.
- [OpenLIT](https://github.com/openlit/openlit): OpenTelemetry-native AI engineering platform for LLM observability, evaluations, guardrails, prompt management, and GPU monitoring.
- [abtop](https://github.com/graykode/abtop): htop-style terminal monitor for AI coding agent sessions, tokens, context windows, rate limits, and ports.
- [agenttrace](https://github.com/luoyuctl/agenttrace): Local-first TUI for inspecting AI coding agent cost, tokens, latency, failures, and reports.

## AIOps

- [Netdata](https://github.com/netdata/netdata): Distributed real-time monitoring for infrastructure metrics, visualization, and alerting.
- [PostHog](https://github.com/PostHog/posthog): Open-source product analytics platform for user behavior tracking and product metrics.

## Agentic Workflow

- [AutoGPT](https://github.com/Significant-Gravitas/Auto-GPT): Autonomous AI agent framework that can break down and execute complex tasks.
- [Langflow](https://github.com/langflow-ai/langflow): Graphical builder for LangChain-style LLM workflows.
- [Dify](https://github.com/langgenius/dify): Open-source LLM application development platform with visual agent workflows and AI app deployment.
- [LangChain](https://github.com/langchain-ai/langchain): Framework for building LLM-powered applications, including agent workflow orchestration.
- [Flowise](https://github.com/FlowiseAI/Flowise): Low-code LLM workflow orchestration tool for visually building AI application chains.
- [crewAI](https://github.com/crewAIInc/crewAI): Framework for collaborative AI agents with role definition and task orchestration.
- [LlamaIndex](https://github.com/run-llama/llama_index): Data framework for LLM applications, supporting structured data retrieval and augmentation.
- [Haystack](https://github.com/deepset-ai/haystack): Extensible framework for question answering and custom AI workflow development.
- [BentoML](https://github.com/bentoml/BentoML): Open-source model serving platform for deploying models across frameworks and orchestrating AI applications.

## DataOps

- [Dagster](https://dagster.io/): Data orchestration platform for modeling data assets and managing the data lifecycle.
- [Apache NiFi](https://nifi.apache.org/): Visual dataflow orchestration for routing, transforming, and coordinating data across systems.
- [DataHub](https://github.com/datahub-project/datahub): Metadata platform for data discovery, lineage, governance, and observability across modern data and AI stacks.
- [Great Expectations](https://github.com/great-expectations/great_expectations): Data quality framework for validating datasets, documenting expectations, and catching pipeline regressions.

## FinOps

- [Infracost](https://github.com/infracost/infracost): Cloud cost forecasting tool for Terraform and Kubernetes cost estimates.
- [kubecost](https://kubecost.com/): Kubernetes cost management and monitoring platform.
- [OpenCost](https://opencost.io/): Open-source tool for tracking and allocating cloud costs in Kubernetes environments.
- [OptScale](https://github.com/hystax/optscale): Open-source FinOps and cloud cost optimization platform for AWS, Azure, GCP, Alibaba Cloud, and Kubernetes.
- [KubeStellar Console](https://github.com/kubestellar/console): Multi-cluster Kubernetes dashboard with AI-powered operations, real-time observability, and CNCF project integrations across edge and cloud clusters.

## Observability

- [Prometheus](https://github.com/prometheus/prometheus): Monitoring system and time-series database widely used for cloud-native metrics and alerting.
- [Grafana Loki](https://github.com/grafana/loki): Log aggregation system designed to index labels efficiently and integrate with Grafana.
- [OpenTelemetry Collector](https://github.com/open-telemetry/opentelemetry-collector): Vendor-neutral collector for receiving, processing, and exporting telemetry data.

## Kubernetes Operations

- [Cilium](https://github.com/cilium/cilium): eBPF-based Kubernetes networking, security, and observability platform.
- [cert-manager](https://github.com/cert-manager/cert-manager): Kubernetes-native certificate management controller for issuing and renewing TLS certificates.
- [KEDA](https://github.com/kedacore/keda): Kubernetes event-driven autoscaler for scaling workloads from external metrics and event sources.
- [External Secrets Operator](https://github.com/external-secrets/external-secrets): Kubernetes operator that syncs secrets from external secret managers into Kubernetes Secrets.
- [Karpenter](https://github.com/kubernetes-sigs/karpenter): Flexible Kubernetes node autoscaler for improving cluster efficiency and workload scheduling.

## Security and Supply Chain

- [Falco](https://github.com/falcosecurity/falco): CNCF runtime security tool for detecting suspicious behavior in containers and Kubernetes.
- [Kyverno](https://github.com/kyverno/kyverno): Kubernetes-native policy engine for validation, mutation, generation, and image verification.
- [Syft](https://github.com/anchore/syft): CLI and library for generating SBOMs from container images and filesystems.
- [Grype](https://github.com/anchore/grype): Vulnerability scanner for container images and filesystems that works well with Syft-generated SBOMs.

## Platform Engineering

A curated technology stack and toolchain for platform engineering.

### API Management Tools

- [Hoppscotch](https://github.com/hoppscotch/hoppscotch): Lightweight API development suite for REST, GraphQL, and WebSocket.
- [Bruno](https://github.com/usebruno/bruno): Fast, Git-friendly open-source API client for managing API collections and running API calls via desktop app or CLI.

### Artifact Management

- [Harbor](https://github.com/goharbor/harbor): Enterprise-grade container registry with security scanning and access control.
- [Skopeo](https://github.com/containers/skopeo): Open-source tool for inspecting, copying, and signing container images.
- [Nexus Repository](https://github.com/sonatype/nexus-public): Universal artifact repository supporting Maven, npm, Docker, and more.
- [ORAS](https://github.com/oras-project/oras): Tool for storing arbitrary content as OCI artifacts.

### CI/CD

- [Apache Airflow](https://airflow.apache.org/): Open-source workflow orchestration platform for data pipelines.
- [Harness](https://github.com/harness/harness): Open-source end-to-end developer platform for source control, CI/CD pipelines, hosted development environments, and artifact registries.
- [Jenkins](https://www.jenkins.io/): Open-source CI/CD automation server with a large plugin ecosystem.
- [argo-cd](https://argo-cd.readthedocs.io/): Popular declarative GitOps CD tool for Kubernetes.
- [argo-workflows](https://github.com/argoproj/argo-workflows): Kubernetes-native workflow engine.
- [Tekton](https://tekton.dev/): Kubernetes-native CI/CD framework with flexible task orchestration.
- [Flux](https://fluxcd.io/): Popular Kubernetes GitOps toolkit.

### Code Service

- [Trivy](https://github.com/aquasecurity/trivy): Comprehensive scanner for containers, code, vulnerabilities, misconfigurations, and SBOMs.
- [SonarQube](https://github.com/SonarSource/sonarqube): Continuous code quality platform supporting 27+ programming languages.
- [reviewdog](https://github.com/reviewdog): Automated code review and analysis tool for many languages and linters.
- [Dependency Track](https://dependencytrack.org/): Open-source software component analysis platform for supply-chain risk, SBOM analysis, and license checks.
- [OpenRewrite](https://docs.openrewrite.org): Automated large-scale code refactoring and modernization tool.
- [Hyades](https://github.com/DependencyTrack/hyades): Next-generation software supply-chain security platform intended to replace Dependency-Track after stabilization.

### Event Mesh

- [CloudEvents](https://cloudevents.io/): Specification for interoperable event-driven systems.
- [Argo Events](https://argoproj.github.io/argo-events/): Event-driven workflow automation framework for Kubernetes.
- [Apache EventMesh](https://eventmesh.apache.org/): Distributed event middleware supporting multiple messaging protocols and event stream management.

### Infrastructure as Code (IaC)

Infrastructure as Code manages and provisions infrastructure through code instead of manual processes.

- [OpenTofu](https://github.com/opentofu/opentofu): Community-driven Terraform fork governed by the Linux Foundation.
- [Pulumi](https://github.com/pulumi/pulumi): IaC tool for building infrastructure on any cloud using familiar programming languages.
- [sops](https://github.com/getsops/sops): Editor for encrypted YAML, JSON, ENV, INI, and binary files using AWS KMS, GCP KMS, Azure Key Vault, age, or PGP.
- [Crossplane](https://github.com/crossplane/crossplane): Kubernetes add-on that lets platform teams compose infrastructure from multiple vendors and expose higher-level self-service APIs.
- [Terragrunt](https://github.com/gruntwork-io/terragrunt): Terraform wrapper for DRY configuration and remote state management.
- [bitnami/sealed-secrets](https://github.com/bitnami-labs/sealed-secrets): Declarative Kubernetes secret management by encrypting secrets for safe storage in Git and decrypting them in-cluster.
- [Checkov](https://github.com/bridgecrewio/checkov): Static analysis tool for Infrastructure as Code security and compliance.
- [helmfile](https://github.com/helmfile): Declarative tool for orchestrating and deploying Helm charts.

### Identity and Access Management (IAM)

Trusting is hard. Knowing who to trust is even harder.

- [keycloak](https://github.com/keycloak/keycloak): Open-source IAM for modern applications and services.
- [oauth2-proxy](https://github.com/oauth2-proxy/oauth2-proxy): Lightweight OAuth2 reverse proxy for Google, Azure, OpenID Connect, and more, with simple authorization checks.
- [zitadel](https://github.com/zitadel/zitadel): Open-source IAM for modern applications and services, focused on simplicity.
- [Casdoor](https://github.com/casdoor/casdoor): Open-source identity management platform supporting OAuth 2.0, OIDC, and SAML.
- [dexidp/dex](https://github.com/dexidp/dex): Lightweight pluggable OpenID Connect (OIDC) and OAuth 2.0 provider.
- [pomerium](https://github.com/pomerium/pomerium): Identity-aware proxy with richer access-control capabilities.

### Internal Developer Platform (IDP)

An internal developer platform is more than a pile of tools; it is not just another management console or dashboard.

- [backstage](https://github.com/backstage/backstage): Open platform for building developer portals that help teams build, deploy, and maintain software.
- [OpenChoreo](https://github.com/openchoreo/openchoreo): Open-source developer platform for Kubernetes with a Backstage-powered portal, CI/CD, GitOps, observability, and platform abstractions.

### IaaS Tools

Lightweight virtualization tools useful for local Kubernetes and container-platform debugging.

- [Minikube](https://github.com/kubernetes/minikube): Local Kubernetes cluster deployment tool.
- [Vagrant](https://github.com/hashicorp/vagrant): Cross-platform virtual machine management tool supporting multiple virtualization backends.
- [lima](https://github.com/lima-vm/lima): Linux virtual machines with automatic file sharing and port forwarding, including heterogeneous VM simulation.
- [multipass](https://github.com/canonical/multipass): Lightweight virtualization tool from Ubuntu.

### Testing Tools

Tools for testing engineers and quality-focused platform teams.

- [googletest](https://github.com/google/googletest): Google Testing and Mocking Framework.
- [Selenium](https://github.com/SeleniumHQ/selenium): Browser automation framework for web application testing.
- [grafana/k6](https://github.com/grafana/k6): Modern load-testing tool using Go and JavaScript, also useful for API testing workflows.
- [JMeter](https://github.com/apache/jmeter): Java-based performance testing tool supporting many protocols.

## License

This document is licensed under [CC BY-NC 4.0][].

[CC BY-NC 4.0]: https://creativecommons.org/licenses/by-nc/4.0/
