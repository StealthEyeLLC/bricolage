# Agent Repository Matrix

## Purpose

This document is the primary comparative synthesis workspace for the Bricolage project.

The goal is NOT to rank entire frameworks. The goal is to identify architectural primitives, low-friction patterns, state-of-the-art implementations, reusable abstractions, unnecessary complexity, and synthesis candidates for a coherent conversational agent architecture.

---

# Core Project Principle

Bricolage prioritizes low-friction architecture, modularity, composability, high capability density, practical usability, implementation realism, state-of-the-art functionality, minimal unnecessary ceremony, direct conversational usefulness, and aggressive synthesis of proven open-source ideas.

Bricolage does NOT aim to maximize enterprise abstraction layers, governance bureaucracy, configuration complexity, documentation volume, testing ceremony, or heavyweight orchestration unless the capability gain is substantial.

---

# Comparative Matrix - Passes 1-5

| Repo / System | Primary Categories | Key Innovations | Friction / Complexity | Synthesis Candidates | Initial Bricolage Judgment |
|---|---|---|---|---|---|
| OpenHands / OpenHands SDK | Software Engineering Agents; Environment Interaction; Tooling; Runtime; Human Interaction | Composable software-agent SDK; sandboxed execution; local-to-remote portability; REST/WebSocket services; visual workspace, CLI, API interfaces; model-agnostic routing; lifecycle control; security analysis; SWE-Bench and GAIA orientation. | Larger system surface than lightweight agents; production-grade execution/sandbox design brings real complexity. | Sandboxed execution layer; software-agent harness; lifecycle model; workspace interface abstraction; remote/cloud execution pattern; model routing boundary. | Very high-value. Do not copy whole stack blindly, but this is one of the strongest candidates for execution/runtime architecture. |
| Codex Cloud / GitHub Agent Workflows | Software Engineering Agents; Human Interaction; Infrastructure; Runtime | Cloud coding-agent workflow through ChatGPT, GitHub, mobile/web, issues/PRs, and cloud sandboxes; positioned as broader enterprise agent substrate beyond coding. | Platform-dependent; not an OSS primitive, but it is the actual operational substrate for Bricolage. | ChatGPT-to-Codex-to-GitHub loop; issue/PR assignment pattern; mobile operator control; repository as persistent state. | Critical operating assumption. Bricolage should be optimized for this conversational cloud loop, not local-machine assumptions. |
| Confucius Code Agent / Confucius SDK | Software Engineering Agents; Runtime; Memory; Tooling; Learning | Industrial-scale OSS coding agent and SDK with unified orchestrator, hierarchical working memory, persistent note-taking across sessions, modular extension system, and meta-agent build-test-improve loop; reports 54.3% Resolve@1 on SWE-Bench-Pro. | New/large system; needs repo/license/maturity inspection. High ambition can hide complexity. | Hierarchical working memory; persistent note system; meta-agent agent-config refinement; industrial repo-scale coding loop. | Very high-signal. Must inspect deeply; may be one of the strongest SWE synthesis sources. |
| DSPy | Cognition & Reasoning; Models, Context & Inference; Evaluation | Declarative LM programs; modules instead of prompt strings; optimizers/compilers; metric-driven prompt/program improvement; assertions for constraint-guided refinement. | Requires adopting a programming model; optimizer/eval loops can become overbuilt if used everywhere. | Declarative cognitive modules; prompt/program compilation; assertions as lightweight verification; metric-driven tuning for reusable reasoning modules. | Essential cognition primitive. Use selectively for high-value reasoning pipelines, not every chat turn. |
| Blueprint First / Source Code Agent | Runtime; Cognition; Safety; Evaluation | Deterministic workflow paradigm: expert-defined source-code execution blueprint controls procedure while LLM is invoked only for bounded subtasks; improved tau-bench performance and efficiency. | Less flexible for open-ended tasks; requires explicit procedural modeling. | Blueprint-first execution; model-as-bounded-tool; deterministic workflow spine; verifiable procedural agents. | Extremely important counterweight to fully generative agents. Steal for operational workflows. |
| AlphaEvolve | Learning; Software Engineering Agents; Cognition; Evaluation | Evolutionary coding agent that uses LLMs to generate algorithm variants and selects via explicit evaluation functions/metrics; general-purpose algorithm discovery framing. | Not open-source in the same sense; requires good evaluators and compute. | Generate-variant-evaluate-select loop; metric-driven algorithm improvement; evolutionary search over code/strategies. | Important synthesis primitive for self-improvement and algorithmic search, not immediate runtime. |
| Pydantic AI | Runtime; Tooling; Models, Context & Inference; Data/State Architecture | Python agent framework from the Pydantic ecosystem emphasizing type-safe agents, structured outputs, dependency injection, validation, and model-provider abstraction. | Framework maturity and lock-in need inspection; type rigor can slow exploratory work if over-applied. | Typed agent contracts; schema-first tool/result validation; dependency injection; structured output boundary. | Strong candidate for low-friction Python agent skeleton if used surgically. |
| Semantic Kernel | Runtime; Skills; Tooling; Memory; Multi-Agent | Microsoft open-source SDK for AI orchestration, plugins, planners/functions, memory/connectors, MCP integration, Azure/OpenAI/local models, and agent abstractions. | Enterprise/cloud ecosystem gravity; can become heavy if Azure-first assumptions dominate. | Skill/plugin model; planner/function abstractions; MCP integration patterns; connector architecture. | Useful as a reference for plugin/connectors and enterprise integration, not necessarily core runtime. |
| CrewAI | Multi-Agent Coordination; Runtime & Orchestration; Skills; Tooling | Role/task/crew abstraction; collaborative agent teams; Flows for controlled event-driven workflows; memory, tools, knowledge/RAG integration; MIT licensed; active 2026 release line. | Can become role-play orchestration theater if overused; enterprise layer may add overhead. | Crew/task vocabulary; role-specialized agents; simple collaborative workflows; task delegation pattern. | Useful multi-agent vocabulary. Synthesize primitives, avoid adopting heavy crew formalism unless it proves useful. |
| CAMEL | Multi-Agent Coordination; Cognition; Evaluation; Research | Large open-source multi-agent research framework around communicative agents, role-playing, agent societies, simulations, and cooperative task-solving. | Role-play/social simulation can become theatrical if not tied to execution outcomes. | Communicative agent protocols; agent society simulation; role-play as controlled research tool; task decomposition dialogues. | Important multi-agent research source. Use for coordination primitives, not default execution. |
| MetaGPT | Multi-Agent Coordination; Software Engineering Agents; Runtime | Multi-agent software company metaphor: product manager, architect, engineer, QA roles; SOP-driven collaboration for software generation. | Heavy role simulation; risk of process theater; may overfit to software-project metaphors. | Standard operating procedure patterns; role-specific artifacts; handoff contracts between planning/design/code/test. | Worth extracting artifact/handoff structure, not full company simulation. |
| AutoGen / AutoGen Studio | Multi-Agent Coordination; Human Interaction; Observability & Evaluation; Runtime | Multi-agent conversational workflows; declarative JSON-based agent specs; no-code/visual workflow building; debugging/evaluation UI; reusable component gallery. | Multi-agent conversation systems can become hard to debug; studio/no-code layer may not fit Bricolage's repo-first flow. | Declarative agent definitions; inspectable conversation graphs; reusable agent components; debugging UI concepts. | Strong ideas for agent interaction protocols and debugging. Probably not the central runtime. |
| AutoGPT / AutoGPT Forge | Runtime; Tooling; Historical Baseline; Agent Platform | Early autonomous goal decomposition with tools, browsing, file management; later ecosystem includes Forge/platform ideas for building agents and marketplace-like agent composition. | Known issues: loops, hallucination, high cost, brittle autonomy; early architecture became cautionary. | Avoid unconstrained goal loops; extract marketplace/platform lessons only after vetting; bounded task decomposition. | Mostly a cautionary ancestor, but Forge/platform layer deserves inspection. |
| BabyAGI | Cognition; Runtime; Memory; Historical Baseline | Minimal autonomous task loop with task creation, prioritization, execution, and memory/vector-store style persistence. | Too simple for robust agents; loops/prioritization can drift. | Minimal task-loop archetype; task queue/prioritization; simple memory loop. | Historical primitive. Useful for understanding the bare minimum agent loop. |
| SuperAGI | Runtime; Tooling; Human Interaction; Agent Platform | Open-source autonomous agent platform with GUI, agent provisioning, toolkits, memory/vector DB integrations, and marketplace-style extensions. | Platform surface and GUI can add friction; may be less relevant than modern primitives. | Agent provisioning UI; tool marketplace concept; memory/toolkit integration patterns. | Large historical platform to inspect for what not to overbuild, plus marketplace ideas. |
| AgentSPEX | Runtime & Orchestration; Infrastructure/State; Evaluation; Skills | Explicit agent workflow specification language; typed steps; branching/loops; parallel execution; reusable submodules; explicit state; harness with tools, sandbox, checkpointing, verification, logging; visual graph/workflow editor. | A new DSL can be friction if too much is formalized too soon. | Explicit workflow/state language; typed steps; portable workflow specs; checkpointing without enterprise bloat; visual/graph inspection concept. | Very important 2026 direction. Consider Bricolage-native lightweight spec format rather than adopting full DSL immediately. |
| Agentproof | Safety; Evaluation; Runtime; State Architecture | Static verification of agent workflow graphs extracted from LangGraph, CrewAI, AutoGen, and Google ADK; checks structural defects and temporal safety policies before runtime. | Verification DSL could become ceremony if overused. Static verification only helps graph-structured workflows. | Lightweight preflight checks for graph topology; unreachable/dead-end detection; human-gate policy checks; witness traces. | Excellent lean safety primitive: verify structure, not bureaucracy. Add when Bricolage has graph workflows. |
| AgentGit | Runtime & Orchestration; Infrastructure/State; Observability; Evaluation | Git-like commit/revert/branching for multi-agent workflows; trajectory branching; A/B exploration; reduced redundant computation/token usage; built atop LangGraph. | Adds state-versioning layer; may be overkill for simple tasks. | Git-like agent state commits; branchable trajectories; rollback/replay; compare alternate reasoning/action paths. | Extremely aligned with GitHub/repo-native Bricolage. Strong primitive candidate. |
| MCP | Tooling & Action Systems; Protocols; Infrastructure; Knowledge & Retrieval | Open standard for model/tool/data integration; JSON-RPC; broad provider adoption including OpenAI and Google DeepMind; reference servers; ChatGPT app support. | Security boundaries are nontrivial; tool execution can be dangerous without whitelisting/schema validation; ecosystem quality varies. | Standard tool/data connector boundary; MCP server registry; permissioned tool invocation; schema-bound tool access. | Essential protocol layer. Adopt as a boundary, but wrap with Bricolage trust/permission model. |
| AGENTS.md standard | Skills; Software Engineering Agents; Human Interaction; Protocols | Repo-native instruction format for coding agents; public reports describe broad adoption and Linux Foundation/AAIF contribution alongside MCP. | May become vague if used as a dumping ground; needs concise rules. | One canonical instruction file for ChatGPT/Codex/other coding agents; repo-native coordination layer. | Immediate Bricolage need. Create and keep powerful, not bureaucratic. |
| A2A / Agent2Agent | Multi-Agent Coordination; Protocols; Infrastructure | Open protocol for agent-to-agent discovery, messaging, and task coordination across systems/vendors; Linux Foundation governance. | Young ecosystem; risk of premature protocol complexity. | External agent interoperability; agent discovery; message/task envelope schemas; vendor-neutral multi-agent protocol boundary. | Important for future interoperability, not necessarily core v0 runtime. |
| ModelScope-Agent | Tooling; Models, Context & Inference; Knowledge & Retrieval; Evaluation | Customizable open-source LLM agent framework connecting open-source LLMs, model APIs, common APIs, tool-use data collection, tool retrieval/registration, memory control, model training, evaluation, and 1000+ public AI models in ModelScopeGPT. | Older generation; ecosystem-specific; broader than Bricolage may need. | Tool retrieval/registration at scale; model/tool marketplace; open-model controller integration; tool-use data pipeline. | Important large-tool-ecosystem source. Extract tool registry/retrieval and model-API bridging ideas. |
| Google ADK / Vertex/Gemini Agent Platform | Runtime; Tooling; Evaluation; Infrastructure | Open-source Agent Development Kit plus enterprise platform: Agent Runtime, Identity, Gateway, Registry, low-code Agent Studio, observability, simulation, deployment, and integrations. | Enterprise platform gravity; not all OSS/free; may be too heavy. | Agent gateway/registry concepts; identity boundary; simulation/evaluation environment; deployment path from local to cloud. | Use as reference architecture for platform capabilities, not initial implementation. |
| Google Antigravity | Software Engineering Agents; Human Interaction; Environment Interaction | Agent-first IDE with editor and manager views; parallel agents across workspaces; verifiable artifacts such as plans, task lists, screenshots, and browser recordings; editor/terminal/browser access. | Proprietary preview; not OSS. | Manager view for parallel agents; artifact-based trust; screenshot/browser-record proof; async coding-agent orchestration. | Strong UX/operation signal even if not source-compatible. Steal the artifact/trust model. |
| Letta / MemGPT | Memory Systems; Runtime; Human Interaction | Stateful agents with explicit memory architecture; long-running agent identity; separation between context-window management and longer-term memory; memory as first-class agent substrate. | Memory systems can become noisy, expensive, or unreliable without disciplined write/read policies. | Explicit memory layers; memory write policies; persona/identity continuity; archival vs working memory separation. | Core memory inspiration. Must synthesize carefully with repo-native/GitHub memory. |
| InfiAgent | Memory Systems; Runtime; Context; Knowledge & Retrieval | Infinite-horizon framework that keeps reasoning context bounded by externalizing persistent state into a file-centric state abstraction; reconstructs context from workspace snapshots plus recent action windows. | Research framework; implementation maturity needs inspection. File-state discipline requires strong conventions. | File-centric persistent state; bounded context loop; workspace snapshot reconstruction; long-horizon research state. | Very aligned with ChatGPT/Codex/GitHub cloud workflow. Strong candidate for Bricolage memory/state philosophy. |
| AutoAgent | Runtime; Skills; Memory; Multi-Agent; Learning | Evolving cognition, contextual decision-making, elastic memory orchestration, closed-loop cognitive evolution, reusable episodic abstraction. | Ambitious and potentially complex; must verify implementation availability and practicality. | Elastic memory orchestrator; cognition update loop; peer/tool capability cognition; compression of redundant trajectories. | Important 2026 adaptive-agent direction. Extract memory/cognition concepts if implementation holds up. |
| AgentSCOPE | Safety; Privacy; Evaluation; Tooling | Privacy Flow Graph evaluates intermediate information flows across agent pipelines, showing privacy violations can occur inside tool-response/query stages even when final output appears clean. | Privacy evaluation can become heavy; benchmark not runtime. | Boundary-by-boundary privacy flow tracing; tool-response privacy checks; contextual integrity annotations. | Important for personal/conversational agents with email/calendar/files. Use as design warning and targeted check, not bureaucracy. |
| browser-use / Browser agents | Environment Interaction; Tooling; Human Interaction | Practical browser automation for agents; web interaction as first-class action space; often built on Playwright-style browser control. | Web automation is brittle; prompt injection/security risk; UI variability. | Browser action interface; page-state extraction; human takeover/approval; browser task loop. | High capability per complexity. Needs safety gates around logged-in/sensitive actions. |
| Playwright | Environment Interaction; Tooling; Evaluation | Mature cross-browser automation API for Chromium/Firefox/WebKit; robust automation substrate; Apache 2.0. | Not an agent framework; low-level automation requires higher-level reasoning wrapper. | Browser execution substrate; deterministic browser actions; screenshots/traces; web task replay. | Likely best low-level browser substrate if Bricolage needs browser actions. |
| Flowise | Human Interaction; Tooling; Runtime; Knowledge & Retrieval | Popular open-source low-code visual builder for LLM apps/agents; node-based flows; Custom MCP node shows user demand for visual tool wiring. | Serious security history: CVE-2025-59528 from CustomMCP node allowed arbitrary code execution; public internet exposure is dangerous. | Visual node graph ideas; low-code tool composition; warning: never execute user config as code; secure node sandboxing. | Useful as visual-builder reference and major security caution. Do not adopt server-exposed low-code execution casually. |
| Dify | Human Interaction; Knowledge & Retrieval; Runtime; Agent Platform | Open-source LLM app/agent platform with workflow builder, RAG, model provider abstraction, operations/monitoring, app deployment patterns. | Platform-heavy; may drag product/SaaS assumptions. | Workflow builder; RAG/app deployment model; model-provider abstraction; prompt/app ops patterns. | Large ecosystem worth inspecting, especially for productized workflow/RAG UX. Not core runtime. |
| E2B / Daytona class | Environment Interaction; Infrastructure; Tooling; Software Engineering Agents | Cloud sandbox/code-interpreter environments for agents, isolated execution, filesystem/process/network boundaries, API-driven workspaces. | Hosted dependency; pricing/limits; OSS status varies by component. | Cloud sandbox abstraction; ephemeral workspaces; code execution service boundary; persistent workspace snapshots. | Important implementation substrate to compare with Codex/OpenHands/Orchard. |
| OpenClaw | Human Interaction; Skills; Tooling; Environment Interaction | Messaging-first autonomous assistant; local-running agent; extensible skill directory; service integrations; MIT licensed; SKILL.md directory convention; persistent local config/history. | Setup/security risk; unvetted skills are dangerous; reported prompt-injection and malicious skill incidents. | Messaging-first agent UX; skill directory; gateway pattern; skill precedence model; strong warning model for broad tool authority. | High-value conversational UX source and major cautionary case. Steal skills/gateway ideas, not unconstrained authority. |
| Moltbook / Agent social networks | Multi-Agent Coordination; Human Interaction; Security | API-first agent-only social network; agents communicate, post, vote, and periodically check in; exposes indirect prompt-injection and agent identity/auth risks. | High security risk; not core build. | Agent-to-agent public forum pattern; check-in loop; adversarial-agent environment lessons. | Mostly a cautionary source for untrusted agent-to-agent communication. |
| SWE-agent | Software Engineering Agents; Evaluation; Runtime | Focused coding-agent loop; repository issue-to-patch flow; SWE-Bench orientation; emphasizes execution and verification against real repos. | Specialized to coding tasks; may not generalize as whole architecture. | Issue-to-patch loop; test-first verification; repo navigation/action loop; coding trajectory logs. | Strong coding-agent primitive. Use with OpenHands/Codex-style execution concepts. |
| AgentForge / AutoCodeAI | Software Engineering Agents; Multi-Agent; Evaluation; Environment Interaction | Execution-grounded multi-agent SWE framework where Planner, Coder, Tester, Debugger, and Critic coordinate through shared memory and every code change must survive Docker sandbox execution before propagation. | Role decomposition can add overhead; Docker sandbox and mandatory verification are heavier but justified for code changes. | Mandatory execution feedback; repository-state decision process; role decomposition only for coding; shared memory around execution results. | Strong SWE primitive. For code-modifying flows, execution feedback should be first-class, not optional. |
| LlamaIndex | Knowledge & Retrieval; Memory; Tooling | Data connectors, indexes, retrieval orchestration, agent/RAG workflows; strong document/data ingestion ecosystem. | Can become a large abstraction layer; many components if adopted wholesale. | Connector/index abstractions; retrieval pipelines; query engines; document-to-agent bridge. | Valuable retrieval primitives. Prefer selective extraction over full dependency lock-in. |
| Haystack | Knowledge & Retrieval; Evaluation; Tooling | Modular RAG pipelines; retrieval/generation components; production-oriented search and NLP pipelines; context engineering orientation. | Pipeline abstraction may be heavier than needed for early Bricolage. | Composable RAG pipeline model; retriever/ranker/generator separations; evaluation patterns; explicit context flow. | Useful comparison baseline for retrieval architecture. |
| RAGPulse | Knowledge & Retrieval; Infrastructure; Economics & Resource Management | Open RAG workload trace from real deployment; shows temporal locality and skewed hot-document access; supports retrieval caching/content-aware batching research. | Serving optimization dataset, not agent framework. | Hot-document caching; retrieval workload trace design; privacy-preserving RAG telemetry. | Useful when Bricolage gets persistent retrieval at scale. Not core now. |
| U-NIAH | Knowledge & Retrieval; Evaluation; Context | Unified long-context/RAG eval with multi-needle and noise settings; compares RAG and long-context models; identifies RAG error patterns. | Synthetic benchmark; not a runtime. | Retrieval stress tests; lost-in-middle evaluation; noise sensitivity checks. | Good lean eval primitive for memory/retrieval quality. |
| LangGraph | Runtime & Orchestration; State Architecture; Multi-Agent | Stateful graph execution for LLM apps/agents; explicit nodes/edges/state; cycles and durable workflows; common base for more advanced systems like AgentGit. | LangChain ecosystem can accumulate abstraction weight; avoid framework lock-in. | State graph runtime; explicit state transitions; durable agent loops; graph inspection. | Major runtime primitive. Synthesize the state graph idea, not necessarily the whole ecosystem. |
| LangSmith / Langfuse class | Observability; Evaluation; Human Interaction | Agent tracing, evals, prompt/version management, dataset runs, replay/trajectory inspection, production monitoring. | Can become vendor/tooling dependency; observability overkill if every toy workflow is traced. | Trace schema; replayable trajectories; eval datasets; failure clustering; prompt/version lineage. | Important, but Bricolage can start with lean repo-native traces before adopting full stack. |
| Orchestral AI | Runtime; Tooling; Models, Context & Inference; Human Interaction | Lightweight Python framework with unified type-safe representation for messages/tools/usage across providers; automatic tool schema generation from Python type hints; sync deterministic execution; streaming; context compaction; approvals; sub-agents; memory; MCP. | New project/paper; need repo maturity check. Synchronous simplicity may limit some large-scale async use cases. | Universal message/tool schema; type-hint-to-tool schema generation; deterministic sync execution; provider-normalization layer. | Strong low-friction candidate. Its anti-framework-bloat stance aligns with Bricolage. |
| MiroFlow | Runtime; Cognition; Knowledge & Retrieval; Evaluation | Agent graph for deep research, optional deep reasoning mode, robust reproducible workflow execution, benchmarked across GAIA, BrowseComp, HLE, xBench-DeepSearch, FutureX. | Deep-research specialization; may optimize for benchmark harnesses over general conversational agents. | Deep research graph; robust workflow replay; reasoning-mode toggle; reproducible research baseline. | Important for research-agent capability. Extract deep-research workflow and reproducibility ideas. |
| Orchard | Environment Interaction; Software Engineering Agents; Learning; Evaluation; Infrastructure | Lightweight environment service for reusable sandbox lifecycle management across task domains; agent harnesses; training/evaluation recipes for SWE, GUI, and personal assistant agents; open agentic modeling framework. | Training/RL layer is beyond immediate ChatGPT/Codex use; large research framework. | Harness-agnostic environment layer; sandbox lifecycle service; reusable task domains; agentic data/training/eval separation. | Very important 2026 source for environment/harness architecture. Adopt environment-layer idea, not full training pipeline now. |
| Agent-Diff | Evaluation; Tooling; Environment Interaction; Observability | Evaluates agents on real API tasks using code execution; state-diff contract separates process from outcome; standardized sandbox scripting layer for APIs like Slack, Box, Linear, Google Calendar. | Benchmark/eval framework, not runtime; API-task scope. | Outcome-based state-diff evaluation; real-service API sandbox; task success as expected state change. | Extremely valuable eval primitive without over-testing ceremony. Use state-diff checks for practical tasks. |
| AgentSight | Observability; Safety; Runtime; Infrastructure | Framework-agnostic AgentOps observability using eBPF boundary tracing; correlates high-level LLM intent with low-level system effects; detects prompt injection, loops, and coordination bottlenecks. | Deep systems instrumentation may be too heavy for early cloud-first setup. | Intent/effect correlation; boundary tracing concept; detecting loops and hidden tool effects. | Conceptually powerful. Keep as advanced observability direction, not immediate dependency. |
| GitAgent | Tooling; Skills; Software Engineering Agents; Infrastructure | Autonomous tool extension from GitHub; uses repositories as external tool resources; learns from GitHub Issues/PRs during integration. | Autonomously importing arbitrary repos is risky and noisy. | GitHub-as-tool-marketplace; repo vetting/integration pipeline; issue/PR mining for operational knowledge. | Very aligned with Bricolage research mission. Needs strong license/security vetting. |
| Ollama | Models, Context & Inference; Infrastructure; Tooling | MIT-licensed local/open-weight model runtime with CLI, local REST API, model management, and integrations with coding assistants and agent tools. | Less relevant while relying on ChatGPT/Codex cloud; local model quality/hardware constraints vary. | Model runtime abstraction; local/offline fallback; OpenAI-like local API surface; model inventory management. | Not core to initial cloud flow, but important optional independence layer. |
| vLLM | Models, Context & Inference; Infrastructure; Economics | Apache-licensed inference engine with PagedAttention, continuous batching, distributed inference, quantization, and OpenAI-compatible APIs. | Infra-heavy; only needed if serving models directly. | Efficient model serving backend; OpenAI-compatible endpoint abstraction; batching/resource scheduling lessons. | Long-term inference substrate candidate, not initial dependency. |
| SGLang | Models, Context & Inference; Infrastructure; Runtime | Apache-licensed structured generation language plus runtime; supports structured outputs, speculative decoding, continuous batching, quantization, OpenAI-style APIs, RadixAttention-style KV reuse. | Infra/research complexity; mostly relevant to self-hosted inference. | Structured generation primitives; constrained decoding; parallel control flow; inference-cache reuse concepts. | Long-term inference/cognition optimization source. |
| Nekro Agent | Tooling; Environment Interaction; Skills; Human Interaction | Extensible AI agent framework for multi-user/chat environments; sandboxed execution; plugin architecture; multimodal interaction; Docker deployment. | Custom license/details need review; chat-platform orientation may not match core build. | Chat-platform agent loop; plugin architecture; sandboxed code execution. | Worth scanning as a chat-native agent pattern. |

