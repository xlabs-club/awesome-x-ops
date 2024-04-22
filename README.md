# awesome-x-ops

Awesome for any ops.

一些关于 AIOps、DataOps、DevOps、GitOps、FinOps、Platform Engineering 的优秀软件、博客，以及配套工具技术。

## AIOps

## DataOps

## FinOps

## Platform Engineering 平台工程

平台工程技术栈和依赖工具链合集。

### API Management

- [usebruno/bruno](https://github.com/usebruno/bruno) - Bruno 是一个快速且 Git 友好的开源 API 客户端，旨在彻底改变以 Postman、Insomnia 和类似工具为代表的现状。可以使用 git 来协作处理 API 集合。
- [grafana/k6](https://github.com/grafana/k6) - 使用 Go 和 JavaScript 的现代负载测试工具。

### CI/CD

- [argo-workflows](https://github.com/argoproj/argo-workflows) - 基于 Kubernetes 的云原生工作流引擎，是一个 Engine。

### Code Service

- [OpenRewrite](https://docs.openrewrite.org) - 自动化大规模代码重构工具，进行代码分析、代码风格一致、框架迁移升级。
- [reviewdog](https://github.com/reviewdog) - 自动代码审查和分析工具，支持所有语言。

### Event Mesh

### IaC

Infrastructure as Code，基础设施即代码，是通过代码而非手动流程来管理和配置基础设施的方法。

- [OpenTofu](https://github.com/opentofu/opentofu) - 开源 IaC 工具，OpenTofu 是由社区驱动的 Terraform 的一个分支，并由 Linux 基金会管理。
- [Crossplane](https://github.com/crossplane/crossplane) - Crossplane 是一个开源的 Kubernetes 插件，它允许平台团队组装来自多个供应商的基础设施，并向应用程序团队公开更高级别的自助服务 API，而不需要编写任何代码。
- [Pulumi](https://github.com/pulumi/pulumi) - 使用熟悉的语言在任何云上直观地构建基础设施，支持任何编程语言的 IaC 工具。
- [helmfile](https://github.com/helmfile) - Helmfile 是一个声明式 Helm Chart 编排和部署工具。
- [sops](https://github.com/getsops/sops) - sops 是加密文件的编辑器，支持 YAML、JSON、ENV、INI 和 BINARY 格式，并可使用 AWS KMS、GCP KMS、Azure Key Vault、age 和 PGP 进行加密。
- [bitnami/sealed-secrets](https://github.com/bitnami-labs/sealed-secrets) - Sealed Secrets 以安全的方式提供声明式 Kubernetes 秘密管理。加密后存放到任何地方比如 Git，在 Kubernetes 集群中通过 Controller 自动解密。

### Identity and Access Management(IAM)

Trusting is hard. Knowing who to trust, even harder. 信任是困难的。知道该信任谁，更难。

- [keycloak](https://github.com/keycloak/keycloak) - keycloak 是一个开源的、面向现代应用和服务的 IAM 软件。
- [zitadel](https://github.com/zitadel/zitadel) - zitadel 是一个开源的、面向现代应用和服务的 IAM 软件，主打简单。
- [dexidp/dex](https://github.com/dexidp/dex) - 插件化的 OpenID Connect (OIDC) 和 OAuth 2.0 提供商，主要是轻，很简单。
- [oauth2-proxy](https://github.com/oauth2-proxy/oauth2-proxy) - 一个轻量级 OAuth2 反向代理，支持 Google、Azure、OpenID Connect 和更多身份提供商的身份验证，同时支持简单的权限校验。
- [pomerium](https://github.com/pomerium/pomerium) - 一个轻量级 OAuth2 反向代理，支持 Google、Azure、OpenID Connect 和更多身份提供商的身份验证，同时支持相对复杂的权限校验。

### IDP

Internal Developer Platform(IDP), 内部开发者平台开源软件。

- [backstage](https://github.com/backstage/backstage) - Backstage 是一个构建开发者门户的开放平台，旨在帮助团队构建、部署和维护软件。

### Virtual Machines

一些轻量级虚拟化工具，通过虚拟机协助搭建 K8S、容器云平台，便于日常调试。

- [lima](https://github.com/lima-vm/lima) - Lima 能够运行具有自动文件共享和端口转发功能的 Linux 虚拟机，支持模拟异构虚拟机。
- [multipass](https://github.com/canonical/multipass) - Ubuntu 出品轻量级虚拟化工具。

## License

本文档采用 [CC BY-NC 4.0][] 许可协议。

[CC BY-NC 4.0]: https://creativecommons.org/licenses/by-nc/4.0/
