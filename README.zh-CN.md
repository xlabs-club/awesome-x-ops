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
- [LLM 知识库](#llm-知识库)：将文档转化为 RAG 知识库、自主推理 Agent 和自维护 Wiki 的开源平台。
- [AI 基础设施](#ai-基础设施)：Web 爬取、AI 友好抽取、搜索情报和 RAG 数据采集。
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

- [LiteLLM](https://github.com/BerriAI/litellm)：兼容 OpenAI API 的 LLM 网关，支持路由、预算、日志和多模型供应商抽象。
- [Langfuse](https://github.com/langfuse/langfuse)：开源 LLM 工程平台，支持链路追踪、Prompt 管理、评估和指标分析。
- [DeepEval](https://github.com/confident-ai/deepeval)：LLM 评估框架，适合在 CI 或生产流程中测试 RAG、Agent 和模型输出。
- [Ragas](https://github.com/explodinggradients/ragas)：面向 RAG 流水线和 LLM 应用的评估框架。
- [Arize Phoenix](https://github.com/Arize-ai/phoenix)：面向 LLM、RAG 和机器学习系统的开源可观测与评估平台。
- [OpenInference](https://github.com/Arize-ai/openinference)：面向 LLM、RAG 和 Agent 应用的 OpenTelemetry 插桩与语义约定。
- [OpenLLMetry](https://github.com/traceloop/openllmetry)：基于 OpenTelemetry 的 LLM 应用和 Agent 工作流可观测性工具。
- [Helicone](https://github.com/Helicone/helicone)：开源 LLM 可观测平台，支持用量、延迟、成本、缓存和请求日志分析。
- [OpenLIT](https://github.com/openlit/openlit)：基于 OpenTelemetry 的 AI 工程平台，支持 LLM 可观测性、评估、护栏、Prompt 管理和 GPU 监控。
- [Grafana AI Observability SDK](https://github.com/grafana/sigil-sdk)：开源 SDK 与编码 Agent 插件，用于将生产环境 Agent 和 LLM 遥测数据发送到 Grafana AI observability。
- [LangWatch](https://github.com/langwatch/langwatch)：开源平台，支持 LLM 监控、评估、链路追踪和 Agent 测试。
- [Opik](https://github.com/comet-ml/opik)：开源平台，用于追踪、评估和监控 LLM 应用、RAG 系统与 Agent 工作流。
- [promptfoo](https://github.com/promptfoo/promptfoo)：开源 CLI 与平台，用于 Prompt 测试、LLM 评估、红队测试和 CI/CD 回归检查。
- [Langtrace](https://github.com/Scale3-Labs/langtrace)：基于 OpenTelemetry 的可观测平台，用于追踪、评估和监控 LLM 应用。
- [Future AGI](https://github.com/future-agi/future-agi)：可自托管平台，用于评估、观测和改进 LLM 与 AI Agent 应用。
- [CozeLoop](https://github.com/coze-dev/coze-loop)：AI Agent 优化平台，覆盖开发、调试、评估和生产监控流程。
- [Judgeval](https://github.com/JudgmentLabs/judgeval)：面向 Agent 的持续改进工具栈，结合环境数据与评估能力，持续改进并监控 Agent 行为。
- [Acontext](https://github.com/memodb-io/Acontext)：开源 AI Agent 记忆层，将可复用的 Agent 技能与上下文转化为可运营的服务。
- [Agenta](https://github.com/Agenta-AI/agenta)：开源 LLMOps 平台，支持 Prompt 管理、调试 playground、评估和可观测性。
- [abtop](https://github.com/graykode/abtop)：类似 htop 的终端监控工具，用于查看 AI 编码 Agent 会话、Token、上下文窗口、速率限制和端口。
- [agenttrace](https://github.com/luoyuctl/agenttrace)：本地优先的 TUI，用于检查 AI 编码 Agent 的成本、Token、延迟、失败和报告。
- [OpenTelemetry MCP Server](https://github.com/traceloop/opentelemetry-mcp-server)：统一的 MCP Server，可查询 Jaeger、Tempo、Traceloop 等后端的 OpenTelemetry 链路，让 AI Agent 能够调查分布式系统。
- [Kitaru](https://github.com/zenml-io/kitaru)：面向生产环境的 AI Agent 录制与回放工具，用于分析运行过程并改进 Agent 行为。
- [ax](https://github.com/Necmttn/ax)：面向 AI 编码 Agent 的本地优先遥测与记忆图，覆盖成本、工具、技能、会话和 OTLP 事件。
- [Mindwalk](https://github.com/cosmtrek/mindwalk)：可视化工具，在代码库 3D 地图上回放编码 Agent 会话，帮助调试和理解 Agent 行为。
- [TensorZero](https://github.com/tensorzero/tensorzero)：开源 LLMOps 平台，整合 LLM 网关、可观测性、评估、优化和实验能力。
- [Evidently](https://github.com/evidentlyai/evidently)：开源 ML 与 LLM 可观测性框架，支持评估、测试、监控和数据质量检查。
- [RagaAI Catalyst](https://github.com/raga-ai-hub/RagaAI-Catalyst)：面向 Agent AI 的可观测与评估 SDK，用于追踪、调试和监控多 Agent LLM 系统。
- [Pydantic Logfire](https://github.com/pydantic/logfire)：面向生产级 LLM 与 Agent 系统的 AI 可观测平台，用于链路追踪和监控。
- [Laminar](https://github.com/lmnr-ai/lmnr)：专为 AI Agent 和 LLM 应用构建的开源可观测平台。
- [whylogs](https://github.com/whylabs/whylogs)：开源数据日志库，用于 ML 和 LLM 数据画像、漂移检测和生产流水线遥测监控。
- [MLflow](https://github.com/mlflow/mlflow)：开源 AI 工程平台，用于调试、评估、监控和优化 Agent、LLM 与机器学习模型。
- [Giskard](https://github.com/Giskard-AI/giskard-oss)：面向 LLM 应用和 AI Agent 的开源评估与测试框架。
- [ZenML](https://github.com/zenml-io/zenml)：面向生产级 ML、LLM 和 Agent 流水线的 AI 平台，支持编排、追踪和部署工作流。
- [Guardrails](https://github.com/guardrails-ai/guardrails)：用于校验 LLM 输出并执行安全、质量和结构化响应检查的框架。
- [Plano](https://github.com/katanemo/plano)：面向 Agent 应用的 AI 原生代理与数据平面，支持路由、安全、编排和可观测性。
- [AgentSight](https://github.com/eunomia-bpf/agentsight)：基于 eBPF 的系统级追踪工具，无需应用插桩即可观测 AI Agent 执行过程。
- [AgentOps](https://github.com/AgentOps-AI/agentops)：用于监控 AI Agent、追踪 LLM 成本、基准测试运行并集成常见 Agent 框架的 Python SDK。
- [Portkey AI Gateway](https://github.com/Portkey-AI/gateway)：AI 网关，用于路由 LLM 流量、应用护栏，并集中管理生产应用的模型访问。
- [Traceloop Hub](https://github.com/traceloop/hub)：基于 Rust 的高性能 LLM 网关，提供统一供应商 API、OpenTelemetry 链路、Prometheus 指标和可配置请求流水线。
- [New API](https://github.com/QuantumNous/new-api)：统一 AI 模型网关，用于聚合供应商、兼容 OpenAI/Claude/Gemini API，并管理企业级模型访问。
- [Manifest](https://github.com/mnfst/manifest)：厂商无关的运行时，通过统一接口将 Agent 和 Agent 驱动框架连接到模型供应商。
- [OmniRoute](https://github.com/diegosouzapw/OmniRoute)：自托管 AI 网关，将多个模型供应商统一到一个端点，支持自动故障转移、路由、MCP/A2A，以及节省 Token 的压缩能力。
- [Otari](https://github.com/mozilla-ai/otari)：Mozilla AI 出品的开源、OpenAI 兼容 LLM 网关，一个端点支持 40+ 供应商，提供虚拟密钥、预算和使用量追踪。
- [BISHENG](https://github.com/dataelement/bisheng)：面向企业 AI 应用的开源 LLM DevOps 平台，覆盖 GenAI 工作流、RAG、Agent、模型管理、评估、数据集和可观测性。
- [OpenObserve](https://github.com/openobserve/openobserve)：开源可观测平台，覆盖日志、指标、链路、前端监控、流水线和 LLM 可观测性。
- [Kubeshark](https://github.com/kubeshark/kubeshark)：基于 eBPF 的 Kubernetes 网络可观测工具，提供 L4/L7 流量上下文、TLS 可见性，以及供 AI 辅助调查使用的 MCP 接口。
- [MCP Gateway](https://github.com/IBM/mcp-context-forge)：面向 MCP、A2A 和 API 工具的 AI 网关、注册表与代理，支持集中发现、护栏和管理。
- [NVIDIA NeMo Guardrails](https://github.com/NVIDIA-NeMo/Guardrails)：用于为基于 LLM 的对话系统加入可编程安全、对话和策略护栏的工具包。
- [Llama Guard](https://github.com/meta-llama/PurpleLlama)：Meta 开源的信任与安全工具集，用于评估和过滤 LLM 输入、输出与模型风险。
- [LLM Guard](https://github.com/protectai/llm-guard)：LLM 交互安全工具包，用于清洗输入输出、检测 Prompt 注入、拦截有害内容并降低数据泄露风险。
- [garak](https://github.com/NVIDIA/garak)：LLM 漏洞扫描器，用于探测 Prompt 注入、越狱、数据泄露、幻觉等生成式 AI 风险。
- [agentic-security](https://github.com/msoedov/agentic_security)：开源 LLM 漏洞扫描器与 AI 红队工具包，用于模糊测试和验证 LLM 护栏对抗攻击能力。
- [Superagent](https://github.com/superagent-ai/superagent)：开源 AI 安全 SDK，用于保护 LLM 应用免受 Prompt 注入、数据泄露和有害输出的影响。
- [PINT Benchmark](https://github.com/lakeraai/pint-benchmark)：开源基准测试工具，用于评估 Prompt 注入检测系统在多种攻击向量下的表现。
- [OpenEvals](https://github.com/langchain-ai/openevals)：现成的评估器集合，用于在开发和 CI 流程中测试 LLM 应用并做回归检查。
- [TruLens](https://github.com/truera/trulens)：LLM 评估与追踪框架，支持反馈函数、护栏和迭代改进工作流，适用于 LLM 实验与 AI Agent。
- [OpenCompass](https://github.com/open-compass/opencompass)：LLM 评估平台，支持 100+ 数据集上对多种模型的评测和可复现基准测试。
- [OpenAI Evals](https://github.com/openai/evals)：用于评估 LLM 和 LLM 系统的框架，提供开源基准测试注册表和评估工作流。
- [PromptWizard](https://github.com/microsoft/PromptWizard)：面向任务、由 Agent 驱动的 Prompt 优化框架，通过迭代式批评与评估改进 Prompt，适合构建可重复的 LLM 工作流。
- [Inspect AI](https://github.com/UKGovernmentBEIS/inspect_ai)：基于 MIT 许可的框架，用于构建、运行和分析可复现的大语言模型评测。
- [Envoy AI Gateway](https://github.com/envoyproxy/ai-gateway)：基于 Envoy 的 AI 网关，用于跨供应商和平台统一管理生成式 AI 服务访问。
- [Higress](https://github.com/higress-group/higress)：基于 Envoy 的 AI 原生 API 网关，用于统一 LLM 供应商访问、金丝雀路由、限流和多模型可观测。
- [Bifrost](https://github.com/maximhq/bifrost)：高性能企业级 AI 网关，支持自适应负载均衡、护栏、集群模式和 1000+ 模型接入。
- [Inference Gateway](https://github.com/inference-gateway/inference-gateway)：云原生 LLM 网关，用于统一模型供应商、路由推理流量，并在 Kubernetes 上提供 OpenTelemetry 友好的运维能力。
- [OneAIFW](https://github.com/funstory-ai/aifw)：轻量级本地 AI 防火墙，可在调用 LLM 前匿名化敏感数据，并在响应后还原。
- [Microsoft MCP Gateway](https://github.com/microsoft/mcp-gateway)：用于运维 MCP Server 的反向代理与管理层，支持会话感知路由和 Kubernetes 生命周期管理。
- [CoAI](https://github.com/coaidev/coai)：多租户 AI 平台，提供统一 LLM 网关、供应商路由、成本管理、计费和模型缓存，适合企业级部署。
- [Kong](https://github.com/Kong/kong)：云原生 API、LLM 和 MCP 网关，支持高级 AI 流量管理、多供应商路由、语义安全和丰富的插件生态。
- [Apache APISIX](https://github.com/apache/apisix)：Apache 动态 API 和 AI 网关，支持 LLM 代理、Token 限流、MCP bridge 和基于插件的 AI 流量管控。
- [LangKit](https://github.com/whylabs/langkit)：开源 LLM 监控工具包，可从 Prompt 和响应中提取信号，包括文本质量、相关性、情感分析和 Prompt 注入检测。
- [AxonHub](https://github.com/looplj/axonhub)：开源 AI 网关，支持故障转移、负载均衡、成本控制和端到端追踪，覆盖 100+ LLM 供应商。
- [MCP Gateway & Registry](https://github.com/agentic-community/mcp-gateway-registry)：企业级 MCP 网关与 AI 资产注册中心，支持 OAuth 认证、语义搜索、审计追踪，为 Agent、Skills 和 MCP Server 提供统一治理。
- [Weights & Biases](https://github.com/wandb/wandb)：AI 开发者平台，提供实验追踪、模型管理和 ML/LLM 工作流监控，覆盖从训练到生产的全流程。
- [ClearML](https://github.com/clearml/clearml)：开源 MLOps/LLMOps 平台，支持实验管理、数据流水线、编排和模型服务。
- [Helicone AI Gateway](https://github.com/Helicone/ai-gateway)：基于 Rust 构建的快速轻量 AI 网关，支持智能路由、缓存、速率限制和内置可观测性，覆盖 100+ LLM 供应商。
- [SMG](https://github.com/lightseekorg/smg)：Rust 编写的引擎无关 LLM 网关，支持 gRPC 管道、KV 缓存感知路由、WASM 插件、MCP 和多租户认证，覆盖 vLLM、TensorRT-LLM、SGLang 和云供应商。
- [EleutherAI LM Eval](https://github.com/EleutherAI/lm-evaluation-harness)：用于语言模型的标准化 few-shot 和 zero-shot 评估框架，覆盖数百个任务和基准测试。
- [Weave](https://github.com/wandb/weave)：用于追踪、评估和改进 LLM 应用的工具包，支持自动版本控制和交互式调试工作流。
- [Pezzo](https://github.com/pezzolabs/pezzo)：开源 LLMOps 平台，支持 Prompt 管理、版本控制、A/B 测试、故障排查和可观测性。
- [Latitude](https://github.com/latitude-dev/latitude-llm)：开源 AI 监控与评估平台，面向生产环境 LLM 应用，支持协作调试、数据集管理和 CI/CD 集成。
- [TraceRoot](https://github.com/traceroot-ai/traceroot)：面向 AI Agent 的开源可观测与自愈层，提供实时监控和自动修复能力。
- [SkillOpt](https://github.com/microsoft/SkillOpt)：微软开源的文本空间优化器，通过轨迹驱动的编辑和验证门控更新，为冻结参数的 LLM Agent 训练可复用的自然语言技能。
- [AgentField](https://github.com/Agent-Field/agentfield)：用于构建、运行和扩展 AI Agent 的控制平面，让 Agent 以可观测、可审计、具备身份感知的 API 和微服务方式运行。
- [Prompty](https://github.com/microsoft/prompty)：基于 Markdown 的 Prompt 格式与工具链，用于创建、管理、调试和评估可移植的 LLM Prompt。
- [Archestra](https://github.com/archestra-ai/archestra)：企业级 AI 平台，提供护栏、MCP 注册中心、网关和编排能力，用于治理 Agent 运维。
- [Databuff](https://github.com/databufflabs/databuff)：AI 原生 OpenTelemetry APM，支持跨链路、指标和服务拓扑的多 Agent 根因分析。
- [RocketplaneIO](https://github.com/olemeyer/rocketplaneIO)：自托管 AI SRE，提供无需插桩的 eBPF 可观测性，以及带护栏、可自验证的 Kubernetes 故障修复能力。
- [AgentProvenance](https://github.com/ByteYellow/AgentProvenance)：面向沙箱 AI Agent 的安全观测工具，将模型意图、应用上下文和运行时遥测汇聚为可验证的证据图谱。
- [AgentCanvas](https://github.com/vstorm-co/agentcanvas)：根据 Logfire trace 生成交互式 HTML 图，展示 Pydantic AI Agent 工作流中的工具、嵌套 Agent、Token 和成本。
- [Kaito](https://github.com/kaito-project/kaito)：Kubernetes AI 工具链 Operator，用于简化 Kubernetes 上的模型部署和 AI 工作负载管理。
- [OME](https://github.com/ome-projects/ome)：Kubernetes Operator，用于管理 LLM 服务、GPU 调度和模型生命周期，支持 SGLang、vLLM、TensorRT-LLM 与 Triton。
- [AURA](https://github.com/mezmo/aura)：面向生产的安全 AI SRE Agent 驾驭框架，提供护栏、状态管理、身份认证、流式执行和运维工具集成。
- [ongrid](https://github.com/ongridio/ongrid)：运维 AI Agent，可通过常见团队聊天界面调查基础设施根因并执行带护栏的修复。
- [Axon](https://github.com/langchain-tracer/Axon)：基于 OpenTelemetry 的 LLM 可观测性 CLI，可实时查看 LLM 和 Agent 链路。
- [Open RAG Eval](https://github.com/vectara/open-rag-eval)：开源 RAG 评估工具包，无需预先准备标准答案即可衡量检索和回答质量。

## AI Serving and Inference Operations AI 推理服务运维

用于在生产环境部署、扩缩容、路由和运维 AI 模型推理负载的工具。

- [Ray Serve](https://github.com/ray-project/ray)：Ray 中的可扩展模型服务库，用于构建分布式在线推理 API 和 LLM 服务负载。
- [KubeTorch](https://github.com/run-house/kubetorch)：面向 Python 的 Kubernetes 控制层，用于在集群资源上分发和运行 AI 工作负载。
- [ModelPlane](https://github.com/modelplaneai/modelplane)：开源 AI 推理控制平面，用于部署、路由和运维推理工作负载。
- [Triton Inference Server](https://github.com/triton-inference-server/server)：优化的推理服务器，用于在 GPU、CPU、云端和边缘环境部署 AI 模型。
- [KServe](https://github.com/kserve/kserve)：Kubernetes 原生平台，用于标准化、可扩展地服务生成式和预测式 AI 推理。
- [AIBrix](https://github.com/vllm-project/aibrix)：云原生基础设施组件，用于高性价比、可扩展地运维 GenAI 和 LLM 推理。
- [Dynamo](https://github.com/ai-dynamo/dynamo)：面向数据中心规模 LLM 与生成式 AI 负载的分布式推理服务框架，支持 Kubernetes 场景下的路由和扩缩容。
- [dstack](https://github.com/dstackai/dstack)：供应商无关的 GPU 供应与编排控制平面，可跨云、Kubernetes 和裸金属运行训练、推理与 Agent 工作负载。
- [llm-d](https://github.com/llm-d/llm-d)：Kubernetes 原生分布式推理栈，面向现代加速器上的高性能 LLM 服务和智能路由。
- [KubeAI](https://github.com/kubeai-project/kubeai)：Kubernetes AI 推理 Operator，用 OpenAI 兼容 API 服务 LLM、VLM、Embedding 和语音模型。
- [SkyPilot](https://github.com/skypilot-org/skypilot)：面向多云与 Kubernetes 的控制平面，用于在异构 GPU 基础设施上运行、扩缩容和管理 AI 工作负载。
- [KubeRay](https://github.com/ray-project/kuberay)：Kubernetes Operator 与工具集，用于部署和管理 Ray 集群及分布式 AI 工作负载。
- [SGLang](https://github.com/sgl-project/sglang)：高性能 LLM 与多模态模型推理服务框架，支持高效注意力机制和结构化输出。
- [vLLM](https://github.com/vllm-project/vllm)：高吞吐、内存高效的 LLM 推理与服务引擎，支持连续批处理与量化。
- [Ollama](https://github.com/ollama/ollama)：本地优先的 LLM 运行工具，适合在本地、边缘或开发环境中快速上手模型推理。
- [llama.cpp](https://github.com/ggml-org/llama.cpp)：高性能 C/C++ LLM 推理引擎，支持量化，为众多本地和服务端 AI 后端提供基础能力。
- [LocalAI](https://github.com/mudler/LocalAI)：自托管的 OpenAI 兼容本地 AI API，支持基于容器部署运行 LLM、图像生成和音频模型。
- [LoRAX](https://github.com/predibase/lorax)：多 LoRA 推理服务器，可在共享基座模型基础设施上托管数千个微调 LLM。
- [NVIDIA GPU Operator](https://github.com/NVIDIA/gpu-operator)：Kubernetes Operator，用于自动化 NVIDIA GPU 驱动安装、配置和生命周期管理。
- [NVIDIA Container Toolkit](https://github.com/NVIDIA/nvidia-container-toolkit)：在 Docker 和 Kubernetes 环境中构建和运行支持 NVIDIA CUDA 的 GPU 加速容器。
- [Volcano](https://github.com/volcano-sh/volcano)：CNCF 批调度系统，用于 AI/ML、大数据和 HPC 工作负载，支持 Gang 调度、队列管理和公平份额策略。
- [Kubeflow Trainer](https://github.com/kubeflow/trainer)：Kubernetes 原生 Operator，用于分布式 AI/ML 模型训练和 LLM 微调，支持 PyTorch、JAX 和 MPI。
- [OpenLLM](https://github.com/bentoml/OpenLLM)：将任意开源 LLM 以 OpenAI 兼容 API 运行，内置聊天 UI、模型目录和云端部署工作流。
- [Oumi](https://github.com/oumi-ai/oumi)：开源 LLM/VLM 微调、评估和部署平台，支持生产就绪的训练与上线工作流。
- [TensorRT-LLM](https://github.com/NVIDIA/TensorRT-LLM)：NVIDIA 官方 LLM 推理优化框架，提供先进的 GPU 优化和高效的运行时编排能力，适用于生产环境部署。
- [Text Generation Inference](https://github.com/huggingface/text-generation-inference)：HuggingFace 的生产级 LLM 推理服务器，支持张量并行、连续批处理和量化。
- [Text Embeddings Inference](https://github.com/huggingface/text-embeddings-inference)：极速文本嵌入与重排序模型推理服务器，具备生产就绪性能。
- [Axolotl](https://github.com/OpenAccess-AI-Collective/axolotl)：开源 LLM 微调框架，支持 LoRA、QLoRA 和全参数训练，覆盖主流模型架构。
- [LLaMA-Factory](https://github.com/hiyouga/LLaMA-Factory)：统一 LLM 微调框架，支持 100+ 模型和 50+ 方法，涵盖 LoRA、QLoRA 和全参数训练，提供 Web UI 工作流。
- [Unsloth](https://github.com/unslothai/unsloth)：开源 LLM 微调加速库，可将微调速度提升 2-5 倍并显著降低内存占用，支持主流模型架构与训练工作流。
- [HAMi](https://github.com/Project-HAMi/HAMi)：异构 GPU 共享中间件，支持 Kubernetes 上的 GPU 显存隔离、设备复用和多租户调度。
- [Llama Deploy](https://github.com/run-llama/llama_deploy)：面向 LlamaIndex Agent 工作流的生产部署框架，支持异步任务编排和服务管理。
- [Semantic Router](https://github.com/vllm-project/semantic-router)：系统级智能混合模型运行时，支持动态模型选择和跨边缘、数据中心及云环境的智能路由。
- [FastChat](https://github.com/lm-sys/FastChat)：用于训练、部署和评估 LLM 的开放平台。Vicuna 和 Chatbot Arena 的发布仓库。
- [text-generation-webui](https://github.com/oobabooga/textgen)：开源桌面应用，可在本地运行 LLM，支持文本、视觉、工具调用和 OpenAI/Anthropic 兼容 API。
- [DS4](https://github.com/antirez/ds4)：高性能本地推理引擎，支持 DeepSeek 4 Flash 和 PRO 模型，针对 Metal、CUDA 和 ROCm 平台优化。
- [RouteLLM](https://github.com/lm-sys/RouteLLM)：用于部署和评估 LLM 路由器的框架，可在保持响应质量的同时将请求转发给更低成本的模型。
- [Rig](https://github.com/0xPlaygrounds/rig)：用于构建模块化、可扩展 LLM 应用的 Rust 框架，提供可组合组件和多供应商集成。
- [Agent Lightning](https://github.com/microsoft/agent-lightning)：用于训练和优化 AI Agent 的框架，可将 Agent 执行过程连接到强化学习及其他训练方法。
- [verl](https://github.com/verl-project/verl)：灵活高效的大语言模型后训练强化学习框架，可用于优化推理和 Agent 工作负载。

## AIOps 智能运维

- [Netdata](https://github.com/netdata/netdata)：分布式实时监控系统，提供基础设施指标收集、可视化和告警功能。
- [Apache HertzBeat](https://github.com/apache/hertzbeat)：Apache 实时可观测与监控系统，支持无 Agent 采集、告警、状态页和 AI 辅助运维。
- [PostHog](https://github.com/PostHog/posthog)：开源产品分析平台，支持用户行为追踪和产品指标分析。
- [SREWorks](https://github.com/alibaba/SREWorks)：云原生 DataOps 与 AIOps 平台，用于运维 Kubernetes 应用和基础设施。
- [OpenSRE](https://github.com/Tracer-Cloud/opensre)：开源 AI SRE 工具包，用于构建具备可观测性、事件管理、告警和自动化根因分析能力的 AI SRE Agent。
- [Keep](https://github.com/keephq/keep)：开源 AIOps 与告警管理平台，支持跨监控工具的告警关联、增强和事件响应自动化。
- [AiSOC](https://github.com/beenuar/AiSOC)：开源 AI 驱动安全运营中心，支持告警融合、Agent 辅助分类、紫队演练和 MITRE ATT&CK 调查工作流。
- [APO](https://github.com/CloudDetail/apo)：AI 驱动的可观测平台，融合 OpenTelemetry、eBPF 和 LLM Agent 工作流，实现自动化根因分析和智能排障。
- [HolmesGPT](https://github.com/HolmesGPT/holmesgpt)：CNCF Sandbox SRE Agent，结合集群上下文、Runbook 和可观测数据调查告警与运维事件。
- [K8sGPT](https://github.com/k8sgpt-ai/k8sgpt)：Kubernetes 故障排查工具，将编码后的 SRE 分析器用于诊断和分流集群问题，并支持可选的 AI 后端。
- [Metaflow](https://github.com/Netflix/metaflow)：面向人的 AI/ML 系统开发框架，支持从原型到生产工作流的开发、版本管理、扩展和部署。

## AI 基础设施

用于 Web 爬取、AI 友好抽取、搜索情报和 RAG 数据采集工作流的基础设施。

- [Firecrawl](https://github.com/firecrawl/firecrawl)：Web 搜索、抓取、爬取与抽取 API，可将网页数据转换为适合 LLM 使用的 Markdown 和结构化输出。
- [Crawl4AI](https://github.com/unclecode/crawl4ai)：面向 LLM 的开源 Web 爬虫与抓取工具，适合构建 RAG、Agent 和 Web 数据流水线。
- [Jina Reader](https://github.com/jina-ai/reader)：URL 转 LLM 输入工具，通过简单前缀将任意网页转为清理后的 LLM 友好 Markdown 格式。
- [Open SEO](https://github.com/every-app/open-seo)：开源 SEO 与搜索情报平台，支持关键词研究、站点审计、反向链接分析和 Google Search Console MCP 工作流。
- [Milvus](https://github.com/milvus-io/milvus)：云原生向量数据库，支持十亿级相似度搜索和非结构化数据检索，适用于 RAG 和 AI 流水线。
- [Qdrant](https://github.com/qdrant/qdrant)：高性能向量搜索引擎，支持丰富过滤、负载存储和生产级扩展，适用于 AI 应用。
- [Chroma](https://github.com/chroma-core/chroma)：以 Embedding 为优先的向量数据库，支持简单的本地开发和客户端-服务端部署，用于构建 LLM 应用。
- [Unstructured](https://github.com/Unstructured-IO/unstructured)：开源 ETL 库，可将 PDF、HTML、Word 等文档转换为干净的结构化数据，适用于 RAG 和 LLM 流水线。
- [MarkItDown](https://github.com/microsoft/markitdown)：微软开源的文件转 Markdown 工具，可将 Office 文档和各类文件转换为 LLM 和 RAG 流水线可用的 Markdown 格式。
- [Docling](https://github.com/docling-project/docling)：IBM 开源文档理解工具包，可将 PDF、DOCX、PPTX、图片和 HTML 大规模转换为 LLM 友好的结构化格式。
- [Weaviate](https://github.com/weaviate/weaviate)：开源向量数据库，结合向量搜索、结构化过滤和生成式 AI 集成能力。
- [pgvector](https://github.com/pgvector/pgvector)：PostgreSQL 的开源向量相似度搜索扩展，广泛用于 RAG 和 AI 嵌入存储。
- [LanceDB](https://github.com/lancedb/lancedb)：面向开发者的嵌入式向量数据库，支持多模态 AI 搜索，采用无服务器架构和零拷贝检索。
- [zvec](https://github.com/alibaba/zvec)：阿里巴巴开源的轻量级、极速进程内向量数据库，用于嵌入式 AI 搜索和检索，Apache-2.0 许可。
- [txtai](https://github.com/neuml/txtai)：一体化 AI 框架，支持语义搜索、LLM 编排和语言模型工作流，内置嵌入和流水线能力。
- [Feast](https://github.com/feast-dev/feast)：面向 AI/ML 的开源特征存储，可在模型训练和在线推理中一致地提供特征数据。
- [Instructor](https://github.com/567-labs/instructor)：面向 LLM 的结构化输出工具，基于 Pydantic 校验，支持自动重试和跨供应商统一 API。
- [pgai](https://github.com/timescale/pgai)：面向 PostgreSQL 的开源 AI 工具套件，支持在 PostgreSQL 上直接构建 RAG、语义搜索和 AI 应用。
- [Browser Use](https://github.com/browser-use/browser-use)：开源 Web 自动化工具包，让 AI Agent 能够浏览网页、提取数据并大规模执行在线自动化任务。
- [Agent-Reach](https://github.com/Panniantong/Agent-Reach)：为 AI Agent 装上观察互联网的眼睛——通过一条 CLI 零 API 费用阅读和搜索 Twitter、Reddit、YouTube、GitHub、Bilibili 等平台。
- [Steel Browser](https://github.com/steel-dev/steel-browser)：开源无头浏览器沙箱，为 AI Agent 和应用提供生产就绪的 Web 自动化基础设施。
- [E2B](https://github.com/e2b-dev/E2B)：开源安全云沙箱，用于运行 AI Agent 代码，提供隔离环境、文件系统访问和真实工具执行能力。
- [headroom](https://github.com/headroomlabs-ai/headroom)：在 LLM 调用前压缩工具输出、日志、文件和 RAG 片段——节省 60-95% Token，效果不变。
- [fastmcp](https://github.com/PrefectHQ/fastmcp)：快速、Pythonic 的方式构建 MCP Server 与 Client，为 AI Agent 工具基础设施提供基础能力。
- [Stagehand](https://github.com/browserbase/stagehand)：开源浏览器 Agent SDK，支持 AI 驱动的 Web 自动化、数据提取和大规模页面交互。
- [FlagEmbedding](https://github.com/FlagOpen/FlagEmbedding)：开源嵌入与重排序模型工具包（BGE 系列），为检索增强 LLM 应用提供核心能力。
- [Open WebUI](https://github.com/open-webui/open-webui)：自托管的 LLM 对话界面，集成 RAG、Web 搜索、工具调用、模型管理和多用户部署能力，适用于内部 AI 平台。
- [Label Studio](https://github.com/HumanSignal/label-studio)：开源数据标注平台，支持图像、文本、音频、视频和时序数据标注，适用于 ML 和 LLM 训练工作流。
- [Argilla](https://github.com/argilla-io/argilla)：面向 AI 工程师和领域专家的开源协作平台，用于构建、管理和版本化 LLM 微调与评估所需的高质量数据集。
- [llmware](https://github.com/llmware-ai/llmware)：统一的开源框架，用于构建企业级 LLM 应用，集成 RAG、文档解析、嵌入和向量数据库编排能力。
- [AgentGateway](https://github.com/agentgateway/agentgateway)：面向 AI Agent 和 MCP Server 的新一代代理网关，提供安全访问、路由和策略管理，用于 Agent 工具集成。
- [Maxun](https://github.com/getmaxun/maxun)：开源无代码平台，支持 Web 抓取、爬取、搜索和 AI 数据提取，可将网站转化为 RAG 和 AI 流水线所需的结构化 API。
- [GPT-Researcher](https://github.com/assafelovic/gpt-researcher)：自主 AI 研究 Agent，支持全面的 Web 研究、报告生成和知识聚合，基于多源数据检索。
- [rtk](https://github.com/rtk-ai/rtk)：CLI 代理工具，可将日常开发命令的 LLM Token 消耗降低 60-90%，降低 AI 基础设施成本。
- [Context7](https://github.com/upstash/context7)：MCP Server，在推理时为 LLM 和 AI 代码编辑器提供最新的代码文档和库参考信息。
- [Pathway](https://github.com/pathwaycom/pathway)：Python ETL 框架，支持流处理、实时分析、LLM 流水线和 RAG，统一批处理和流式执行。
- [MindsDB](https://github.com/mindsdb/mindshub)：AI 数据库平台，将模型连接到数据源，支持 AI 驱动的查询、自动化和 Agent 工作流。
- [Open Connector](https://github.com/oomol-lab/open-connector)：开源认证网关，通过 SDK、CLI、MCP、HTTP 和 OpenAPI 将 1000+ SaaS 提供商连接到 AI Agent。
- [MCP Use](https://github.com/mcp-use/mcp-use)：全栈 MCP 框架，用于构建面向 ChatGPT、Claude 等 AI 助手的 MCP 应用、Server 和 Agent 工具。
- [Composio](https://github.com/ComposioHQ/composio)：Agent 工具集成平台，提供托管工具包、工具搜索、身份认证、上下文管理和沙箱执行能力。
- [PageIndex](https://github.com/VectifyAI/PageIndex)：与向量无关、基于推理的文档索引系统，用于对长文档执行检索增强生成。
- [Onyx](https://github.com/onyx-dot-app/onyx)：开源 AI 平台，面向企业搜索和 AI Chat，整合检索、数据连接器、Agent 工作流与自托管部署能力。
- [Agent Starter Pack](https://github.com/GoogleCloudPlatform/agent-starter-pack)：面向生产的 AI Agent 模板，内置 CI/CD、评估和可观测性，并提供 Google Cloud 部署路径。
- [MCP Inspector](https://github.com/modelcontextprotocol/inspector)：带有 Web 客户端和代理的开发者工具，用于通过多种传输方式交互式测试和调试 MCP Server。

## LLM 知识库

用于从非结构化文档构建、管理和查询 LLM 知识库的开源平台。

- [RAGFlow](https://github.com/infiniflow/ragflow)：领先的开源 RAG 引擎，融合深度文档理解、知识库管理和 Agent 能力，适合企业知识工作流。
- [FastGPT](https://github.com/labring/FastGPT)：基于 LLM 的知识库应用平台，提供开箱即用的数据处理、模型调用、RAG 和可视化工作流编排。
- [AnythingLLM](https://github.com/Mintplex-Labs/anything-llm)：本地优先的文档对话和 Agent 平台，可将任意文档转化为上下文感知的 LLM 知识库。
- [WeKnora](https://github.com/Tencent/WeKnora)：开源 LLM 知识平台，可将原始文档转化为可查询的 RAG、自主推理 Agent 和自维护 Wiki。
- [MaxKB](https://github.com/1Panel-dev/MaxKB)：开源企业级智能体平台，支持基于知识库的 RAG、多模型接入和可视化工作流设计。
- [GraphRAG](https://github.com/microsoft/graphrag)：微软开源的模块化图谱 RAG 系统，可从文档中提取知识图谱以提升检索质量。
- [Mem0](https://github.com/mem0ai/mem0)：面向 AI Agent 的通用记忆层，支持多级记忆、实体链接和时间推理，实现个性化交互。
- [Zep](https://github.com/getzep/zep)：开源 AI Agent 记忆层，提供长期记忆召回、用户事实和知识图谱能力，实现持久的 Agent 记忆。
- [AutoRAG](https://github.com/Marker-Inc-Korea/AutoRAG)：开源 RAG 评估与优化框架，通过 AutoML 风格自动化进行流水线调优。
- [MemPalace](https://github.com/MemPalace/mempalace)：开源 AI 记忆系统，提供基准测试最优的持久化知识存储能力，适用于 AI Agent 和 LLM 应用。
- [LightRAG](https://github.com/HKUDS/LightRAG)：简洁高效的 RAG 框架，基于图谱检索，支持增量更新和高效知识图谱构建。
- [Kotaemon](https://github.com/Cinnamon/kotaemon)：开源的 RAG 文档问答工具，支持多模型接入和可定制 UI，实现与文档的智能对话交互。
- [Quivr](https://github.com/QuivrHQ/quivr)：面向应用集成的 RAG 平台，支持任意 LLM、向量存储和文件类型，让团队专注产品而非 RAG 实现细节。
- [R2R](https://github.com/sciphi-ai/r2r)：生产就绪的 AI 检索系统，支持 Agentic RAG 和 RESTful API，适合企业级知识工作流。
- [Langchain-Chatchat](https://github.com/chatchat-space/Langchain-Chatchat)：基于 LangChain 和 ChatGLM、Qwen、Llama 等本地 LLM 的 RAG 与 Agent 应用平台，支持知识库管理。

## Agentic Workflow 智能体工作流

- [AutoGPT](https://github.com/Significant-Gravitas/Auto-GPT)：自主 AI Agent 框架，能够分解并执行复杂任务。
- [Langflow](https://github.com/langflow-ai/langflow)：LangChain 风格的图形化构建器，支持拖拽式构建 LLM 工作流。
- [Dify](https://github.com/langgenius/dify)：开源 LLM 应用开发平台，支持可视化 Agent 工作流和 AI 应用部署。
- [LangChain](https://github.com/langchain-ai/langchain)：构建 LLM 驱动应用的开发框架，支持 Agent 工作流编排。
- [Flowise](https://github.com/FlowiseAI/Flowise)：低代码 LLM 工作流编排工具，支持可视化构建 AI 应用链。
- [crewAI](https://github.com/crewAIInc/crewAI)：面向协作式 AI Agent 的框架，支持角色定义和任务编排。
- [LlamaIndex](https://github.com/run-llama/llama_index)：LLM 数据框架，支持结构化数据检索和增强。
- [Haystack](https://github.com/deepset-ai/haystack)：可扩展的问答系统框架，支持自定义 AI 工作流构建。
- [BentoML](https://github.com/bentoml/BentoML)：开源模型服务平台，支持多框架模型部署和 AI 应用编排。
- [trpc-agent-go](https://github.com/trpc-group/trpc-agent-go)：用于构建生产级 Agent 系统的 Go 框架，支持图工作流、工具、记忆、评估和可观测性。
- [LangGraph](https://github.com/langchain-ai/langgraph)：用于构建有状态多 Actor Agent 的框架，支持图编排、持久化和人机协作工作流。
- [DSPy](https://github.com/stanfordnlp/dspy)：用于编程而非提示 LLM 的框架，支持模块化 AI 系统构建和 Prompt 自动优化算法。
- [Pydantic AI](https://github.com/pydantic/pydantic-ai)：类型安全的 Python Agent 框架，支持模型无关、结构化输出、评估、MCP 集成和持久化执行。
- [VoltAgent](https://github.com/VoltAgent/voltagent)：开源 TypeScript AI Agent 工程平台，提供多 Agent 框架、LLM 可观测性、MCP 支持和 RAG 能力。
- [AutoGen](https://github.com/microsoft/autogen)：微软的多 Agent 对话框架，用于构建复杂的智能体 AI 应用，支持灵活的对话模式和人机协作工作流。
- [Agno](https://github.com/agno-agi/agno)：开源 Agent 平台，支持构建、运行和管理 AI Agent 平台，模型无关且配备生产级工具链。
- [Mastra](https://github.com/mastra-ai/mastra)：现代 TypeScript 框架，用于构建生产级 AI 应用和多 Agent 系统，内置可观测能力。
- [Letta](https://github.com/letta-ai/letta)：用于构建有状态 AI Agent 的平台，支持高级长期记忆、学习和自我进化能力。
- [mission-control](https://github.com/builderz-labs/mission-control)：可自托管的 AI Agent 编排平台，支持任务分发、多 Agent 工作流、支出监控和运维治理。
- [kiwiq](https://github.com/rcortx/kiwiq)：生产级多 Agent 编排平台，支持 JSON 定义 Agent、多层记忆和内置可观测性。
- [DeerFlow](https://github.com/bytedance/deer-flow)：字节跳动开源的长周期 SuperAgent 框架，支持沙箱、记忆、工具和多 Agent 协调，可进行研究、编码和创作。
- [CopilotKit](https://github.com/CopilotKit/CopilotKit)：面向 Agent 和生成式 UI 的前端技术栈，支持 React、Angular 和移动端。AG-UI Protocol 的创建者，用于 Agent 与用户的交互。
- [Aegra](https://github.com/aegra/aegra)：开源自托管 AI Agent 后端，基于 FastAPI 和 PostgreSQL 构建，是托管式 Agent 部署平台的零锁定替代方案。
- [CowAgent](https://github.com/zhayujie/CowAgent)：开源超级 AI 助手与 Agent 驾驭框架，支持任务规划、工具与技能执行，通过记忆和知识实现自我进化（原 chatgpt-on-wechat）。
- [Activepieces](https://github.com/activepieces/activepieces)：开源 AI 自动化平台，内置约 400 个 MCP Server，支持无代码 AI Agent 工作流、自动化和 MCP 集成。
- [NanoBot](https://github.com/HKUDS/nanobot)：轻量级开源 AI Agent，适用于工具调用、对话和自动化工作流，支持可扩展插件架构。
- [Harbor Framework](https://github.com/harbor-framework/harbor)：用于在可复现环境和并行实验中评估与改进 Agent 和语言模型的框架。
- [LangBot](https://github.com/langbot-app/LangBot)：面向生产的多平台机器人平台，支持 Agent 工作流、知识库、插件，以及与多种聊天系统集成。
- [Dapr Agents](https://github.com/dapr/dapr-agents)：与 CNCF 生态契合的 Agent 框架，提供持久化工作流、状态、消息、MCP 集成和 Kubernetes 原生运维能力，帮助构建可靠且可观测的 AI Agent。
- [Workflow SDK](https://github.com/vercel/workflow)：用于 TypeScript 的 SDK，为异步应用和 AI Agent 增加持久化执行、可靠性和可观测性。
- [LiveKit Agents](https://github.com/livekit/agents)：用于构建生产级实时语音和多模态 AI Agent 的框架，集成模型、工具和电话系统。

## DataOps

- [Dagster](https://dagster.io/)：数据编排平台，支持数据资产建模和全生命周期管理。
- [Apache NiFi](https://nifi.apache.org/)：可视化数据流编排工具，支持数据路由、转换和系统间协调。
- [DataHub](https://github.com/datahub-project/datahub)：面向现代数据与 AI 技术栈的元数据平台，支持数据发现、血缘、治理和可观测性。
- [OpenMetadata](https://github.com/open-metadata/OpenMetadata)：统一元数据平台，支持数据发现、血缘、治理和数据可观测性。
- [Great Expectations](https://github.com/great-expectations/great_expectations)：数据质量框架，用于验证数据集、记录数据期望并发现流水线回归。
- [Soda Core](https://github.com/sodadata/soda-core)：面向现代数据栈的数据契约和质量检查引擎，用于验证数据流水线。
- [Elementary](https://github.com/elementary-data/elementary)：dbt 原生数据可观测平台，用于监控流水线、测试、新鲜度和异常。
- [OpenLineage](https://github.com/OpenLineage/OpenLineage)：用于在数据流水线和平台之间采集血缘元数据的开放标准与工具集。
- [Marquez](https://github.com/MarquezProject/marquez)：元数据服务，用于采集、聚合并可视化作业和数据集之间的数据血缘。
- [Temporal](https://github.com/temporalio/temporal)：持久化执行平台，用于构建可靠的工作流、后台任务和长周期业务流程。
- [Kestra](https://github.com/kestra-io/kestra)：事件驱动的编排与调度平台，支持声明式数据、基础设施和运维工作流。
- [n8n](https://github.com/n8n-io/n8n)：公平代码的工作流自动化平台，内置 AI 能力，用于连接服务并构建自动化数据和运维流水线。
- [dbt](https://github.com/dbt-labs/dbt-core)：数据转换工具，帮助数据分析师和工程师用软件工程最佳实践转换数据。
- [Prefect](https://github.com/PrefectHQ/prefect)：工作流编排框架，用于构建具备调度、缓存、重试和事件驱动自动化的弹性数据流水线。
- [Flyte](https://github.com/flyteorg/flyte)：可扩展的 AI 与数据编排平台，使用强类型和 Kubernetes 原生执行构建可复现的声明式机器学习流水线。

### Streaming Operations 流式数据运维

- [Kafbat UI](https://github.com/kafbat/kafka-ui)：开源 Web UI，用于管理 Apache Kafka 集群、Topic、消费者、Schema 和 Kafka Connect。
- [Apache SeaTunnel](https://github.com/apache/seatunnel)：分布式数据集成平台，适合大规模批处理和流式数据传输。

## FinOps

- [Infracost](https://github.com/infracost/infracost)：云成本预测工具，支持 Terraform 和 Kubernetes 成本估算。
- [kubecost](https://kubecost.com/)：Kubernetes 成本管理与监控工具。
- [OpenCost](https://opencost.io/)：开源工具，用于跟踪和分摊 Kubernetes 环境中的云成本。
- [OptScale](https://github.com/hystax/optscale)：开源 FinOps 与云成本优化平台，支持 AWS、Azure、GCP、阿里云和 Kubernetes。
- [Cloud Custodian](https://github.com/cloud-custodian/cloud-custodian)：基于 policy-as-code 的云治理和成本优化规则引擎，支持自动化资源处置。
- [OpenMeter](https://github.com/openmeterio/openmeter)：面向 AI、API 和 DevOps 的开源计量与计费平台，支持实时用量聚合与按量计费。
- [NadirClaw](https://github.com/NadirRouter/NadirClaw)：开源 LLM 路由器和 AI 成本优化工具，自动将简单请求路由至低成本模型、将复杂请求路由至高级模型，通过 OpenAI 兼容代理节省 40-70% 的 API 开销。
- [KubeStellar Console](https://github.com/kubestellar/console)：多集群 Kubernetes 控制台，提供 AI 辅助运维、实时可观测性和边缘/云集群管理能力。

## Observability 可观测性

- [Prometheus](https://github.com/prometheus/prometheus)：云原生广泛采用的监控系统和时序数据库，适用于指标采集与告警。
- [VictoriaMetrics](https://github.com/VictoriaMetrics/VictoriaMetrics)：高性能、成本友好的时序数据库和监控栈，适合大规模 Prometheus 兼容指标场景。
- [Grafana Mimir](https://github.com/grafana/mimir)：可水平扩展、多租户的 Prometheus 指标长期存储后端。
- [Grafana Tempo](https://github.com/grafana/tempo)：面向大规模链路数据的分布式追踪后端，以较低索引开销存储高容量 trace。
- [Perses](https://github.com/perses/perses)：CNCF 可观测性可视化项目，用于基于 Prometheus、Tempo、Loki 等数据源构建仪表盘。
- [Grafana Loki](https://github.com/grafana/loki)：面向标签索引设计的日志聚合系统，可与 Grafana 深度集成。
- [OpenTelemetry Collector](https://github.com/open-telemetry/opentelemetry-collector)：厂商中立的遥测数据采集器，支持接收、处理和导出指标、日志与链路数据。
- [OpenTelemetry Collector Contrib](https://github.com/open-telemetry/opentelemetry-collector-contrib)：OpenTelemetry Collector 的社区发行版，提供面向生产系统的遥测采集、处理和导出组件。
- [OpenTelemetry Semantic Conventions](https://github.com/open-telemetry/semantic-conventions)：标准化遥测属性与命名约定，让不同工具和领域中的链路、指标与日志保持一致。
- [SigNoz](https://github.com/SigNoz/signoz)：基于 OpenTelemetry 的开源可观测平台，整合指标、链路、日志、仪表盘和告警。
- [Jaeger](https://github.com/jaegertracing/jaeger)：CNCF 分布式链路追踪平台，用于监控和排查微服务系统。
- [Vector](https://github.com/vectordotdev/vector)：高性能可观测数据流水线，用于采集、转换和路由日志与指标。
- [Grafana Alloy](https://github.com/grafana/alloy)：OpenTelemetry Collector 发行版，提供可编程流水线，用于采集、处理和转发可观测性信号。
- [Grafana](https://github.com/grafana/grafana)：开源监控、可观测与数据可视化平台，支持仪表盘、告警和多数据源探索。
- [Pixie](https://github.com/pixie-io/pixie)：Kubernetes 原生可观测平台，基于 eBPF 自动采集指标、事件、链路和网络遥测，无需手动插桩。
- [Parca](https://github.com/parca-dev/parca)：持续性能剖析平台，用于分析 CPU 和内存使用随时间的变化，提升性能、可靠性和基础设施效率。
- [Kepler](https://github.com/sustainable-computing-io/kepler)：Kubernetes 功耗与能耗 Exporter，用 Prometheus 衡量容器、Pod 和节点的能耗指标。
- [Inspektor Gadget](https://github.com/inspektor-gadget/inspektor-gadget)：基于 eBPF 的检查工具集，用于采集 Kubernetes 与 Linux 的底层运维遥测。
- [Robusta](https://github.com/robusta-dev/robusta)：Kubernetes 告警增强与自动化平台，支持 Prometheus 告警、Runbook 和修复工作流。
- [Coroot](https://github.com/coroot/coroot)：开源可观测性与 APM 平台，整合指标、日志、链路、性能剖析、SLO 和 AI 辅助根因分析。
- [Pyrra](https://github.com/pyrra-dev/pyrra)：面向 Prometheus 的 SLO 管理工具，让服务等级目标更易访问、可操作和团队使用。
- [Superlog](https://github.com/superloglabs/superlog)：开源可观测性工具，利用 AI Agent 检测问题并自动修复，实现软件自愈。
- [Monoscope](https://github.com/monoscope-tech/monoscope)：开源可观测平台，支持 S3 原生存储、OpenTelemetry 原生采集、自然语言查询和 AI Agent 驱动的异常检测与定时报告。
- [DeepFlow](https://github.com/deepflowio/deepflow)：基于 eBPF 的可观测平台，支持分布式追踪、性能剖析、网络遥测和自动应用拓扑发现。
- [Parseable](https://github.com/parseablehq/parseable)：基于 Rust 和数据湖架构的可观测平台，统一采集应用、Agent 和基础设施的日志、指标、链路与事件。

## Kubernetes Operations Kubernetes 运维

- [Cilium](https://github.com/cilium/cilium)：基于 eBPF 的 Kubernetes 网络、安全和可观测性平台。
- [Traefik](https://github.com/traefik/traefik)：云原生应用代理和入口控制器，支持自动服务发现、中间件和多协议。
- [kgateway](https://github.com/kgateway-dev/kgateway)：基于 Envoy 的云原生 API 与 AI 网关，支持 Kubernetes 入口流量管理、AI 服务路由。
- [Istio](https://github.com/istio/istio)：主流开源服务网格，用于连接、保护和观测微服务，支持流量管理、安全策略和遥测。
- [Linkerd](https://github.com/linkerd/linkerd2)：超轻量、安全优先的 CNCF 服务网格，支持零配置双向 TLS 和最小资源开销。
- [Headlamp](https://github.com/kubernetes-sigs/headlamp)：可扩展的 Kubernetes Web UI，用于集群可见性、资源管理和运维插件集成。
- [cert-manager](https://github.com/cert-manager/cert-manager)：Kubernetes 原生证书管理控制器，用于签发和续期 TLS 证书。
- [KEDA](https://github.com/kedacore/keda)：Kubernetes 事件驱动自动伸缩器，可基于外部指标和事件源扩缩容工作负载。
- [Velero](https://github.com/velero-io/velero)：Kubernetes 备份、恢复和迁移工具，支持集群资源与持久卷保护。
- [External Secrets Operator](https://github.com/external-secrets/external-secrets)：Kubernetes Operator，可将外部 Secret 管理系统中的密钥同步为 Kubernetes Secrets。
- [Reloader](https://github.com/stakater/Reloader)：Kubernetes 控制器，可在引用的 ConfigMap 或 Secret 变更时触发工作负载滚动重启。
- [Karpenter](https://github.com/kubernetes-sigs/karpenter)：灵活的 Kubernetes 节点自动扩缩容工具，用于提升集群效率和调度效果。
- [Koordinator](https://github.com/koordinator-sh/koordinator)：Kubernetes 调度系统，用于工作负载混部、资源优化和成本感知的集群运维。
- [Capsule](https://github.com/projectcapsule/capsule)：Kubernetes 多租户框架，帮助平台团队通过策略化租户边界委派命名空间管理。
- [vCluster](https://github.com/loft-sh/vcluster)：运行在命名空间内的虚拟 Kubernetes 集群，适合多租户、隔离和平台工程工作流。
- [Chaos Mesh](https://github.com/chaos-mesh/chaos-mesh)：Kubernetes 原生混沌工程平台，用于在受控故障下测试系统韧性。
- [Goldilocks](https://github.com/FairwindsOps/goldilocks)：Kubernetes 资源推荐仪表盘，基于 VPA 洞察帮助调优工作负载 requests 和 limits。
- [Glasskube](https://github.com/glasskube/glasskube)：Kubernetes 包管理器，提供 GUI 与 CLI，支持依赖感知和 GitOps 化的应用运维。
- [Botkube](https://github.com/kubeshop/botkube)：Kubernetes ChatOps 助手，用于监控集群、暴露事件并帮助团队调试部署。
- [mirrord](https://github.com/metalbear-co/mirrord)：Kubernetes 开发工具，让本地进程使用集群网络、环境变量和流量上下文运行。
- [OpenKruise](https://github.com/openkruise/kruise)：CNCF Kubernetes 工作负载自动化套件，支持高级应用部署、弹性伸缩和生命周期管理。
- [kOps](https://github.com/kubernetes/kops)：生产级 Kubernetes 集群生命周期工具，支持跨云环境的安装、升级和运维。
- [KubeOne](https://github.com/kubermatic/kubeone)：Kubernetes 集群生命周期管理工具，用于自动化云端、本地、边缘和 IoT 环境的集群运维。
- [Tilt](https://github.com/tilt-dev/tilt)：本地 Kubernetes 开发工具，支持多服务微服务的实时更新和声明式开发环境配置。
- [Knative](https://github.com/knative/serving)：CNCF Kubernetes Serverless 平台，支持缩容到零、请求驱动计算和事件驱动工作负载。
- [k3s](https://github.com/k3s-io/k3s)：轻量级 Kubernetes 发行版，专为边缘、IoT、CI 和资源受限环境设计。
- [containerd](https://github.com/containerd/containerd)：行业标准容器运行时，为 Docker、Kubernetes 和云原生平台提供核心容器生命周期管理。
- [Talos Linux](https://github.com/siderolabs/talos)：专为 Kubernetes 构建的现代 Linux 发行版，支持 API 驱动配置、不可变根文件系统和零接触 provisioning。
- [KubeEdge](https://github.com/kubeedge/kubeedge)：CNCF Kubernetes 原生边缘计算框架，支持将容器化应用延伸到边缘节点，实现云边协同。
- [Rook](https://github.com/rook/rook)：CNCF Kubernetes 存储编排器，为 Ceph、NFS 等存储系统提供自管理、自扩容和自修复的存储服务。
- [MinIO](https://github.com/minio/minio)：高性能 S3 兼容对象存储，原生支持 Kubernetes，适用于 AI/ML 数据湖、分析和云原生应用。
- [KubeVirt](https://github.com/kubevirt/kubevirt)：Kubernetes 原生虚拟化平台，可在 Kubernetes 上与容器一同运行和管理虚拟机。

## Security and Supply Chain 安全与供应链

- [Falco](https://github.com/falcosecurity/falco)：CNCF 运行时安全工具，用于检测容器和 Kubernetes 中的可疑行为。
- [Tetragon](https://github.com/cilium/tetragon)：基于 eBPF 的安全可观测与运行时执行工具，实时检测和拦截内核、容器及网络层的可疑活动。
- [Kyverno](https://github.com/kyverno/kyverno)：Kubernetes 原生策略引擎，支持校验、变更、生成和镜像验证。
- [Open Policy Agent](https://github.com/open-policy-agent/opa)：通用 policy-as-code 策略引擎，适用于 Kubernetes、CI/CD、API 和基础设施场景。
- [Gatekeeper](https://github.com/open-policy-agent/gatekeeper)：基于 OPA 的 Kubernetes 准入控制器，用于在集群中执行策略和审计约束。
- [Syft](https://github.com/anchore/syft)：用于从容器镜像和文件系统生成 SBOM 的 CLI 与库。
- [Grype](https://github.com/anchore/grype)：面向容器镜像和文件系统的漏洞扫描器，可与 Syft 生成的 SBOM 配合使用。
- [Kubescape](https://github.com/kubescape/kubescape)：Kubernetes 安全平台，支持风险分析、合规、错误配置扫描，以及 CI/CD 或集群检查。
- [Gitleaks](https://github.com/gitleaks/gitleaks)：Secret 扫描工具，用于在 Git 仓库、文件和 CI/CD 流程中发现硬编码凭据。
- [TruffleHog](https://github.com/trufflesecurity/trufflehog)：Secret 扫描工具，可在 Git、文件系统、CI 日志和云端来源中发现、验证并分析泄露凭据。
- [Prowler](https://github.com/prowler-cloud/prowler)：多云安全与合规平台，用于审计 AWS、Azure、GCP、Kubernetes 和 SaaS 环境。
- [KubeArmor](https://github.com/kubearmor/KubeArmor)：Kubernetes 运行时安全加固系统，基于 LSM 策略实现最小权限工作负载防护。
- [Kubewarden](https://github.com/kubewarden/adm-controller)：Kubernetes 准入策略引擎，通过 WebAssembly 策略实现 policy-as-code 治理。
- [cosign](https://github.com/sigstore/cosign)：Sigstore 工具，用于签名和验证容器镜像、Blob 与软件制品，并支持透明日志。
- [SLSA GitHub Generator](https://github.com/slsa-framework/slsa-github-generator)：用于在 GitHub Actions 中为构建和发布制品生成 SLSA provenance 的工作流。
- [Chainloop](https://github.com/chainloop-dev/chainloop)：软件供应链控制平面，用于收集 SDLC 证据、attestation、SBOM、VEX、SARIF 和策略检查结果。
- [SafeDep vet](https://github.com/safedep/vet)：基于 policy-as-code 的工具，用于发现恶意、有漏洞或高风险的开源依赖包。
- [OSV-Scanner](https://github.com/google/osv-scanner)：使用 OSV.dev 数据的漏洞扫描器，可在源码、lockfile、SBOM 和容器镜像中发现已知漏洞。
- [OpenSSF Scorecard](https://github.com/ossf/scorecard)：面向开源项目的自动化安全健康检查工具，覆盖依赖、CI/CD、分支保护和漏洞治理等信号。
- [GUAC](https://github.com/guacsec/guac)：软件供应链图谱，可聚合 SBOM、SLSA attestation、漏洞和依赖元数据用于风险分析。
- [ORT](https://github.com/oss-review-toolkit/ort)：用于自动化开源合规检查的工具集，覆盖依赖、License、版权、漏洞和 SBOM 生成。
- [CycloneDX CLI](https://github.com/CycloneDX/cyclonedx-cli)：用于校验、转换、合并和比对 CycloneDX SBOM 及相关格式的命令行工具。
- [Dependency-Track](https://github.com/DependencyTrack/dependency-track)：组件分析平台，用于跟踪 SBOM、漏洞、License 和软件供应链风险。
- [ToolHive](https://github.com/stacklok/toolhive)：企业级 MCP Server 安全运行与管理平台，提供隔离、生命周期控制和运维治理能力。
- [Tracecat](https://github.com/TracecatHQ/tracecat)：面向团队和 AI Agent 的开源安全自动化平台，支持事件驱动编排、监控和低代码工作流。
- [OneCLI](https://github.com/onecli/onecli)：开源凭据网关，内置密钥保险库，让 AI Agent 无需暴露密钥即可安全访问服务。
- [OpenAnt](https://github.com/knostic/OpenAnt)：基于 LLM 的开源漏洞发现工具，可主动发现 AI 系统中经过验证的安全漏洞。
- [AI-Infra-Guard](https://github.com/Tencent/AI-Infra-Guard)：全栈 AI 红队平台，用于扫描 AI 基础设施、Agent、技能、MCP Server 和 LLM 越狱漏洞。
- [Cybersecurity AI (CAI)](https://github.com/aliasrobotics/cai)：开源框架，用于将 AI Agent 应用于网络安全研究和防御性安全工作流。
- [AgentShield](https://github.com/affaan-m/agentshield)：AI Agent 安全扫描器，通过 CLI 或 GitHub Action 检测 Agent 配置、MCP Server 和工具权限中的漏洞。
- [Crust](https://github.com/BakeLens/crust)：本地 AI Agent 安全网关，可拦截工具调用及 MCP/ACP 流量，阻止危险操作、扫描 Secret 并执行运行时规则。
- [Adrian](https://github.com/secureagentics/Adrian)：开源 AI Agent 运行时安全工具，实时监控和控制 AI Agent，在 Agent 执行动作前拦截恶意工具调用、Prompt 注入和策略偏移。
- [Agent Governance Toolkit](https://github.com/microsoft/agent-governance-toolkit)：用于自主 AI Agent 的策略执行、零信任身份、执行沙箱和可靠性工程工具包。
- [SkillSpector](https://github.com/NVIDIA/SkillSpector)：AI Agent Skill 安全扫描器，用于检测漏洞、恶意模式和其他安全风险。
- [Agent Scan](https://github.com/snyk/agent-scan)：面向 AI Agent、MCP Server 和 Agent Skill 的安全扫描器。
- [Agent Safehouse](https://github.com/eugene1g/agent-safehouse)：本地 AI Agent 沙箱，只允许 Agent 访问所需的文件系统路径。
- [AgentDojo](https://github.com/ethz-spylab/agentdojo)：用于评估工具调用型 LLM Agent 中 Prompt 注入攻击与防御的动态环境。
- [nono](https://github.com/nolabs-ai/nono)：零配置、最小权限的 AI Agent 沙箱，可在 macOS、Linux 和 Windows WSL2 上隔离运行 Agent 及其调用的工具。
- [Pipelock](https://github.com/luckyPipewrench/pipelock)：开源 AI Agent 防火墙，可检查 MCP、A2A、HTTP 和 WebSocket 出站流量，识别 Prompt 注入、SSRF、Secret 泄露和高风险工具调用链。
- [Agentic Radar](https://github.com/splx-ai/agentic-radar)：面向 Agent 工作流的安全扫描器，可可视化工具与 MCP Server，并将发现的漏洞映射到安全框架。
- [deepsec](https://github.com/vercel-labs/deepsec)：基于 Agent 的代码安全扫描工具，用于检查大型代码库中的隐蔽漏洞，并导出结果供审查。
- [Agent Threat Rules](https://github.com/Agent-Threat-Rule/agent-threat-rules)：面向 AI Agent 安全威胁的开源检测规则标准，覆盖 Prompt 注入、MCP 风险、工具滥用等行为。

## Platform Engineering 平台工程

平台工程技术栈和工具链合集。

### API Management API 管理

- [Hoppscotch](https://github.com/hoppscotch/hoppscotch)：轻量级 API 开发工具套件，支持 REST、GraphQL 和 WebSocket。
- [Bruno](https://github.com/usebruno/bruno)：快速且 Git 友好的开源 API 客户端，支持管理 API 集合并通过桌面端或 CLI 执行调用。

### Artifact 制品管理

- [Harbor](https://github.com/goharbor/harbor)：企业级容器镜像仓库，支持安全扫描和访问控制。
- [Skopeo](https://github.com/containers/skopeo)：用于检查、复制和签署容器镜像的开源工具。
- [Nexus Repository](https://github.com/sonatype/nexus-public)：通用制品仓库，支持 Maven、npm、Docker 等格式。
- [ORAS](https://github.com/oras-project/oras)：将任意内容存储为 OCI Artifact 的工具。

### CI/CD

- [Apache Airflow](https://airflow.apache.org/)：开源工作流编排平台，常用于数据流水线。
- [Harness](https://github.com/harness/harness)：开源端到端开发者平台，支持源码管理、CI/CD 流水线、托管开发环境和制品仓库。
- [Jenkins](https://www.jenkins.io/)：开源 CI/CD 自动化服务器，拥有丰富插件生态。
- [argo-cd](https://argo-cd.readthedocs.io/)：流行的 Kubernetes 声明式 GitOps CD 工具。
- [Argo Rollouts](https://github.com/argoproj/argo-rollouts)：Kubernetes 渐进式交付控制器，支持蓝绿发布、金丝雀发布和基于实验的部署。
- [argo-workflows](https://github.com/argoproj/argo-workflows)：Kubernetes 原生工作流引擎。
- [Tekton](https://tekton.dev/)：Kubernetes 原生 CI/CD 框架，提供灵活的任务编排能力。
- [Flux](https://fluxcd.io/)：流行的 Kubernetes GitOps 工具包。
- [PipeCD](https://github.com/pipe-cd/pipecd)：CNCF 持续交付平台，支持跨多种部署目标管理应用、基础设施和平台运维。
- [Dagger](https://github.com/dagger/dagger)：开源自动化引擎，用于在 CI/CD 流水线中构建、测试和交付代码，支持可编程的容器化工作流。

### Code Search and Understanding 代码搜索与理解

- [sourcebot](https://github.com/sourcebot-dev/sourcebot)：自托管的代码搜索与理解工具，帮助人类和 AI Agent 导航、查询和理解大型代码库。
- [Codebase Memory MCP](https://github.com/DeusData/codebase-memory-mcp)：代码智能 MCP Server，可将代码库索引为持久化知识图谱，支持 158 种语言的亚毫秒级查询。
- [Semble](https://github.com/MinishLab/semble)：面向 AI Agent 优化的代码搜索引擎，基于嵌入检索，Token 消耗比 grep 方案减少约 98%。
- [OpenSrc](https://github.com/vercel-labs/opensrc)：按需获取 npm 包的真实源码，为 AI 编码 Agent 提供更深的库上下文，提升代码生成准确性。

### AI Coding Tools AI 编码工具

- [Aider](https://github.com/Aider-AI/aider)：终端中的 AI 结对编程工具，支持多文件编辑、Git 集成和主流 LLM。
- [Continue](https://github.com/continuedev/continue)：开源 AI 代码助手，以自动驾驶模式集成到 IDE 中，支持自定义上下文和模型。
- [Tabby](https://github.com/TabbyML/tabby)：自托管的 AI 编码助手，提供代码补全、对话和 Agent 能力，可完全在本地运行。
- [Cline](https://github.com/cline/cline)：自主编码 Agent，以 SDK、IDE 扩展和 CLI 助手形式提供，支持 AI 驱动开发工作流。
- [OpenHands](https://github.com/All-Hands-AI/OpenHands)：AI 驱动开发平台，通过 Agent 工作流实现自动化编码、代码审查和软件工程任务。
- [SWE-agent](https://github.com/SWE-agent/SWE-agent)：基于 LLM 的智能 Agent，可自动解决 GitHub Issue 和修复 Bug，支持迭代式工具调用工作流。
- [GPT-Pilot](https://github.com/Pythagora-io/gpt-pilot)：AI 开发者，可从自然语言规格说明构建生产就绪应用，支持人机协作引导。
- [OpenAI Codex CLI](https://github.com/openai/codex)：轻量级终端 AI 编码 Agent，在命令行中提供 AI 驱动的代码编辑和任务自动化能力。
- [Void](https://github.com/voideditor/void)：开源 AI 代码编辑器，提供智能代码补全、编辑和 Agent 编码工作流。
- [Goose](https://github.com/aaif-goose/goose)：开源可扩展 AI Agent，可用任意 LLM 安装、执行、编辑和测试代码，超越代码建议进入完整任务执行。
- [Qwen Code](https://github.com/QwenLM/qwen-code)：开源终端 AI 编码 Agent，支持多文件编辑、任务规划和 MCP Server 集成。
- [Open SWE](https://github.com/langchain-ai/open-swe)：LangChain 出品的开源异步编码 Agent，支持并行任务执行的自动化软件工程。
- [OpenCode](https://github.com/anomalyco/opencode)：开源编码 Agent——快速、轻量的 CLI 编码工具，以低 Token 开销和广泛 LLM 支持著称。
- [Gemini CLI](https://github.com/google-gemini/gemini-cli)：谷歌开源的 AI Agent，将 Gemini 的强大能力带入终端，用于编码、文件编辑和任务自动化。
- [OpenWiki](https://github.com/langchain-ai/openwiki)：用于为代码库编写和维护 Agent 文档的 CLI 工具，随代码演进自动保持文档同步。

### Developer Environments 开发环境

- [Coder](https://github.com/coder/coder)：自托管远程开发平台，可在任意基础设施上为开发者和 AI Agent 配置安全、预配置的工作空间。
- [DevPod](https://github.com/loft-sh/devpod)：开源、仅客户端的开发环境工具，可在任意云、Kubernetes 或本地机器上创建可复现、基础设施无关的工作空间。

### Code Service 代码服务

- [Trivy](https://github.com/aquasecurity/trivy)：全面的容器、代码、漏洞、错误配置和 SBOM 扫描工具。
- [SonarQube](https://github.com/SonarSource/sonarqube)：持续代码质量平台，支持 27+ 编程语言。
- [Open Code Review](https://github.com/alibaba/open-code-review)：阿里巴巴开源混合代码审查工具，结合确定性流水线与 LLM Agent，提供精确的行级审查反馈。
- [reviewdog](https://github.com/reviewdog)：自动代码审查和分析工具，支持多种语言和 linter。
- [PR-Agent](https://github.com/The-PR-Agent/pr-agent)：开源的 AI 驱动 PR 审查工具，支持自动代码审查、描述生成和跨 Git 平台的优化建议。
- [opencommit](https://github.com/di-sukharev/opencommit)：AI 驱动的 CLI 工具，使用 LLM 生成有意义的 Git 提交信息，支持所有主流模型供应商和本地模型。
- [OpenReview](https://github.com/vercel-labs/openreview)：开源、可自托管的 AI 代码审查机器人，基于 Vercel 部署，支持自动化 Pull Request 审查。
- [Dependency Track](https://dependencytrack.org/)：开源软件组件分析平台，支持供应链风险、SBOM 和 License 检查。
- [OpenRewrite](https://docs.openrewrite.org)：自动化大规模代码重构与现代化工具。
- [Hyades](https://github.com/DependencyTrack/hyades)：下一代软件供应链安全平台，稳定后计划替代 Dependency-Track。

### Event Mesh 事件网格

- [CloudEvents](https://cloudevents.io/)：用于事件驱动系统互操作的事件规范。
- [Argo Events](https://argoproj.github.io/argo-events/)：Kubernetes 事件驱动工作流自动化框架。
- [Apache EventMesh](https://eventmesh.apache.org/)：分布式事件中间件，支持多种消息协议和事件流管理。

### Feature Management and Experimentation 特性管理与实验

- [GrowthBook](https://github.com/growthbook/growthbook)：开源特性开关、实验和产品分析平台，用于更安全的渐进式交付。
- [Flagsmith](https://github.com/Flagsmith/flagsmith)：开源特性开关与远程配置服务，支持自托管或托管模式下的发布控制。
- [GO Feature Flag](https://github.com/thomaspoignant/go-feature-flag)：基于 OpenFeature 构建的自托管云原生特性开关方案，轻量级 Go 部署，支持多供应商。

### Infrastructure as Code (IaC)

Infrastructure as Code，基础设施即代码，是通过代码而非手动流程来管理和配置基础设施的方法。

- [OpenTofu](https://github.com/opentofu/opentofu)：由社区驱动、Linux Foundation 治理的 Terraform 分支。
- [Pulumi](https://github.com/pulumi/pulumi)：支持使用熟悉编程语言在任意云上构建基础设施的 IaC 工具。
- [sops](https://github.com/getsops/sops)：加密文件编辑器，支持 YAML、JSON、ENV、INI 和二进制文件。
- [Crossplane](https://github.com/crossplane/crossplane)：Kubernetes 插件，让平台团队组合多云基础设施并暴露高层自助服务 API。
- [Terragrunt](https://github.com/gruntwork-io/terragrunt)：Terraform 包装工具，提供 DRY 配置和远程状态管理。
- [bitnami/sealed-secrets](https://github.com/bitnami-labs/sealed-secrets)：声明式 Kubernetes Secret 管理工具，可安全地将加密 Secret 存放在 Git 中。
- [Checkov](https://github.com/bridgecrewio/checkov)：基础设施即代码静态分析工具，支持安全合规检查。
- [helmfile](https://github.com/helmfile)：声明式 Helm Chart 编排和部署工具。
- [Atlantis](https://github.com/runatlantis/atlantis)：面向 Terraform 的 Pull Request 自动化工具，支持计划、应用和协作式基础设施评审。

### Identity and Access Management (IAM)

信任很难，知道该信任谁更难。

- [keycloak](https://github.com/keycloak/keycloak)：面向现代应用和服务的开源 IAM。
- [OpenBao](https://github.com/openbao/openbao)：开源 Secret 管理系统，用于存储和分发密钥、证书与加密密钥。
- [oauth2-proxy](https://github.com/oauth2-proxy/oauth2-proxy)：轻量级 OAuth2 反向代理，支持多种身份提供商和简单授权校验。
- [zitadel](https://github.com/zitadel/zitadel)：面向现代应用和服务的开源 IAM，强调简单易用。
- [Casdoor](https://github.com/casdoor/casdoor)：开源身份管理平台，支持 OAuth 2.0、OIDC 和 SAML。
- [Cerbos](https://github.com/cerbos/cerbos)：开源核心、语言无关的授权层，支持基于上下文感知的访问控制策略管理应用资源权限。
- [dexidp/dex](https://github.com/dexidp/dex)：轻量级、可插拔的 OpenID Connect (OIDC) 与 OAuth 2.0 Provider。
- [pomerium](https://github.com/pomerium/pomerium)：身份感知代理，提供更丰富的访问控制能力。
- [Infisical](https://github.com/Infisical/infisical)：开源密钥管理平台，支持 Secret 管理、证书自动化和特权访问管理，覆盖开发和生产环境。
- [Metorial](https://github.com/metorial/metorial)：开源 AI Agent 身份与访问层，统一外部系统的认证、细粒度权限、集成管理和审计追踪。

### Internal Developer Platform (IDP)

内部开发者平台不只是工具堆叠，也不只是再做一个管理控制台。

- [backstage](https://github.com/backstage/backstage)：用于构建开发者门户的开放平台，帮助团队构建、部署和维护软件。
- [Kratix](https://github.com/syntasso/kratix)：用于构建平台 API 的框架，帮助团队在 Kubernetes 上组合和运营内部平台。
- [OpenChoreo](https://github.com/openchoreo/openchoreo)：面向 Kubernetes 的开源开发者平台，集成 Backstage 门户、CI/CD、GitOps、可观测性和平台抽象能力。
- [KubeVela](https://github.com/kubevela/kubevela)：CNCF 应用交付平台，用于管理混合云和多集群环境中的 Kubernetes 工作负载。
- [Score](https://github.com/score-spec/spec)：平台无关的 workload 规范，可一次描述服务并生成不同环境所需的平台配置。
- [Superplane](https://github.com/superplanehq/superplane)：面向平台工程工作流的开源控制平面，连接服务、流水线和环境。
- [Agyn](https://github.com/agynio/platform)：Kubernetes 原生运行时，将 Claude Code、Codex 等 AI 编码 Agent 从个人电脑迁移到具备企业控制能力的基础设施。

### IaaS Tools IaaS 工具

适合本地 Kubernetes、容器平台调试的轻量级虚拟化工具。

- [Minikube](https://github.com/kubernetes/minikube)：本地 Kubernetes 集群部署工具。
- [Vagrant](https://github.com/hashicorp/vagrant)：跨平台虚拟机管理工具，支持多种虚拟化后端。
- [lima](https://github.com/lima-vm/lima)：支持自动文件共享和端口转发的 Linux 虚拟机工具，也可模拟异构虚拟机。
- [multipass](https://github.com/canonical/multipass)：Ubuntu 出品的轻量级虚拟化工具。

### Testing Tools 测试工具

面向测试工程师和质量导向平台团队的工具。

- [googletest](https://github.com/google/googletest)：Google Testing and Mocking Framework。
- [Selenium](https://github.com/SeleniumHQ/selenium)：浏览器自动化框架，支持 Web 应用测试。
- [grafana/k6](https://github.com/grafana/k6)：使用 Go 和 JavaScript 的现代负载测试工具，也适合 API 测试流程。
- [JMeter](https://github.com/apache/jmeter)：Java 编写的性能测试工具，支持多种协议。
- [Tracetest](https://github.com/kubeshop/tracetest)：基于 OpenTelemetry 的链路测试工具，用于验证分布式工作流和可观测性插桩。

## License 许可协议

本文档采用 [CC BY-NC 4.0][] 许可协议。

[CC BY-NC 4.0]: https://creativecommons.org/licenses/by-nc/4.0/
