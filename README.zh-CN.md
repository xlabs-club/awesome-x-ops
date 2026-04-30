# awesome-x-ops

面向现代 X-Ops 的开源工具地图：覆盖 AI Ops、LLM/Agent 可观测性、平台工程、GitOps、DataOps、FinOps、DevSecOps，以及生产级运维工具链。

语言：[English](README.md) | 简体中文

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![License: CC BY-NC 4.0](https://img.shields.io/badge/license-CC%20BY--NC%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc/4.0/)

## 为什么做 awesome-x-ops？

今天的运维不再只是基础设施监控或 CI/CD 胶水。现代团队需要一张实用地图，把 AI 原生应用、LLM 可观测性、平台工程、软件交付、云成本、安全和开发者体验串起来。

本清单关注能帮助团队构建、运行、观测、保护和优化生产系统的工具。

## 精选地图

- [LLM 和 Agent 可观测性栈](#llm-和-agent-可观测性)：面向 LLM 与 Agent 系统的追踪、Prompt 监控、评估、反馈和生产遥测。
- [平台工程栈](#platform-engineering-平台工程)：内部开发者平台、IAM、IaC、制品、API 工具、CI/CD 和测试。
- [GitOps 与 Kubernetes 运维栈](#kubernetes-operations-kubernetes-运维)：集群网络、弹性伸缩、部署和运行时运维。
- [FinOps 栈](#finops)：云和 Kubernetes 成本可见性、分摊与预测。
- [DevSecOps 与供应链安全栈](#security-and-supply-chain-安全与供应链)：策略、运行时安全、SBOM、扫描和软件供应链风险管理。
- [DataOps 栈](#dataops)：数据流、编排和数据资产生命周期工具。

## 适合谁？

- 构建内部开发者平台的平台工程团队。
- 正在升级运维体系的 DevOps、SRE 和基础设施团队。
- 需要在生产环境运行 LLM、RAG 和 Agent 应用的 AI 工程团队。
- 希望在采购或自研前评估可靠开源选项的工程负责人。
- 希望让生产级运维工具被更多人发现的开源维护者。

## 收录原则

- 内容保持简洁、高效、准确、相关。
- 有可靠项目仓库时，优先使用 GitHub 链接。
- 只收录经过验证、可靠、优秀的项目。
- 已存在或等价覆盖的项目必须忽略。
- 可按需要新增或优化分类，但不加入无关内容。
- 优先收录生产级开源项目，不收录浅层 demo、弃坑实验或纯营销页面。

## 增长与贡献

本项目目标是成为现代 X-Ops 的实用开源地图。欢迎贡献能提升准确性、覆盖度或导航体验的内容，但不要把它变成链接垃圾场。

- 通过 [Issues](https://github.com/xlabs-club/awesome-x-ops/issues) 推荐缺失项目。
- 按 [CONTRIBUTING.md](CONTRIBUTING.md) 提交聚焦的 Pull Request。
- 描述保持简短，并说明项目为什么属于运维或平台工程上下文。

## LLM 和 Agent 可观测性

用于追踪、评估、调试和生产化运行 LLM、RAG 与 Agent 应用的工具。

- [Langfuse](https://github.com/langfuse/langfuse)：开源 LLM 工程平台，支持链路追踪、Prompt 管理、评估和指标分析。
- [OpenLLMetry](https://github.com/traceloop/openllmetry)：基于 OpenTelemetry 的 LLM 应用和 Agent 工作流可观测性工具。
- [Arize Phoenix](https://github.com/Arize-ai/phoenix)：面向 LLM、RAG 和机器学习系统的开源可观测与评估平台。
- [Helicone](https://github.com/Helicone/helicone)：开源 LLM 可观测平台，支持用量、延迟、成本、缓存和请求日志分析。
- [DeepEval](https://github.com/confident-ai/deepeval)：LLM 评估框架，适合在 CI 或生产流程中测试 RAG、Agent 和模型输出。
- [Ragas](https://github.com/explodinggradients/ragas)：面向 RAG 流水线和 LLM 应用的评估框架。
- [LiteLLM](https://github.com/BerriAI/litellm)：兼容 OpenAI API 的 LLM 网关，支持路由、预算、日志和多模型供应商抽象。

## AIOps 智能运维

- [Netdata](https://github.com/netdata/netdata)：分布式实时监控系统，提供基础设施指标收集、可视化和告警功能。
- [PostHog](https://github.com/PostHog/posthog)：开源产品分析平台，支持用户行为追踪和产品指标分析。

## Agentic Workflow 智能体工作流

- [AutoGPT](https://github.com/Significant-Gravitas/Auto-GPT)：自主 AI Agent 框架，能够分解并执行复杂任务。
- [LangChain](https://github.com/langchain-ai/langchain)：构建 LLM 驱动应用的开发框架，支持 Agent 工作流编排。
- [crewAI](https://github.com/crewAIInc/crewAI)：面向协作式 AI Agent 的框架，支持角色定义和任务编排。
- [Dify](https://github.com/langgenius/dify)：开源 LLM 应用开发平台，支持可视化 Agent 工作流和 AI 应用部署。
- [Flowise](https://github.com/FlowiseAI/Flowise)：低代码 LLM 工作流编排工具，支持可视化构建 AI 应用链。
- [Langflow](https://github.com/langflow-ai/langflow)：LangChain 风格的图形化构建器，支持拖拽式构建 LLM 工作流。
- [BentoML](https://github.com/bentoml/BentoML)：开源模型服务平台，支持多框架模型部署和 AI 应用编排。
- [Haystack](https://github.com/deepset-ai/haystack)：可扩展的问答系统框架，支持自定义 AI 工作流构建。
- [LlamaIndex](https://github.com/run-llama/llama_index)：LLM 数据框架，支持结构化数据检索和增强。

## DataOps

- [Apache NiFi](https://nifi.apache.org/)：可视化数据流编排工具，支持数据路由、转换和系统间协调。
- [Dagster](https://dagster.io/)：数据编排平台，支持数据资产建模和全生命周期管理。

## FinOps

- [kubecost](https://kubecost.com/)：Kubernetes 成本管理与监控工具。
- [OpenCost](https://opencost.io/)：开源工具，用于跟踪和分摊 Kubernetes 环境中的云成本。
- [Infracost](https://github.com/infracost/infracost)：云成本预测工具，支持 Terraform 和 Kubernetes 成本估算。
- [KubeStellar Console](https://github.com/kubestellar/console)：多集群 Kubernetes 控制台，提供 AI 辅助运维、实时可观测性和边缘/云集群管理能力。

## Observability 可观测性

- [OpenTelemetry Collector](https://github.com/open-telemetry/opentelemetry-collector)：厂商中立的遥测数据采集器，支持接收、处理和导出指标、日志与链路数据。
- [Prometheus](https://github.com/prometheus/prometheus)：云原生广泛采用的监控系统和时序数据库，适用于指标采集与告警。
- [Grafana Loki](https://github.com/grafana/loki)：面向标签索引设计的日志聚合系统，可与 Grafana 深度集成。

## Kubernetes Operations Kubernetes 运维

- [Cilium](https://github.com/cilium/cilium)：基于 eBPF 的 Kubernetes 网络、安全和可观测性平台。
- [Karpenter](https://github.com/kubernetes-sigs/karpenter)：灵活的 Kubernetes 节点自动扩缩容工具，用于提升集群效率和调度效果。

## Security and Supply Chain 安全与供应链

- [Kyverno](https://github.com/kyverno/kyverno)：Kubernetes 原生策略引擎，支持校验、变更、生成和镜像验证。
- [Falco](https://github.com/falcosecurity/falco)：CNCF 运行时安全工具，用于检测容器和 Kubernetes 中的可疑行为。

## Platform Engineering 平台工程

平台工程技术栈和工具链合集。

### API Management API 管理

- [Bruno](https://github.com/usebruno/bruno)：快速且 Git 友好的开源 API 客户端，支持管理 API 集合并通过桌面端或 CLI 执行调用。
- [Hoppscotch](https://github.com/hoppscotch/hoppscotch)：轻量级 API 开发工具套件，支持 REST、GraphQL 和 WebSocket。

### Artifact 制品管理

- [ORAS](https://github.com/oras-project/oras)：将任意内容存储为 OCI Artifact 的工具。
- [Skopeo](https://github.com/containers/skopeo)：用于检查、复制和签署容器镜像的开源工具。
- [Harbor](https://github.com/goharbor/harbor)：企业级容器镜像仓库，支持安全扫描和访问控制。
- [Nexus Repository](https://github.com/sonatype/nexus-public)：通用制品仓库，支持 Maven、npm、Docker 等格式。

### CI/CD

- [argo-workflows](https://github.com/argoproj/argo-workflows)：Kubernetes 原生工作流引擎。
- [argo-cd](https://argo-cd.readthedocs.io/)：流行的 Kubernetes 声明式 GitOps CD 工具。
- [Flux](https://fluxcd.io/)：流行的 Kubernetes GitOps 工具包。
- [Apache Airflow](https://airflow.apache.org/)：开源工作流编排平台，常用于数据流水线。
- [Jenkins](https://www.jenkins.io/)：开源 CI/CD 自动化服务器，拥有丰富插件生态。
- [Tekton](https://tekton.dev/)：Kubernetes 原生 CI/CD 框架，提供灵活的任务编排能力。

### Code Service 代码服务

- [OpenRewrite](https://docs.openrewrite.org)：自动化大规模代码重构与现代化工具。
- [reviewdog](https://github.com/reviewdog)：自动代码审查和分析工具，支持多种语言和 linter。
- [Dependency Track](https://dependencytrack.org/)：开源软件组件分析平台，支持供应链风险、SBOM 和 License 检查。
- [Hyades](https://github.com/DependencyTrack/hyades)：下一代软件供应链安全平台，稳定后计划替代 Dependency-Track。
- [SonarQube](https://github.com/SonarSource/sonarqube)：持续代码质量平台，支持 27+ 编程语言。
- [Trivy](https://github.com/aquasecurity/trivy)：全面的容器、代码、漏洞、错误配置和 SBOM 扫描工具。

### Event Mesh 事件网格

- [CloudEvents](https://cloudevents.io/)：用于事件驱动系统互操作的事件规范。
- [Apache EventMesh](https://eventmesh.apache.org/)：分布式事件中间件，支持多种消息协议和事件流管理。
- [Argo Events](https://argoproj.github.io/argo-events/)：Kubernetes 事件驱动工作流自动化框架。

### Infrastructure as Code (IaC)

Infrastructure as Code，基础设施即代码，是通过代码而非手动流程来管理和配置基础设施的方法。

- [Pulumi](https://github.com/pulumi/pulumi)：支持使用熟悉编程语言在任意云上构建基础设施的 IaC 工具。
- [OpenTofu](https://github.com/opentofu/opentofu)：由社区驱动、Linux Foundation 治理的 Terraform 分支。
- [Crossplane](https://github.com/crossplane/crossplane)：Kubernetes 插件，让平台团队组合多云基础设施并暴露高层自助服务 API。
- [helmfile](https://github.com/helmfile)：声明式 Helm Chart 编排和部署工具。
- [sops](https://github.com/getsops/sops)：加密文件编辑器，支持 YAML、JSON、ENV、INI 和二进制文件。
- [bitnami/sealed-secrets](https://github.com/bitnami-labs/sealed-secrets)：声明式 Kubernetes Secret 管理工具，可安全地将加密 Secret 存放在 Git 中。
- [Terragrunt](https://github.com/gruntwork-io/terragrunt)：Terraform 包装工具，提供 DRY 配置和远程状态管理。
- [Checkov](https://github.com/bridgecrewio/checkov)：基础设施即代码静态分析工具，支持安全合规检查。

### Identity and Access Management (IAM)

信任很难，知道该信任谁更难。

- [keycloak](https://github.com/keycloak/keycloak)：面向现代应用和服务的开源 IAM。
- [zitadel](https://github.com/zitadel/zitadel)：面向现代应用和服务的开源 IAM，强调简单易用。
- [dexidp/dex](https://github.com/dexidp/dex)：轻量级、可插拔的 OpenID Connect (OIDC) 与 OAuth 2.0 Provider。
- [oauth2-proxy](https://github.com/oauth2-proxy/oauth2-proxy)：轻量级 OAuth2 反向代理，支持多种身份提供商和简单授权校验。
- [pomerium](https://github.com/pomerium/pomerium)：身份感知代理，提供更丰富的访问控制能力。
- [Casdoor](https://github.com/casdoor/casdoor)：开源身份管理平台，支持 OAuth 2.0、OIDC 和 SAML。

### Internal Developer Platform (IDP)

内部开发者平台不只是工具堆叠，也不只是再做一个管理控制台。

- [backstage](https://github.com/backstage/backstage)：用于构建开发者门户的开放平台，帮助团队构建、部署和维护软件。

### IaaS Tools IaaS 工具

适合本地 Kubernetes、容器平台调试的轻量级虚拟化工具。

- [lima](https://github.com/lima-vm/lima)：支持自动文件共享和端口转发的 Linux 虚拟机工具，也可模拟异构虚拟机。
- [multipass](https://github.com/canonical/multipass)：Ubuntu 出品的轻量级虚拟化工具。
- [Vagrant](https://github.com/hashicorp/vagrant)：跨平台虚拟机管理工具，支持多种虚拟化后端。
- [Minikube](https://github.com/kubernetes/minikube)：本地 Kubernetes 集群部署工具。

### Testing Tools 测试工具

面向测试工程师和质量导向平台团队的工具。

- [grafana/k6](https://github.com/grafana/k6)：使用 Go 和 JavaScript 的现代负载测试工具，也适合 API 测试流程。
- [googletest](https://github.com/google/googletest)：Google Testing and Mocking Framework。
- [JMeter](https://github.com/apache/jmeter)：Java 编写的性能测试工具，支持多种协议。
- [Selenium](https://github.com/SeleniumHQ/selenium)：浏览器自动化框架，支持 Web 应用测试。

## License 许可协议

本文档采用 [CC BY-NC 4.0][] 许可协议。

[CC BY-NC 4.0]: https://creativecommons.org/licenses/by-nc/4.0/
