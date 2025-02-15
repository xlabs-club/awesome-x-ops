# awesome-x-ops

Awesome for any ops.

一些关于 AI、DataOps、DevOps、GitOps、FinOps、Platform Engineering 的优秀软件、博客，以及配套工具技术。

## AIOps 智能运维

- [NetData](https://github.com/netdata/netdata)：分布式实时监控系统，提供基础设施指标收集、可视化和告警功能。
- [PostHog](https://github.com/PostHog/posthog)：开源产品分析平台，支持用户行为追踪和产品指标分析。

## Agentic Workflow 智能体工作流

- [AutoGPT](https://github.com/Significant-Gravitas/Auto-GPT)：自主 AI 代理框架，能够自主分解和执行复杂任务。
- [LangChain](https://github.com/langchain-ai/langchain)：构建 LLM 驱动应用的开发框架，支持智能体工作流编排。
- [crewAI](https://github.com/joaomdmoura/crewAI)：面向协作式 AI 代理的框架，支持角色定义和任务编排。
- [Dify](https://github.com/langgenius/dify)：开源的 LLM 应用开发平台，支持可视化 Agent 工作流编排和 AI 应用部署。
- [Flowise](https://github.com/FlowiseAI/Flowise)：低代码 LLM 工作流编排工具，支持可视化构建 AI 应用链。
- [Langflow](https://github.com/langflow-ai/langflow)：LangChain 的图形化版本，支持拖拽式构建 LLM 工作流。
- [BentoML](https://github.com/bentoml/BentoML)：开源模型服务平台，支持多框架模型部署和 AI 应用编排。
- [Haystack](https://github.com/deepset-ai/haystack)：可扩展的问答系统框架，支持自定义 AI 工作流构建。
- [LlamaIndex](https://github.com/run-llama/llama_index)：LLM 数据框架，支持结构化数据检索和增强。

## DataOps

- [Apache NiFi](https://nifi.apache.org/)：可视化数据流编排工具，支持数据路由、转换和系统间协调。
- [Dagster](https://dagster.io/)：数据编排平台，支持数据资产建模和全生命周期管理。

## FinOps

- [kubecost](https://kubecost.com/)：Kubernetes 成本管理与监控工具。
- [OpenCost](https://opencost.io/)：一个开源工具，用于跟踪和分配 Kubernetes 环境的云成本。
- [Infracost](https://github.com/infracost/infracost)：云成本预测工具，支持 Terraform 和 Kubernetes 成本估算。

## Platform Engineering 平台工程

平台工程技术栈和工具链合集。

### API Management Tools

- [Bruno](https://github.com/usebruno/bruno)：Bruno 是一个快速且 Git 友好的开源 API 客户端，旨在彻底改变以 Postman、Insomnia 和类似工具为代表的现状。使用 Git 来协作处理 API 集合，使用客户端或 cli 命令行来执行 API 调用。
- [Hoppscotch](https://github.com/hoppscotch/hoppscotch)：轻量级 API 开发工具套件，支持 REST、GraphQL 和 WebSocket。

### Artifact 制品管理

- [ORAS](https://github.com/oras-project/oras)：一个将任意内容存储为 OCI 格式容器镜像的工具。
- [Skopeo](https://github.com/containers/skopeo)：用于检查、复制和签署容器镜像的开源工具，镜像同步和拷贝的利器。
- [Harbor](https://github.com/goharbor/harbor)：企业级容器镜像仓库，支持安全扫描和访问控制。
- [Nexus Repository](https://github.com/sonatype/nexus-public)：通用制品管理工具，支持 Maven、NPM、Docker 等格式。

### CI/CD

- [argo-workflows](https://github.com/argoproj/argo-workflows)：基于 Kubernetes 的云原生工作流引擎，是一个 Engine。
- [argo-cd](https://argo-cd.readthedocs.io/)：相当流行的一款用于 Kubernetes 的声明式 GitOps CD 工具。
- [Flux](https://fluxcd.io/)：相当流行的又一款 Kubernetes 的 GitOps 工具包。
- [Apache Airflow](https://airflow.apache.org/)：一个开源的数据管道工作流编排工具。
- [Jenkins](https://www.jenkins.io/)：一个开源的 CI/CD 自动化服务器，有丰富的插件，重量级软件。
- [Tekton](https://tekton.dev/)：Kubernetes 原生 CI/CD 框架，提供灵活的任务编排能力。

### Code Service

- [OpenRewrite](https://docs.openrewrite.org)：自动化大规模代码重构工具，进行代码分析、代码风格一致、框架迁移升级。
- [reviewdog](https://github.com/reviewdog)：自动代码审查和分析工具，支持所有语言。
- [Dependency Track](https://dependencytrack.org/)：开源软件组件合规分析检测平台，帮助识别和管理供应链风险，支持 SBOM 分析、License 检查。
- [Hyades](https://github.com/DependencyTrack/hyades)：下一代软件供应链安全平台，准备替代 Dependency-Track，静待发布稳定版本。
- [SonarQube](https://github.com/SonarSource/sonarqube)：代码质量持续检测平台，支持 27+编程语言。
- [Trivy](https://github.com/aquasecurity/trivy)：全面的容器/代码安全扫描工具，支持 SBOM 生成。

### Event Mesh

- [CloudEvents](https://cloudevents.io/)：一个事件规范，用于实现事件驱动系统的互操作性。
- [Apache Event Mesh](https://eventmesh.apache.org/)：分布式事件中间件，支持多种消息协议和事件流管理。
- [Argo Events](https://argoproj.github.io/argo-events/)：一个事件驱动的 Kubernetes 工作流编排工具。

### Infrastructure as Code(IaC)

Infrastructure as Code，基础设施即代码，是通过代码而非手动流程来管理和配置基础设施的方法。

- [Pulumi](https://github.com/pulumi/pulumi)：使用熟悉的语言在任何云上直观地构建基础设施，支持任何编程语言的 IaC 工具。
- [OpenTofu](https://github.com/opentofu/opentofu)：开源 IaC 工具，OpenTofu 是由社区驱动的 Terraform 的一个分支，并由 Linux 基金会管理。
- [Crossplane](https://github.com/crossplane/crossplane)：Crossplane 是一个开源的 Kubernetes 插件，它允许平台团队组装来自多个供应商的基础设施，并向应用程序团队公开更高级别的自助服务 API，而不需要编写任何代码。
- [helmfile](https://github.com/helmfile)：Helmfile 是一个声明式 Helm Chart 编排和部署工具。
- [sops](https://github.com/getsops/sops)：sops 是加密文件的编辑器，支持 YAML、JSON、ENV、INI 和 BINARY 格式，并可使用 AWS KMS、GCP KMS、Azure Key Vault、age 和 PGP 进行加密。
- [bitnami/sealed-secrets](https://github.com/bitnami-labs/sealed-secrets)：Sealed Secrets 以安全的方式提供声明式 Kubernetes 秘密管理。加密后存放到任何地方比如 Git，在 Kubernetes 集群中通过 Controller 自动解密。
- [Terragrunt](https://github.com/gruntwork-io/terragrunt)：Terraform 的增强工具，提供 DRY 配置和远程状态管理。
- [Checkov](https://github.com/bridgecrewio/checkov)：基础设施即代码静态分析工具，支持安全合规检查。

### Identity and Access Management(IAM)

Trusting is hard. Knowing who to trust, even harder. 信任是困难的。知道该信任谁，更难。

- [keycloak](https://github.com/keycloak/keycloak)：keycloak 是一个开源的、面向现代应用和服务的 IAM 软件。
- [zitadel](https://github.com/zitadel/zitadel)：zitadel 是一个开源的、面向现代应用和服务的 IAM 软件，主打简单。
- [dexidp/dex](https://github.com/dexidp/dex)：插件化的 OpenID Connect (OIDC) 和 OAuth 2.0 提供商，主要是轻，很简单。
- [oauth2-proxy](https://github.com/oauth2-proxy/oauth2-proxy)：一个轻量级 OAuth2 反向代理，支持 Google、Azure、OpenID Connect 和更多身份提供商的身份验证，同时支持简单的权限校验。
- [pomerium](https://github.com/pomerium/pomerium)：一个轻量级 OAuth2 反向代理，支持 Google、Azure、OpenID Connect 和更多身份提供商的身份验证，同时支持相对复杂的权限校验。
- [Casdoor](https://github.com/casdoor/casdoor)：开源身份管理平台，支持 OAuth 2.0/OIDC/SAML 协议。

### Internal Developer Platform(IDP)

内部开发者平台，不仅仅是一大堆工具的集合，不是再建一个管理平台 Console 或者 Dashboard。

- [backstage](https://github.com/backstage/backstage)：Backstage 是一个构建开发者门户的开放平台，旨在帮助团队构建、部署和维护软件。

### IaaS Tools

一些轻量级虚拟化工具，通过虚拟机协助搭建 K8S、容器云平台，便于日常调试。

- [lima](https://github.com/lima-vm/lima)：Lima 能够运行具有自动文件共享和端口转发功能的 Linux 虚拟机，支持模拟异构虚拟机。
- [multipass](https://github.com/canonical/multipass)：Ubuntu 出品轻量级虚拟化工具。
- [Vagrant](https://github.com/hashicorp/vagrant)：跨平台虚拟机管理工具，支持多种虚拟化后端。
- [Minikube](https://github.com/kubernetes/minikube)：本地 Kubernetes 集群部署工具。

### Tester Tools

专为测试人员准备的工具集。

- [grafana/k6](https://github.com/grafana/k6)：使用 Go 和 JavaScript 的现代负载测试工具，也可以用来作为 API 管理和测试工具。
- [googletest](https://github.com/google/googletest)：Google Testing and Mocking Framework。
- [JMeter](https://github.com/apache/jmeter)：Java 编写的性能测试工具，支持多种协议。
- [Selenium](https://github.com/SeleniumHQ/selenium)：浏览器自动化框架，支持 Web 应用测试。

## License

本文档采用 [CC BY-NC 4.0][] 许可协议。

[CC BY-NC 4.0]: https://creativecommons.org/licenses/by-nc/4.0/
