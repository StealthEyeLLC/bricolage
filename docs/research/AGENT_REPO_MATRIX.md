# Agent Repository Matrix

## Purpose

This document is the primary comparative synthesis workspace for the Bricolage project.

The goal is NOT to rank entire frameworks.

The goal is to:
- identify architectural primitives
- identify low-friction patterns
- identify state-of-the-art implementations
- identify reusable abstractions
- identify overengineering and unnecessary complexity
- synthesize the best ideas into a coherent architecture

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

Bricolage does NOT aim to:

- maximize enterprise abstraction layers
- maximize governance bureaucracy
- maximize configuration complexity
- maximize documentation volume
- maximize testing ceremony
- recreate heavyweight orchestration stacks unless clearly justified

The synthesis process should strongly prefer:

- elegant primitives
- composable interfaces
- high leverage abstractions
- runtime simplicity
- understandable systems
- direct conversational usefulness
- aggressive synthesis of proven open-source ideas

Complexity should only be adopted when the capability gain is substantial.

---

# Comparative Matrix - Passes 1-2

| Repo / System | Primary Categories | Key Innovations | Friction / Complexity | Synthesis Candidates | Initial Bricolage Judgment |
|---|---|---|---|---|---|
| OpenHands / OpenHands SDK | Software Engineering Agents; Environment Interaction; Tooling; Runtime; Human Interaction | Composable software-agent SDK; sandboxed execution; local-to-remote portability; REST/WebSocket services; visual workspace, CLI, API interfaces; model-agnostic routing; lifecycle control; security analysis; SWE-Bench and GAIA orientation. | Larger system surface than lightweight agents; production-grade execution/sandbox design brings real complexity. | Sandboxed execution layer; software-agent harness; lifecycle model; workspace interface abstraction; remote/cloud execution pattern; model routing boundary. | Very high-value. Do not copy whole stack blindly, but this is one of the strongest candidates for execution/runtime architecture. |
| DSPy | Cognition & Reasoning; Models, Context & Inference; Evaluation | Declarative LM programs; modules instead of prompt strings; optimizers/compilers; metric-driven prompt/program improvement; assertions for constraint-guided refinement. | Requires adopting a programming model; optimizer/eval loops can become overbuilt if used everywhere. | Declarative cognitive modules; prompt/program compilation; assertions as lightweight verification; metric-driven tuning for reusable reasoning modules. | Essential cognition primitive. Use selectively for high-value reasoning pipelines, not every chat turn. |
| CrewAI | Multi-Agent Coordination; Runtime & Orchestration; Skills; Tooling | Role/task/crew abstraction; collaborative agent teams; Flows for controlled event-driven workflows; memory, tools, knowledge/RAG integration; MIT licensed. | Can become role-play orchestration theater if overused; enterprise layer may add overhead. | Crew/task vocabulary; role-specialized agents; simple collaborative workflows; task delegation pattern. | Useful multi-agent vocabulary. Synthesize primitives, avoid adopting heavy crew formalism unless it proves useful. |
| AutoGen / AutoGen Studio | Multi-Agent Coordination; Human Interaction; Observability & Evaluation; Runtime | Multi-agent conversational workflows; declarative JSON-based agent specs; no-code/visual workflow building; debugging/evaluation UI; reusable component gallery. | Multi-agent conversation systems can become hard to debug; studio/no-code layer may not fit Bricolage's repo-first flow. | Declarative agent definitions; inspectable conversation graphs; reusable agent components; debugging UI concepts. | Strong ideas for agent interaction protocols and debugging. Probably not the central runtime. |
| AgentSPEX | Runtime & Orchestration; Infrastructure/State; Evaluation; Skills | Explicit agent workflow specification language; typed steps; branching/loops; parallel execution; reusable submodules; explicit state; harness with tools, sandbox, checkpointing, verification, logging; visual graph/workflow editor. | A new DSL can be friction if too much is formalized too soon. | Explicit workflow/state language; typed steps; portable workflow specs; checkpointing without enterprise bloat; visual/graph inspection concept. | Very important 2026 direction. Consider Bricolage-native lightweight spec format rather than adopting full DSL immediately. |
| AgentGit | Runtime & Orchestration; Infrastructure/State; Observability; Evaluation | Git-like commit/revert/branching for multi-agent workflows; trajectory branching; A/B exploration; reduced redundant computation/token usage; built atop LangGraph. | Adds state-versioning layer; may be overkill for simple tasks. | Git-like agent state commits; branchable trajectories; rollback/replay; compare alternate reasoning/action paths. | Extremely aligned with GitHub/repo-native Bricolage. Strong primitive candidate. |
| MCP | Tooling & Action Systems; Protocols; Infrastructure; Knowledge & Retrieval | Open standard for connecting models/agents to tools, data sources, prompts, and external systems; JSON-RPC-based; broad provider adoption; reference servers for GitHub, Git, Postgres, Slack, Puppeteer, etc. | Security boundaries are nontrivial; tool execution can be dangerous without whitelisting/schema validation; ecosystem quality varies. | Standard tool/data connector boundary; MCP server registry; permissioned tool invocation; schema-bound tool access. | Essential protocol layer. Adopt as a boundary, but wrap with Bricolage trust/permission model. |
| A2A / Agent2Agent | Multi-Agent Coordination; Protocols; Infrastructure | Open protocol for agent-to-agent discovery, messaging, and task coordination across systems/vendors; Linux Foundation governance. | Young ecosystem; risk of premature protocol complexity. | External agent interoperability; agent discovery; message/task envelope schemas; vendor-neutral multi-agent protocol boundary. | Important for future interoperability, not necessarily core v0 runtime. |
| Letta / MemGPT | Memory Systems; Runtime; Human Interaction | Stateful agents with explicit memory architecture; long-running agent identity; separation between context-window management and longer-term memory; memory as first-class agent substrate. | Memory systems can become noisy, expensive, or unreliable without disciplined write/read policies. | Explicit memory layers; memory write policies; persona/identity continuity; archival vs working memory separation. | Core memory inspiration. Must synthesize carefully with repo-native/GitHub memory. |
| browser-use / Browser agents | Environment Interaction; Tooling; Human Interaction | Practical browser automation for agents; web interaction as first-class action space; often built on Playwright-style browser control. | Web automation is brittle; prompt injection/security risk; UI variability. | Browser action interface; page-state extraction; human takeover/approval; browser task loop. | High capability per complexity. Needs safety gates around logged-in/sensitive actions. |
| Playwright | Environment Interaction; Tooling; Evaluation | Mature cross-browser automation API for Chromium/Firefox/WebKit; robust automation substrate; Apache 2.0. | Not an agent framework; low-level automation requires higher-level reasoning wrapper. | Browser execution substrate; deterministic browser actions; screenshots/traces; web task replay. | Likely best low-level browser substrate if Bricolage needs browser actions. |
| SWE-agent | Software Engineering Agents; Evaluation; Runtime | Focused coding-agent loop; repository issue-to-patch flow; SWE-Bench orientation; emphasizes execution and verification against real repos. | Specialized to coding tasks; may not generalize as whole architecture. | Issue-to-patch loop; test-first verification; repo navigation/action loop; coding trajectory logs. | Strong coding-agent primitive. Use with OpenHands/Codex-style execution concepts. |
| LlamaIndex | Knowledge & Retrieval; Memory; Tooling | Data connectors, indexes, retrieval orchestration, agent/RAG workflows; strong document/data ingestion ecosystem. | Can become a large abstraction layer; many components if adopted wholesale. | Connector/index abstractions; retrieval pipelines; query engines; document-to-agent bridge. | Valuable retrieval primitives. Prefer selective extraction over full dependency lock-in. |
| Haystack | Knowledge & Retrieval; Evaluation; Tooling | Modular RAG pipelines; retrieval/generation components; production-oriented search and NLP pipelines; context engineering orientation. | Pipeline abstraction may be heavier than needed for early Bricolage. | Composable RAG pipeline model; retriever/ranker/generator separations; evaluation patterns; explicit context flow. | Useful comparison baseline for retrieval architecture. |
| LangGraph | Runtime & Orchestration; State Architecture; Multi-Agent | Stateful graph execution for LLM apps/agents; explicit nodes/edges/state; cycles and durable workflows; common base for more advanced systems like AgentGit. | LangChain ecosystem can accumulate abstraction weight; avoid framework lock-in. | State graph runtime; explicit state transitions; durable agent loops; graph inspection. | Major runtime primitive. Synthesize the state graph idea, not necessarily the whole ecosystem. |
| OpenClaw | Human Interaction; Skills; Tooling; Environment Interaction | Messaging-first autonomous assistant; local-running agent; extensible skill directory; service integrations; MIT licensed; reported 100+ built-in skills. | New/fast-moving; setup/security risk; ecosystem maturity needs deeper validation. | Conversational/messaging-first task interface; skill directory; personal assistant operating mode; gateway pattern. | Interesting for Bricolage’s conversational-agent UX. Needs deeper source inspection. |
| AutoAgent | Runtime; Skills; Memory; Multi-Agent; Learning | Evolving cognition, on-the-fly contextual decision-making, elastic memory orchestration, closed-loop cognitive evolution, reusable episodic abstraction. | Ambitious and potentially complex; must verify implementation availability and practicality. | Elastic memory orchestrator; cognition update loop; peer/tool capability cognition; compression of redundant trajectories. | Important 2026 adaptive-agent direction. Extract memory/cognition concepts if implementation holds up. |
| Nekro Agent | Tooling; Environment Interaction; Skills; Human Interaction | Extensible AI agent framework for multi-user/chat environments; sandboxed execution; plugin architecture; multimodal interaction; Docker deployment. | Custom license/details need review; chat-platform orientation may not match core build. | Chat-platform agent loop; plugin architecture; sandboxed code execution. | Worth scanning as a chat-native agent pattern. |
| SGLang / vLLM class | Models, Context & Inference; Infrastructure | Efficient inference serving; structured generation; high-throughput model runtime patterns; OpenAI-compatible serving surfaces. | Mostly relevant when Bricolage runs its own models or inference layer. | Inference abstraction; structured output constraints; throughput-oriented serving boundary. | Not urgent for ChatGPT/Codex cloud-first use, but important long-term. |
| Orchestral AI | Runtime; Tooling; Models, Context & Inference; Human Interaction | Lightweight Python framework with unified type-safe representation for messages/tools/usage across providers; automatic tool schema generation from Python type hints; synchronous deterministic execution; streaming; context compaction; approvals; sub-agents; memory; MCP. | New project/paper; need repo maturity check. Synchronous simplicity may limit some large-scale async use cases. | Universal message/tool schema; type-hint-to-tool schema generation; deterministic sync execution; provider-normalization layer. | Strong low-friction candidate. Its anti-framework-bloat stance aligns with Bricolage. |
| MiroFlow | Runtime; Cognition; Knowledge & Retrieval; Evaluation | Agent graph for deep research, optional deep reasoning mode, robust reproducible workflow execution, benchmarked across GAIA, BrowseComp, HLE, xBench-DeepSearch, FutureX. | Deep-research specialization; may optimize for benchmark harnesses over general conversational agents. | Deep research graph; robust workflow replay; reasoning-mode toggle; reproducible research baseline. | Important for research-agent capability. Extract deep-research workflow and reproducibility ideas. |
| Orchard | Environment Interaction; Software Engineering Agents; Learning; Evaluation; Infrastructure | Lightweight environment service for reusable sandbox lifecycle management across task domains; agent harnesses; training/evaluation recipes for SWE, GUI, and personal assistant agents; open agentic modeling framework. | Training/RL layer is beyond immediate ChatGPT/Codex use; large research framework. | Harness-agnostic environment layer; sandbox lifecycle service; reusable task domains; agentic data/training/eval separation. | Very important 2026 source for environment/harness architecture. Adopt environment-layer idea, not full training pipeline now. |
| Agent-Diff | Evaluation; Tooling; Environment Interaction; Observability | Evaluates agents on real API tasks using code execution; state-diff contract separates process from outcome; standardized sandbox scripting layer for APIs like Slack, Box, Linear, Google Calendar. | Benchmark/eval framework, not runtime; API-task scope. | Outcome-based state-diff evaluation; real-service API sandbox; task success as expected state change. | Extremely valuable eval primitive without over-testing ceremony. Use state-diff checks for practical tasks. |
| AgentSight | Observability; Safety; Runtime; Infrastructure | Framework-agnostic AgentOps observability using eBPF boundary tracing; correlates high-level LLM intent with low-level system effects; detects prompt injection, loops, and coordination bottlenecks. | Deep systems instrumentation may be too heavy for early cloud-first setup. | Intent/effect correlation; boundary tracing concept; detecting loops and hidden tool effects. | Conceptually powerful. Keep as advanced observability direction, not immediate dependency. |
| GitAgent | Tooling; Skills; Software Engineering Agents; Infrastructure | Autonomous tool extension from GitHub; uses repositories as external tool resources; learns from GitHub Issues/PRs during integration. | Autonomously importing arbitrary repos is risky and noisy. | GitHub-as-tool-marketplace; repo vetting/integration pipeline; issue/PR mining for operational knowledge. | Very aligned with Bricolage research mission. Needs strong license/security vetting. |
| RAGPulse | Knowledge & Retrieval; Infrastructure; Economics & Resource Management | Open RAG workload trace from real deployment; shows temporal locality and skewed hot-document access; supports retrieval caching/content-aware batching research. | Serving optimization dataset, not agent framework. | Hot-document caching; retrieval workload trace design; privacy-preserving RAG telemetry. | Useful when Bricolage gets persistent retrieval at scale. Not core now. |
| U-NIAH | Knowledge & Retrieval; Evaluation; Context | Unified long-context/RAG eval with multi-needle and noise settings; compares RAG and long-context models; identifies RAG error patterns. | Synthetic benchmark; not a runtime. | Retrieval stress tests; lost-in-middle evaluation; noise sensitivity checks. | Good lean eval primitive for memory/retrieval quality. |
| AutoGPT | Runtime; Tooling; Historical Baseline | Early autonomous goal decomposition with tools, browsing, file management; popularized autonomous agents. | Known issues: loops, hallucination, high cost, brittle autonomy. | Negative lessons: avoid unconstrained loops, avoid vague goal autonomy, require outcome checks. | More useful as a cautionary ancestor than a direct source. |