---

# Emerging Synthesis Signals

## 1. Strongest core primitives so far

- explicit state graph execution
- branchable/replayable trajectories
- sandboxed software execution
- cloud/mobile conversational operation through ChatGPT + Codex + GitHub
- mandatory execution-grounded verification for code changes
- hierarchical working memory plus persistent notes for large repos
- blueprint-first deterministic workflow spine with LLMs as bounded tools
- evolutionary generate/evaluate/select loops for algorithmic improvement
- declarative cognitive modules
- typed/schema-validated agent/tool contracts
- MCP-style tool boundaries
- AGENTS.md-style repo-native agent instruction layer
- file-centric long-horizon state externalization
- browser automation as a first-class environment
- persistent memory with explicit write/read policies
- multi-agent role/task coordination only where execution value is real
- role-specific artifacts and handoff contracts, not roleplay for its own sake
- repo-native state and knowledge
- outcome/state-diff evaluation instead of heavy benchmark bureaucracy
- static graph preflight checks for obvious workflow failures
- environment/harness abstraction separated from agent logic
- privacy/information-flow checks at tool boundaries
- elastic memory compression and episodic abstraction
- provider-normalized message/tool schema
- intent/effect observability concept
- structured generation and inference runtime abstractions for later self-hosting
- visual workflow builders as UX references, not necessarily runtime foundations

