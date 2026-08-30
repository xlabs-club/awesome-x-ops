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

**Selection guidance:** Prefer tools that connect traces to prompts, model versions, evaluations, and cost or latency signals; for RAG, favor evaluation workflows that measure retrieval and answer quality without requiring brittle golden-answer sets; use gateway, security, and serving tools in their dedicated sections when observability is not their primary operational purpose.

**Production checklist:** Before adopting a tool, verify OpenTelemetry or an exportable trace format, retention and redaction controls, reproducible evaluation runs, framework coverage, and a clear path from an alert to the underlying prompt, tool call, model, and cost. A dashboard without failure evidence is just a very colorful shrug.

**Regression gate:** Keep a small, versioned evaluation set in CI, compare retrieval and answer-quality metrics separately, and define rollback thresholds before changing prompts, models, retrievers, or gateway policies. “It looked good in the demo” is not a release strategy.

**EvalOps selection guidance:** Prefer evaluation tools that separate retrieval, generation, tool-use, safety, latency, and cost signals; support fixed datasets plus sampled production traces; and emit machine-readable results for CI or release gates. LLM-as-a-judge is useful evidence, not ground truth—pin the judge model and rubric, sample human review, and keep failed cases replayable.

**Operational evidence checklist:** For production rollouts, record the trace and evaluation schema, sampling and PII-redaction policy, owner for each alert, retention and replay limits, and the rollback trigger. If a tool cannot export evidence that another system can inspect, it is an integration risk—not just a missing checkbox.

**Gateway boundary:** Treat routing, rate limits, budgets, retries, and provider failover as gateway concerns; keep tracing, evaluation, and prompt or response analysis here only when they are the tool’s primary operational purpose. This avoids counting one gateway as three observability platforms with different hats.

**Gateway selection guidance:** Choose the smallest control surface that covers provider abstraction, routing policy, quotas, retries, and auditability. Before production rollout, verify streaming behavior, timeout and fallback semantics, tenant isolation, secret rotation, cost attribution, and metrics or traces that remain useful when an upstream provider is degraded.