---

# Early Synthesis Signals

## 1. The strongest core primitives so far

- explicit state graph execution
- branchable/replayable trajectories
- sandboxed software execution
- declarative cognitive modules
- MCP-style tool boundaries
- browser automation as a first-class environment
- persistent memory with explicit write/read policies
- multi-agent role/task coordination without role-play bloat
- repo-native state and knowledge
- outcome/state-diff evaluation instead of heavy benchmark bureaucracy
- environment/harness abstraction separated from agent logic
- elastic memory compression and episodic abstraction
- provider-normalized message/tool schema
- intent/effect observability concept

## 2. Bricolage should avoid

- adopting giant frameworks whole
- stacking orchestration frameworks on top of each other
- role-based agent theater without execution value
- creating a DSL before workflow pressure proves it is needed
- over-indexing on eval/governance ceremony before core capability
- custom tool integrations when MCP/open standards already solve the boundary
- unconstrained autonomous loops without state/outcome checks
- autonomous repo/tool ingestion without license/security review

## 3. Bricolage should aggressively adopt/synthesize

- OpenHands-style execution/workspace/sandbox primitives
- DSPy-style declarative reasoning modules where repeatable reasoning matters
- LangGraph/AgentGit-style state graph and branchable trajectory concepts
- MCP as the default tool/data connector boundary
- CrewAI/AutoGen multi-agent ideas only where multiple agents truly add value
- Letta/MemGPT-style explicit memory layers, adapted to repo-native persistence
- browser-use/Playwright-style browser actions for real-world task automation
- Agent-Diff-style state-diff success contracts
- Orchard-style environment/harness layer
- Orchestral-style provider-normalized low-friction tool/message schema
- AutoAgent-style elastic memory only if it remains controllable