## 2. Bricolage should avoid

- adopting giant frameworks whole
- stacking orchestration frameworks on top of each other
- role-based agent theater without execution value
- creating a DSL before workflow pressure proves it is needed
- over-indexing on eval/governance ceremony before core capability
- custom tool integrations when MCP/open standards already solve the boundary
- unconstrained autonomous loops without state/outcome checks
- autonomous repo/tool ingestion without license/security review
- broad personal-service authority without explicit scope and human control
- agent-to-agent exposure to untrusted content without prompt-injection boundaries
- publicly exposed low-code execution servers without strong sandboxing

## 3. Bricolage should aggressively adopt/synthesize

- ChatGPT/Codex/GitHub as the first operational substrate
- OpenHands-style execution/workspace/sandbox primitives
- Confucius-style hierarchical working memory and persistent notes
- AgentForge-style execution-grounded coding verification
- InfiAgent-style file-centric state externalization
- Blueprint-first deterministic workflow for strict procedures
- Pydantic AI / Orchestral-style typed tool/result contracts
- DSPy-style declarative reasoning modules where repeatable reasoning matters
- LangGraph/AgentGit-style state graph and branchable trajectory concepts
- MCP as the default tool/data connector boundary
- AGENTS.md as the repo-native Codex/agent control file
- MetaGPT-style artifact handoffs only where useful
- CrewAI/CAMEL/AutoGen multi-agent ideas only where multiple agents truly add value
- Letta/MemGPT-style explicit memory layers, adapted to repo-native persistence
- browser-use/Playwright-style browser actions for real-world task automation
- Agent-Diff-style state-diff success contracts
- Agentproof-style static graph sanity checks
- Orchard/E2B/Daytona-style environment/harness layer
- OpenClaw-style skill directories with explicit safety/permission constraints
- Google Antigravity-style verifiable artifacts for trust
- ModelScope-Agent-style tool registry/retrieval for large capability libraries

