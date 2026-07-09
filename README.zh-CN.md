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
- [LangWatch](https://github.com/langwatch/langwatch)：开源平台，支持 LLM 监控、评估、链路追踪和 Agent 测试。
- [Opik](https://github.com/comet-ml/opik)：开源平台，用于追踪、评估和监控 LLM 应用、RAG 系统与 Agent 工作流。
- [promptfoo](https://github.com/promptfoo/promptfoo)：开源 CLI 与平台，用于 Prompt 测试、LLM 评估、红队测试和 CI/CD 回归检查。
- [Langtrace](https://github.com/Scale3-Labs/langtrace)：基于 OpenTelemetry 的可观测平台，用于追踪、评估和监控 LLM 应用。
- [Future AGI](https://github.com/future-agi/future-agi)：可自托管平台，用于评估、观测和改进 LLM 与 AI Agent 应用。
- [CozeLoop](https://github.com/coze-dev/coze-loop)：AI Agent 优化平台，覆盖开发、调试、评估和生产监控流程。
- [Agenta](https://github.com/Agenta-AI/agenta)：开源 LLMOps 平台，支持 Prompt 管理、调试 playground、评估和可观测性。
- [abtop](https://github.com/graykode/abtop)：类似 htop 的终端监控工具，用于查看 AI 编码 Agent 会话、Token、上下文窗口、速率限制和端口。
- [agenttrace](https://github.com/luoyuctl/agenttrace)：本地优先的 TUI，用于检查 AI 编码 Agent 的成本、Token、延迟、失败和报告。
- [ax](https://github.com/Necmttn/ax)：面向 AI 编码 Agent 的本地优先遥测与记忆图，覆盖成本、工具、技能、会话和 OTLP 事件。
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
- [BISHENG](https://github.com/dataelement/bisheng)：面向企业 AI 应用的开源 LLM DevOps 平台，覆盖 GenAI 工作流、RAG、Agent、模型管理、评估、数据集和可观测性。
- [OpenObserve](https://github.com/openobserve/openobserve)：开源可观测平台，覆盖日志、指标、链路、前端监控、流水线和 LLM 可观测性。
- [MCP Gateway](https://github.com/IBM/mcp-context-forge)：面向 MCP、A2A 和 API 工具的 AI 网关、注册表与代理，支持集中发现、护栏和管理。
- [NVIDIA NeMo Guardrails](https://github.com/NVIDIA-NeMo/Guardrails)：用于为基于 LLM 的对话系统加入可编程安全、对话和策略护栏的工具包。
- [Llama Guard](https://github.com/meta-llama/PurpleLlama)：Meta 开源的信任与安全工具集，用于评估和过滤 LLM 输入、输出与模型风险。
- [LLM Guard](https://github.com/protectai/llm-guard)：LLM 交互安全工具包，用于清洗输入输出、检测 Prompt 注入、拦截有害内容并降低数据泄露风险。
- [garak](https://github.com/NVIDIA/garak)：LLM 漏洞扫描器，用于探测 Prompt 注入、越狱、数据泄露、幻觉等生成式 AI 风险。
- [Superagent](https://github.com/superagent-ai/superagent)：开源 AI 安全 SDK，用于保护 LLM 应用免受 Prompt 注入、数据泄露和有害输出的影响。
- [OpenEvals](https://github.com/langchain-ai/openevals)：现成的评估器集合，用于在开发和 CI 流程中测试 LLM 应用并做回归检查。
- [TruLens](https://github.com/truera/trulens)：LLM 评估与追踪框架，支持反馈函数、护栏和迭代改进工作流，适用于 LLM 实验与 AI Agent。
- [OpenCompass](https://github.com/open-compass/opencompass)：LLM 评估平台，支持 100+ 数据集上对多种模型的评测和可复现基准测试。
- [OpenAI Evals](https://github.com/openai/evals)：用于评估 LLM 和 LLM 系统的框架，提供开源基准测试注册表和评估工作流。
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
- [Weights & Biases](https://github.com/wandb/wandb)：AI 开发者平台，提供实验追踪、模型管理和 ML/LLM 工作流监控，覆盖从训练到生产的全流程。
- [ClearML](https://github.com/clearml/clearml)：开源 MLOps/LLMOps 平台，支持实验管理、数据流水线、编排和模型服务。

## AI Serving and Inference Operations AI 推理服务运维

用于在生产环境部署、扩缩容、路由和运维 AI 模型推理负载的工具。

- [Ray Serve](https://github.com/ray-project/ray)：Ray 中的可扩展模型服务库，用于构建分布式在线推理 API 和 LLM 服务负载。
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
- [LoRAX](https://github.com/predibase/lorax)：多 LoRA 推理服务器，可在共享基座模型基础设施上托管数千个微调 LLM。
- [NVIDIA GPU Operator](https://github.com/NVIDIA/gpu-operator)：Kubernetes Operator，用于自动化 NVIDIA GPU 驱动安装、配置和生命周期管理。
- [NVIDIA Container Toolkit](https://github.com/NVIDIA/nvidia-container-toolkit)：在 Docker 和 Kubernetes 环境中构建和运行支持 NVIDIA CUDA 的 GPU 加速容器。
- [Volcano](https://github.com/volcano-sh/volcano)：CNCF 批调度系统，用于 AI/ML、大数据和 HPC 工作负载，支持 Gang 调度、队列管理和公平份额策略。
- [Kubeflow Trainer](https://github.com/kubeflow/trainer)：Kubernetes 原生 Operator，用于分布式 AI/ML 模型训练和 LLM 微调，支持 PyTorch、JAX 和 MPI。
- [OpenLLM](https://github.com/bentoml/OpenLLM)：将任意开源 LLM 以 OpenAI 兼容 API 运行，内置聊天 UI、模型目录和云端部署工作流。
- [Oumi](https://github.com/oumi-ai/oumi)：开源 LLM/VLM 微调、评估和部署平台，支持生产就绪的训练与上线工作流。

## AIOps 智能运维

- [Netdata](https://github.com/netdata/netdata)：分布式实时监控系统，提供基础设施指标收集、可视化和告警功能。
- [Apache HertzBeat](https://github.com/apache/hertzbeat)：Apache 实时可观测与监控系统，支持无 Agent 采集、告警、状态页和 AI 辅助运维。
- [PostHog](https://github.com/PostHog/posthog)：开源产品分析平台，支持用户行为追踪和产品指标分析。
- [SREWorks](https://github.com/alibaba/SREWorks)：云原生 DataOps 与 AIOps 平台，用于运维 Kubernetes 应用和基础设施。
- [OpenSRE](https://github.com/Tracer-Cloud/opensre)：开源 AI SRE 工具包，用于构建具备可观测性、事件管理、告警和自动化根因分析能力的 AI SRE Agent。
- [Keep](https://github.com/keephq/keep)：开源 AIOps 与告警管理平台，支持跨监控工具的告警关联、增强和事件响应自动化。

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
- [Weaviate](https://github.com/weaviate/weaviate)：开源向量数据库，结合向量搜索、结构化过滤和生成式 AI 集成能力。
- [pgvector](https://github.com/pgvector/pgvector)：PostgreSQL 的开源向量相似度搜索扩展，广泛用于 RAG 和 AI 嵌入存储。
- [LanceDB](https://github.com/lancedb/lancedb)：面向开发者的嵌入式向量数据库，支持多模态 AI 搜索，采用无服务器架构和零拷贝检索。
- [txtai](https://github.com/neuml/txtai)：一体化 AI 框架，支持语义搜索、LLM 编排和语言模型工作流，内置嵌入和流水线能力。
- [Feast](https://github.com/feast-dev/feast)：面向 AI/ML 的开源特征存储，可在模型训练和在线推理中一致地提供特征数据。
- [Instructor](https://github.com/567-labs/instructor)：面向 LLM 的结构化输出工具，基于 Pydantic 校验，支持自动重试和跨供应商统一 API。
- [pgai](https://github.com/timescale/pgai)：面向 PostgreSQL 的开源 AI 工具套件，支持在 PostgreSQL 上直接构建 RAG、语义搜索和 AI 应用。
- [Browser Use](https://github.com/browser-use/browser-use)：开源 Web 自动化工具包，让 AI Agent 能够浏览网页、提取数据并大规模执行在线自动化任务。
- [Steel Browser](https://github.com/steel-dev/steel-browser)：开源无头浏览器沙箱，为 AI Agent 和应用提供生产就绪的 Web 自动化基础设施。
- [E2B](https://github.com/e2b-dev/E2B)：开源安全云沙箱，用于运行 AI Agent 代码，提供隔离环境、文件系统访问和真实工具执行能力。

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
- [KubeStellar Console](https://github.com/kubestellar/console)：多集群 Kubernetes 控制台，提供 AI 辅助运维、实时可观测性和边缘/云集群管理能力。

## Observability 可观测性

- [Prometheus](https://github.com/prometheus/prometheus)：云原生广泛采用的监控系统和时序数据库，适用于指标采集与告警。
- [VictoriaMetrics](https://github.com/VictoriaMetrics/VictoriaMetrics)：高性能、成本友好的时序数据库和监控栈，适合大规模 Prometheus 兼容指标场景。
- [Grafana Mimir](https://github.com/grafana/mimir)：可水平扩展、多租户的 Prometheus 指标长期存储后端。
- [Grafana Tempo](https://github.com/grafana/tempo)：面向大规模链路数据的分布式追踪后端，以较低索引开销存储高容量 trace。
- [Perses](https://github.com/perses/perses)：CNCF 可观测性可视化项目，用于基于 Prometheus、Tempo、Loki 等数据源构建仪表盘。
- [Grafana Loki](https://github.com/grafana/loki)：面向标签索引设计的日志聚合系统，可与 Grafana 深度集成。
- [OpenTelemetry Collector](https://github.com/open-telemetry/opentelemetry-collector)：厂商中立的遥测数据采集器，支持接收、处理和导出指标、日志与链路数据。
- [SigNoz](https://github.com/SigNoz/signoz)：基于 OpenTelemetry 的开源可观测平台，整合指标、链路、日志、仪表盘和告警。
- [Jaeger](https://github.com/jaegertracing/jaeger)：CNCF 分布式链路追踪平台，用于监控和排查微服务系统。
- [Vector](https://github.com/vectordotdev/vector)：高性能可观测数据流水线，用于采集、转换和路由日志与指标。
- [Grafana Alloy](https://github.com/grafana/alloy)：OpenTelemetry Collector 发行版，提供可编程流水线，用于采集、处理和转发可观测性信号。
- [Pixie](https://github.com/pixie-io/pixie)：Kubernetes 原生可观测平台，基于 eBPF 自动采集指标、事件、链路和网络遥测，无需手动插桩。
- [Parca](https://github.com/parca-dev/parca)：持续性能剖析平台，用于分析 CPU 和内存使用随时间的变化，提升性能、可靠性和基础设施效率。
- [Kepler](https://github.com/sustainable-computing-io/kepler)：Kubernetes 功耗与能耗 Exporter，用 Prometheus 衡量容器、Pod 和节点的能耗指标。
- [Inspektor Gadget](https://github.com/inspektor-gadget/inspektor-gadget)：基于 eBPF 的检查工具集，用于采集 Kubernetes 与 Linux 的底层运维遥测。
- [Robusta](https://github.com/robusta-dev/robusta)：Kubernetes 告警增强与自动化平台，支持 Prometheus 告警、Runbook 和修复工作流。
- [Coroot](https://github.com/coroot/coroot)：开源可观测性与 APM 平台，整合指标、日志、链路、性能剖析、SLO 和 AI 辅助根因分析。
- [Pyrra](https://github.com/pyrra-dev/pyrra)：面向 Prometheus 的 SLO 管理工具，让服务等级目标更易访问、可操作和团队使用。
- [Superlog](https://github.com/superloglabs/superlog)：开源可观测性工具，利用 AI Agent 检测问题并自动修复，实现软件自愈。

## Kubernetes Operations Kubernetes 运维

- [Cilium](https://github.com/cilium/cilium)：基于 eBPF 的 Kubernetes 网络、安全和可观测性平台。
- [Istio](https://github.com/istio/istio)：主流开源服务网格，用于连接、保护和观测微服务，支持流量管理、安全策略和遥测。
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
- [k3s](https://github.com/k3s-io/k3s)：轻量级 Kubernetes 发行版，专为边缘、IoT、CI 和资源受限环境设计。
- [containerd](https://github.com/containerd/containerd)：行业标准容器运行时，为 Docker、Kubernetes 和云原生平台提供核心容器生命周期管理。
- [Talos Linux](https://github.com/siderolabs/talos)：专为 Kubernetes 构建的现代 Linux 发行版，支持 API 驱动配置、不可变根文件系统和零接触 provisioning。

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
- [Tracecat](https://github.com/TracecatHQ/tracecat)：面向团队和 AI Agent 的开源安全自动化平台，支持事件驱动编排、监控和低代码工作流。
- [OneCLI](https://github.com/onecli/onecli)：开源凭据网关，内置密钥保险库，让 AI Agent 无需暴露密钥即可安全访问服务。
- [OpenAnt](https://github.com/knostic/OpenAnt)：基于 LLM 的开源漏洞发现工具，可主动发现 AI 系统中经过验证的安全漏洞。

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

### Code Service 代码服务

- [Trivy](https://github.com/aquasecurity/trivy)：全面的容器、代码、漏洞、错误配置和 SBOM 扫描工具。
- [SonarQube](https://github.com/SonarSource/sonarqube)：持续代码质量平台，支持 27+ 编程语言。
- [reviewdog](https://github.com/reviewdog)：自动代码审查和分析工具，支持多种语言和 linter。
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
- [dexidp/dex](https://github.com/dexidp/dex)：轻量级、可插拔的 OpenID Connect (OIDC) 与 OAuth 2.0 Provider。
- [pomerium](https://github.com/pomerium/pomerium)：身份感知代理，提供更丰富的访问控制能力。
- [Infisical](https://github.com/Infisical/infisical)：开源密钥管理平台，支持 Secret 管理、证书自动化和特权访问管理，覆盖开发和生产环境。

### Internal Developer Platform (IDP)

内部开发者平台不只是工具堆叠，也不只是再做一个管理控制台。

- [backstage](https://github.com/backstage/backstage)：用于构建开发者门户的开放平台，帮助团队构建、部署和维护软件。
- [Kratix](https://github.com/syntasso/kratix)：用于构建平台 API 的框架，帮助团队在 Kubernetes 上组合和运营内部平台。
- [OpenChoreo](https://github.com/openchoreo/openchoreo)：面向 Kubernetes 的开源开发者平台，集成 Backstage 门户、CI/CD、GitOps、可观测性和平台抽象能力。
- [KubeVela](https://github.com/kubevela/kubevela)：CNCF 应用交付平台，用于管理混合云和多集群环境中的 Kubernetes 工作负载。
- [Score](https://github.com/score-spec/spec)：平台无关的 workload 规范，可一次描述服务并生成不同环境所需的平台配置。
- [Superplane](https://github.com/superplanehq/superplane)：面向平台工程工作流的开源控制平面，连接服务、流水线和环境。

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