---

# Evaluation Lens

Every repository or framework should be evaluated according to:

## 1. Capability Density
How much useful functionality is achieved relative to complexity?

## 2. Architectural Clarity
How understandable and composable is the architecture?

## 3. Operational Friction
How difficult is the system to:
- run
- maintain
- extend
- debug
- reason about

## 4. Modularity
Can useful subsystems be extracted independently?

## 5. Extensibility
Can the architecture evolve cleanly?

## 6. Runtime Simplicity
Does the runtime architecture remain understandable?

## 7. State Management Quality
How coherent and manageable is state?

## 8. Practical Utility
Does the system solve real-world problems effectively?

## 9. Production Viability
Can the architecture realistically support production workloads?

## 10. Innovation Value
Does the project contribute genuinely novel or superior ideas?

## 11. Conversational Leverage
Does it make the ChatGPT/Codex/GitHub cloud workflow more powerful from an iPhone-first operator loop?

---

# Research Source Notes - Passes 1-2

These notes capture the source-grounded basis for the first population passes. They are not exhaustive and should be replaced or expanded with repo-level citations as deeper inspection continues.

- OpenHands SDK paper: composable software-agent SDK, sandboxed execution, local-to-remote portability, REST/WebSocket services, multiple user interfaces, model-agnostic routing, lifecycle control, security analysis, SWE-Bench/GAIA evaluation.
- DSPy paper: declarative modules, LM pipelines as computational graphs, compiler/optimizer, metric-driven improvement, prompt/program abstraction.
- DSPy Assertions paper: computational constraints for self-refining LM pipelines.
- CrewAI public summary: open-source Python multi-agent framework with crews, roles, goals, tasks, delegation, tools, memory, knowledge sources, Flows, MIT license.
- AutoGen Studio paper: declarative JSON specs, no-code multi-agent workflow authoring, debugging/evaluation UI, reusable components.
- AgentSPEX paper: typed workflow specs, branching/loops, explicit state, tools, sandboxing, checkpointing, verification, logging, visual editor.
- AgentGit paper: Git-like commit/revert/branching for multi-agent workflows, trajectory comparison, reduced redundant computation/token usage.
- MCP public sources: open standard for model-tool/data integration, JSON-RPC, broad adoption, Linux Foundation/AAIF direction, reference servers.
- A2A public sources: open protocol for agent communication, discovery, messaging, task coordination, Linux Foundation governance.
- Playwright public sources: mature Apache 2.0 browser automation substrate across Chromium, Firefox, and WebKit.
- AutoAgent paper: evolving cognition, contextual decision-making, elastic memory orchestration, reusable episodic abstractions, closed-loop cognitive evolution.
- Orchestral AI paper: lightweight provider-normalized agent framework with type-safe message/tool representations and deterministic sync execution.
- MiroFlow paper: agent graph, optional deep reasoning, robust reproducible deep-research workflows, broad benchmark coverage.
- Orchard paper: lightweight environment service, sandbox lifecycle management, harness-agnostic environment primitives, SWE/GUI/personal-assistant recipes.
- Agent-Diff paper: state-diff evaluation contracts for real-world API tasks via sandboxed code execution.
- AgentSight paper: framework-agnostic observability by correlating LLM intent and system effects through boundary tracing.
- GitAgent paper: autonomous GitHub repository integration as tool extension, including learning from Issues/PRs.
- RAGPulse paper: real-world RAG workload trace showing temporal locality and hot-document skew.
- U-NIAH paper: unified RAG/long-context evaluation for multi-needle/noisy retrieval settings.
- AutoGPT public summary: historically important autonomous agent, but useful mainly as cautionary evidence for loop/cost/hallucination failure modes.

---

# Current Philosophy

The project should remain:

- ambitious
- synthesis-first
- conversational-agent-first
- cloud-native through ChatGPT + Codex + GitHub
- architecture-focused
- implementation-aware
- minimally bureaucratic

The repository structure itself should emerge naturally from:

- repeated architectural patterns
- implementation pressure
- synthesis discoveries
- operational requirements

rather than from premature formalization.