---

# Evaluation Lens

Every repository or framework should be evaluated according to capability density, architectural clarity, operational friction, modularity, extensibility, runtime simplicity, state management quality, practical utility, production viability, innovation value, and conversational leverage from the ChatGPT/Codex/GitHub cloud loop.

---

# Research Source Notes - Passes 1-5

These notes capture the source-grounded basis for the population passes. They are not exhaustive and should be replaced or expanded with repo-level citations as deeper inspection continues.

- OpenHands SDK paper: composable software-agent SDK, sandboxed execution, local-to-remote portability, REST/WebSocket services, multiple user interfaces, model-agnostic routing, lifecycle control, security analysis, SWE-Bench/GAIA evaluation.
- Codex public/current summaries: ChatGPT web/mobile/GitHub/IDE/cloud coding-agent workflows, issue/PR assignment, cloud execution, and broader enterprise-agent positioning.
- Confucius Code Agent paper: industrial-scale OSS coding agent, hierarchical working memory, persistent notes, modular extension, meta-agent build-test-improve loop, SWE-Bench-Pro performance.
- DSPy paper: declarative modules, LM pipelines as computational graphs, compiler/optimizer, metric-driven improvement, prompt/program abstraction.
- Blueprint First / Source Code Agent paper: deterministic workflow blueprint, LLM as bounded subtask tool, tau-bench improvement and efficiency.
- AlphaEvolve public sources: LLM plus evolutionary computation for algorithm discovery using evaluation functions and variant selection.
- Pydantic AI public docs/summaries: type-safe Python agent framework, structured outputs, dependency injection, validation, provider abstraction.
- Semantic Kernel public docs/summaries: Microsoft agent SDK, plugins/functions, planners, memory/connectors, MCP and Azure/OpenAI/local integrations.
- CrewAI public summary: open-source Python multi-agent framework with crews, roles, goals, tasks, delegation, tools, memory, knowledge sources, Flows, MIT license, and active 2026 release line.
- CAMEL public repo/papers: communicative agents, role-playing, agent societies, simulations, multi-agent research.
- MetaGPT public repo/papers: software-company multi-agent metaphor, SOPs, role-specific artifacts, software generation.
- AutoGen Studio paper: declarative JSON specs, no-code multi-agent workflow authoring, debugging/evaluation UI, reusable components.
- AutoGPT public summaries: early autonomous agent, MIT license, loops/hallucinations/cost failures, Forge/platform lineage.
- BabyAGI public sources: minimal task creation/prioritization/execution loop and memory.
- SuperAGI public sources: autonomous agent platform, GUI, provisioning, toolkits, memory/vector DBs, marketplace-style extensions.
- AgentSPEX paper: typed workflow specs, branching/loops, explicit state, tools, sandboxing, checkpointing, verification, logging, visual editor.
- Agentproof paper: static verification of workflow graphs across LangGraph, CrewAI, AutoGen, and Google ADK; structural checks and temporal policy automata.
- AgentGit paper: Git-like commit/revert/branching for multi-agent workflows, trajectory comparison, reduced redundant computation/token usage.
- MCP public sources: open standard for model-tool/data integration, JSON-RPC, broad adoption by OpenAI/Google DeepMind, ChatGPT app support, reference servers.
- AGENTS.md public reports: repo-native standard for coordinating AI coding agents, contributed to Linux Foundation/AAIF, broad project adoption.
- A2A public sources: open protocol for agent communication, discovery, messaging, task coordination, Linux Foundation governance.
- ModelScope-Agent paper: customizable open-source LLM agent framework, tool retrieval/registration, memory control, training/evaluation, 1000+ public AI model integration.
- Google ADK/Gemini Enterprise public sources: Agent Development Kit, Agent Runtime, Identity, Gateway, Registry, Agent Studio, observability, simulation, deployment.
- Google Antigravity public sources: agent-first IDE, manager/editor views, parallel agents, verifiable artifacts such as plans/screenshots/browser recordings.
- AgentSCOPE paper: contextual privacy and Privacy Flow Graphs for intermediate agent/tool information flows.
- Playwright public sources: mature Apache 2.0 browser automation substrate across Chromium, Firefox, and WebKit.
- Flowise public/security reports: low-code LLM/agent builder; CustomMCP node vulnerability CVE-2025-59528 enabled arbitrary code execution in exposed instances.
- Dify public docs/summaries: open-source LLM app/agent platform, workflow builder, RAG, model providers, observability/operations.
- OpenClaw/Moltbook public sources: messaging-first autonomous assistant, MIT license, local gateway, SKILL.md directory convention, broad skill library, and significant prompt-injection/malicious-skill warnings.
- AutoAgent paper: evolving cognition, contextual decision-making, elastic memory orchestration, reusable episodic abstractions, closed-loop cognitive evolution.
- InfiAgent paper: infinite-horizon file-centric state abstraction, bounded context loop, workspace snapshots plus recent action windows.
- Orchestral AI paper: lightweight provider-normalized agent framework with type-safe message/tool representations and deterministic sync execution.
- MiroFlow paper: agent graph, optional deep reasoning, robust reproducible deep-research workflows, broad benchmark coverage.
- Orchard paper: lightweight environment service, sandbox lifecycle management, harness-agnostic environment primitives, SWE/GUI/personal-assistant recipes.
- Agent-Diff paper: state-diff evaluation contracts for real-world API tasks via sandboxed code execution.
- AgentSight paper: framework-agnostic observability by correlating LLM intent and system effects through boundary tracing.
- AgentForge paper: execution-grounded multi-agent SWE verification with Docker sandbox, role decomposition, shared memory, and SWE-Bench Lite result.
- GitAgent paper: autonomous GitHub repository integration as tool extension, including learning from Issues/PRs.
- RAGPulse paper: real-world RAG workload trace showing temporal locality and hot-document skew.
- U-NIAH paper: unified RAG/long-context evaluation for multi-needle/noisy retrieval settings.
- Ollama public summary: MIT local/cloud model runtime with CLI, REST API, model management, integrations with coding assistants and agents.
- vLLM public summary: Apache 2.0 inference engine with PagedAttention, batching, distributed inference, quantization, OpenAI-compatible APIs.
- SGLang public summary: Apache 2.0 structured generation language/runtime with constrained decoding, continuous batching, speculative execution, KV-cache reuse.

---

# Current Philosophy

The project should remain ambitious, synthesis-first, conversational-agent-first, cloud-native through ChatGPT + Codex + GitHub, architecture-focused, implementation-aware, and minimally bureaucratic.

The repository structure itself should emerge naturally from repeated architectural patterns, implementation pressure, synthesis discoveries, and operational requirements rather than from premature formalization.