- [LiteLLM](https://github.com/BerriAI/litellm): OpenAI-compatible LLM gateway with routing, budgets, logging, and provider abstraction.
- [Switchyard](https://github.com/NVIDIA-NeMo/Switchyard): LLM traffic router for selecting models and providers, benchmarking performance, and optimizing cost while preserving OpenAI and Anthropic API compatibility.
- [Langfuse](https://github.com/langfuse/langfuse): Open-source LLM engineering platform for traces, prompt management, evaluations, and metrics.
- [Litefuse](https://github.com/litefuse/litefuse): Open-source LLM engineering platform for collaboratively developing, monitoring, evaluating, and debugging AI applications with self-hosted deployment.
- [DeepEval](https://github.com/confident-ai/deepeval): LLM evaluation framework for testing RAG, agents, and model outputs in CI or production workflows.
- [Ragas](https://github.com/explodinggradients/ragas): Evaluation framework for RAG pipelines and LLM applications.
- [Arize Phoenix](https://github.com/Arize-ai/phoenix): Open-source observability and evaluation platform for LLM, RAG, and ML systems.
- [OpenInference](https://github.com/Arize-ai/openinference): OpenTelemetry instrumentation and semantic conventions for tracing LLM, RAG, and agent applications.
- [Agent Telemetry Semantic Conventions](https://github.com/agent-telemetry-spec/atsc): Vendor-neutral, OpenTelemetry-compatible semantic conventions for interoperable AI agent observability.
- [OpenLLMetry](https://github.com/traceloop/openllmetry): OpenTelemetry-based observability for LLM applications and agent workflows.
- [Multi-agent Observability with OpenTelemetry](https://github.com/chrisipanaque/multi-agent-observability-opentelemetry): OpenTelemetry reference implementation for tracing LangGraph multi-agent systems, including routing decisions, tool calls, LLM invocations, metrics, and OTLP export.
- [Helicone](https://github.com/Helicone/helicone): Open-source observability platform for LLM usage, latency, cost, caching, and request logs.
- [OpenLIT](https://github.com/openlit/openlit): OpenTelemetry-native AI engineering platform for LLM observability, evaluations, guardrails, prompt management, and GPU monitoring.
- [Grafana AI Observability SDK](https://github.com/grafana/sigil-sdk): Open-source SDKs and coding-agent plugins for sending production agent and LLM telemetry to Grafana AI observability.
- [LangWatch](https://github.com/langwatch/langwatch): Open-source platform for LLM monitoring, evaluations, traces, and agent testing.
- [ClaudeSec](https://github.com/aanjaneyasinghdhoni/ClaudeSec): Fully local observability and security dashboard for AI coding agents, with OpenTelemetry traces, command auditing, threat detection, and optional enforcement.
- [Opik](https://github.com/comet-ml/opik): Open-source platform for tracing, evaluating, and monitoring LLM applications, RAG systems, and agent workflows.
- [ClawMetry](https://github.com/vivekchand/clawmetry): Local-first observability and governance dashboard for 26 AI agent runtimes, with sessions, tool calls, token costs, alerts, approvals, and OpenTelemetry export.
- [Exgentic](https://github.com/Exgentic/exgentic): General agent evaluation framework for standardized, reproducible testing across agents, benchmarks, and domains.
- [promptfoo](https://github.com/promptfoo/promptfoo): Open-source CLI and platform for prompt testing, LLM evaluations, red teaming, and CI/CD regression checks.
- [Langtrace](https://github.com/Scale3-Labs/langtrace): OpenTelemetry-based observability platform for tracing, evaluating, and monitoring LLM applications.
- [Future AGI](https://github.com/future-agi/future-agi): Self-hostable platform for evaluating, observing, and improving LLM and AI agent applications.
- [CozeLoop](https://github.com/coze-dev/coze-loop): AI agent optimization platform covering development, debugging, evaluation, and production monitoring workflows.
- [Judgeval](https://github.com/JudgmentLabs/judgeval): Continuous-improvement stack for agents, combining environment data and evaluations to improve and monitor agent behavior.
- [Acontext](https://github.com/memodb-io/Acontext): Open-source memory layer for AI agents that turns reusable agent skills and context into an operational service.
- [Agenta](https://github.com/Agenta-AI/agenta): Open-source LLMOps platform for prompt management, playgrounds, evaluations, and observability.
- [abtop](https://github.com/graykode/abtop): htop-style terminal monitor for AI coding agent sessions, tokens, context windows, rate limits, and ports.
- [agenttrace](https://github.com/luoyuctl/agenttrace): Local-first TUI for inspecting AI coding agent cost, tokens, latency, failures, and reports.
- [agentacct](https://github.com/mikehasa/agentacct): Local-first terminal dashboard that joins coding-agent session usage with recorded work steps, checks, provider limits, and estimated cost.
- [agentglass](https://github.com/SirAllap/agentglass): Local-first cockpit for monitoring coding-agent sessions, tool calls, tokens, costs, and latency through hooks or OpenTelemetry, with optional approval controls.
- [OpenTelemetry MCP Server](https://github.com/traceloop/opentelemetry-mcp-server): Unified MCP server for querying OpenTelemetry traces across Jaeger, Tempo, Traceloop, and other backends so AI agents can investigate distributed systems.
- [Langfuse MCP Server](https://github.com/avivsinai/langfuse-mcp): MCP server and agent skill for querying Langfuse traces, debugging agent runs, inspecting sessions, and managing prompts from AI coding clients.
- [Agent Diff](https://github.com/agent-diff-bench/agent-diff): Interactive, sandboxed replicas of third-party APIs for deterministic AI agent evaluation and reinforcement-learning experiments without external side effects.
- [MCP State Twin](https://github.com/augety121/MCP-State-Twin): Deterministic, forkable, stateful MCP test worlds for reproducible AI agent evaluation without side effects in production systems.
- [SCALE-CUA](https://github.com/THUDM/SCALE-CUA): Open framework for computer-use agents with verifiable task synthesis, online reinforcement learning, and OSWorld or ScienceBoard evaluation.
- [ClawLens](https://github.com/nk3750/clawlens): Local OpenClaw observability plugin with tool-call audit logs, risk scoring, live sessions, and operator-controlled guardrails.
- [Opik MCP](https://github.com/comet-ml/opik-mcp): MCP server for reading Opik traces, logging evaluation scores, and managing prompts from AI coding clients.
- [NeMo Relay](https://github.com/NVIDIA/NeMo-Relay): Multi-language agent runtime and middleware library for managing execution scopes, lifecycle events, and tool or LLM call telemetry.
- [Kitaru](https://github.com/zenml-io/kitaru): Production AI agent recording and replay toolkit for analyzing runs and improving agent behavior.
- [ax](https://github.com/Necmttn/ax): Local-first telemetry and memory graph for AI coding agents, covering costs, tools, skills, sessions, and OTLP events.
- [Mindwalk](https://github.com/cosmtrek/mindwalk): Visualization tool that replays coding-agent sessions on a 3D map of your codebase for debugging and understanding agent behavior.
- [TensorZero](https://github.com/tensorzero/tensorzero): Open-source LLMOps platform that combines an LLM gateway, observability, evaluations, optimization, and experimentation.
- [cascadeflow](https://github.com/lemony-ai/cascadeflow): Cascading runtime for AI agents that makes cost, latency, quality, and policy decisions inside the agent loop.
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
- [LLM Gateway](https://github.com/theopenco/llmgateway): Open-source gateway for routing, managing, and analyzing LLM requests across multiple providers through one API.
- [AI Proxy](https://github.com/labring/aiproxy): High-performance AI gateway with OpenAI-, Claude-, and Gemini-compatible protocols, multi-channel management, rate limiting, multi-tenant isolation, and monitoring.
- [LLMIO](https://github.com/atopos31/llmio): Go-based LLM gateway with weighted provider routing, an admin UI, request tracing, latency and token metrics, cost tracking, and failure handling.
- [OpenZiti LLM Gateway](https://github.com/openziti/llm-gateway): Zero-trust, OpenAI-compatible gateway with identity-based access, semantic routing, and load balancing across hosted and self-hosted model providers.
- [Portkey AI Gateway](https://github.com/Portkey-AI/gateway): AI gateway for routing LLM traffic, applying guardrails, and centralizing model access for production applications.
- [Braintrust AI Proxy](https://github.com/braintrustdata/braintrust-proxy): Self-hostable unified AI model proxy with provider-neutral access, response caching, and request observability hooks.
- [Shepherd Model Gateway (SMG)](https://github.com/smg-project/smg): High-performance, engine-agnostic LLM gateway with cache-aware routing, HTTP/gRPC workers, multi-tenant controls, MCP support, and OpenTelemetry metrics and traces.
- [GoModel](https://github.com/ENTERPILOT/GoModel): Go-based AI gateway with OpenAI and Anthropic-compatible APIs, provider routing, failover, observability, cost tracking, and multi-tenant controls.
- [Traceloop Hub](https://github.com/traceloop/hub): High-performance Rust LLM gateway with a unified provider API, OpenTelemetry traces, Prometheus metrics, and configurable request pipelines.
- [New API](https://github.com/QuantumNous/new-api): Unified AI model gateway for aggregating providers, normalizing OpenAI/Claude/Gemini-compatible APIs, and managing enterprise model access.
- [Manifest](https://github.com/mnfst/manifest): Provider-agnostic runtime that connects agents and agent harnesses to model providers through a unified interface.
- [OmniRoute](https://github.com/diegosouzapw/OmniRoute): Self-hosted AI gateway that unifies many model providers behind one endpoint with automatic fallback, routing, MCP/A2A support, and token-saving compression.
- [Otari](https://github.com/mozilla-ai/otari): Open-source, OpenAI-compatible LLM gateway from Mozilla AI with one endpoint for 40+ providers, virtual keys, budgets, and usage tracking.
- [1flowbase](https://github.com/taichuy/1flowbase): Self-hosted AI gateway for composing multi-model workflows behind OpenAI-compatible virtual models with traces, token usage, latency, and cost visibility.
- [BISHENG](https://github.com/dataelement/bisheng): Open LLM DevOps platform for enterprise AI applications, with GenAI workflows, RAG, agents, model management, evaluation, datasets, and observability.
- [OpenObserve](https://github.com/openobserve/openobserve): Open-source observability platform for logs, metrics, traces, frontend monitoring, pipelines, and LLM observability.
- [Kubeshark](https://github.com/kubeshark/kubeshark): eBPF-powered Kubernetes network observability with L4/L7 traffic context, TLS visibility, and an MCP interface for AI-assisted investigation.
- [MCP Gateway](https://github.com/IBM/mcp-context-forge): AI gateway, registry, and proxy for MCP, A2A, and API tools with centralized discovery, guardrails, and management.
- [Supergateway](https://github.com/supercorp-ai/supergateway): Lightweight bridge that runs MCP stdio servers over SSE and converts SSE connections back to stdio for interoperable deployments.
- [NVIDIA NeMo Guardrails](https://github.com/NVIDIA-NeMo/Guardrails): Toolkit for adding programmable safety, dialog, and policy guardrails to LLM-based conversational systems.
- [Llama Guard](https://github.com/meta-llama/PurpleLlama): Meta's open trust and safety toolkit for evaluating and filtering LLM inputs, outputs, and model risks.
- [LLM Guard](https://github.com/protectai/llm-guard): Security toolkit for sanitizing LLM inputs and outputs, detecting prompt injection, blocking harmful content, and reducing data leakage.
- [garak](https://github.com/NVIDIA/garak): LLM vulnerability scanner for probing prompt injection, jailbreaks, data leakage, hallucination, and other generative AI risks.
- [agentic-security](https://github.com/msoedov/agentic_security): Open-source LLM vulnerability scanner and AI red teaming kit for fuzzing and testing LLM guardrails against adversarial attacks.
- [SlowMist Agent Security](https://github.com/slowmist/slowmist-agent-security): Agent security review framework for adversarial environments, centered on treating every external input as untrusted until verified.
- [Superagent](https://github.com/superagent-ai/superagent): Open-source AI security SDK for protecting LLM applications against prompt injections, data leaks, and harmful outputs.
- [PINT Benchmark](https://github.com/lakeraai/pint-benchmark): Open-source benchmark for evaluating prompt injection detection systems across diverse attack vectors.
- [FuzzyAI](https://github.com/cyberark/FuzzyAI): Apache-2.0 LLM fuzzing tool for finding and mitigating jailbreak vulnerabilities in LLM APIs.
- [OpenEvals](https://github.com/langchain-ai/openevals): Ready-made evaluators for testing and regression-checking LLM applications in development and CI workflows.
- [RAGEval](https://github.com/BytePioneer-AI/RAGEval): Open-source RAG evaluation system for automating dataset-based quality checks across retrieval and generation workflows.
- [TruLens](https://github.com/truera/trulens): Evaluation and tracking framework for LLM experiments and AI agents with feedback functions, guardrails, and iterative improvement workflows.
- [OpenCompass](https://github.com/open-compass/opencompass): LLM evaluation platform supporting a wide range of models across 100+ datasets with reproducible benchmarks.
- [Lighteval](https://github.com/huggingface/lighteval): Modular toolkit for reproducible LLM evaluations across multiple backends, tasks, metrics, and distributed execution environments.
- [OpenAI Evals](https://github.com/openai/evals): Framework for evaluating LLMs and LLM systems with an open-source registry of benchmarks and evaluation workflows.
- [Hugging Face Evaluation Guidebook](https://github.com/huggingface/evaluation-guidebook): Practical guide to LLM evaluation metrics, methods, and lessons from operating large-model evaluation programs.
- [AgentBench](https://github.com/THUDM/AgentBench): Apache-2.0 benchmark for evaluating LLMs as agents across diverse environments and tasks.
- [Olmes](https://github.com/allenai/olmes): Reproducible and flexible framework for evaluating language models across configurable benchmarks and evaluation workflows.
- [PromptWizard](https://github.com/microsoft/PromptWizard): Task-aware, agent-driven prompt optimization framework that uses iterative critique and evaluation to improve prompts for repeatable LLM workflows.
- [Inspect AI](https://github.com/UKGovernmentBEIS/inspect_ai): MIT-licensed framework for building, running, and analyzing reproducible evaluations of large language models.
- [HELM](https://github.com/stanford-crfm/helm): Open-source framework for holistic, reproducible, and transparent evaluation of language and multimodal models.
- [Envoy AI Gateway](https://github.com/envoyproxy/ai-gateway): Envoy-based gateway for managing unified access to generative AI services across providers and platforms.
- [Higress](https://github.com/higress-group/higress): AI-native API gateway built on Envoy for unified LLM provider access, canary routing, rate limiting, and multi-model observability.
- [Bifrost](https://github.com/maximhq/bifrost): High-performance enterprise AI gateway with adaptive load balancing, guardrails, cluster mode, and 1000+ model support.
- [TokenHub](https://github.com/astaxie/TokenHub): Enterprise AI gateway for unified model access, request governance, traceability, and usage attribution.
- [CliRelay](https://github.com/kittors/CliRelay): Self-hosted AI gateway for coding CLIs with a unified endpoint, multi-tenant console, request logs, and spend quotas.
- [Adaline Gateway](https://github.com/adaline/gateway): Fully local TypeScript gateway SDK for calling 300+ LLMs with batching, retries, caching, callbacks, and OpenTelemetry integration.
- [Inference Gateway](https://github.com/inference-gateway/inference-gateway): Cloud-native LLM gateway for unifying providers, routing inference traffic, and exposing OpenTelemetry-friendly operations on Kubernetes.
- [OneAIFW](https://github.com/funstory-ai/aifw): Lightweight local AI firewall for anonymizing sensitive data before LLM calls and restoring it after responses.
- [Microsoft MCP Gateway](https://github.com/microsoft/mcp-gateway): Reverse proxy and management layer for operating MCP servers with session-aware routing and Kubernetes lifecycle support.
- [CoAI](https://github.com/coaidev/coai): Multi-tenant AI platform with a unified LLM gateway, provider routing, cost management, billing, and model cache for enterprise deployments.
- [Kong](https://github.com/Kong/kong): Cloud-native API, LLM, and MCP gateway with advanced AI traffic management, multi-provider routing, semantic security, and rich plugin ecosystem.
- [Apache APISIX](https://github.com/apache/apisix): Apache dynamic API and AI gateway with LLM proxying, token-based rate limiting, MCP bridge, and plugin-based AI traffic control.
- [LangKit](https://github.com/whylabs/langkit): Open-source toolkit for monitoring LLMs by extracting signals from prompts and responses, including text quality, relevance, sentiment, and prompt injection detection.
- [AxonHub](https://github.com/looplj/axonhub): Open-source AI gateway with failover, load balancing, cost control, and end-to-end tracing across 100+ LLM providers.
- [MCP Gateway & Registry](https://github.com/agentic-community/mcp-gateway-registry): Enterprise MCP gateway and AI asset registry with OAuth, semantic search, audit trails, and unified governance for agents, skills, and MCP servers.
- [Weights & Biases](https://github.com/wandb/wandb): AI developer platform for experiment tracking, model management, and monitoring ML/LLM workflows from training to production.
- [ClearML](https://github.com/clearml/clearml): Open-source MLOps/LLMOps platform for experiment management, data pipelines, orchestration, and model serving.
- [Helicone AI Gateway](https://github.com/Helicone/ai-gateway): Fast, lightweight Rust-based AI gateway with smart routing, caching, rate limiting, and built-in observability across 100+ LLM providers.
- [EleutherAI LM Eval](https://github.com/EleutherAI/lm-evaluation-harness): Standardized framework for few-shot and zero-shot evaluation of language models across hundreds of tasks and benchmarks.
- [Weave](https://github.com/wandb/weave): Toolkit for tracing, evaluating, and improving LLM applications with automatic versioning and interactive debugging workflows.
- [Pezzo](https://github.com/pezzolabs/pezzo): Open-source LLMOps platform for prompt management, version control, A/B testing, troubleshooting, and observability.
- [Latitude](https://github.com/latitude-dev/latitude-llm): Open-source AI monitoring and evaluation platform for production LLM applications with collaborative debugging, dataset management, and CI/CD integration.
- [TraceRoot](https://github.com/traceroot-ai/traceroot): Open-source observability and self-healing layer for AI agents, providing real-time monitoring and automated remediation.
- [SkillOpt](https://github.com/microsoft/SkillOpt): Microsoft's text-space optimizer that trains reusable natural-language skills for frozen LLM agents through trajectory-driven edits and validation-gated updates.
- [AgentField](https://github.com/Agent-Field/agentfield): Control plane for building, running, and scaling observable, auditable, identity-aware AI agents as APIs and microservices.
- [Prompty](https://github.com/microsoft/prompty): Markdown-based prompt format and tooling for creating, managing, debugging, and evaluating portable LLM prompts.
- [Databuff](https://github.com/databufflabs/databuff): AI-native OpenTelemetry APM with multi-agent root-cause analysis across traces, metrics, and service topology.
- [RocketplaneIO](https://github.com/olemeyer/rocketplaneIO): Self-hosted AI SRE for Kubernetes with zero-instrumentation eBPF observability and guardrailed, self-verifying remediation.
- [AgentProvenance](https://github.com/ByteYellow/AgentProvenance): Security-oriented observability for sandboxed AI agents, combining model intent, application context, and runtime telemetry into verifiable evidence graphs.
- [AgentCanvas](https://github.com/vstorm-co/agentcanvas): Interactive HTML diagrams for visualizing Pydantic AI agent workflows from Logfire traces, including tools, nested agents, tokens, and cost.
- [Kaito](https://github.com/kaito-project/kaito): Kubernetes AI Toolchain Operator for simplifying model deployment and AI workload management on Kubernetes.
- [OME](https://github.com/ome-projects/ome): Kubernetes operator for LLM serving, GPU scheduling, and model lifecycle management across SGLang, vLLM, TensorRT-LLM, and Triton.
- [AURA](https://github.com/mezmo/aura): Production-oriented harness for safe AI SRE agents, with guardrails, state management, authentication, streaming, and operational tool integrations.
- [ongrid](https://github.com/ongridio/ongrid): Ops AI agent that investigates infrastructure root causes and performs guarded remediation through common team-chat interfaces.
- [Agents Observe](https://github.com/simple10/agents-observe): Real-time observability dashboard for Claude Code and Codex agents with session replay, filtering, and token usage statistics.
- [Pi Agent Observability](https://github.com/disler/pi-agent-observability): Local observability stack for the Pi coding agent, streaming turns, tool calls, model changes, and token-cost telemetry into a dashboard for replay and comparison.
- [Open RAG Eval](https://github.com/vectara/open-rag-eval): Open-source RAG evaluation toolkit for measuring retrieval and answer quality without requiring golden answers.
- [Axon](https://github.com/langchain-tracer/Axon): OpenTelemetry-native LLM observability CLI for viewing LLM and agent traces in real time.
- [EvalScope](https://github.com/modelscope/evalscope): LLM evaluation framework for capability benchmarks, agent-loop evaluation with recorded traces, inference performance testing, and interactive result analysis.
- [Kiln](https://github.com/Kiln-AI/kiln): Open-source workbench for building and improving AI systems with collaborative evals, prompt optimization, RAG, agents, synthetic data, and production deployment support.
- [Google ADK Python](https://github.com/google/adk-python): Code-first Python toolkit for building, evaluating, and deploying production-oriented AI agents with flexible orchestration and tool integration.
- [Google ADK Go](https://github.com/google/adk-go): Code-first Go toolkit for building, evaluating, and deploying production-oriented AI agents with flexible orchestration and tool integration.
- [AssetOpsBench](https://github.com/IBM/AssetOpsBench): Benchmark and framework for building, orchestrating, and evaluating domain-specific industrial AI agents across reproducible asset-operations scenarios.
- [Observal](https://github.com/Observal/Observal): Local registry and analytics platform for governing and understanding AI agents, MCP servers, and reusable agent skills.
- [Agent Prism](https://github.com/evilmartians/agent-prism): React components for visualizing AI agent traces and making multi-step agent execution easier to inspect.
- [Dash0 Agent Skills](https://github.com/dash0hq/agent-skills): OpenTelemetry skills and reference material for AI coding assistants, covering instrumentation patterns and telemetry quality.
- [tma1](https://github.com/tma1-ai/tma1): Local-first observability for coding agents that records LLM calls and exposes logs, metrics, traces, and cost data through hooks and MCP.
- [VictoriaMetrics MCP Server](https://github.com/VictoriaMetrics/mcp-victoriametrics): MCP server for querying VictoriaMetrics from AI assistants and agents, bringing time-series observability context into operational investigations.
- [AgentLens](https://github.com/dreadnode/agent-lens): Harness for running multi-session Claude Code and Codex trajectories with standardized traces, file-change attribution, and replay for agent behavior research.
- [BigQuery Agent Analytics SDK](https://github.com/GoogleCloudPlatform/BigQuery-Agent-Analytics-SDK): Open-source Python SDK for analyzing, evaluating, and curating production agent traces stored in BigQuery.
- [Claude Code Hooks Multi-Agent Observability](https://github.com/disler/claude-code-hooks-multi-agent-observability): Real-time monitoring and visualization for Claude Code agent swarms through hook event tracking, session filters, and live updates.
- [MC Agent Toolkit](https://github.com/monte-carlo-data/mc-agent-toolkit): Agent skills and plugins that bring data lineage, monitoring, validation, alerting, and metadata checks into AI coding workflows.
- [AgentOps Accelerator](https://github.com/Azure/agentops): Open-source CLI and framework for continuous agent evaluation, safety testing, observability, and release-readiness evidence.
- [Smithers](https://github.com/smithersai/smithers): Agent workflow orchestrator with live run observability, human approval gates, and rewind, fork, and replay support across coding-agent runtimes.
- [agent-inspect](https://github.com/rajudandigam/agent-inspect): Local TypeScript agent debugging and regression-testing toolkit that turns runs into execution trees, deterministic contracts, CI gates, and safe evidence bundles.
- [brain0](https://github.com/Brain0-ai/brain0): Offline decision graph for AI-written code that links commits to agent prompts and read context, with drift detection, DLP auditing, risk signals, and signed provenance.
- [TokenTelemetry](https://github.com/VasiHemanth/tokentelemetry): Local dashboard for tracking tokens, costs, tool calls, sessions, and reasoning across coding and autonomous agents.
- [Agent-Blackbox](https://github.com/TaewoooPark/Agent-Blackbox): Local-first flight recorder and context-efficiency profiler for coding agents, with replayable session maps, cost analysis, and task-outcome signals.
- [Mira](https://github.com/everruns/mira): Rust-first evaluation framework for multi-turn, tool-using, long-running agent trajectories with operational budgets and CI-native reports.
- [Tracely](https://github.com/Jwuthri/Tracely): Trace-native CI/CD for AI agents that turns production failures into hermetic regression cases, replays them in CI, and blocks regressions without model spend.
- [aws-bench](https://github.com/aws-bench/aws-bench): Benchmark for evaluating coding agents on real AWS tasks in disposable environments, with verifiers for diagnosis, provisioning, and operations.
- [claw-swe-bench](https://github.com/opensquilla/claw-swe-bench): Adapter framework for evaluating OpenClaw-style agent harnesses on reproducible SWE-bench issue-resolution tasks.
- [OpenAgent Eval](https://github.com/OpenAgentHQ/openagent-eval): Local-first, framework-agnostic evaluation framework for RAG systems and AI agents with CLI, SDK, and multiple metrics.
- [OpenJudge](https://github.com/agentscope-ai/OpenJudge): Open-source evaluation framework for AI applications with reusable graders, scenario-specific rubrics, scalable runs, and reward signals for continuous optimization.
- [AgentEval (.NET)](https://github.com/AgentEvalHQ/AgentEval): .NET toolkit for evaluating AI agents with tool-use validation, RAG quality metrics, stochastic testing, and model comparison.
- [LLM Space](https://github.com/deer-flow/llm-space): Local-first desktop workspace for prototyping agents, inspecting harness steps, replaying failures, and evaluating agent performance.
- [NeMo Gym](https://github.com/NVIDIA-NeMo/Gym): Open framework for evaluating and improving models and agents through configurable environments and evaluation workflows.
- [Agent Evaluation](https://github.com/awslabs/agent-evaluation): Generative AI evaluation framework for concurrent multi-turn virtual-agent testing, custom targets, hooks, and CI/CD integration.
- [AgentArk](https://github.com/P90-RushB/AgentArk): Open environment framework for reproducible multimodal-agent evaluation, replay, and reinforcement-learning workflows with verifiable task feedback.
- [Intellagent](https://github.com/plurai-ai/intellagent): Framework for diagnosing and optimizing agents through realistic simulated interactions and repeatable evaluation workflows.
- [Rhesis](https://github.com/rhesis-ai/rhesis): Open-source collaboration layer where domain experts annotate agent behavior and engineering teams turn findings into evaluation and improvement loops.
- [o11y-bench](https://github.com/grafana/o11y-bench): Open benchmark for evaluating AI agents on observability tasks in reproducible Harbor environments.
- [Dokimos](https://github.com/dokimos-dev/dokimos): Java and Kotlin LLM and agent evaluation framework with JUnit and CI integration, tool-call validation, quality metrics, and cost or latency tracking.
- [eval-guide](https://github.com/microsoft/eval-guide): Microsoft toolkit for planning agent evaluations, generating test cases, interpreting results, and triaging failures in Copilot Studio workflows.
- [SkillEvaluator](https://github.com/NVIDIA/SkillEvaluator): Multi-tier framework for validating, deduplicating, security-scanning, and live-evaluating AI agent skills with quality gates and reproducible reports.
- [AgentEval](https://github.com/canwhite/AgentEval): Agent evaluation framework for testing tool use, task completion, and behavior across repeatable scenarios.
- [Bananalyzer](https://github.com/reworkd/bananalyzer): Open-source framework for evaluating AI agents on web tasks with reproducible test environments and result analysis.
- [Nasiko](https://github.com/Nasiko-Labs/nasiko): AI agent developer control plane for registry, deployment, routing, health monitoring, observability, and lifecycle operations.
- [Nexent](https://github.com/ModelEngine-Group/nexent): Zero-code platform for generating production-oriented AI agents with governed tools, skills, memory, orchestration, feedback loops, and control planes.
- [numbat](https://github.com/perplexityai/numbat): Local endpoint visibility for AI agent activity with hook-based monitoring, CEL detections, optional pre-action blocking, and forensic reconstruction.
- [continuous-eval](https://github.com/relari-ai/continuous-eval): Open-source data-driven evaluation framework for LLM-powered applications, covering retrieval, generation, and end-to-end pipeline quality metrics.
- [UQLM](https://github.com/cvs-health/uqlm): Apache-2.0 Python package for uncertainty quantification in LLMs, detecting hallucinations and low-confidence outputs in production agent workflows.
- [APIPark](https://github.com/APIParkLab/APIPark): Cloud-native AI and API gateway for unified LLM provider management, request routing, load balancing, multi-model failover, usage analytics, and API governance.

## AI Serving and Inference Operations

Tools for deploying, scaling, routing, and operating AI model inference workloads in production.

**Selection guidance:** Separate the serving engine from the control plane: choose engines for throughput, latency, batching, and hardware support; choose operators and gateways for rollout safety, routing, quotas, autoscaling, and telemetry. Prefer projects with reproducible benchmarks and an explicit upgrade or rollback path.

**Rollout gate:** Before shifting production traffic, record a baseline for throughput, tail latency, error rate, GPU utilization, and cost per request; canary model and runtime changes with representative prompts; and keep the previous artifact and routing policy ready for rollback. A faster token/sec number is not a release if the p99 or failure recovery got worse.

- [GenAI Factory](https://github.com/GoogleCloudPlatform/genai-factory): Production-oriented blueprints for deploying generative AI infrastructure on Google Cloud with infrastructure as code and security best practices.
- [GenAI on EKS Starter Kit](https://github.com/aws-samples/sample-genai-on-eks-starter-kit): Kubernetes deployment blueprint combining an AI gateway, LLM serving, vector databases, embedding models, and observability on Amazon EKS.
- [Ray Serve](https://github.com/ray-project/ray): Scalable model serving library in Ray for building distributed online inference APIs and LLM serving workloads.
- [KubeTorch](https://github.com/run-house/kubetorch): Python-native Kubernetes control layer for distributing and running AI workloads across cluster resources.
- [ModelPlane](https://github.com/modelplaneai/modelplane): Open-source control plane for deploying, routing, and operating AI inference workloads.
- [Polyaxon](https://github.com/polyaxon/polyaxon): Open-source AI infrastructure and orchestration platform for managing reproducible ML and LLM workloads across development and production.
- [Triton Inference Server](https://github.com/triton-inference-server/server): Optimized inference server for deploying AI models across GPUs, CPUs, and cloud or edge environments.
- [KServe](https://github.com/kserve/kserve): Kubernetes-native platform for standardized, scalable generative and predictive AI inference serving.
- [Seldon Core](https://github.com/seldonio/seldon-core): MLOps framework for packaging, deploying, monitoring, and managing thousands of production ML models on Kubernetes.
- [LitServe](https://github.com/Lightning-AI/LitServe): Minimal Python framework for building custom AI inference servers with explicit control over batching, request logic, and scaling.
- [AIBrix](https://github.com/vllm-project/aibrix): Cloud-native infrastructure components for cost-efficient, scalable GenAI and LLM inference operations.
- [Dynamo](https://github.com/ai-dynamo/dynamo): Distributed inference serving framework for datacenter-scale LLM and generative AI workloads with Kubernetes-oriented routing and scaling.
- [dstack](https://github.com/dstackai/dstack): Vendor-agnostic control plane for provisioning GPUs and orchestrating training, inference, and agent workloads across clouds, Kubernetes, and bare metal.
- [llm-d](https://github.com/llm-d/llm-d): Kubernetes-native distributed inference stack for high-performance LLM serving with intelligent routing on modern accelerators.
- [GPUd](https://github.com/leptonai/gpud): GPU monitoring and diagnostics tool that automates health checks and issue identification for AI infrastructure.
- [KubeAI](https://github.com/kubeai-project/kubeai): Kubernetes-native inference operator for deploying and scaling LLMs, VLMs, embeddings, rerankers, and speech-to-text models with OpenAI-compatible APIs.
- [Kthena](https://github.com/volcano-sh/kthena): Kubernetes-native AI serving platform for scalable model serving and production inference operations.
- [SkyPilot](https://github.com/skypilot-org/skypilot): Multi-cloud and Kubernetes control plane for running, scaling, and managing AI workloads across heterogeneous GPU infrastructure.
- [GPUStack](https://github.com/gpustack/gpustack): GPU cluster manager for high-performance AI model serving with vLLM and SGLang, plus on-demand GPU instances.
- [KubeRay](https://github.com/ray-project/kuberay): Kubernetes operator and toolkit for deploying and managing Ray clusters and distributed AI workloads.
- [SGLang](https://github.com/sgl-project/sglang): High-performance serving framework for large language models and multimodal models with efficient attention and structured outputs.
- [vLLM](https://github.com/vllm-project/vllm): High-throughput and memory-efficient inference and serving engine for LLMs with continuous batching and quantization.
- [GuideLLM](https://github.com/vllm-project/guidellm): Benchmarking tool for evaluating LLM deployments with real-world latency, throughput, and performance measurements.
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
- [OpenVINO Model Server](https://github.com/openvinotoolkit/model_server): Scalable inference server for OpenVINO-optimized models, exposing production-friendly APIs for deploying AI models.
- [Axolotl](https://github.com/OpenAccess-AI-Collective/axolotl): Open-source LLM fine-tuning framework with support for LoRA, QLoRA, and full-parameter training across popular model architectures.
- [LLaMA-Factory](https://github.com/hiyouga/LLaMA-Factory): Unified framework for LLM fine-tuning with 100+ models and 50+ methods, supporting LoRA, QLoRA, and full-parameter training with web UI workflows.
- [Unsloth](https://github.com/unslothai/unsloth): Open-source library for 2-5x faster LLM fine-tuning with significant memory reduction, supporting major model architectures and training workflows.
- [HAMi](https://github.com/Project-HAMi/HAMi): Heterogeneous GPU sharing middleware for Kubernetes with device memory isolation and multi-tenant scheduling.
- [Llama Deploy](https://github.com/run-llama/llama_deploy): Production deployment framework for LlamaIndex agentic workflows with asynchronous task orchestration and service management.
- [Semantic Router](https://github.com/vllm-project/semantic-router): System-level intelligent runtime for Mixture-of-Models, enabling dynamic model selection and intelligent routing across edge, data center, and cloud environments.
- [FastChat](https://github.com/lm-sys/FastChat): Open platform for training, serving, and evaluating LLMs. Release repo for Vicuna and Chatbot Arena.
- [text-generation-webui](https://github.com/oobabooga/textgen): Open-source desktop app for running LLMs locally with text, vision, tool-calling, and OpenAI/Anthropic-compatible API support.
- [DS4](https://github.com/antirez/ds4): High-performance local inference engine for DeepSeek 4 Flash and PRO, optimized for Metal, CUDA, and ROCm platforms.
- [RouteLLM](https://github.com/lm-sys/RouteLLM): Framework for serving and evaluating LLM routers that direct requests to cheaper models while preserving response quality.
- [Rig](https://github.com/0xPlaygrounds/rig): Rust framework for building modular, scalable LLM applications with composable components and provider integrations.
- [Agent Lightning](https://github.com/microsoft/agent-lightning): Framework for training and optimizing AI agents by connecting agent execution with reinforcement learning and other training methods.
- [verl](https://github.com/verl-project/verl): Flexible and efficient reinforcement-learning framework for post-training large language models and optimizing reasoning or agent workloads.
- [aikit](https://github.com/kaito-project/aikit): Kubernetes-native toolkit for fine-tuning, building, and deploying open-source LLMs with buildkit-based image construction and GPU-accelerated inference.
- [NVIDIA NVCF](https://github.com/NVIDIA/nvcf): Platform for deploying and routing GPU-accelerated inference, streaming, and batch workloads at scale.
- [Grove](https://github.com/ai-dynamo/grove): Kubernetes enhancements for topology-aware gang scheduling and autoscaling of distributed AI workloads.
- [Cube Studio](https://github.com/data-infra/cube-studio): Cloud-native AI platform for Kubernetes with MLOps workflows, distributed training, GPU virtualization, inference serving, and LLMOps capabilities.

## AIOps

- [Netdata](https://github.com/netdata/netdata): Distributed real-time monitoring for infrastructure metrics, visualization, and alerting.
- [Apache HertzBeat](https://github.com/apache/hertzbeat): Apache real-time observability and monitoring system with agentless collection, alerting, status pages, and AI-assisted operations.
- [PostHog](https://github.com/PostHog/posthog): Open-source product analytics platform for user behavior tracking and product metrics.
- [SREWorks](https://github.com/alibaba/SREWorks): Cloud-native DataOps and AIOps platform for operating Kubernetes-based applications and infrastructure.
- [OpenSRE](https://github.com/Tracer-Cloud/opensre): Open-source toolkit for building AI SRE agents with observability, incident management, alerting, and automated root-cause analysis.
- [Keep](https://github.com/keephq/keep): Open-source AIOps and alert management platform for correlating, enriching, and automating incident response across monitoring tools.
- [AiSOC](https://github.com/beenuar/AiSOC): Open-source AI-powered Security Operations Center for alert fusion, agent-assisted triage, purple-team drills, and MITRE ATT&CK investigation workflows.
- [APO](https://github.com/CloudDetail/apo): AI-powered observability platform combining OpenTelemetry, eBPF, and LLM agentic workflows for automated root-cause analysis and intelligent troubleshooting.
- [HolmesGPT](https://github.com/HolmesGPT/holmesgpt): CNCF Sandbox SRE agent that investigates alerts and operational incidents using cluster context, runbooks, and observability data.
- [K8sGPT](https://github.com/k8sgpt-ai/k8sgpt): Kubernetes troubleshooting tool that applies codified SRE analyzers to diagnose and triage cluster issues with optional AI backends.
- [kagent](https://github.com/kagent-dev/kagent): Kubernetes-native framework for building, deploying, and managing AI agents with MCP tools and OpenTelemetry tracing for infrastructure operations.
- [Metaflow](https://github.com/Netflix/metaflow): Human-centric framework for developing, versioning, scaling, and deploying production AI/ML systems from prototypes to reliable workflows.
- [Chaterm](https://github.com/chaterm/Chaterm): Open-source AI terminal for cloud and infrastructure management, enabling natural-language deployment, troubleshooting, and automation across SSH, Kubernetes, and cloud services.
- [Versus Incident](https://github.com/VersusControl/versus-incident): Self-hosted AI SRE agent that learns normal system behavior and routes novel or unexpected incidents to chat and on-call platforms.
- [Flawless](https://github.com/William-Lu-stack/Flawless): AI-native SRE control plane for Kubernetes and cloud infrastructure, connecting evidence, human approval, controlled remediation, rollback, and recovery verification in an auditable loop.
- [Nudgebee](https://github.com/nudgebee/nudgebee): Open-source SRE copilot for Kubernetes and major clouds, combining observability, FinOps, runbook automation, incident response, and ChatOps workflows.
- [AIOpsLab](https://github.com/microsoft/AIOpsLab): Holistic framework for designing, developing, and evaluating autonomous AIOps agents against reproducible operations scenarios.
- [SREGym](https://github.com/SREGym/SREGym): Benchmark and experimentation framework for evaluating whether AI agents can diagnose and resolve production incidents in reproducible SRE environments.

## AI Infrastructure

Infrastructure for web crawling, AI-ready extraction, search intelligence, and RAG data acquisition workflows.

**Selection guidance:** Separate acquisition from retrieval: crawlers and parsers should expose provenance, incremental refresh, rate-limit controls, and failure visibility; vector or hybrid search layers should make indexing, filtering, access control, and relevance evaluation explicit. Prefer components that can be operated independently rather than opaque end-to-end demos.

- [MinerU](https://github.com/opendatalab/MinerU): High-accuracy document parsing engine that converts PDFs, Office files, and images into structured Markdown or JSON for LLM, RAG, and agent workflows.
- [MetaMCP](https://github.com/metatool-ai/metamcp): Self-hosted MCP aggregator, orchestrator, middleware, and gateway for composing and governing tool servers.
- [Firecrawl](https://github.com/firecrawl/firecrawl): Web search, scraping, crawling, and extraction API that turns web data into LLM-ready Markdown and structured outputs.
- [anydoc](https://github.com/firecrawl/anydoc): Fast Rust library with Node.js, Python, and WebAssembly bindings for converting office documents, PDFs, and other files into clean, LLM-ready Markdown.
- [Crawl4AI](https://github.com/unclecode/crawl4ai): Open-source LLM-friendly web crawler and scraper for building RAG, agent, and web data pipelines.
- [Jina Reader](https://github.com/jina-ai/reader): URL-to-LLM converter that turns any web page into clean, LLM-friendly Markdown with a simple prefix.
- [Open SEO](https://github.com/every-app/open-seo): Open-source SEO and search intelligence platform for keyword research, site audits, backlink analysis, and Google Search Console MCP workflows.
- [Milvus](https://github.com/milvus-io/milvus): Cloud-native vector database for billion-scale similarity search and unstructured data retrieval in RAG and AI pipelines.
- [Qdrant](https://github.com/qdrant/qdrant): High-performance vector search engine with rich filtering, payload storage, and production-ready scalability for AI applications.
- [Chroma](https://github.com/chroma-core/chroma): Embedding-first vector database for building LLM applications with simple local development and client-server deployment.
- [Unstructured](https://github.com/Unstructured-IO/unstructured): Open-source ETL library for converting PDFs, HTML, Word, and other documents into clean structured data for RAG and LLM pipelines.
- [MarkItDown](https://github.com/microsoft/markitdown): Microsoft's open-source tool for converting files and Office documents to Markdown for LLM and RAG data pipelines.
- [Docling](https://github.com/docling-project/docling): IBM's open-source document understanding toolkit for converting PDFs, DOCX, PPTX, images, and HTML into LLM-ready structured formats at scale.
- [PaddleOCR](https://github.com/PaddlePaddle/PaddleOCR): Open-source OCR toolkit for converting PDFs and images into structured data for multilingual AI and RAG pipelines.
- [Pathway LLM App](https://github.com/pathwaycom/llm-app): Ready-to-run templates for production RAG, AI pipelines, and enterprise search with live data connectors and Docker-friendly deployment.
- [Cognita](https://github.com/truefoundry/cognita): Open-source modular RAG framework for building production applications with configurable data ingestion, retrieval, and serving components.
- [SuperDuper](https://github.com/superduper-io/superduper): Open-source framework for building custom AI applications and agents directly on existing data stores, with integrated model, data, and deployment workflows.
- [Weaviate](https://github.com/weaviate/weaviate): Open-source vector database combining vector search with structured filtering and generative AI integrations.
- [pgvector](https://github.com/pgvector/pgvector): Open-source vector similarity search extension for PostgreSQL, widely used for RAG and AI embedding storage.
- [LanceDB](https://github.com/lancedb/lancedb): Developer-friendly embedded vector database for multimodal AI search with serverless architecture and zero-copy retrieval.
- [zvec](https://github.com/alibaba/zvec): Lightweight, lightning-fast in-process vector database from Alibaba for embedded AI search and retrieval, Apache-2.0.
- [Manticore Search](https://github.com/manticoresoftware/manticoresearch): Open-source search database for full-text, vector, and hybrid search with real-time indexing and SQL.
- [USearch](https://github.com/unum-cloud/USearch): Fast, compact open-source vector search and clustering engine with bindings for multiple languages.
- [txtai](https://github.com/neuml/txtai): All-in-one AI framework for semantic search, LLM orchestration, and language model workflows with embeddings and pipelines.
- [Feast](https://github.com/feast-dev/feast): Open-source feature store for AI/ML that serves features consistently for model training and online inference.
- [Instructor](https://github.com/567-labs/instructor): Structured outputs for LLMs with Pydantic validation, automatic retries, and provider-agnostic API.
- [pgai](https://github.com/timescale/pgai): Open-source suite for building RAG, semantic search, and AI applications directly on PostgreSQL with vector and AI tooling.
- [Browser Use](https://github.com/browser-use/browser-use): Open-source web automation toolkit that enables AI agents to browse websites, extract data, and automate online tasks at scale.
- [Agent-Reach](https://github.com/Panniantong/Agent-Reach): Give your AI agent eyes to see the entire internet — read and search Twitter, Reddit, YouTube, GitHub, Bilibili, and more via one CLI with zero API fees.
- [Steel Browser](https://github.com/steel-dev/steel-browser): Open-source headless browser sandbox for AI agents and applications, providing production-ready web automation infrastructure.
- [E2B](https://github.com/e2b-dev/E2B): Open-source secure cloud sandbox for running AI agent code with isolated environments, file system access, and real-world tool execution.
- [headroom](https://github.com/headroomlabs-ai/headroom): Compress tool outputs, logs, files, and RAG chunks before reaching the LLM — 60-95% fewer tokens, same answers.
- [fastmcp](https://github.com/PrefectHQ/fastmcp): The fast, Pythonic way to build MCP servers and clients for AI agent tool infrastructure.
- [Stagehand](https://github.com/browserbase/stagehand): Open-source SDK for building browser agents with AI-powered web automation, extraction, and interaction at scale.
- [FlagEmbedding](https://github.com/FlagOpen/FlagEmbedding): Open-source toolkit for embedding and reranking models (BGE series) powering retrieval-augmented LLM applications.
- [Open WebUI](https://github.com/open-webui/open-webui): Self-hosted LLM chat interface with RAG, web search, tool integration, model management, and multi-user deployment for internal AI platforms.
- [InsForge](https://github.com/InsForge/InsForge): Open-source backend platform for agentic coding that provides database, authentication, storage, compute, hosting, and an AI gateway for full-stack applications.
- [Label Studio](https://github.com/HumanSignal/label-studio): Open-source data labeling platform for images, text, audio, video, and time series in ML and LLM training workflows.
- [Argilla](https://github.com/argilla-io/argilla): Open-source collaboration platform for building, curating, and versioning high-quality datasets for LLM fine-tuning and evaluation.
- [llmware](https://github.com/llmware-ai/llmware): Unified open-source framework for enterprise LLM applications with integrated RAG, parsing, embedding, and vector database orchestration.
- [AgentGateway](https://github.com/agentgateway/agentgateway): Next-generation agentic proxy for AI agents and MCP servers, providing secure access, routing, and policy management for agent tool integrations.
- [Lunar.dev](https://github.com/TheLunarCompany/lunar): Open-source gateway for governing and optimizing third-party API and MCP traffic from applications and AI agents with visibility, policy enforcement, and traffic shaping.
- [Jarvis Registry](https://github.com/ascending-llc/jarvis-registry): Enterprise MCP and A2A gateway with identity-aware access control, tool discovery, OpenTelemetry tracing, and Prometheus metrics.
- [Maxun](https://github.com/getmaxun/maxun): Open-source no-code platform for web scraping, crawling, search, and AI data extraction, turning websites into structured APIs for RAG and AI pipelines.
- [GPT-Researcher](https://github.com/assafelovic/gpt-researcher): Autonomous AI agent for comprehensive web research, report generation, and knowledge synthesis using multi-source data retrieval.
- [rtk](https://github.com/rtk-ai/rtk): CLI proxy that reduces LLM token consumption by 60-90% on common dev commands, lowering AI infrastructure costs in development workflows.
- [Context7](https://github.com/upstash/context7): MCP server that provides up-to-date code documentation and library references to LLMs and AI code editors at inference time.
- [Pathway](https://github.com/pathwaycom/pathway): Python ETL framework for stream processing, real-time analytics, LLM pipelines, and RAG with unified batch-and-streaming execution.
- [MindsDB](https://github.com/mindsdb/mindshub): AI database platform that connects models to data sources, enabling AI-powered queries, automations, and agent workflows.
- [Open Connector](https://github.com/oomol-lab/open-connector): Open-source auth gateway connecting 1000+ SaaS providers to AI agents through SDK, CLI, MCP, HTTP, and OpenAPI.
- [MCP Use](https://github.com/mcp-use/mcp-use): Fullstack MCP framework for building MCP applications, servers, and agent tools for ChatGPT, Claude, and other AI assistants.
- [Composio](https://github.com/ComposioHQ/composio): Agent tool-integration platform with managed toolkits, tool search, authentication, context management, and sandboxed execution.
- [PageIndex](https://github.com/VectifyAI/PageIndex): Vectorless, reasoning-based document indexing system for retrieval-augmented generation over long documents.
- [Onyx](https://github.com/onyx-dot-app/onyx): Open-source AI platform for enterprise search and AI chat, combining retrieval, connectors, agent workflows, and self-hosted deployment.
- [MCP Inspector](https://github.com/modelcontextprotocol/inspector): Developer tool with a web client and proxy for interactively testing and debugging MCP servers across supported transports.
- [MCP Router](https://github.com/mcp-router/mcp-router): Unified MCP server management application for discovering, configuring, and operating MCP servers from one interface.
- [DB-GPT](https://github.com/eosphoros-ai/DB-GPT): Open-source agentic AI data assistant for building data products, Text-to-SQL, RAG, and multi-agent workflows over private data.
- [BoxLite](https://github.com/boxlite-ai/boxlite): Daemonless micro-VM runtime for AI agents — hardware-isolated, OCI-native execution environments embeddable as a library or deployed as a server.
- [Docker MCP Gateway](https://github.com/docker/mcp-gateway): Docker CLI plugin and gateway for securely running, deploying, and managing MCP servers in local or production workflows.
- [Unla](https://github.com/AmoyLab/Unla): Lightweight MCP gateway that exposes existing MCP servers and APIs through a managed endpoint with Docker deployment and a management UI.
- [HelixDB](https://github.com/HelixDB/helix-db): Rust-built graph-vector database for knowledge graphs, AI memory, and unified access to relational, document, key-value, and vector data.
- [RocketRide](https://github.com/rocketride-org/rocketride-server): Open-source AI pipeline builder and runtime with a C++ core, extensible nodes, vector database integrations, and IDE/CLI workflows for production AI systems.
- [Golf](https://github.com/golf-mcp/golf): Production-ready MCP server framework with authentication, observability, debugging, telemetry, and runtime capabilities for deploying secure agent infrastructure.
- [Airweave](https://github.com/airweave-ai/airweave): Open-source context retrieval layer that syncs diverse data sources into searchable context for AI agents and applications.
- [OpenSandbox](https://github.com/opensandbox-group/OpenSandbox): Secure, fast, and extensible sandbox runtime for isolating AI agent code and tool execution.
- [Kubernetes Agent Sandbox](https://github.com/kubernetes-sigs/agent-sandbox): Kubernetes API and controller for managing isolated, stateful, singleton workloads such as AI agent runtimes.
- [KARS](https://github.com/Azure/kars): Microsoft’s Kubernetes reference stack for running AI agents with hardened per-agent sandboxes, governed egress, and encrypted inter-agent communication.
- [Pullrun](https://github.com/pullrun/pullrun): AI agent sandbox runtime that boots OCI images in Firecracker microVMs, Linux containers, or Apple Silicon VMs with native MCP support.
- [AgentENV](https://github.com/kvcache-ai/AgentENV): Distributed platform for running large numbers of snapshot-backed Firecracker agent environments with fast startup, pause, fork, and E2B-compatible APIs.
- [AgentOS](https://github.com/rivet-dev/agentos): Library that gives AI agents an operating-system-like runtime in an existing backend using WebAssembly and V8 isolates.
- [Cua](https://github.com/trycua/cua): Open-source computer-use infrastructure with cross-platform drivers, fleets, and benchmarks for agent training, evaluation, and data generation.
- [Apache Doris](https://github.com/apache/doris): Real-time analytics and hybrid-search database for AI agents and operational data workloads.
- [Dormice](https://github.com/BitMiracle-AI/Dormice): Self-hosted, E2B-compatible agent sandbox runtime where sandboxes persist indefinitely and idle costs nothing.
- [Agent-Sandbox](https://github.com/agent-sandbox/agent-sandbox): Enterprise-grade sandbox platform for AI agents, supporting secure execution of untrusted LLM-generated code, browser use, and computer use.
- [OpenKruise Agents](https://github.com/openkruise/agents): Kubernetes operator and best-practice guide for rapid, cost-effective agent sandbox lifecycle management at scale.
- [ArtifactFS](https://github.com/cloudflare/artifact-fs): FUSE filesystem driver that mounts large git repos instantly with on-demand hydration, eliminating clone latency for agents, sandboxes, and containers.
- [Docker Compose for Agents](https://github.com/docker/compose-for-agents): Docker Compose examples for running open-source LLMs, tools, and agent runtimes as reproducible local or deployment workflows.

## LLM Knowledge

Open-source platforms for building, managing, and querying LLM-powered knowledge bases from unstructured documents.

**Selection guidance:** Treat ingestion, retrieval, evaluation, and serving as separate failure domains. Prefer projects with incremental re-indexing, source citations, connector or parser coverage, access-control boundaries, and measurable retrieval or answer-quality checks. A chatbot that cannot explain where an answer came from is a demo wearing a production badge.

**RAG release gate:** Keep ingestion, retrieval, and generation metrics separate; pin parser, embedding, and reranker versions; retain source and chunk identifiers for replay; and canary index or prompt changes against a fixed evaluation set before full rollout. If retrieval quality regresses, roll back the index or retriever first instead of compensating with a larger model.

- [Graphify](https://github.com/Graphify-Labs/graphify): Zero-server code intelligence engine that builds an explorable knowledge graph from code, documentation, schemas, configs, and PDFs for agent-assisted code understanding.
- [Agentset](https://github.com/agentset-ai/agentset): Open-source platform for building, evaluating, and shipping production-ready RAG and agentic applications with ingestion, vector indexing, citations, hosting, and developer APIs.
- [RAGFlow](https://github.com/infiniflow/ragflow): Leading open-source RAG engine that combines deep document understanding, knowledge base management, and agent capabilities for enterprise knowledge workflows.
- [FastGPT](https://github.com/labring/FastGPT): Knowledge-based LLM application platform with out-of-the-box data processing, model invocation, RAG, and visual workflow orchestration.
- [AnythingLLM](https://github.com/Mintplex-Labs/anything-llm): Local-first document chat and agent platform that turns any document into a context-aware LLM knowledge base.
- [WeKnora](https://github.com/Tencent/WeKnora): Open-source LLM knowledge platform that turns raw documents into a queryable RAG, an autonomous reasoning agent, and a self-maintaining Wiki.
- [MaxKB](https://github.com/1Panel-dev/MaxKB): Open-source enterprise platform for building knowledge base agents with RAG, multi-model support, and visual workflow design.
- [GraphRAG](https://github.com/microsoft/graphrag): Microsoft's modular graph-based RAG system for extracting knowledge graphs from documents and improving retrieval quality.
- [HippoRAG](https://github.com/OSU-NLP-Group/HippoRAG): RAG framework inspired by human long-term memory that combines knowledge graphs and personalized PageRank for continuous knowledge integration.
- [Mem0](https://github.com/mem0ai/mem0): Universal memory layer for AI agents with multi-level memory, entity linking, and temporal reasoning for personalized interactions.
- [Zep](https://github.com/getzep/zep): Open-source memory layer for AI agents providing long-term recall, user facts, and knowledge graph capabilities for persistent agent memory.
- [Graphiti](https://github.com/getzep/graphiti): Open-source engine for building temporally aware, real-time knowledge graphs that give AI agents structured, continuously updated context.
- [Memori](https://github.com/MemoriLabs/Memori): LLM-agnostic memory infrastructure that turns agent execution and conversations into persistent, structured state for production systems.
- [Memvid](https://github.com/memvid/memvid): Serverless, single-file memory layer for agents that provides local-first retrieval without the operational overhead of a multi-service RAG stack.
- [AutoRAG](https://github.com/Marker-Inc-Korea/AutoRAG): Open-source framework for RAG evaluation and optimization with AutoML-style automation for pipeline tuning.
- [MemoryBench](https://github.com/supermemoryai/memorybench): Unified benchmark for evaluating conversational memory and RAG across multiple datasets.
- [MemPalace](https://github.com/MemPalace/mempalace): Open-source AI memory system with best-in-class benchmarks, providing persistent knowledge storage for AI agents and LLM applications.
- [LightRAG](https://github.com/HKUDS/LightRAG): Simple and fast RAG framework with graph-based retrieval, supporting incremental updates and efficient knowledge graph construction.
- [Kotaemon](https://github.com/Cinnamon/kotaemon): Open-source RAG-based document QA tool with multi-model support and a customizable UI for chatting with documents.
- [Quivr](https://github.com/QuivrHQ/quivr): Opinionated RAG platform for integrating GenAI into applications, supporting any LLM, vector store, and file type.
- [R2R](https://github.com/sciphi-ai/r2r): Production-ready AI retrieval system with agentic RAG and a RESTful API for enterprise knowledge workflows.
- [Langchain-Chatchat](https://github.com/chatchat-space/Langchain-Chatchat): RAG and Agent application platform based on LangChain and local LLMs such as ChatGLM, Qwen, and Llama with knowledge base management.
- [Semantica](https://github.com/semantica-agi/semantica): Graph-native infrastructure for connecting context, knowledge, and accountable evidence in AI systems.
- [Cognee](https://github.com/topoteretes/cognee): Open-source AI memory platform that gives agents persistent long-term memory through a self-hosted knowledge graph and vector database engine.
- [OpenViking](https://github.com/volcengine/OpenViking): Self-evolving context database for AI agents that unifies agent memory, knowledge RAG, and skills into a single retrieval surface.
- [DocsGPT](https://github.com/arc53/DocsGPT): Self-hosted private AI platform for enterprise search, document analysis, agent building, and multi-model assistants.
- [LLM Wiki](https://github.com/nashsu/llm_wiki): Cross-platform document workspace that incrementally builds an organized, interconnected knowledge base instead of re-answering from scratch on every query.
- [SurfSense](https://github.com/MODSetter/SurfSense): Open-source NotebookLM alternative for researching live web sources through a self-hosted application, API, or MCP server.
- [Vespa](https://github.com/vespa-engine/vespa): Production AI search and serving platform for combining vector, lexical, and structured retrieval with real-time ranking and recommendations.
- [Yuxi](https://github.com/xerrors/Yuxi): Self-hosted, multi-tenant knowledge-agent platform combining RAG, knowledge graphs, multi-agent workflows, MCP/Skills, sandboxing, and access control.

## Agentic Workflow

- [Paperclip](https://github.com/paperclipai/paperclip): Open-source control plane for coordinating teams of AI agents with goals, org charts, approvals, budgets, persistent work, and audit trails.
- [LoopX](https://github.com/huangruiteng/loopx): Provider-neutral, local-first control plane for long-horizon agents with durable state, governance, recovery, evidence, and human-agent collaboration.
- [AutoGPT](https://github.com/Significant-Gravitas/Auto-GPT): Autonomous AI agent framework that can break down and execute complex tasks.
- [Atmosphere](https://github.com/Atmosphere/atmosphere): Portable JVM agent runtime that unifies model providers and agent frameworks with streaming, tool calls, human approvals, governance, and MCP or A2A support.
- [Google AX](https://github.com/google/ax): Open-source distributed agent runtime for coordinating agent applications across scalable execution environments.
- [AgentScope Runtime](https://github.com/agentscope-ai/agentscope-runtime): Production-oriented runtime for agent applications with secure tool sandboxing, Agent-as-a-Service APIs, scalable deployment, and full-stack observability.
- [SandBase Harness](https://github.com/sandbaseai/sandbase-harness): Self-hosted agent runtime with MCP tools, persistent sessions, approval gates, audit/replay, and backend-selectable execution sandboxes.
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
- [CopilotKit](https://github.com/CopilotKit/CopilotKit): Frontend stack for agents and generative UI with React, Angular, and mobile support. Makers of the AG-UI Protocol for agent-user interaction.
- [Aegra](https://github.com/aegra/aegra): Open-source self-hosted AI agent backend built with FastAPI and PostgreSQL, a zero-lock-in alternative to managed agent deployment platforms.
- [CowAgent](https://github.com/zhayujie/CowAgent): Open-source super AI assistant and agent harness that plans tasks, runs tools and skills, and self-evolves with memory and knowledge (formerly chatgpt-on-wechat).
- [Activepieces](https://github.com/activepieces/activepieces): Open-source AI automation platform with ~400 built-in MCP servers for no-code AI agent workflows, automation, and MCP integrations.
- [NanoBot](https://github.com/HKUDS/nanobot): Lightweight, open-source AI agent for tools, chats, and automated workflows with extensible plugin architecture.
- [Harbor Framework](https://github.com/harbor-framework/harbor): Framework for evaluating and improving agents and language models across reproducible environments and parallel experiments.
- [LangBot](https://github.com/langbot-app/LangBot): Production-oriented multi-platform bot platform with agent workflows, knowledge bases, plugins, and integrations for chat systems.
- [Dapr Agents](https://github.com/dapr/dapr-agents): CNCF-aligned framework for resilient, observable AI agents with durable workflows, state, messaging, MCP integration, and Kubernetes-native operations.
- [Agent Control Plane](https://github.com/humanlayer/agentcontrolplane): Distributed scheduler for unsupervised, long-running agents with asynchronous tool calls, human feedback gates, and MCP support.
- [Agent Control](https://github.com/agentcontrol/agent-control): Apache-2.0 control plane for governing agent runtime behavior at scale with configurable policies and extensibility.
- [Workflow SDK](https://github.com/vercel/workflow): TypeScript SDK for adding durable execution, reliability, and observability to asynchronous applications and AI agents.
- [Amazon Bedrock AgentCore Samples](https://github.com/awslabs/agentcore-samples): Production-oriented examples for deploying AI agents with evaluation, observability, and operational patterns on AWS.
- [LiveKit Agents](https://github.com/livekit/agents): Framework for building production-ready realtime voice and multimodal AI agents with integrations for models, tools, and telephony.
- [Heym](https://github.com/heymrun/heym): Self-hosted AI workflow platform with visual and prompt-driven workflows, RAG, MCP, human approval, observability, evaluations, and token-cost tracking.
- [Rapida](https://github.com/rapidaai/voice-ai): Open-source, end-to-end voice AI orchestration platform for real-time agents, integrating audio streaming, STT, TTS, VAD, multi-channel delivery, and observability.
- [Google Cloud Agent Starter Pack](https://github.com/GoogleCloudPlatform/agent-starter-pack): Production-oriented templates for deploying AI agents to Google Cloud with built-in CI/CD, evaluation, observability, and common enterprise integrations.
- [LiteLLM Agent Control Plane](https://github.com/LiteLLM-Labs/litellm-agent-control-plane): Self-hosted control plane for running agents across multiple runtimes with unified access, persistent sessions, scheduled jobs, and shared team management.
- [Claude Code Router](https://github.com/musistudio/claude-code-router): Local control plane for routing Claude Code requests across model providers and orchestrating agent capabilities.
- [ClawManager](https://github.com/Yuan-lab-LLM/ClawManager): Kubernetes-native control plane for governing AI agent instances, runtime orchestration, AI access, and reusable resources across agent runtimes.
- [Archestra](https://github.com/archestra-ai/archestra): Enterprise AI platform with guardrails, an MCP registry, gateway, and orchestration for governed agent operations.
- [Microsoft Agent Framework](https://github.com/microsoft/agent-framework): MIT-licensed framework for building, orchestrating, and deploying AI agents and multi-agent workflows across Python and .NET.
- [OpenAI Agents SDK](https://github.com/openai/openai-agents-python): Lightweight Python framework for multi-agent workflows with tools, handoffs, guardrails, and tracing-oriented runtime patterns.
- [Strands Agents Harness SDK](https://github.com/strands-agents/harness-sdk): Apache-2.0 SDK for building and controlling production AI-agent harnesses in Python and TypeScript across models and clouds.
- [OxyGent](https://github.com/jd-opensource/OxyGent): Modular, observable, and evolvable multi-agent framework with a unified abstraction for composing production agent systems.
- [Deep Agents](https://github.com/langchain-ai/deepagents): Batteries-included agent harness for long-running tasks with planning, subagents, filesystem access, and operational workflow composition.
- [LongHorizon-Harness](https://github.com/AMAP-ML/LongHorizon-Harness): Loop-engineering harness for running Claude Code, Codex, and DeepSeek Harness across desktop apps and terminals with checkpoints, verification, recovery, and long-running task state.
- [Google ADK JavaScript](https://github.com/google/adk-js): Code-first TypeScript toolkit for building, evaluating, and deploying AI agents with flexible orchestration and tool integration.
- [Google ADK Java](https://github.com/google/adk-java): Code-first Java toolkit for building, evaluating, and deploying AI agents with flexible orchestration and tool integration.
- [Ouroboros](https://github.com/Q00/ouroboros): Self-improving Agent OS with interview-gated, staged evaluation and budgeted evolution loops across 13 coding-agent runtimes including Claude Code, Codex, and Gemini CLI.

## DataOps

- [Dagster](https://dagster.io/): Data orchestration platform for modeling data assets and managing the data lifecycle.
- [Apache NiFi](https://nifi.apache.org/): Visual dataflow orchestration for routing, transforming, and coordinating data across systems.
- [DataHub](https://github.com/datahub-project/datahub): Metadata platform for data discovery, lineage, governance, and observability across modern data and AI stacks.
- [OpenMetadata](https://github.com/open-metadata/OpenMetadata): Unified metadata platform for data discovery, lineage, governance, and data observability.
- [Great Expectations](https://github.com/great-expectations/great_expectations): Data quality framework for validating datasets, documenting expectations, and catching pipeline regressions.
- [Dingo](https://github.com/MigoXLab/dingo): Open-source AI data-quality evaluation tool for validating LLM datasets, detecting hallucinations, and checking RAG application quality.
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
- [Airbyte](https://github.com/airbytehq/airbyte): Open-source data integration platform for building ELT pipelines from APIs, databases, and files to warehouses, lakes, and AI applications.
- [Mage](https://github.com/mage-ai/mage-ai): Open-source data pipeline platform for building, running, and managing AI-ready data integrations and transformations.
- [DVC](https://github.com/iterative/dvc): Open-source data version control and ML experiment management for tracking datasets, models, and pipelines.

### Streaming Operations

Streaming systems provide the event transport and analytics foundation for telemetry, RAG refreshes, usage metering, and other continuously updated operational data flows.

- [Kafbat UI](https://github.com/kafbat/kafka-ui): Open-source web UI for managing Apache Kafka clusters, topics, consumers, schemas, and Kafka Connect.
- [Apache SeaTunnel](https://github.com/apache/seatunnel): Distributed data integration platform for high-volume batch and streaming data movement.

## FinOps

- [Infracost](https://github.com/infracost/infracost): Cloud cost forecasting tool for Terraform and Kubernetes cost estimates.
- [kubecost](https://kubecost.com/): Kubernetes cost management and monitoring platform.
- [OpenCost](https://opencost.io/): Open-source tool for tracking and allocating cloud costs in Kubernetes environments.
- [OptScale](https://github.com/hystax/optscale): Open-source FinOps and cloud cost optimization platform for AWS, Azure, GCP, Alibaba Cloud, and Kubernetes.
- [Cloud Custodian](https://github.com/cloud-custodian/cloud-custodian): Policy-as-code rules engine for cloud governance, cost optimization, and automated resource actions.
- [OpenMeter](https://github.com/openmeterio/openmeter): Open-source metering and billing for AI, API, and DevOps with real-time usage aggregation and usage-based pricing.
- [Trench](https://github.com/FrigadeHQ/trench): Self-hosted analytics infrastructure built on Kafka and ClickHouse for high-volume event tracking and real-time operational analytics.
- [NadirClaw](https://github.com/NadirRouter/NadirClaw): Open-source LLM router and AI cost optimizer that routes simple prompts to cheap models and complex ones to premium, saving 40-70% on API costs with an OpenAI-compatible proxy.
- [KubeStellar Console](https://github.com/kubestellar/console): Multi-cluster Kubernetes dashboard with AI-powered operations, real-time observability, and CNCF project integrations across edge and cloud clusters.

## Observability

- [Prometheus](https://github.com/prometheus/prometheus): Monitoring system and time-series database widely used for cloud-native metrics and alerting.
- [VictoriaMetrics](https://github.com/VictoriaMetrics/VictoriaMetrics): Fast, cost-efficient time-series database and monitoring stack for Prometheus-compatible metrics at scale.
- [Grafana Mimir](https://github.com/grafana/mimir): Horizontally scalable, multi-tenant long-term storage backend for Prometheus metrics.
- [Thanos](https://github.com/thanos-io/thanos): CNCF highly available Prometheus setup with long-term storage, global query view, and downsampling for multi-cluster metrics.
- [Grafana Tempo](https://github.com/grafana/tempo): Distributed tracing backend for high-volume trace storage with minimal indexing overhead.
- [Perses](https://github.com/perses/perses): CNCF observability visualization project for building dashboards across Prometheus, Tempo, Loki, and related data sources.
- [Grafana Loki](https://github.com/grafana/loki): Log aggregation system designed to index labels efficiently and integrate with Grafana.
- [OpenTelemetry Collector](https://github.com/open-telemetry/opentelemetry-collector): Vendor-neutral collector for receiving, processing, and exporting telemetry data.
- [OpenTelemetry Collector Contrib](https://github.com/open-telemetry/opentelemetry-collector-contrib): Community distribution of OpenTelemetry Collector components for collecting, processing, and exporting telemetry across production systems.
- [OpenTelemetry Semantic Conventions](https://github.com/open-telemetry/semantic-conventions): Standardized telemetry attributes and naming conventions that make traces, metrics, and logs consistent across tools and domains.
- [SigNoz](https://github.com/SigNoz/signoz): OpenTelemetry-native observability platform combining metrics, traces, logs, dashboards, and alerts.
- [HyperDX](https://github.com/hyperdxio/hyperdx): Open-source observability platform unifying session replays, logs, metrics, traces, and errors, powered by ClickHouse and OpenTelemetry.
- [Jaeger](https://github.com/jaegertracing/jaeger): CNCF distributed tracing platform for monitoring and troubleshooting microservices.
- [Vector](https://github.com/vectordotdev/vector): High-performance observability data pipeline for collecting, transforming, and routing logs and metrics.
- [Grafana Alloy](https://github.com/grafana/alloy): OpenTelemetry Collector distribution with programmable pipelines for collecting, processing, and forwarding observability signals.
- [Grafana](https://github.com/grafana/grafana): Open-source platform for monitoring, observability, and data visualization with dashboards, alerts, and multi-data-source exploration.
- [Pixie](https://github.com/pixie-io/pixie): Kubernetes-native observability platform that uses eBPF to capture metrics, events, traces, and network telemetry without manual instrumentation.
- [Grafana Beyla](https://github.com/grafana/beyla): eBPF-based auto-instrumentation for web applications and network metrics without code changes, exporting OpenTelemetry data.
- [Parca](https://github.com/parca-dev/parca): Continuous profiling platform for analyzing CPU and memory usage over time to improve performance, reliability, and infrastructure efficiency.
- [Kepler](https://github.com/sustainable-computing-io/kepler): Kubernetes power and energy exporter for measuring container, pod, and node energy consumption with Prometheus.
- [Inspektor Gadget](https://github.com/inspektor-gadget/inspektor-gadget): eBPF-based inspection toolkit for collecting low-level Kubernetes and Linux operational telemetry.
- [Robusta](https://github.com/robusta-dev/robusta): Kubernetes alert enrichment and automation platform for Prometheus alerts, runbooks, and remediation workflows.
- [Coroot](https://github.com/coroot/coroot): Open-source observability and APM platform with metrics, logs, traces, profiling, SLOs, and AI-assisted root-cause analysis.
- [Pyrra](https://github.com/pyrra-dev/pyrra): SLO management tool for Prometheus that makes service-level objectives accessible, actionable, and easy to use for everyone.
- [Superlog](https://github.com/superloglabs/superlog): Open-source observability tool that uses AI agents to self-heal software by detecting issues and automating fixes.
- [Monoscope](https://github.com/monoscope-tech/monoscope): Open-source observability platform with S3-native storage, OpenTelemetry-native ingest, natural language queries, and AI agents for anomaly detection and scheduled reports.
- [DeepFlow](https://github.com/deepflowio/deepflow): eBPF-based observability platform for distributed tracing, profiling, network telemetry, and automatic application topology discovery.
- [Qtap](https://github.com/qpoint-io/qtap): eBPF agent that captures pre-encrypted network traffic with process, container, host, and protocol context for security auditing and troubleshooting.
- [Parseable](https://github.com/parseablehq/parseable): Rust-based, data-lake observability platform for logs, metrics, traces, and events across applications, agents, and infrastructure.
- [Traccia](https://github.com/traccia-ai/traccia-py): OpenTelemetry-based Python SDK for AI-agent tracing, token and cost tracking, guardrail detection, governance evidence, and OTLP export.
- [PandaProbe](https://github.com/chirpz-ai/pandaprobe): Open-source agent engineering platform for traces, evaluations, and metrics across LangGraph, CrewAI, Claude Agent SDK, and other agent runtimes.
- [Claude Tap](https://github.com/liaohch3/claude-tap): Local trace viewer that intercepts and inspects coding-agent API traffic from Claude Code, Codex CLI, Gemini CLI, Cursor CLI, OpenCode, and other clients.
- [Grafana Agento11y](https://github.com/grafana/agento11y): Grafana's practical AI observability project for collecting useful telemetry from agent and LLM workflows.
- [FailproofAI](https://github.com/FailproofAI/failproofai): Observability and policy enforcement for AI-agent harnesses, with run capture, runtime reliability checks, and a local dashboard.
- [Agent Beacon](https://github.com/Asymptote-Labs/agent-beacon): Unified telemetry layer for AI agents running locally, in CI, or in the cloud, with a local dashboard and security-team workflows.
- [dt-evals](https://github.com/dynatrace-oss/dt-evals): Apache-2.0 CLI with evaluators for AI applications and agents, including LLM-as-a-judge workflows that support observability feedback loops.
- [EfficientAI](https://github.com/EfficientAI-tech/efficientAI): Open-source voice AI evaluation platform for testing, comparing, and shipping reliable voice agents.
- [AI Eval Platform](https://github.com/huangyiminghappy/ai-eval-platform): Open-source evaluation platform for RAG, AI agents, multi-turn conversations, LLM-as-a-judge workflows, endpoint testing, reports, and blind human review.
- [Foglamp](https://github.com/foglamp-labs/foglamp): Apache-2.0 self-hosted observability layer for the Vercel AI SDK, covering token usage, cost, latency, traces, and prompt or response logs.
- [HUATUO](https://github.com/ccfos/huatuo): Apache-2.0 eBPF-based observability for Linux kernels, AI-agent sandboxes, and heterogeneous infrastructure, with automatic tracing and continuous profiling.
- [CPA Manager Plus](https://github.com/seakee/CPA-Manager-Plus): Self-hosted management panel and AI gateway observability dashboard for request history, usage, cost, quotas, failures, and account health.
- [LoongSuite Pilot](https://github.com/alibaba/loongsuite-pilot): Local-first OpenTelemetry collector for coding-agent events from Claude Code, Codex, Cursor, and other clients, including token, cost, trace, and security-audit telemetry.

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
- [k9s](https://github.com/derailed/k9s): Terminal UI for managing Kubernetes clusters with resource views, logs, and context switching.
- [containerd](https://github.com/containerd/containerd): Industry-standard container runtime providing the core container lifecycle management for Docker, Kubernetes, and cloud-native platforms.
- [Talos Linux](https://github.com/siderolabs/talos): Modern Linux distribution built specifically for Kubernetes with API-driven configuration, immutable root filesystem, and zero-touch provisioning.
- [KubeEdge](https://github.com/kubeedge/kubeedge): CNCF Kubernetes-native edge computing framework for extending containerized applications to edge nodes with cloud-edge synergy.
- [Rook](https://github.com/rook/rook): CNCF storage orchestrator for Kubernetes, providing self-managing, self-scaling, and self-healing storage services for Ceph, NFS, and other providers.
- [MinIO](https://github.com/minio/minio): High-performance, S3-compatible object storage with native Kubernetes support for AI/ML data lakes, analytics, and cloud-native applications.
- [KubeVirt](https://github.com/kubevirt/kubevirt): Kubernetes-native virtualization platform for running and managing virtual machines alongside containers on Kubernetes.
- [KubeSphere](https://github.com/kubesphere/kubesphere): Container platform for multi-cloud, datacenter, and edge Kubernetes management with integrated DevOps, observability, service mesh, and multi-tenancy.
- [Kueue](https://github.com/kubernetes-sigs/kueue): Kubernetes-native job queueing system for managing batch, AI/ML, and other queued workloads with quotas and fair sharing.
- [OpenClaw Operator](https://github.com/paperclipinc/openclaw-operator): Kubernetes operator for deploying and managing OpenClaw AI agent instances with security, observability, and lifecycle controls.

## Security and Supply Chain

**Selection guidance:** Separate pre-deployment testing from runtime enforcement: use reproducible probes and regression cases to catch prompt-injection or jailbreak regressions, then keep runtime policy, isolation, and audit evidence independent of any single model vendor. A green scan is a gate, not proof of safety.

- [Fast LLM Security Guardrails](https://github.com/ZenGuard-AI/fast-llm-security-guardrails): Low-latency trust layer for screening and enforcing security policies around AI-agent and LLM interactions.
- [Falco](https://github.com/falcosecurity/falco): CNCF runtime security tool for detecting suspicious behavior in containers and Kubernetes.
- [Tetragon](https://github.com/cilium/tetragon): eBPF-based security observability and runtime enforcement tool for detecting and blocking suspicious kernel, container, and network activity in real time.
- [Kyverno](https://github.com/kyverno/kyverno): Kubernetes-native policy engine for validation, mutation, generation, and image verification.
- [Open Policy Agent](https://github.com/open-policy-agent/opa): General-purpose policy engine for policy-as-code across Kubernetes, CI/CD, APIs, and infrastructure.
- [Gatekeeper](https://github.com/open-policy-agent/gatekeeper): Kubernetes admission controller that enforces OPA policies and audit constraints across clusters.
- [Syft](https://github.com/anchore/syft): CLI and library for generating SBOMs from container images and filesystems.
- [Grype](https://github.com/anchore/grype): Vulnerability scanner for container images and filesystems that works well with Syft-generated SBOMs.
- [Kubescape](https://github.com/kubescape/kubescape): Kubernetes security platform for risk analysis, compliance, misconfiguration scanning, and CI/CD or cluster checks.
- [kube-bench](https://github.com/aquasecurity/kube-bench): Security scanner that checks Kubernetes deployments against the CIS Kubernetes Benchmark.
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
- [ToolHive](https://github.com/stacklok/toolhive): Enterprise platform for securely running and managing MCP servers with isolation, lifecycle controls, and operational governance.
- [Tracecat](https://github.com/TracecatHQ/tracecat): Open-source security automation platform for teams and AI agents with event-driven orchestration, monitoring, and low-code workflows.
- [OneCLI](https://github.com/onecli/onecli): Open-source credential gateway with built-in vault for giving AI agents access to services without exposing secrets.
- [Privacy Filter](https://github.com/packyme/privacy-filter): Pure-Go privacy gateway that redacts PII and secrets before prompts reach an LLM, with HTTP, gRPC, and embeddable package interfaces.
- [Preloop](https://github.com/preloop/preloop): Self-hostable AI agent control plane combining an MCP firewall, model gateway, policy-as-code, human approvals, runtime observability, budgets, and audit trails.
- [hoop](https://github.com/hoophq/hoop): Open-source layer-7 gateway for engineers and AI agents that masks sensitive data, blocks dangerous infrastructure operations, supports approvals, and records sessions across databases, Kubernetes, SSH, APIs, and MCP.
- [Octelium](https://github.com/octelium/octelium): Self-hosted zero-trust access platform that also operates as an API, AI/LLM, MCP, Kubernetes, and container application gateway.
- [OpenAnt](https://github.com/knostic/OpenAnt): Open-source LLM-based vulnerability discovery tool for proactively finding verified security flaws in AI systems.
- [AI-Infra-Guard](https://github.com/Tencent/AI-Infra-Guard): Full-stack AI red teaming platform for scanning AI infrastructure, agents, skills, MCP servers, and LLM jailbreak vulnerabilities.
- [MCP Security Hub](https://github.com/FuzzingLabs/mcp-security-hub): Collection of offensive-security MCP servers that brings tools such as Nmap, Ghidra, Nuclei, SQLMap, and Hashcat to AI assistants for authorized security workflows.
- [Anthropic Cybersecurity Skills](https://github.com/mukul975/Anthropic-Cybersecurity-Skills): Apache-2.0 collection of structured cybersecurity skills for AI agents, mapped to ATT&CK, NIST CSF, MITRE ATLAS, D3FEND, and AI RMF.
- [Kubernetes AI-BOM](https://github.com/GoogleCloudPlatform/k8s-aibom): Kubernetes controller that generates CycloneDX ML-BOM documents for AI workloads with traceable runtime evidence.
- [Cybersecurity AI (CAI)](https://github.com/aliasrobotics/cai): Open-source framework for applying AI agents to cybersecurity research and defensive security workflows.
- [AgentShield](https://github.com/affaan-m/agentshield): AI agent security scanner for detecting vulnerabilities in agent configurations, MCP servers, and tool permissions via CLI or GitHub Action.
- [Agent Threat Rules](https://github.com/Agent-Threat-Rule/agent-threat-rules): Open detection-rule standard for AI agent threats, with executable rules covering prompt injection, tool abuse, data exfiltration, and related attack categories.
- [Cisco Skill Scanner](https://github.com/cisco-ai-defense/skill-scanner): Security scanner for AI agent skills that helps identify risky behavior before skills are deployed.
- [Crust](https://github.com/BakeLens/crust): Local AI-agent security gateway that intercepts tool calls and MCP/ACP traffic to block dangerous actions, scan secrets, and enforce runtime rules.
- [Adrian](https://github.com/secureagentics/Adrian): Open-source runtime AI agent security tool that monitors and controls AI agents in real time, catching malicious tool use, prompt injection, and policy drift before the agent acts.
- [Sage](https://github.com/gendigitalinc/sage): Lightweight Agent Detection & Response layer that guards AI-agent commands, files, and web requests.
- [Doberman](https://github.com/fu351/Doberman-Core): Runtime guardrails and adaptive authorization for AI coding agents, with MCP or host-hook enforcement, approvals, audit logs, and fail-closed policy decisions.
- [Agent3σ-Canary](https://github.com/antgroup/Agent3Sigma-Canary): Sandboxed framework for evaluating AI agent security in realistic tool-using workflows, with trajectory-based scoring across safety, awareness, and task utility.
- [AgentDojo](https://github.com/ethz-spylab/agentdojo): Dynamic environment for evaluating attacks and defenses against LLM agents in realistic tool-use workflows.
- [Agent Governance Toolkit](https://github.com/microsoft/agent-governance-toolkit): Toolkit for policy enforcement, zero-trust identity, execution sandboxing, and reliability engineering for autonomous AI agents.
- [PyRIT](https://github.com/microsoft/PyRIT): Open-source framework for proactively identifying and testing generative AI risks through configurable red-team attack strategies.
- [Open Agent Auth](https://github.com/alibaba/open-agent-auth): Enterprise framework for agent-operation authorization with cryptographic identity binding, fine-grained permissions, and semantic audit trails.
- [SkillSpector](https://github.com/NVIDIA/SkillSpector): Security scanner for AI agent skills that detects vulnerabilities, malicious patterns, and other security risks.
- [CodeInspectus](https://github.com/Synvoya/codeinspectus): Local-first MCP server and CLI that combines SAST, secret, dependency, and AI-code-specific checks into a scan-fix-rescan workflow for AI-generated applications.
- [DefenseClaw](https://github.com/cisco-ai-defense/defenseclaw): Open-source governance toolkit for agentic AI security, helping assess and control risks in autonomous AI systems.
- [Apache Casbin Gateway](https://github.com/apache/casbin-gateway): Apache-licensed AI and MCP security gateway for HTTP access control, policy enforcement, and web application firewall integration.
- [Semia](https://github.com/berabuddies/Semia): Security audit tool for AI agent skills that checks skill packages for suspicious behavior and security risks.
- [Agent Safehouse](https://github.com/eugene1g/agent-safehouse): Sandbox for local AI agents that limits filesystem access to only the paths they need.
- [SCAM](https://github.com/1Password/SCAM): Open-source benchmark that tests whether AI agents recognize and report security threats during realistic, multi-turn workplace tasks.
- [nono](https://github.com/nolabs-ai/nono): Zero-setup, least-privilege sandbox for running AI agents and the tools they invoke across macOS, Linux, and Windows WSL2.
- [Pipelock](https://github.com/luckyPipewrench/pipelock): Open-source AI agent firewall that inspects MCP, A2A, HTTP, and WebSocket egress for prompt injection, SSRF, secret exfiltration, and risky tool-call chains.
- [Agentic Radar](https://github.com/splx-ai/agentic-radar): Security scanner for agentic workflows that visualizes tools and MCP servers and maps discovered vulnerabilities to security frameworks.
- [agentgg](https://github.com/agentgg-dev/agentgg): Agentic SAST scanner for repository and pull-request diffs, using tool-enabled agents to investigate code paths and turn confirmed findings into reusable detectors.
- [deepsec](https://github.com/vercel-labs/deepsec): Agent-powered security harness for scanning large codebases, investigating hard-to-find vulnerabilities, and exporting findings for review.
- [RAG/LLM Security Scanner](https://github.com/olegnazarov/rag-security-scanner): MIT-licensed scanner for testing RAG and LLM applications against prompt injection, data leakage, function abuse, and context manipulation.
- [Aegis](https://github.com/Justin0504/Aegis): Runtime policy enforcement for AI agents with cryptographic audit trails, human approval gates, and an emergency kill switch.
- [Tirith](https://github.com/sheeki03/tirith): Terminal security tool for developers and AI agents that intercepts homograph URLs, pipe-to-shell, ANSI injection, obfuscated payloads, and data exfiltration before execution.
- [Varlock](https://github.com/dmno-dev/varlock): AI-safe environment variable format that separates machine-readable schemas for agents from human-readable secrets, preventing accidental credential exposure in agent configs.
- [Cisco MCP Scanner](https://github.com/cisco-ai-defense/mcp-scanner): Security scanner for MCP servers that identifies potential threats and security findings before agents depend on their tool integrations.
- [OctoBus](https://github.com/chaitin/OctoBus): Local single-binary gateway for managing pluggable services and exposing selected capabilities through gRPC, Connect RPC, and MCP.
- [yoloAI](https://github.com/kstenerud/yoloai): Sandboxed runner for AI coding agents with disposable project copies, controlled credentials and network access, reviewable diffs, and selectable isolation backends.
- [Sandbox0](https://github.com/sandbox0-ai/sandbox0): Kubernetes-native runtime for persistent, encrypted AI-agent sandboxes with durable rootfs checkpoints, gVisor support, and separated storage and compute.
- [OpenHack](https://github.com/openhackai/OpenHack): Open-source agentic security scanner and verifier for finding and validating vulnerabilities in codebases with open-source models.
- [AgentStalker](https://github.com/Gach0ng/AgentStalker): End-to-end LLM agent security audit framework combining static modeling, attack synthesis, sandbox replay, MCP auditing, and evidence-backed reports.
- [Agent Security Bench (ASB)](https://github.com/agiresearch/ASB): Research benchmark and attack framework for systematically evaluating adversarial attacks and defenses across LLM-based agent scenarios.
- [OWASP Agent Observability Standard](https://github.com/OWASP/www-project-agent-observability-standard): OWASP project defining inspectable, traceable, and instrumentable observability practices for trustworthy AI agents.
- [Agent Security Harness](https://github.com/msaleme/red-team-blue-team-agent-fabric): Executable security-testing harness for AI agents covering MCP, A2A, tool-use governance, and agentic supply-chain scenarios.
- [OWASP Agent Security Regression Harness](https://github.com/OWASP/Agent-Security-Regression-Harness): Vendor-neutral harness for executable security regression scenarios against agentic applications and MCP-integrated systems, with policy assertions, traces, and machine-readable CI results.
- [Rogue](https://github.com/rogue-security/rogue): AI agent evaluation and red-team platform for regression testing, policy validation, adversarial probing, and security reporting across agent protocols.
- [Augustus](https://github.com/praetorian-inc/augustus): Apache-2.0 LLM security testing framework that detects prompt injection, jailbreaks, and adversarial weaknesses with 190+ probes across 28 model providers.
- [SkillHub](https://github.com/iflytek/skillhub): Self-hosted registry for publishing and versioning agent skills with RBAC, audit logs, and Docker or Kubernetes deployment.
- [MEDUSA](https://github.com/Pantheon-Security/medusa): AI-first security scanner for AI/ML applications, agents, MCP servers, and code, with supply-chain, prompt-injection, secret, and vulnerability detection.
- [Arcjet JS](https://github.com/arcjet/arcjet-js): Runtime security SDK for AI applications and agents with prompt-injection detection, tool-call authorization, sensitive-data redaction, bot protection, and rate limiting.
- [ADR](https://github.com/uber/ADR): Apache-2.0 agentic AI detection and response system combining agent telemetry, security benchmarking, and threat detection for enterprise AI agents.
- [iFixAi](https://github.com/ifixai-ai/iFixAi): Apache-2.0 framework for independently auditing AI agents with reproducible inspections and scored reports across capability, reliability, safety, and operational behavior.
- [MCP Security Checklist](https://github.com/slowmist/MCP-Security-Checklist): Practical security checklist for MCP hosts, clients, servers, multi-MCP deployments, and tool-ecosystem integrations.
- [Google Security Operations MCP Server](https://github.com/google/mcp-security): Official MCP servers for integrating Google SecOps, Google Threat Intelligence, Security Command Center, and SOAR capabilities with AI assistants.
- [Spring AI MCP Security](https://github.com/spring-ai-community/mcp-security): Spring AI security and authorization support for MCP clients, servers, and authorization servers, including OAuth 2.0 flows.
- [mcp-context-protector](https://github.com/trailofbits/mcp-context-protector): Trail of Bits security wrapper for MCP servers with configuration pinning, tool-response quarantine, and prompt-injection defenses.
- [Agent Scan](https://github.com/snyk/agent-scan): Security scanner for AI agents, MCP servers, and agent skills, designed to catch risks before agent components enter a workflow.
- [Strix](https://github.com/usestrix/strix): Open-source AI penetration-testing tool that uses autonomous agents to discover and validate application vulnerabilities with proof-of-concept exploits.
- [Shannon](https://github.com/KeygraphHQ/shannon): Autonomous AI pentester for web applications and APIs that combines source analysis with live exploit validation before vulnerabilities reach production.
- [Pentest AI](https://github.com/0xSteph/pentest-ai): Open-source AI pentester that validates every finding with machine oracles, shipping replayable proof capsules for verified vulnerabilities.
- [Akto](https://github.com/akto-api-security/akto): Open-source AI security platform for testing and securing AI agents, MCP servers, LLM integrations, and GenAI applications against API-level threats.
- [Prompt Injection Defenses](https://github.com/tldrsec/prompt-injection-defenses): Comprehensive guide cataloging every practical and proposed defense against prompt injection attacks on LLM systems.
- [AIRT](https://github.com/0x4D31/airt): Free, open-source AI red teaming course with hands-on Docker labs covering adversarial testing and security evaluation of LLM systems.

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
- [Flagger](https://github.com/fluxcd/flagger): Kubernetes progressive delivery operator for canary, A/B testing, and blue-green deployments with automated analysis.
- [argo-workflows](https://github.com/argoproj/argo-workflows): Kubernetes-native workflow engine.
- [Tekton](https://tekton.dev/): Kubernetes-native CI/CD framework with flexible task orchestration.
- [Flux](https://fluxcd.io/): Popular Kubernetes GitOps toolkit.
- [PipeCD](https://github.com/pipe-cd/pipecd): CNCF continuous delivery platform for applications, infrastructure, and platform operations across multiple deployment targets.
- [Dagger](https://github.com/dagger/dagger): Open-source automation engine for building, testing, and shipping code in CI/CD pipelines with programmable, containerized workflows.

### Code Search and Understanding

- [sourcebot](https://github.com/sourcebot-dev/sourcebot): Self-hosted code search and understanding tool for humans and AI agents to navigate, query, and comprehend large codebases.
- [Codebase Memory MCP](https://github.com/DeusData/codebase-memory-mcp): Code intelligence MCP server that indexes codebases into persistent knowledge graphs for AI agents with sub-ms queries across 158 languages.
- [Semble](https://github.com/MinishLab/semble): Code search engine optimized for AI agents, using embeddings-based retrieval with ~98% fewer tokens than grep-based approaches.
- [OpenSrc](https://github.com/vercel-labs/opensrc): Fetch real source code for npm packages on-demand, giving AI coding agents deeper library context for more accurate code generation.

### AI Coding Tools

- [agents-cli](https://github.com/google/agents-cli): CLI and reusable skills for scaffolding, evaluating, deploying, publishing, and observing production AI agents on Google Cloud.
- [9Router](https://github.com/decolua/9router): Self-hosted AI router for connecting coding agents to multiple providers with automatic fallback, routing, and token-usage reduction.
- [Aider](https://github.com/Aider-AI/aider): AI pair programming tool that works in your terminal with multi-file editing, git integration, and support for leading LLMs.
- [Continue](https://github.com/continuedev/continue): Open-source AI code assistant that integrates with IDEs as an autopilot for software development with customizable context and models.
- [Tabby](https://github.com/TabbyML/tabby): Self-hosted AI coding assistant with code completion, chat, and agent capabilities that can run fully on-premises.
- [Cline](https://github.com/cline/cline): Autonomous coding agent available as an SDK, IDE extension, and CLI assistant for AI-driven development workflows.
- [OpenHands](https://github.com/All-Hands-AI/OpenHands): AI-driven development platform for automated coding, code review, and software engineering tasks with agent-based workflows.
- [SWE-agent](https://github.com/SWE-agent/SWE-agent): LLM-powered agent that automatically resolves GitHub issues and fixes bugs with iterative, tool-using workflows.
- [GPT-Pilot](https://github.com/Pythagora-io/gpt-pilot): AI developer that builds production-ready applications from natural language specifications with human-in-the-loop guidance.
- [OpenAI Codex CLI](https://github.com/openai/codex): Lightweight coding agent that runs in the terminal, providing AI-powered code editing and task automation from the command line.
- [Void](https://github.com/voideditor/void): Open-source AI code editor with intelligent code completion, editing, and agentic coding workflows in a modern editor environment.
- [Goose](https://github.com/aaif-goose/goose): Open-source extensible AI agent that installs, executes, edits, and tests code with any LLM, going beyond code suggestions into full task execution.
- [Qwen Code](https://github.com/QwenLM/qwen-code): Open-source AI coding agent that runs in the terminal with multi-file editing, task planning, and MCP server integration.
- [Open SWE](https://github.com/langchain-ai/open-swe): Open-source asynchronous coding agent from LangChain for automated software engineering with parallel task execution.
- [OpenCode](https://github.com/anomalyco/opencode): The open source coding agent — fast, lightweight CLI coding agent with low token overhead and broad LLM support.
- [Gemini CLI](https://github.com/google-gemini/gemini-cli): Google's open-source AI agent that brings Gemini's power into the terminal for coding, file editing, and task automation.
- [OpenWiki](https://github.com/langchain-ai/openwiki): CLI that writes and maintains agent documentation for codebases, automatically keeping docs in sync as the code evolves.
- [VibeKit](https://github.com/superagent-ai/vibekit): Safety layer for coding agents that provides isolated sandboxes, sensitive-data redaction, and built-in execution observability.
- [CodeBurn](https://github.com/getagentseal/codeburn): Free local tool for tracking AI coding token usage and cost across 31 tools and agents, with breakdowns by model, project, task, and client.
- [Sourcery](https://github.com/sourcery-ai/sourcery): Instant AI code review tool that provides automated feedback on pull requests and changes.
- [Kodus](https://github.com/kodustech/kodus-ai): Open-source AI code review agent with full control over model choice and costs, supporting multi-provider LLMs and enterprise-grade deployment.
- [h5i](https://github.com/h5i-dev/h5i): Apache-2.0 platform for auditable AI coding-agent workspaces, with sandboxed Git worktrees, multi-agent orchestration, prompt and context tracking, review gates, and token-efficient logs.

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
- [OpenReview](https://github.com/vercel-labs/openreview): Open-source, self-hosted AI code review bot that runs automated pull request reviews with Vercel-powered deployment.
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
- [GO Feature Flag](https://github.com/thomaspoignant/go-feature-flag): Self-hosted cloud-native feature flag solution built on OpenFeature, with lightweight Go deployment and multi-provider support.

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

- [OpenFGA](https://github.com/openfga/openfga): High-performance authorization engine inspired by Google Zanzibar for fine-grained, relationship-based access control.
- [keycloak](https://github.com/keycloak/keycloak): Open-source IAM for modern applications and services.
- [OpenBao](https://github.com/openbao/openbao): Open-source secrets management system for storing and distributing secrets, certificates, and keys.
- [oauth2-proxy](https://github.com/oauth2-proxy/oauth2-proxy): Lightweight OAuth2 reverse proxy for Google, Azure, OpenID Connect, and more, with simple authorization checks.
- [zitadel](https://github.com/zitadel/zitadel): Open-source IAM for modern applications and services, focused on simplicity.
- [Casdoor](https://github.com/casdoor/casdoor): Open-source identity management platform supporting OAuth 2.0, OIDC, and SAML.
- [Cerbos](https://github.com/cerbos/cerbos): Open-core, language-agnostic authorization layer with context-aware access control policies for application resources.
- [dexidp/dex](https://github.com/dexidp/dex): Lightweight pluggable OpenID Connect (OIDC) and OAuth 2.0 provider.
- [pomerium](https://github.com/pomerium/pomerium): Identity-aware proxy with richer access-control capabilities.
- [Infisical](https://github.com/Infisical/infisical): Open-source platform for secrets management, certificate automation, and privileged access management across development and production environments.
- [Metorial](https://github.com/metorial/metorial): Open-source identity and access layer for AI agents, standardizing authentication, scoped permissions, integrations, and auditability for external systems.

### Internal Developer Platform (IDP)

An internal developer platform is more than a pile of tools; it is not just another management console or dashboard.

- [backstage](https://github.com/backstage/backstage): Open platform for building developer portals that help teams build, deploy, and maintain software.
- [Kratix](https://github.com/syntasso/kratix): Framework for building platform APIs that let teams compose and operate internal platforms on Kubernetes.
- [OpenChoreo](https://github.com/openchoreo/openchoreo): Open-source developer platform for Kubernetes with a Backstage-powered portal, CI/CD, GitOps, observability, and platform abstractions.
- [KubeVela](https://github.com/kubevela/kubevela): CNCF application delivery platform for managing Kubernetes workloads across hybrid and multi-cluster environments.
- [Score](https://github.com/score-spec/spec): Platform-agnostic workload specification for describing services once and generating environment-specific platform configuration.
- [Superplane](https://github.com/superplanehq/superplane): Open-source control plane for platform engineering workflows across services, pipelines, and environments.
- [Agyn](https://github.com/agynio/platform): Kubernetes-native runtime for moving AI coding agents from laptops to company infrastructure with enterprise controls.

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
