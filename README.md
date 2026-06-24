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
- [OpenInference](https://github.com/Arize-ai/openinference): OpenTelemetry instrumentation and semantic conventions for tracing LLM, RAG, and agent applications.
- [OpenLLMetry](https://github.com/traceloop/openllmetry): OpenTelemetry-based observability for LLM applications and agent workflows.
- [Helicone](https://github.com/Helicone/helicone): Open-source observability platform for LLM usage, latency, cost, caching, and request logs.
- [OpenLIT](https://github.com/openlit/openlit): OpenTelemetry-native AI engineering platform for LLM observability, evaluations, guardrails, prompt management, and GPU monitoring.
- [LangWatch](https://github.com/langwatch/langwatch): Open-source platform for LLM monitoring, evaluations, traces, and agent testing.
- [Opik](https://github.com/comet-ml/opik): Open-source platform for tracing, evaluating, and monitoring LLM applications, RAG systems, and agent workflows.
- [promptfoo](https://github.com/promptfoo/promptfoo): Open-source CLI and platform for prompt testing, LLM evaluations, red teaming, and CI/CD regression checks.
- [Langtrace](https://github.com/Scale3-Labs/langtrace): OpenTelemetry-based observability platform for tracing, evaluating, and monitoring LLM applications.
- [Future AGI](https://github.com/future-agi/future-agi): Self-hostable platform for evaluating, observing, and improving LLM and AI agent applications.
- [CozeLoop](https://github.com/coze-dev/coze-loop): AI agent optimization platform covering development, debugging, evaluation, and production monitoring workflows.
- [Agenta](https://github.com/Agenta-AI/agenta): Open-source LLMOps platform for prompt management, playgrounds, evaluations, and observability.
- [abtop](https://github.com/graykode/abtop): htop-style terminal monitor for AI coding agent sessions, tokens, context windows, rate limits, and ports.
- [agenttrace](https://github.com/luoyuctl/agenttrace): Local-first TUI for inspecting AI coding agent cost, tokens, latency, failures, and reports.
- [ax](https://github.com/Necmttn/ax): Local-first telemetry and memory graph for AI coding agents, covering costs, tools, skills, sessions, and OTLP events.
- [TensorZero](https://github.com/tensorzero/tensorzero): Open-source LLMOps platform that combines an LLM gateway, observability, evaluations, optimization, and experimentation.
- [Evidently](https://github.com/evidentlyai/evidently): Open-source ML and LLM observability framework for evaluation, testing, monitoring, and data quality checks.
- [RagaAI Catalyst](https://github.com/raga-ai-hub/RagaAI-Catalyst): Agent AI observability and evaluation SDK for tracing, debugging, and monitoring multi-agent LLM systems.
- [Pydantic Logfire](https://github.com/pydantic/logfire): AI observability platform for tracing and monitoring production LLM and agent systems.
- [Laminar](https://github.com/lmnr-ai/lmnr): Open-source observability platform purpose-built for AI agents and LLM applications.
- [MLflow](https://github.com/mlflow/mlflow): Open-source AI engineering platform for debugging, evaluating, monitoring, and optimizing agents, LLMs, and ML models.
- [Giskard](https://github.com/Giskard-AI/giskard-oss): Open-source evaluation and testing framework for LLM applications and AI agents.
- [ZenML](https://github.com/zenml-io/zenml): AI platform for production ML, LLM, and agent pipelines with orchestration, tracking, and deployment workflows.
- [Guardrails](https://github.com/guardrails-ai/guardrails): Framework for validating LLM outputs and enforcing safety, quality, and structured response checks.
- [Plano](https://github.com/katanemo/plano): AI-native proxy and data plane for agentic applications with routing, safety, orchestration, and observability.
- [AgentSight](https://github.com/eunomia-bpf/agentsight): eBPF-based system-level tracing for observing AI agent execution without application instrumentation.
- [AgentOps](https://github.com/AgentOps-AI/agentops): Python SDK for monitoring AI agents, tracking LLM costs, benchmarking runs, and integrating with common agent frameworks.
- [Portkey AI Gateway](https://github.com/Portkey-AI/gateway): AI gateway for routing LLM traffic, applying guardrails, and centralizing model access for production applications.

## AIOps

- [Netdata](https://github.com/netdata/netdata): Distributed real-time monitoring for infrastructure metrics, visualization, and alerting.
- [Apache HertzBeat](https://github.com/apache/hertzbeat): Apache real-time observability and monitoring system with agentless collection, alerting, status pages, and AI-assisted operations.
- [PostHog](https://github.com/PostHog/posthog): Open-source product analytics platform for user behavior tracking and product metrics.
- [SREWorks](https://github.com/alibaba/SREWorks): Cloud-native DataOps and AIOps platform for operating Kubernetes-based applications and infrastructure.

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
- [trpc-agent-go](https://github.com/trpc-group/trpc-agent-go): Go framework for production agent systems with graph workflows, tools, memory, evaluation, and observability.

## DataOps

- [Dagster](https://dagster.io/): Data orchestration platform for modeling data assets and managing the data lifecycle.
- [Apache NiFi](https://nifi.apache.org/): Visual dataflow orchestration for routing, transforming, and coordinating data across systems.
- [DataHub](https://github.com/datahub-project/datahub): Metadata platform for data discovery, lineage, governance, and observability across modern data and AI stacks.
- [OpenMetadata](https://github.com/open-metadata/OpenMetadata): Unified metadata platform for data discovery, lineage, governance, and data observability.
- [Great Expectations](https://github.com/great-expectations/great_expectations): Data quality framework for validating datasets, documenting expectations, and catching pipeline regressions.
- [Soda Core](https://github.com/sodadata/soda-core): Data contracts and quality checks engine for validating data pipelines in modern data stacks.
- [Elementary](https://github.com/elementary-data/elementary): dbt-native data observability platform for monitoring pipelines, tests, freshness, and anomalies.
- [OpenLineage](https://github.com/OpenLineage/OpenLineage): Open standard and tooling for collecting lineage metadata across data pipelines and platforms.
- [Marquez](https://github.com/MarquezProject/marquez): Metadata service for collecting, aggregating, and visualizing data lineage across jobs and datasets.
- [Temporal](https://github.com/temporalio/temporal): Durable execution platform for building reliable workflows, background jobs, and long-running business processes.
- [Kestra](https://github.com/kestra-io/kestra): Event-driven orchestration and scheduling platform for declarative data, infrastructure, and operational workflows.

### Streaming Operations

- [Kafbat UI](https://github.com/kafbat/kafka-ui): Open-source web UI for managing Apache Kafka clusters, topics, consumers, schemas, and Kafka Connect.
- [Apache SeaTunnel](https://github.com/apache/seatunnel): Distributed data integration platform for high-volume batch and streaming data movement.

## FinOps

- [Infracost](https://github.com/infracost/infracost): Cloud cost forecasting tool for Terraform and Kubernetes cost estimates.
- [kubecost](https://kubecost.com/): Kubernetes cost management and monitoring platform.
- [OpenCost](https://opencost.io/): Open-source tool for tracking and allocating cloud costs in Kubernetes environments.
- [OptScale](https://github.com/hystax/optscale): Open-source FinOps and cloud cost optimization platform for AWS, Azure, GCP, Alibaba Cloud, and Kubernetes.
- [Cloud Custodian](https://github.com/cloud-custodian/cloud-custodian): Policy-as-code rules engine for cloud governance, cost optimization, and automated resource actions.
- [KubeStellar Console](https://github.com/kubestellar/console): Multi-cluster Kubernetes dashboard with AI-powered operations, real-time observability, and CNCF project integrations across edge and cloud clusters.

## Observability

- [Prometheus](https://github.com/prometheus/prometheus): Monitoring system and time-series database widely used for cloud-native metrics and alerting.
- [VictoriaMetrics](https://github.com/VictoriaMetrics/VictoriaMetrics): Fast, cost-efficient time-series database and monitoring stack for Prometheus-compatible metrics at scale.
- [Grafana Mimir](https://github.com/grafana/mimir): Horizontally scalable, multi-tenant long-term storage backend for Prometheus metrics.
- [Grafana Tempo](https://github.com/grafana/tempo): Distributed tracing backend for high-volume trace storage with minimal indexing overhead.
- [Perses](https://github.com/perses/perses): CNCF observability visualization project for building dashboards across Prometheus, Tempo, Loki, and related data sources.
- [Grafana Loki](https://github.com/grafana/loki): Log aggregation system designed to index labels efficiently and integrate with Grafana.
- [OpenTelemetry Collector](https://github.com/open-telemetry/opentelemetry-collector): Vendor-neutral collector for receiving, processing, and exporting telemetry data.
- [SigNoz](https://github.com/SigNoz/signoz): OpenTelemetry-native observability platform combining metrics, traces, logs, dashboards, and alerts.
- [Jaeger](https://github.com/jaegertracing/jaeger): CNCF distributed tracing platform for monitoring and troubleshooting microservices.
- [Vector](https://github.com/vectordotdev/vector): High-performance observability data pipeline for collecting, transforming, and routing logs and metrics.
- [Grafana Alloy](https://github.com/grafana/alloy): OpenTelemetry Collector distribution with programmable pipelines for collecting, processing, and forwarding observability signals.
- [Pixie](https://github.com/pixie-io/pixie): Kubernetes-native observability platform that uses eBPF to capture metrics, events, traces, and network telemetry without manual instrumentation.
- [Parca](https://github.com/parca-dev/parca): Continuous profiling platform for analyzing CPU and memory usage over time to improve performance, reliability, and infrastructure efficiency.
- [Kepler](https://github.com/sustainable-computing-io/kepler): Kubernetes power and energy exporter for measuring container, pod, and node energy consumption with Prometheus.
- [Inspektor Gadget](https://github.com/inspektor-gadget/inspektor-gadget): eBPF-based inspection toolkit for collecting low-level Kubernetes and Linux operational telemetry.
- [Robusta](https://github.com/robusta-dev/robusta): Kubernetes alert enrichment and automation platform for Prometheus alerts, runbooks, and remediation workflows.
- [Coroot](https://github.com/coroot/coroot): Open-source observability and APM platform with metrics, logs, traces, profiling, SLOs, and AI-assisted root-cause analysis.

## Kubernetes Operations

- [Cilium](https://github.com/cilium/cilium): eBPF-based Kubernetes networking, security, and observability platform.
- [Headlamp](https://github.com/kubernetes-sigs/headlamp): Extensible Kubernetes web UI for cluster visibility, resource management, and operational plugins.
- [cert-manager](https://github.com/cert-manager/cert-manager): Kubernetes-native certificate management controller for issuing and renewing TLS certificates.
- [KEDA](https://github.com/kedacore/keda): Kubernetes event-driven autoscaler for scaling workloads from external metrics and event sources.
- [Velero](https://github.com/velero-io/velero): Kubernetes backup, restore, and migration tool for cluster resources and persistent volumes.
- [External Secrets Operator](https://github.com/external-secrets/external-secrets): Kubernetes operator that syncs secrets from external secret managers into Kubernetes Secrets.
- [Reloader](https://github.com/stakater/Reloader): Kubernetes controller that triggers rolling workload restarts when referenced ConfigMaps or Secrets change.
- [Karpenter](https://github.com/kubernetes-sigs/karpenter): Flexible Kubernetes node autoscaler for improving cluster efficiency and workload scheduling.
- [Koordinator](https://github.com/koordinator-sh/koordinator): Kubernetes scheduling system for workload colocation, resource optimization, and cost-aware cluster operations.
- [Capsule](https://github.com/projectcapsule/capsule): Kubernetes multi-tenancy framework that lets platform teams delegate namespaces with policy-based tenant boundaries.
- [vCluster](https://github.com/loft-sh/vcluster): Virtual Kubernetes clusters that run inside namespaces for multi-tenancy, isolation, and platform engineering workflows.
- [Chaos Mesh](https://github.com/chaos-mesh/chaos-mesh): Kubernetes-native chaos engineering platform for testing system resilience under controlled failures.
- [Goldilocks](https://github.com/FairwindsOps/goldilocks): Kubernetes resource recommendation dashboard that helps tune workload requests and limits from VPA insights.
- [Glasskube](https://github.com/glasskube/glasskube): Kubernetes package manager with GUI and CLI support for dependency-aware, GitOps-ready application operations.
- [Botkube](https://github.com/kubeshop/botkube): Kubernetes ChatOps assistant for monitoring clusters, surfacing events, and helping teams debug deployments.
- [mirrord](https://github.com/metalbear-co/mirrord): Kubernetes development tool that lets local processes run with cluster networking, environment, and traffic context.
- [OpenKruise](https://github.com/openkruise/kruise): CNCF Kubernetes workload automation suite for advanced application deployment, scaling, and lifecycle management.
- [kOps](https://github.com/kubernetes/kops): Production-grade Kubernetes cluster lifecycle tool for installation, upgrades, and operations across cloud environments.
- [KubeOne](https://github.com/kubermatic/kubeone): Kubernetes cluster lifecycle management tool for automating operations across cloud, on-prem, edge, and IoT environments.

## Security and Supply Chain

- [Falco](https://github.com/falcosecurity/falco): CNCF runtime security tool for detecting suspicious behavior in containers and Kubernetes.
- [Kyverno](https://github.com/kyverno/kyverno): Kubernetes-native policy engine for validation, mutation, generation, and image verification.
- [Open Policy Agent](https://github.com/open-policy-agent/opa): General-purpose policy engine for policy-as-code across Kubernetes, CI/CD, APIs, and infrastructure.
- [Gatekeeper](https://github.com/open-policy-agent/gatekeeper): Kubernetes admission controller that enforces OPA policies and audit constraints across clusters.
- [Syft](https://github.com/anchore/syft): CLI and library for generating SBOMs from container images and filesystems.
- [Grype](https://github.com/anchore/grype): Vulnerability scanner for container images and filesystems that works well with Syft-generated SBOMs.
- [Kubescape](https://github.com/kubescape/kubescape): Kubernetes security platform for risk analysis, compliance, misconfiguration scanning, and CI/CD or cluster checks.
- [Gitleaks](https://github.com/gitleaks/gitleaks): Secrets scanner for detecting hardcoded credentials in Git repositories, files, and CI/CD workflows.
- [TruffleHog](https://github.com/trufflesecurity/trufflehog): Secrets scanner that finds, verifies, and analyzes leaked credentials across Git, filesystems, CI logs, and cloud sources.
- [Prowler](https://github.com/prowler-cloud/prowler): Multi-cloud security and compliance platform for auditing AWS, Azure, GCP, Kubernetes, and SaaS environments.
- [KubeArmor](https://github.com/kubearmor/KubeArmor): Kubernetes runtime security enforcement system for least-privilege workload hardening with LSM-based policies.
- [Kubewarden](https://github.com/kubewarden/adm-controller): Kubernetes admission policy engine that runs WebAssembly policies for policy-as-code governance.
- [cosign](https://github.com/sigstore/cosign): Sigstore tool for signing and verifying container images, blobs, and software artifacts with transparency log support.
- [SLSA GitHub Generator](https://github.com/slsa-framework/slsa-github-generator): GitHub Actions workflows for generating SLSA provenance for builds and release artifacts.
- [Chainloop](https://github.com/chainloop-dev/chainloop): Software supply-chain control plane for collecting SDLC evidence, attestations, SBOMs, VEX, SARIF, and policy checks.
- [SafeDep vet](https://github.com/safedep/vet): Policy-as-code tool for detecting malicious, vulnerable, or risky open-source package dependencies.
- [OSV-Scanner](https://github.com/google/osv-scanner): Vulnerability scanner that uses OSV.dev data to find known vulnerabilities across source, lockfiles, SBOMs, and container images.
- [OpenSSF Scorecard](https://github.com/ossf/scorecard): Automated security health checker for open-source projects, covering dependency, CI/CD, branch protection, and vulnerability hygiene signals.
- [GUAC](https://github.com/guacsec/guac): Software supply-chain graph that aggregates SBOMs, SLSA attestations, vulnerabilities, and dependency metadata for risk analysis.
- [ORT](https://github.com/oss-review-toolkit/ort): Toolkit for automating open-source compliance checks across dependencies, licenses, copyrights, vulnerabilities, and SBOM generation.
- [CycloneDX CLI](https://github.com/CycloneDX/cyclonedx-cli): Command-line tool for validating, converting, merging, and diffing CycloneDX SBOMs and related formats.
- [Dependency-Track](https://github.com/DependencyTrack/dependency-track): Component analysis platform for tracking SBOMs, vulnerabilities, licenses, and software supply-chain risk.

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
- [Argo Rollouts](https://github.com/argoproj/argo-rollouts): Kubernetes progressive delivery controller for blue-green, canary, and experiment-based deployments.
- [argo-workflows](https://github.com/argoproj/argo-workflows): Kubernetes-native workflow engine.
- [Tekton](https://tekton.dev/): Kubernetes-native CI/CD framework with flexible task orchestration.
- [Flux](https://fluxcd.io/): Popular Kubernetes GitOps toolkit.
- [PipeCD](https://github.com/pipe-cd/pipecd): CNCF continuous delivery platform for applications, infrastructure, and platform operations across multiple deployment targets.

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

### Feature Management and Experimentation

- [GrowthBook](https://github.com/growthbook/growthbook): Open-source feature flagging, experimentation, and product analytics platform for safer progressive delivery.
- [Flagsmith](https://github.com/Flagsmith/flagsmith): Open-source feature flag and remote configuration service for self-hosted or managed release control.

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
- [Atlantis](https://github.com/runatlantis/atlantis): Pull request automation for Terraform workflows, plans, applies, and collaborative infrastructure reviews.

### Identity and Access Management (IAM)

Trusting is hard. Knowing who to trust is even harder.

- [keycloak](https://github.com/keycloak/keycloak): Open-source IAM for modern applications and services.
- [OpenBao](https://github.com/openbao/openbao): Open-source secrets management system for storing and distributing secrets, certificates, and keys.
- [oauth2-proxy](https://github.com/oauth2-proxy/oauth2-proxy): Lightweight OAuth2 reverse proxy for Google, Azure, OpenID Connect, and more, with simple authorization checks.
- [zitadel](https://github.com/zitadel/zitadel): Open-source IAM for modern applications and services, focused on simplicity.
- [Casdoor](https://github.com/casdoor/casdoor): Open-source identity management platform supporting OAuth 2.0, OIDC, and SAML.
- [dexidp/dex](https://github.com/dexidp/dex): Lightweight pluggable OpenID Connect (OIDC) and OAuth 2.0 provider.
- [pomerium](https://github.com/pomerium/pomerium): Identity-aware proxy with richer access-control capabilities.

### Internal Developer Platform (IDP)

An internal developer platform is more than a pile of tools; it is not just another management console or dashboard.

- [backstage](https://github.com/backstage/backstage): Open platform for building developer portals that help teams build, deploy, and maintain software.
- [Kratix](https://github.com/syntasso/kratix): Framework for building platform APIs that let teams compose and operate internal platforms on Kubernetes.
- [OpenChoreo](https://github.com/openchoreo/openchoreo): Open-source developer platform for Kubernetes with a Backstage-powered portal, CI/CD, GitOps, observability, and platform abstractions.
- [KubeVela](https://github.com/kubevela/kubevela): CNCF application delivery platform for managing Kubernetes workloads across hybrid and multi-cluster environments.
- [Score](https://github.com/score-spec/spec): Platform-agnostic workload specification for describing services once and generating environment-specific platform configuration.
- [Superplane](https://github.com/superplanehq/superplane): Open-source control plane for platform engineering workflows across services, pipelines, and environments.

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
- [Tracetest](https://github.com/kubeshop/tracetest): OpenTelemetry-based trace testing tool for validating distributed workflows and observability instrumentation.

## License

This document is licensed under [CC BY-NC 4.0][].

[CC BY-NC 4.0]: https://creativecommons.org/licenses/by-nc/4.0/
