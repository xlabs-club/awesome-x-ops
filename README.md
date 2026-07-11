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
- [LLM Knowledge](#llm-knowledge): open-source platforms for turning documents into RAG knowledge bases, autonomous reasoning agents, and self-maintaining wikis.
- [AI Infrastructure](#ai-infrastructure): web crawling, AI-ready extraction, search intelligence, and RAG data acquisition.
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
- [whylogs](https://github.com/whylabs/whylogs): Open-source data logging library for profiling ML and LLM data quality, drift detection, and telemetry monitoring in production pipelines.
- [MLflow](https://github.com/mlflow/mlflow): Open-source AI engineering platform for debugging, evaluating, monitoring, and optimizing agents, LLMs, and ML models.
- [Giskard](https://github.com/Giskard-AI/giskard-oss): Open-source evaluation and testing framework for LLM applications and AI agents.
- [ZenML](https://github.com/zenml-io/zenml): AI platform for production ML, LLM, and agent pipelines with orchestration, tracking, and deployment workflows.
- [Guardrails](https://github.com/guardrails-ai/guardrails): Framework for validating LLM outputs and enforcing safety, quality, and structured response checks.
- [Plano](https://github.com/katanemo/plano): AI-native proxy and data plane for agentic applications with routing, safety, orchestration, and observability.
- [AgentSight](https://github.com/eunomia-bpf/agentsight): eBPF-based system-level tracing for observing AI agent execution without application instrumentation.
- [AgentOps](https://github.com/AgentOps-AI/agentops): Python SDK for monitoring AI agents, tracking LLM costs, benchmarking runs, and integrating with common agent frameworks.
- [Portkey AI Gateway](https://github.com/Portkey-AI/gateway): AI gateway for routing LLM traffic, applying guardrails, and centralizing model access for production applications.
- [BISHENG](https://github.com/dataelement/bisheng): Open LLM DevOps platform for enterprise AI applications, with GenAI workflows, RAG, agents, model management, evaluation, datasets, and observability.
- [OpenObserve](https://github.com/openobserve/openobserve): Open-source observability platform for logs, metrics, traces, frontend monitoring, pipelines, and LLM observability.
- [MCP Gateway](https://github.com/IBM/mcp-context-forge): AI gateway, registry, and proxy for MCP, A2A, and API tools with centralized discovery, guardrails, and management.
- [NVIDIA NeMo Guardrails](https://github.com/NVIDIA-NeMo/Guardrails): Toolkit for adding programmable safety, dialog, and policy guardrails to LLM-based conversational systems.
- [Llama Guard](https://github.com/meta-llama/PurpleLlama): Meta's open trust and safety toolkit for evaluating and filtering LLM inputs, outputs, and model risks.
- [LLM Guard](https://github.com/protectai/llm-guard): Security toolkit for sanitizing LLM inputs and outputs, detecting prompt injection, blocking harmful content, and reducing data leakage.
- [garak](https://github.com/NVIDIA/garak): LLM vulnerability scanner for probing prompt injection, jailbreaks, data leakage, hallucination, and other generative AI risks.
- [agentic-security](https://github.com/msoedov/agentic_security): Open-source LLM vulnerability scanner and AI red teaming kit for fuzzing and testing LLM guardrails against adversarial attacks.
- [Superagent](https://github.com/superagent-ai/superagent): Open-source AI security SDK for protecting LLM applications against prompt injections, data leaks, and harmful outputs.
- [PINT Benchmark](https://github.com/lakeraai/pint-benchmark): Open-source benchmark for evaluating prompt injection detection systems across diverse attack vectors.
- [OpenEvals](https://github.com/langchain-ai/openevals): Ready-made evaluators for testing and regression-checking LLM applications in development and CI workflows.
- [TruLens](https://github.com/truera/trulens): Evaluation and tracking framework for LLM experiments and AI agents with feedback functions, guardrails, and iterative improvement workflows.
- [OpenCompass](https://github.com/open-compass/opencompass): LLM evaluation platform supporting a wide range of models across 100+ datasets with reproducible benchmarks.
- [OpenAI Evals](https://github.com/openai/evals): Framework for evaluating LLMs and LLM systems with an open-source registry of benchmarks and evaluation workflows.
- [Envoy AI Gateway](https://github.com/envoyproxy/ai-gateway): Envoy-based gateway for managing unified access to generative AI services across providers and platforms.
- [Higress](https://github.com/higress-group/higress): AI-native API gateway built on Envoy for unified LLM provider access, canary routing, rate limiting, and multi-model observability.
- [Bifrost](https://github.com/maximhq/bifrost): High-performance enterprise AI gateway with adaptive load balancing, guardrails, cluster mode, and 1000+ model support.
- [Inference Gateway](https://github.com/inference-gateway/inference-gateway): Cloud-native LLM gateway for unifying providers, routing inference traffic, and exposing OpenTelemetry-friendly operations on Kubernetes.
- [OneAIFW](https://github.com/funstory-ai/aifw): Lightweight local AI firewall for anonymizing sensitive data before LLM calls and restoring it after responses.
- [Microsoft MCP Gateway](https://github.com/microsoft/mcp-gateway): Reverse proxy and management layer for operating MCP servers with session-aware routing and Kubernetes lifecycle support.
- [CoAI](https://github.com/coaidev/coai): Multi-tenant AI platform with a unified LLM gateway, provider routing, cost management, billing, and model cache for enterprise deployments.
- [Kong](https://github.com/Kong/kong): Cloud-native API, LLM, and MCP gateway with advanced AI traffic management, multi-provider routing, semantic security, and rich plugin ecosystem.
- [Apache APISIX](https://github.com/apache/apisix): Apache dynamic API and AI gateway with LLM proxying, token-based rate limiting, MCP bridge, and plugin-based AI traffic control.
- [LangKit](https://github.com/whylabs/langkit): Open-source toolkit for monitoring LLMs by extracting signals from prompts and responses, including text quality, relevance, sentiment, and prompt injection detection.
- [AxonHub](https://github.com/looplj/axonhub): Open-source AI gateway with failover, load balancing, cost control, and end-to-end tracing across 100+ LLM providers.
- [Weights & Biases](https://github.com/wandb/wandb): AI developer platform for experiment tracking, model management, and monitoring ML/LLM workflows from training to production.
- [ClearML](https://github.com/clearml/clearml): Open-source MLOps/LLMOps platform for experiment management, data pipelines, orchestration, and model serving.
- [Helicone AI Gateway](https://github.com/Helicone/ai-gateway): Fast, lightweight Rust-based AI gateway with smart routing, caching, rate limiting, and built-in observability across 100+ LLM providers.
- [EleutherAI LM Eval](https://github.com/EleutherAI/lm-evaluation-harness): Standardized framework for few-shot and zero-shot evaluation of language models across hundreds of tasks and benchmarks.
- [Weave](https://github.com/wandb/weave): Toolkit for tracing, evaluating, and improving LLM applications with automatic versioning and interactive debugging workflows.
- [Pezzo](https://github.com/pezzolabs/pezzo): Open-source LLMOps platform for prompt management, version control, A/B testing, troubleshooting, and observability.
- [Latitude](https://github.com/latitude-dev/latitude-llm): Open-source AI monitoring and evaluation platform for production LLM applications with collaborative debugging, dataset management, and CI/CD integration.
- [TraceRoot](https://github.com/traceroot-ai/traceroot): Open-source observability and self-healing layer for AI agents, providing real-time monitoring and automated remediation.

## AI Serving and Inference Operations

Tools for deploying, scaling, routing, and operating AI model inference workloads in production.

- [Ray Serve](https://github.com/ray-project/ray): Scalable model serving library in Ray for building distributed online inference APIs and LLM serving workloads.
- [Triton Inference Server](https://github.com/triton-inference-server/server): Optimized inference server for deploying AI models across GPUs, CPUs, and cloud or edge environments.
- [KServe](https://github.com/kserve/kserve): Kubernetes-native platform for standardized, scalable generative and predictive AI inference serving.
- [AIBrix](https://github.com/vllm-project/aibrix): Cloud-native infrastructure components for cost-efficient, scalable GenAI and LLM inference operations.
- [Dynamo](https://github.com/ai-dynamo/dynamo): Distributed inference serving framework for datacenter-scale LLM and generative AI workloads with Kubernetes-oriented routing and scaling.
- [dstack](https://github.com/dstackai/dstack): Vendor-agnostic control plane for provisioning GPUs and orchestrating training, inference, and agent workloads across clouds, Kubernetes, and bare metal.
- [llm-d](https://github.com/llm-d/llm-d): Kubernetes-native distributed inference stack for high-performance LLM serving with intelligent routing on modern accelerators.
- [KubeAI](https://github.com/kubeai-project/kubeai): Kubernetes AI inference operator for serving LLMs, VLMs, embeddings, and speech models with OpenAI-compatible APIs.
- [SkyPilot](https://github.com/skypilot-org/skypilot): Multi-cloud and Kubernetes control plane for running, scaling, and managing AI workloads across heterogeneous GPU infrastructure.
- [KubeRay](https://github.com/ray-project/kuberay): Kubernetes operator and toolkit for deploying and managing Ray clusters and distributed AI workloads.
- [SGLang](https://github.com/sgl-project/sglang): High-performance serving framework for large language models and multimodal models with efficient attention and structured outputs.
- [vLLM](https://github.com/vllm-project/vllm): High-throughput and memory-efficient inference and serving engine for LLMs with continuous batching and quantization.
- [Ollama](https://github.com/ollama/ollama): Local-first LLM runner for getting started quickly with models locally, on edge, or in development environments.
- [llama.cpp](https://github.com/ggml-org/llama.cpp): High-performance C/C++ LLM inference engine with quantization, powering many local and server-side AI backends.
- [LocalAI](https://github.com/mudler/LocalAI): Self-hosted, OpenAI-compatible local AI API for running LLMs, image generation, and audio models with container-based deployment.
- [LoRAX](https://github.com/predibase/lorax): Multi-LoRA inference server for hosting thousands of fine-tuned LLMs on shared base model infrastructure.
- [NVIDIA GPU Operator](https://github.com/NVIDIA/gpu-operator): Kubernetes operator for automating NVIDIA GPU driver installation, configuration, and lifecycle management.
- [NVIDIA Container Toolkit](https://github.com/NVIDIA/nvidia-container-toolkit): Build and run GPU-accelerated containers with NVIDIA CUDA support in Docker and Kubernetes environments.
- [Volcano](https://github.com/volcano-sh/volcano): CNCF batch scheduling system for AI/ML, big data, and HPC workloads with gang scheduling, queue management, and fair-share policies.
- [Kubeflow Trainer](https://github.com/kubeflow/trainer): Kubernetes-native operator for distributed AI/ML model training and LLM fine-tuning with PyTorch, JAX, and MPI support.
- [OpenLLM](https://github.com/bentoml/OpenLLM): Run any open-source LLM as an OpenAI-compatible API endpoint with built-in chat UI, model catalog, and cloud deployment workflows.
- [Oumi](https://github.com/oumi-ai/oumi): Open-source platform for fine-tuning, evaluating, and deploying any open-source LLM or VLM with production-ready training and deployment workflows.
- [TensorRT-LLM](https://github.com/NVIDIA/TensorRT-LLM): NVIDIA's official LLM inference optimization framework with state-of-the-art GPU optimizations and efficient runtime orchestration for production deployments.
- [Text Generation Inference](https://github.com/huggingface/text-generation-inference): HuggingFace's production-grade inference server for LLMs with tensor parallelism, continuous batching, and quantization support.
- [Text Embeddings Inference](https://github.com/huggingface/text-embeddings-inference): Blazing-fast inference server for text embedding and reranking models with production-ready performance.
- [Axolotl](https://github.com/OpenAccess-AI-Collective/axolotl): Open-source LLM fine-tuning framework with support for LoRA, QLoRA, and full-parameter training across popular model architectures.
- [LLaMA-Factory](https://github.com/hiyouga/LLaMA-Factory): Unified framework for LLM fine-tuning with 100+ models and 50+ methods, supporting LoRA, QLoRA, and full-parameter training with web UI workflows.
- [Unsloth](https://github.com/unslothai/unsloth): Open-source library for 2-5x faster LLM fine-tuning with significant memory reduction, supporting major model architectures and training workflows.
- [HAMi](https://github.com/Project-HAMi/HAMi): Heterogeneous GPU sharing middleware for Kubernetes with device memory isolation and multi-tenant scheduling.
- [Llama Deploy](https://github.com/run-llama/llama_deploy): Production deployment framework for LlamaIndex agentic workflows with asynchronous task orchestration and service management.
- [Semantic Router](https://github.com/vllm-project/semantic-router): System-level intelligent runtime for Mixture-of-Models, enabling dynamic model selection and intelligent routing across edge, data center, and cloud environments.

## AIOps

- [Netdata](https://github.com/netdata/netdata): Distributed real-time monitoring for infrastructure metrics, visualization, and alerting.
- [Apache HertzBeat](https://github.com/apache/hertzbeat): Apache real-time observability and monitoring system with agentless collection, alerting, status pages, and AI-assisted operations.
- [PostHog](https://github.com/PostHog/posthog): Open-source product analytics platform for user behavior tracking and product metrics.
- [SREWorks](https://github.com/alibaba/SREWorks): Cloud-native DataOps and AIOps platform for operating Kubernetes-based applications and infrastructure.
- [OpenSRE](https://github.com/Tracer-Cloud/opensre): Open-source toolkit for building AI SRE agents with observability, incident management, alerting, and automated root-cause analysis.
- [Keep](https://github.com/keephq/keep): Open-source AIOps and alert management platform for correlating, enriching, and automating incident response across monitoring tools.
- [AiSOC](https://github.com/beenuar/AiSOC): Open-source AI-powered Security Operations Center for alert fusion, agent-assisted triage, purple-team drills, and MITRE ATT&CK investigation workflows.

## AI Infrastructure

Infrastructure for web crawling, AI-ready extraction, search intelligence, and RAG data acquisition workflows.

- [Firecrawl](https://github.com/firecrawl/firecrawl): Web search, scraping, crawling, and extraction API that turns web data into LLM-ready Markdown and structured outputs.
- [Crawl4AI](https://github.com/unclecode/crawl4ai): Open-source LLM-friendly web crawler and scraper for building RAG, agent, and web data pipelines.
- [Jina Reader](https://github.com/jina-ai/reader): URL-to-LLM converter that turns any web page into clean, LLM-friendly Markdown with a simple prefix.
- [Open SEO](https://github.com/every-app/open-seo): Open-source SEO and search intelligence platform for keyword research, site audits, backlink analysis, and Google Search Console MCP workflows.
- [Milvus](https://github.com/milvus-io/milvus): Cloud-native vector database for billion-scale similarity search and unstructured data retrieval in RAG and AI pipelines.
- [Qdrant](https://github.com/qdrant/qdrant): High-performance vector search engine with rich filtering, payload storage, and production-ready scalability for AI applications.
- [Chroma](https://github.com/chroma-core/chroma): Embedding-first vector database for building LLM applications with simple local development and client-server deployment.
- [Unstructured](https://github.com/Unstructured-IO/unstructured): Open-source ETL library for converting PDFs, HTML, Word, and other documents into clean structured data for RAG and LLM pipelines.
- [MarkItDown](https://github.com/microsoft/markitdown): Microsoft's open-source tool for converting files and Office documents to Markdown for LLM and RAG data pipelines.
- [Docling](https://github.com/docling-project/docling): IBM's open-source document understanding toolkit for converting PDFs, DOCX, PPTX, images, and HTML into LLM-ready structured formats at scale.
- [Weaviate](https://github.com/weaviate/weaviate): Open-source vector database combining vector search with structured filtering and generative AI integrations.
- [pgvector](https://github.com/pgvector/pgvector): Open-source vector similarity search extension for PostgreSQL, widely used for RAG and AI embedding storage.
- [LanceDB](https://github.com/lancedb/lancedb): Developer-friendly embedded vector database for multimodal AI search with serverless architecture and zero-copy retrieval.
- [txtai](https://github.com/neuml/txtai): All-in-one AI framework for semantic search, LLM orchestration, and language model workflows with embeddings and pipelines.
- [Feast](https://github.com/feast-dev/feast): Open-source feature store for AI/ML that serves features consistently for model training and online inference.
- [Instructor](https://github.com/567-labs/instructor): Structured outputs for LLMs with Pydantic validation, automatic retries, and provider-agnostic API.
- [pgai](https://github.com/timescale/pgai): Open-source suite for building RAG, semantic search, and AI applications directly on PostgreSQL with vector and AI tooling.
- [Browser Use](https://github.com/browser-use/browser-use): Open-source web automation toolkit that enables AI agents to browse websites, extract data, and automate online tasks at scale.
- [Steel Browser](https://github.com/steel-dev/steel-browser): Open-source headless browser sandbox for AI agents and applications, providing production-ready web automation infrastructure.
- [E2B](https://github.com/e2b-dev/E2B): Open-source secure cloud sandbox for running AI agent code with isolated environments, file system access, and real-world tool execution.
- [headroom](https://github.com/headroomlabs-ai/headroom): Compress tool outputs, logs, files, and RAG chunks before reaching the LLM — 60-95% fewer tokens, same answers.
- [fastmcp](https://github.com/PrefectHQ/fastmcp): The fast, Pythonic way to build MCP servers and clients for AI agent tool infrastructure.
- [Stagehand](https://github.com/browserbase/stagehand): Open-source SDK for building browser agents with AI-powered web automation, extraction, and interaction at scale.
- [FlagEmbedding](https://github.com/FlagOpen/FlagEmbedding): Open-source toolkit for embedding and reranking models (BGE series) powering retrieval-augmented LLM applications.
- [Open WebUI](https://github.com/open-webui/open-webui): Self-hosted LLM chat interface with RAG, web search, tool integration, model management, and multi-user deployment for internal AI platforms.
- [Label Studio](https://github.com/HumanSignal/label-studio): Open-source data labeling platform for images, text, audio, video, and time series in ML and LLM training workflows.
- [Argilla](https://github.com/argilla-io/argilla): Open-source collaboration platform for building, curating, and versioning high-quality datasets for LLM fine-tuning and evaluation.
- [llmware](https://github.com/llmware-ai/llmware): Unified open-source framework for enterprise LLM applications with integrated RAG, parsing, embedding, and vector database orchestration.
- [AgentGateway](https://github.com/agentgateway/agentgateway): Next-generation agentic proxy for AI agents and MCP servers, providing secure access, routing, and policy management for agent tool integrations.
- [Maxun](https://github.com/getmaxun/maxun): Open-source no-code platform for web scraping, crawling, search, and AI data extraction, turning websites into structured APIs for RAG and AI pipelines.
- [GPT-Researcher](https://github.com/assafelovic/gpt-researcher): Autonomous AI agent for comprehensive web research, report generation, and knowledge synthesis using multi-source data retrieval.

## LLM Knowledge

Open-source platforms for building, managing, and querying LLM-powered knowledge bases from unstructured documents.

- [RAGFlow](https://github.com/infiniflow/ragflow): Leading open-source RAG engine that combines deep document understanding, knowledge base management, and agent capabilities for enterprise knowledge workflows.
- [FastGPT](https://github.com/labring/FastGPT): Knowledge-based LLM application platform with out-of-the-box data processing, model invocation, RAG, and visual workflow orchestration.
- [AnythingLLM](https://github.com/Mintplex-Labs/anything-llm): Local-first document chat and agent platform that turns any document into a context-aware LLM knowledge base.
- [WeKnora](https://github.com/Tencent/WeKnora): Open-source LLM knowledge platform that turns raw documents into a queryable RAG, an autonomous reasoning agent, and a self-maintaining Wiki.
- [MaxKB](https://github.com/1Panel-dev/MaxKB): Open-source enterprise platform for building knowledge base agents with RAG, multi-model support, and visual workflow design.
- [GraphRAG](https://github.com/microsoft/graphrag): Microsoft's modular graph-based RAG system for extracting knowledge graphs from documents and improving retrieval quality.
- [Mem0](https://github.com/mem0ai/mem0): Universal memory layer for AI agents with multi-level memory, entity linking, and temporal reasoning for personalized interactions.
- [Zep](https://github.com/getzep/zep): Open-source memory layer for AI agents providing long-term recall, user facts, and knowledge graph capabilities for persistent agent memory.
- [AutoRAG](https://github.com/Marker-Inc-Korea/AutoRAG): Open-source framework for RAG evaluation and optimization with AutoML-style automation for pipeline tuning.

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
- [LangGraph](https://github.com/langchain-ai/langgraph): Framework for building stateful, multi-actor agents with graph-based orchestration, persistence, and human-in-the-loop workflows.
- [DSPy](https://github.com/stanfordnlp/dspy): Framework for programming—not prompting—LLMs with modular AI system building and prompt optimization algorithms.
- [Pydantic AI](https://github.com/pydantic/pydantic-ai): Type-safe Python agent framework with model-agnostic support, structured outputs, evals, MCP integration, and durable execution.
- [VoltAgent](https://github.com/VoltAgent/voltagent): Open-source TypeScript AI agent engineering platform with multi-agent framework, LLM observability, MCP support, and RAG capabilities.
- [AutoGen](https://github.com/microsoft/autogen): Microsoft's multi-agent conversation framework for building complex agentic AI applications with flexible conversation patterns and human-in-the-loop workflows.
- [Agno](https://github.com/agno-agi/agno): Open-source platform for building, running, and managing AI agent platforms with model-agnostic support and production-grade tooling.
- [Mastra](https://github.com/mastra-ai/mastra): Modern TypeScript framework for building production AI-powered applications and multi-agent systems with built-in observability.
- [Letta](https://github.com/letta-ai/letta): Platform for building stateful AI agents with advanced long-term memory, learning, and self-improvement capabilities over time.
- [mission-control](https://github.com/builderz-labs/mission-control): Self-hosted AI agent orchestration platform for dispatching tasks, running multi-agent workflows, monitoring spend, and governing operations.
- [kiwiq](https://github.com/rcortx/kiwiq): Production-grade multi-agent orchestration platform with JSON-defined agents, multi-tier memory, and built-in observability.
- [DeerFlow](https://github.com/bytedance/deer-flow): ByteDance's open-source long-horizon SuperAgent harness that researches, codes, and creates with sandboxes, memory, tools, and multi-agent coordination.

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
- [n8n](https://github.com/n8n-io/n8n): Fair-code workflow automation platform with native AI capabilities for connecting services and building automated data and ops pipelines.
- [dbt](https://github.com/dbt-labs/dbt-core): Data transformation tool that enables analysts and engineers to transform data with software engineering best practices.
- [Prefect](https://github.com/PrefectHQ/prefect): Workflow orchestration framework for building resilient data pipelines with scheduling, caching, retries, and event-based automations.
- [Flyte](https://github.com/flyteorg/flyte): Scalable AI and data orchestration platform for building reproducible, declarative ML pipelines with strong typing and Kubernetes-native execution.

### Streaming Operations

- [Kafbat UI](https://github.com/kafbat/kafka-ui): Open-source web UI for managing Apache Kafka clusters, topics, consumers, schemas, and Kafka Connect.
- [Apache SeaTunnel](https://github.com/apache/seatunnel): Distributed data integration platform for high-volume batch and streaming data movement.

## FinOps

- [Infracost](https://github.com/infracost/infracost): Cloud cost forecasting tool for Terraform and Kubernetes cost estimates.
- [kubecost](https://kubecost.com/): Kubernetes cost management and monitoring platform.
- [OpenCost](https://opencost.io/): Open-source tool for tracking and allocating cloud costs in Kubernetes environments.
- [OptScale](https://github.com/hystax/optscale): Open-source FinOps and cloud cost optimization platform for AWS, Azure, GCP, Alibaba Cloud, and Kubernetes.
- [Cloud Custodian](https://github.com/cloud-custodian/cloud-custodian): Policy-as-code rules engine for cloud governance, cost optimization, and automated resource actions.
- [OpenMeter](https://github.com/openmeterio/openmeter): Open-source metering and billing for AI, API, and DevOps with real-time usage aggregation and usage-based pricing.
- [NadirClaw](https://github.com/NadirRouter/NadirClaw): Open-source LLM router and AI cost optimizer that routes simple prompts to cheap models and complex ones to premium, saving 40-70% on API costs with an OpenAI-compatible proxy.
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
- [Grafana](https://github.com/grafana/grafana): Open-source platform for monitoring, observability, and data visualization with dashboards, alerts, and multi-data-source exploration.
- [Pixie](https://github.com/pixie-io/pixie): Kubernetes-native observability platform that uses eBPF to capture metrics, events, traces, and network telemetry without manual instrumentation.
- [Parca](https://github.com/parca-dev/parca): Continuous profiling platform for analyzing CPU and memory usage over time to improve performance, reliability, and infrastructure efficiency.
- [Kepler](https://github.com/sustainable-computing-io/kepler): Kubernetes power and energy exporter for measuring container, pod, and node energy consumption with Prometheus.
- [Inspektor Gadget](https://github.com/inspektor-gadget/inspektor-gadget): eBPF-based inspection toolkit for collecting low-level Kubernetes and Linux operational telemetry.
- [Robusta](https://github.com/robusta-dev/robusta): Kubernetes alert enrichment and automation platform for Prometheus alerts, runbooks, and remediation workflows.
- [Coroot](https://github.com/coroot/coroot): Open-source observability and APM platform with metrics, logs, traces, profiling, SLOs, and AI-assisted root-cause analysis.
- [Pyrra](https://github.com/pyrra-dev/pyrra): SLO management tool for Prometheus that makes service-level objectives accessible, actionable, and easy to use for everyone.
- [Superlog](https://github.com/superloglabs/superlog): Open-source observability tool that uses AI agents to self-heal software by detecting issues and automating fixes.

## Kubernetes Operations

- [Cilium](https://github.com/cilium/cilium): eBPF-based Kubernetes networking, security, and observability platform.
- [Traefik](https://github.com/traefik/traefik): Cloud-native application proxy and ingress controller with automatic service discovery, middleware, and multi-protocol support.
- [kgateway](https://github.com/kgateway-dev/kgateway): Cloud-native API and AI gateway built on Envoy for Kubernetes ingress, traffic management, and AI service routing.
- [Istio](https://github.com/istio/istio): Leading open-source service mesh for connecting, securing, and observing microservices with traffic management, security policies, and telemetry.
- [Linkerd](https://github.com/linkerd/linkerd2): Ultralight, security-first CNCF service mesh for Kubernetes with zero-config mutual TLS and minimal resource footprint.
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
- [Tilt](https://github.com/tilt-dev/tilt): Local Kubernetes development tool for multi-service microservices with live updates and declarative dev environment configuration.
- [Knative](https://github.com/knative/serving): CNCF serverless platform for Kubernetes with scale-to-zero, request-driven compute, and event-driven workloads.
- [k3s](https://github.com/k3s-io/k3s): Lightweight Kubernetes distribution designed for edge, IoT, CI, and resource-constrained environments.
- [containerd](https://github.com/containerd/containerd): Industry-standard container runtime providing the core container lifecycle management for Docker, Kubernetes, and cloud-native platforms.
- [Talos Linux](https://github.com/siderolabs/talos): Modern Linux distribution built specifically for Kubernetes with API-driven configuration, immutable root filesystem, and zero-touch provisioning.
- [KubeEdge](https://github.com/kubeedge/kubeedge): CNCF Kubernetes-native edge computing framework for extending containerized applications to edge nodes with cloud-edge synergy.
- [Rook](https://github.com/rook/rook): CNCF storage orchestrator for Kubernetes, providing self-managing, self-scaling, and self-healing storage services for Ceph, NFS, and other providers.
- [MinIO](https://github.com/minio/minio): High-performance, S3-compatible object storage with native Kubernetes support for AI/ML data lakes, analytics, and cloud-native applications.
- [KubeVirt](https://github.com/kubevirt/kubevirt): Kubernetes-native virtualization platform for running and managing virtual machines alongside containers on Kubernetes.

## Security and Supply Chain

- [Falco](https://github.com/falcosecurity/falco): CNCF runtime security tool for detecting suspicious behavior in containers and Kubernetes.
- [Tetragon](https://github.com/cilium/tetragon): eBPF-based security observability and runtime enforcement tool for detecting and blocking suspicious kernel, container, and network activity in real time.
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
- [Tracecat](https://github.com/TracecatHQ/tracecat): Open-source security automation platform for teams and AI agents with event-driven orchestration, monitoring, and low-code workflows.
- [OneCLI](https://github.com/onecli/onecli): Open-source credential gateway with built-in vault for giving AI agents access to services without exposing secrets.
- [OpenAnt](https://github.com/knostic/OpenAnt): Open-source LLM-based vulnerability discovery tool for proactively finding verified security flaws in AI systems.
- [AI-Infra-Guard](https://github.com/Tencent/AI-Infra-Guard): Full-stack AI red teaming platform for scanning AI infrastructure, agents, skills, MCP servers, and LLM jailbreak vulnerabilities.
- [AgentShield](https://github.com/affaan-m/agentshield): AI agent security scanner for detecting vulnerabilities in agent configurations, MCP servers, and tool permissions via CLI or GitHub Action.
- [Adrian](https://github.com/secureagentics/Adrian): Open-source runtime AI agent security tool that monitors and controls AI agents in real time, catching malicious tool use, prompt injection, and policy drift before the agent acts.

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
- [Dagger](https://github.com/dagger/dagger): Open-source automation engine for building, testing, and shipping code in CI/CD pipelines with programmable, containerized workflows.

### Code Search and Understanding

- [sourcebot](https://github.com/sourcebot-dev/sourcebot): Self-hosted code search and understanding tool for humans and AI agents to navigate, query, and comprehend large codebases.

### AI Coding Tools

- [Aider](https://github.com/Aider-AI/aider): AI pair programming tool that works in your terminal with multi-file editing, git integration, and support for leading LLMs.
- [Continue](https://github.com/continuedev/continue): Open-source AI code assistant that integrates with IDEs as an autopilot for software development with customizable context and models.
- [Tabby](https://github.com/TabbyML/tabby): Self-hosted AI coding assistant with code completion, chat, and agent capabilities that can run fully on-premises.
- [Cline](https://github.com/cline/cline): Autonomous coding agent available as an SDK, IDE extension, and CLI assistant for AI-driven development workflows.
- [OpenHands](https://github.com/All-Hands-AI/OpenHands): AI-driven development platform for automated coding, code review, and software engineering tasks with agent-based workflows.
- [SWE-agent](https://github.com/SWE-agent/SWE-agent): LLM-powered agent that automatically resolves GitHub issues and fixes bugs with iterative, tool-using workflows.
- [GPT-Pilot](https://github.com/Pythagora-io/gpt-pilot): AI developer that builds production-ready applications from natural language specifications with human-in-the-loop guidance.

### Developer Environments

- [Coder](https://github.com/coder/coder): Self-hosted remote development platform for provisioning secure, pre-configured workspaces for developers and AI agents on any infrastructure.
- [DevPod](https://github.com/loft-sh/devpod): Open-source, client-only development environment tool for creating reproducible, infrastructure-agnostic workspaces on any cloud, Kubernetes, or local machine.

### Code Service

- [Trivy](https://github.com/aquasecurity/trivy): Comprehensive scanner for containers, code, vulnerabilities, misconfigurations, and SBOMs.
- [SonarQube](https://github.com/SonarSource/sonarqube): Continuous code quality platform supporting 27+ programming languages.
- [Open Code Review](https://github.com/alibaba/open-code-review): Open-source hybrid code review tool combining deterministic pipelines with LLM agents for precise, line-level feedback at scale.
- [reviewdog](https://github.com/reviewdog): Automated code review and analysis tool for many languages and linters.
- [PR-Agent](https://github.com/The-PR-Agent/pr-agent): Open-source AI-powered PR reviewer for automated code review, description generation, and improvement suggestions across git platforms.
- [opencommit](https://github.com/di-sukharev/opencommit): AI-powered CLI that generates meaningful git commit messages using LLMs, supporting all major providers and local models.
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
- [Cerbos](https://github.com/cerbos/cerbos): Open-core, language-agnostic authorization layer with context-aware access control policies for application resources.
- [dexidp/dex](https://github.com/dexidp/dex): Lightweight pluggable OpenID Connect (OIDC) and OAuth 2.0 provider.
- [pomerium](https://github.com/pomerium/pomerium): Identity-aware proxy with richer access-control capabilities.
- [Infisical](https://github.com/Infisical/infisical): Open-source platform for secrets management, certificate automation, and privileged access management across development and production environments.

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
