# Agent Repository Matrix

## Purpose

This document is the primary comparative synthesis workspace for the Bricolage project.

The goal is NOT to rank entire frameworks.

The goal is to identify architectural primitives, low-friction patterns, state-of-the-art implementations, reusable abstractions, unnecessary complexity, and synthesis candidates for a coherent conversational agent architecture.

---

# Core Project Principle

Bricolage prioritizes:

- low-friction architecture
- modularity
- composability
- high capability density
- practical usability
- implementation realism
- state-of-the-art functionality
- minimal unnecessary ceremony
- direct conversational usefulness
- aggressive synthesis of proven open-source ideas

Bricolage does NOT aim to maximize enterprise abstraction layers, governance bureaucracy, configuration complexity, documentation volume, testing ceremony, or heavyweight orchestration unless the capability gain is substantial.

---

# Comparative Matrix - Passes 1-3

| Repo / System | Primary Categories | Key Innovations | Friction / Complexity | Synthesis Candidates | Initial Bricolage Judgment |
|---|---|---|---|---|---|
| OpenHands / OpenHands SDK | Software Engineering Agents; Environment Interaction; Tooling; Runtime; Human Interaction | Composable software-agent SDK; sandboxed execution; local-to-remote portability; REST/WebSocket services; visual workspace, CLI, API interfaces; model-agnostic routing; lifecycle control; security analysis; SWE-Bench and GAIA orientation. | Larger system surface than lightweight agents; production-grade execution/sandbox design brings real complexity. | Sandboxed execution layer; software-agent harness; lifecycle model; workspace interface abstraction; remote/cloud execution pattern; model routing boundary. | Very high-value. Do not copy whole stack blindly, but this is one of the strongest candidates for execution/runtime architecture. |
| DSPy | Cognition & Reasoning; Models, Context & Inference; Evaluation | Declarative LM programs; modules instead of prompt strings; optimizers/compilers; metric-driven prompt/program improvement; assertions for constraint-guided refinement. | Requires adopting a programming model; optimizer/eval loops can become overbuilt if used everywhere. | Declarative cognitive modules; prompt/program compilation; assertions as lightweight verification; metric-driven tuning for reusable reasoning modules. | Essential cognition primitive. Use selectively for high-value reasoning pipelines, not every chat turn. |
| CrewAI | Multi-Agent Coordination; Runtime & Orchestration; Skills; Tooling | Role/task/crew abstraction; collaborative agent teams; Flows for controlled event-driven workflows; memory, tools, knowledge/RAG integration; MIT licensed; current public release line shows active 2026 development. | Can become role-play orchestration theater if overused; enterprise layer may add overhead. | Crew/task vocabulary; role-specialized agents; simple collaborative workflows; task delegation pattern. | Useful multi-agent vocabulary. Synthesize primitives, avoid adopting heavy crew formalism unless it proves useful. |
| AutoGen / AutoGen Studio | Multi-Agent Coordination; Human Interaction; Observability & Evaluation; Runtime | Multi-agent conversational workflows; declarative JSON-based agent specs; no-code/visual workflow building; debugging/evaluation UI; reusable component gallery. | Multi-agent conversation systems can become hard to debug; studio/no-code layer may not fit Bricolage's repo-first flow. | Declarative agent definitions; inspectable conversation graphs; reusable agent components; debugging UI concepts. | Strong ideas for agent interaction protocols and debugging. Probably not the central runtime. |
| AgentSPEX | Runtime & Orchestration; Infrastructure/State; Evaluation; Skills | Explicit agent workflow specification language; typed steps; branching/loops; parallel execution; reusable submodules; explicit state; harness with tools, sandbox, checkpointing, verification, logging; visual graph/workflow editor. | A new DSL can be friction if too much is formalized too soon. | Explicit workflow/state language; typed steps; portable workflow specs; checkpointing without enterprise bloat; visual/graph inspection concept. | Very important 2026 direction. Consider Bricolage-native lightweight spec format rather than adopting full DSL immediately. |
| AgentGit | Runtime & Orchestration; Infrastructure/State; Observability; Evaluation | Git-like commit/revert/branching for multi-agent workflows; trajectory branching; A/B exploration; reduced redundant computation/token usage; built atop LangGraph. | Adds state-versioning layer; may be overkill for simple tasks. | Git-like agent state commits; branchable trajectories; rollback/replay; compare alternate reasoning/action paths. | Extremely aligned with GitHub/repo-native Bricolage. Strong primitive candidate. |
| MCP | Tooling & Action Systems; Protocols; Infrastructure; Knowledge & Retrieval | Open standard for connecting models/agents to tools, data sources, prompts, and external systems; JSON-RPC-based; broad provider adoption; reference servers for GitHub, Git, Postgres, Slack, Puppeteer, etc.; donated to Linux Foundation/AAIF as an open neutral standard. | Security boundaries are nontrivial; tool execution can be dangerous without whitelisting/schema validation; ecosystem quality varies. | Standard tool/data connector boundary; MCP server registry; permissioned tool invocation; schema-bound tool access. | Essential protocol layer. Adopt as a boundary, but wrap with Bricolage trust/permission model. |
| AGENTS.md standard | Skills; Software Engineering Agents; Human Interaction; Protocols | Repo-native instruction format for coding agents; public reports describe broad adoption and Linux Foundation/AAIF contribution alongside MCP. | May become vague if used as a dumping ground; needs concise rules. | One canonical instruction file for ChatGPT/Codex/other coding agents; repo-native coordination layer. | Immediate Bricolage need. Create and keep powerful, not bureaucratic. |
| A2A / Agent2Agent | Multi-Agent Coordination; Protocols; Infrastructure | Open protocol for agent-to-agent discovery, messaging, and task coordination across systems/vendors; Linux Foundation governance. | Young ecosystem; risk of premature protocol complexity. | External agent interoperability; agent discovery; message/task envelope schemas; vendor-neutral multi-agent protocol boundary. | Important for future interoperability, not necessarily core v0 runtime. |
| Letta / MemGPT | Memory Systems; Runtime; Human Interaction | Stateful agents with explicit memory architecture; long-running agent identity; separation between context-window management and longer-term memory; memory as first-class agent substrate. | Memory systems can become noisy, expensive, or unreliable without disciplined write/read policies. | Explicit memory layers; memory write policies; persona/identity continuity; archival vs working memory separation. | Core memory inspiration. Must synthesize carefully with repo-native/GitHub memory. |
| InfiAgent | Memory Systems; Runtime; Context; Knowledge & Retrieval | Infinite-horizon framework that keeps reasoning context bounded by externalizing persistent state into a file-centric state abstraction; reconstructs context from workspace snapshots plus recent action windows. | Research framework; implementation maturity needs inspection. File-state discipline requires strong conventions. | File-centric persistent state; bounded context loop; workspace snapshot reconstruction; long-horizon research state. | Very aligned with ChatGPT/Codex/GitHub cloud workflow. Strong candidate for Bricolage memory/state philosophy. |
| AutoAgent | Runtime; Skills; Memory; Multi-Agent; Learning | Evolving cognition, on-the-fly contextual decision-making, elastic memory orchestration, closed-loop cognitive evolution, reusable episodic abstraction. | Ambitious and potentially complex; must verify implementation availability and practicality. | Elastic memory orchestrator; cognition update loop; peer/tool capability cognition; compression of redundant trajectories. | Important 2026 adaptive-agent direction. Extract memory/cognition concepts if implementation holds up. |
| browser-use / Browser agents | Environment Interaction; Tooling; Human Interaction | Practical browser automation for agents; web interaction as first-class action space; often built on Playwright-style browser control. | Web automation is brittle; prompt injection/security risk; UI variability. | Browser action interface; page-state extraction; human takeover/approval; browser task loop. | High capability per complexity. Needs safety gates around logged-in/sensitive actions. |
| Playwright | Environment Interaction; Tooling; Evaluation | Mature cross-browser automation API for Chromium/Firefox/WebKit; robust automation substrate; Apache 2.0. | Not an agent framework; low-level automation requires higher-level reasoning wrapper. | Browser execution substrate; deterministic browser actions; screenshots/traces; web task replay. | Likely best low-level browser substrate if Bricolage needs browser actions. |
| OpenClaw | Human Interaction; Skills; Tooling; Environment Interaction | Messaging-first autonomous assistant; local-running agent; extensible skill directory; service integrations; MIT licensed; skills as directories with SKILL.md; configuration/history stored locally for persistent adaptive behavior. | Setup/security risk; unvetted skills are dangerous; reports include overreach incidents and enterprise/government restrictions. | Messaging-first agent UX; skill directory; gateway pattern; skill precedence model; strong warning model for broad tool authority. | High-value conversational UX source and also a major cautionary case. Steal skills/gateway ideas, not unconstrained authority. |
| SWE-agent | Software Engineering Agents; Evaluation; Runtime | Focused coding-agent loop; repository issue-to-patch flow; SWE-Bench orientation; emphasizes execution and verification against real repos. | Specialized to coding tasks; may not generalize as whole architecture. | Issue-to-patch loop; test-first verification; repo navigation/action loop; coding trajectory logs. | Strong coding-agent primitive. Use with OpenHands/Codex-style execution concepts. |
| AgentForge / AutoCodeAI | Software Engineering Agents; Multi-Agent; Evaluation; Environment Interaction | Execution-grounded multi-agent SWE framework where Planner, Coder, Tester, Debugger, and Critic coordinate through shared memory and every code change must survive Docker sandbox execution before propagation; reported 40 percent SWE-Bench Lite resolution. | Role decomposition can add overhead; Docker sandbox and mandatory verification are heavier but justified for code changes. | Mandatory execution feedback; repository-state decision process; role decomposition only for coding; shared memory around execution results. | Strong SWE primitive. For code-modifying flows, execution feedback should be first-class, not optional. |
| LlamaIndex | Knowledge & Retrieval; Memory; Tooling | Data connectors, indexes, retrieval orchestration, agent/RAG workflows; strong document/data ingestion ecosystem. | Can become a large abstraction layer; many components if adopted wholesale. | Connector/index abstractions; retrieval pipelines; query engines; document-to-agent bridge. | Valuable retrieval primitives. Prefer selective extraction over full dependency lock-in. |
| Haystack | Knowledge & Retrieval; Evaluation; Tooling | Modular RAG pipelines; retrieval/generation components; production-oriented search and NLP pipelines; context engineering orientation. | Pipeline abstraction may be heavier than needed for early Bricolage. | Composable RAG pipeline model; retriever/ranker/generator separations; evaluation patterns; explicit context flow. | Useful comparison baseline for retrieval architecture. |
| RAGPulse | Knowledge & Retrieval; Infrastructure; Economics & Resource Management | Open RAG workload trace from real deployment; shows temporal locality and skewed hot-document access; supports retrieval caching/content-aware batching research. | Serving optimization dataset, not agent framework. | Hot-document caching; retrieval workload trace design; privacy-preserving RAG telemetry. | Useful when Bricolage gets persistent retrieval at scale. Not core now. |
| U-NIAH | Knowledge & Retrieval; Evaluation; Context | Unified long-context/RAG eval with multi-needle and noise settings; compares RAG and long-context models; identifies RAG error patterns. | Synthetic benchmark; not a runtime. | Retrieval stress tests; lost-in-middle evaluation; noise sensitivity checks. | Good lean eval primitive for memory/retrieval quality. |
| LangGraph | Runtime & Orchestration; State Architecture; Multi-Agent | Stateful graph execution for LLM apps/agents; explicit nodes/edges/state; cycles and durable workflows; common base for more advanced systems like AgentGit. | LangChain ecosystem can accumulate abstraction weight; avoid framework lock-in. | State graph runtime; explicit state transitions; durable agent loops; graph inspection. | Major runtime primitive. Synthesize the state graph idea, not necessarily the whole ecosystem. |
| Orchestral AI | Runtime; Tooling; Models, Context & Inference; Human Interaction | Lightweight Python framework with unified type-safe representation for messages/tools/usage across providers; automatic tool schema generation from Python type hints; synchronous deterministic execution; streaming; context compaction; approvals; sub-agents; memory; MCP. | New project/paper; need repo maturity check. Synchronous simplicity may limit some large-scale async use cases. | Universal message/tool schema; type-hint-to-tool schema generation; deterministic sync execution; provider-normalization layer. | Strong low-friction candidate. Its anti-framework-bloat stance aligns with Bricolage. |
| MiroFlow | Runtime; Cognition; Knowledge & Retrieval; Evaluation | Agent graph for deep research, optional deep reasoning mode, robust reproducible workflow execution, benchmarked across GAIA, BrowseComp, HLE, xBench-DeepSearch, FutureX. | Deep-research specialization; may optimize for benchmark harnesses over general conversational agents. | Deep research graph; robust workflow replay; reasoning-mode toggle; reproducible research baseline. | Important for research-agent capability. Extract deep-research workflow and reproducibility ideas. |
| Orchard | Environment Interaction; Software Engineering Agents; Learning; Evaluation; Infrastructure | Lightweight environment service for reusable sandbox lifecycle management across task domains; agent harnesses; training/evaluation recipes for SWE, GUI, and personal assistant agents; open agentic modeling framework. | Training/RL layer is beyond immediate ChatGPT/Codex use; large research framework. | Harness-agnostic environment layer; sandbox lifecycle service; reusable task domains; agentic data/training/eval separation. | Very important 2026 source for environment/harness architecture. Adopt environment-layer idea, not full training pipeline now. |
| Agent-Diff | Evaluation; Tooling; Environment Interaction; Observability | Evaluates agents on real API tasks using code execution; state-diff contract separates process from outcome; standardized sandbox scripting layer for APIs like Slack, Box, Linear, Google Calendar. | Benchmark/eval framework, not runtime; API-task scope. | Outcome-based state-diff evaluation; real-service API sandbox; task success as expected state change. | Extremely valuable eval primitive without over-testing ceremony. Use state-diff checks for practical tasks. |
| AgentSight | Observability; Safety; Runtime; Infrastructure | Framework-agnostic AgentOps observability using eBPF boundary tracing; correlates high-level LLM intent with low-level system effects; detects prompt injection, loops, and coordination bottlenecks. | Deep systems instrumentation may be too heavy for early cloud-first setup. | Intent/effect correlation; boundary tracing concept; detecting loops and hidden tool effects. | Conceptually powerful. Keep as advanced observability direction, not immediate dependency. |
| GitAgent | Tooling; Skills; Software Engineering Agents; Infrastructure | Autonomous tool extension from GitHub; uses repositories as external tool resources; learns from GitHub Issues/PRs during integration. | Autonomously importing arbitrary repos is risky and noisy. | GitHub-as-tool-marketplace; repo vetting/integration pipeline; issue/PR mining for operational knowledge. | Very aligned with Bricolage research mission. Needs strong license/security vetting. |
| Ollama | Models, Context & Inference; Infrastructure; Tooling | MIT-licensed local/open-weight model runtime with CLI, local REST API, model management, and integrations with coding assistants and agent tools. | Less relevant while relying on ChatGPT/Codex cloud; local model quality/hardware constraints vary. | Model runtime abstraction; local/offline fallback; OpenAI-like local API surface; model inventory management. | Not core to initial cloud flow, but important optional independence layer. |
| vLLM | Models, Context & Inference; Infrastructure; Economics | Apache-licensed inference engine with PagedAttention, continuous batching, distributed inference, quantization, and OpenAI-compatible APIs. | Infra-heavy; only needed if serving models directly. | Efficient model serving backend; OpenAI-compatible endpoint abstraction; batching/resource scheduling lessons. | Long-term inference substrate candidate, not initial dependency. |
| SGLang | Models, Context & Inference; Infrastructure; Runtime | Apache-licensed structured generation language plus runtime; supports structured outputs, speculative decoding, continuous batching, quantization, OpenAI-style APIs, RadixAttention-style KV reuse. | Infra/research complexity; mostly relevant to self-hosted inference. | Structured generation primitives; constrained decoding; parallel control flow; inference-cache reuse concepts. | Long-term inference/cognition optimization source. |
| Nekro Agent | Tooling; Environment Interaction; Skills; Human Interaction | Extensible AI agent framework for multi-user/chat environments; sandboxed execution; plugin architecture; multimodal interaction; Docker deployment. | Custom license/details need review; chat-platform orientation may not match core build. | Chat-platform agent loop; plugin architecture; sandboxed code execution. | Worth scanning as a chat-native agent pattern. |
| AutoGPT | Runtime; Tooling; Historical Baseline | Early autonomous goal decomposition with tools, browsing, file management; popularized autonomous agents. | Known issues: loops, hallucination, high cost, brittle autonomy. | Negative lessons: avoid unconstrained loops, avoid vague goal autonomy, require outcome checks. | More useful as a cautionary ancestor than a direct source. |

---

# Emerging Synthesis Signals

## 1. Strongest core primitives so far

- explicit state graph execution
- branchable/replayable trajectories
- sandboxed software execution
- mandatory execution-grounded verification for code changes
- declarative cognitive modules
- MCP-style tool boundaries
- AGENTS.md-style repo-native agent instruction layer
- file-centric long-horizon state externalization
- browser automation as a first-class environment
- persistent memory with explicit write/read policies
- multi-agent role/task coordination only where execution value is real
- repo-native state and knowledge
- outcome/state-diff evaluation instead of heavy benchmark bureaucracy
- environment/harness abstraction separated from agent logic
- elastic memory compression and episodic abstraction
- provider-normalized message/tool schema
- intent/effect observability concept
- structured generation and inference runtime abstractions for later self-hosting

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

## 3. Bricolage should aggressively adopt/synthesize

- OpenHands-style execution/workspace/sandbox primitives
- AgentForge-style execution-grounded coding verification
- InfiAgent-style file-centric state externalization
- DSPy-style declarative reasoning modules where repeatable reasoning matters
- LangGraph/AgentGit-style state graph and branchable trajectory concepts
- MCP as the default tool/data connector boundary
- AGENTS.md as the repo-native Codex/agent control file
- CrewAI/AutoGen multi-agent ideas only where multiple agents truly add value
- Letta/MemGPT-style explicit memory layers, adapted to repo-native persistence
- browser-use/Playwright-style browser actions for real-world task automation
- Agent-Diff-style state-diff success contracts
- Orchard-style environment/harness layer
- Orchestral-style provider-normalized low-friction tool/message schema
- OpenClaw-style skill directories with explicit safety/permission constraints

---

# Evaluation Lens

Every repository or framework should be evaluated according to:

1. Capability density: useful functionality relative to complexity.
2. Architectural clarity: how understandable and composable the architecture is.
3. Operational friction: difficulty to run, maintain, extend, debug, and reason about.
4. Modularity: whether useful subsystems can be extracted independently.
5. Extensibility: whether the architecture can evolve cleanly.
6. Runtime simplicity: whether the execution model stays understandable.
7. State management quality: how coherent and manageable state is.
8. Practical utility: whether the system solves real-world problems effectively.
9. Production viability: whether the architecture can support real workloads.
10. Innovation value: whether the project contributes genuinely novel/superior ideas.
11. Conversational leverage: whether it strengthens ChatGPT/Codex/GitHub cloud workflows from an iPhone-first operator loop.

---

# Research Source Notes - Passes 1-3

These notes capture the source-grounded basis for the population passes. They are not exhaustive and should be replaced or expanded with repo-level citations as deeper inspection continues.

- OpenHands SDK paper: composable software-agent SDK, sandboxed execution, local-to-remote portability, REST/WebSocket services, multiple user interfaces, model-agnostic routing, lifecycle control, security analysis, SWE-Bench/GAIA evaluation.
- DSPy paper: declarative modules, LM pipelines as computational graphs, compiler/optimizer, metric-driven improvement, prompt/program abstraction.
- DSPy Assertions paper: computational constraints for self-refining LM pipelines.
- CrewAI public summary: open-source Python multi-agent framework with crews, roles, goals, tasks, delegation, tools, memory, knowledge sources, Flows, MIT license, and active 2026 release line.
- AutoGen Studio paper: declarative JSON specs, no-code multi-agent workflow authoring, debugging/evaluation UI, reusable components.
- AgentSPEX paper: typed workflow specs, branching/loops, explicit state, tools, sandboxing, checkpointing, verification, logging, visual editor.
- AgentGit paper: Git-like commit/revert/branching for multi-agent workflows, trajectory comparison, reduced redundant computation/token usage.
- MCP public sources: open standard for model-tool/data integration, JSON-RPC, broad adoption, Linux Foundation/AAIF direction, reference servers.
- AGENTS.md public reports: repo-native standard for coordinating AI coding agents, contributed to Linux Foundation/AAIF, broad project adoption.
- A2A public sources: open protocol for agent communication, discovery, messaging, task coordination, Linux Foundation governance.
- Playwright public sources: mature Apache 2.0 browser automation substrate across Chromium, Firefox, and WebKit.
- OpenClaw public sources: messaging-first autonomous assistant, MIT license, local gateway, SKILL.md directory convention, broad skill library, and major safety warnings.
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
- AutoGPT public summary: historically important autonomous agent, but useful mainly as cautionary evidence for loop/cost/hallucination failure modes.

---

# Current Philosophy

The project should remain ambitious, synthesis-first, conversational-agent-first, cloud-native through ChatGPT + Codex + GitHub, architecture-focused, implementation-aware, and minimally bureaucratic.

The repository structure itself should emerge naturally from repeated architectural patterns, implementation pressure, synthesis discoveries, and operational requirements rather than from premature formalization.
