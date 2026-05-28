# Canonical Agent Taxonomy v1

## Purpose

This document defines the canonical top-level ontology for the Bricolage project.

Bricolage is not intended to be merely another agent framework. It is intended to become:

- a synthesis architecture
- a research codification project
- a canonical agent systems ontology
- an interoperability layer
- a reference implementation
- an agent operating system architecture

The purpose of this taxonomy is to:

1. Create a unified vocabulary for agentic systems.
2. Decompose modern agent architectures into canonical domains.
3. Enable comparative analysis of open-source agent repositories.
4. Prevent framework lock-in.
5. Support synthesis of best-in-class architectural primitives.
6. Serve as the foundation for engineering specifications and implementation.

---

# Taxonomy Principles

The taxonomy is designed to be:

- architecture-first
- implementation-agnostic
- extensible
- synthesis-oriented
- research-compatible
- production-compatible
- future-compatible

The top-level categories represent foundational architectural domains.

Subcategories, repositories, frameworks, standards, protocols, and implementations will be mapped beneath these domains.

---

# The Canonical 15 Top-Level Categories

## 1. Runtime & Orchestration

### Core Question
How does the system execute?

### Includes
- execution loops
- workflow orchestration
- graph execution
- schedulers
- event systems
- concurrency
- async execution
- distributed execution
- state transitions
- task queues

### Example Systems
- LangGraph
- Temporal
- Prefect
- Ray

---

## 2. Cognition & Reasoning

### Core Question
How does the system think?

### Includes
- planning
- decomposition
- reflection
- self-critique
- search strategies
- replanning
- uncertainty handling
- world models
- deliberate reasoning
- reasoning trees

### Example Systems
- ReAct
- Reflexion
- Tree of Thoughts
- DSPy reasoning patterns

---

## 3. Memory Systems

### Core Question
How does the system remember?

### Includes
- short-term memory
- long-term memory
- episodic memory
- semantic memory
- procedural memory
- vector memory
- graph memory
- memory compression
- forgetting systems
- retrieval memory

### Example Systems
- MemGPT
- Letta
- Zep

---

## 4. Knowledge & Retrieval

### Core Question
How does the system access knowledge?

### Includes
- RAG systems
- embeddings
- indexing
- reranking
- GraphRAG
- retrieval orchestration
- chunking
- document understanding
- semantic search
- retrieval pipelines

### Example Systems
- LlamaIndex
- Haystack
- GraphRAG architectures

---

## 5. Tooling & Action Systems

### Core Question
How does the system take action?

### Includes
- tool calling
- MCP integration
- API execution
- shell execution
- browser automation
- desktop automation
- action validation
- tool registries
- permission gates
- execution abstractions

### Example Systems
- MCP ecosystems
- browser-use
- OpenHands tooling

---

## 6. Multi-Agent Coordination

### Core Question
How do multiple agents collaborate?

### Includes
- delegation
- role systems
- swarms
- hierarchies
- messaging
- consensus
- negotiation
- distributed cognition
- shared memory
- coordination protocols

### Example Systems
- CrewAI
- AutoGen
- CAMEL
- A2A systems

---

## 7. Skills & Capability Composition

### Core Question
How are reusable abilities represented?

### Includes
- skills
- plugins
- capability graphs
- workflow templates
- reusable procedures
- dynamic loading
- modular capabilities
- task abstractions
- capability registries

### Example Systems
- plugin architectures
- reusable workflow systems
- skill registries

---

## 8. Environment Interaction

### Core Question
What environments can the system operate within?

### Includes
- browsers
- desktops
- terminals
- filesystems
- containers
- cloud systems
- robotics abstractions
- virtual machines
- simulated environments

### Example Systems
- OpenHands
- browser agents
- computer-use systems

---

## 9. Software Engineering Agents

### Core Question
How does the system perform software engineering tasks?

### Includes
- repository understanding
- patch generation
- debugging
- testing
- verification
- CI/CD integration
- code execution
- autonomous coding loops
- SWE benchmarks

### Example Systems
- SWE-agent
- OpenHands
- Devin-style architectures

---

## 10. Human Interaction & Collaboration

### Core Question
How do humans interact with and control the system?

### Includes
- conversational UX
- interruptibility
- approvals
- explainability
- multimodal interfaces
- collaborative editing
- visualization
- notifications
- human-in-the-loop systems

### Example Systems
- copilots
- IDE assistants
- collaborative AI systems

---

## 11. Observability & Evaluation

### Core Question
How do we understand and measure the system?

### Includes
- tracing
- telemetry
- replay
- debugging
- eval harnesses
- regression testing
- trajectory analysis
- metrics
- verification systems
- benchmarks

### Example Systems
- LangSmith
- OpenTelemetry
- SWE-bench
- GAIA

---

## 12. Safety, Governance & Security

### Core Question
How do we keep the system safe and controllable?

### Includes
- sandboxing
- permissions
- policy engines
- constitutional systems
- approvals
- audit trails
- governance models
- security boundaries
- risk mitigation

### Example Systems
- guardrail systems
- container isolation
- approval workflows

---

## 13. Learning & Adaptation

### Core Question
How does the system improve over time?

### Includes
- self-improvement
- reinforcement learning
- finetuning
- trajectory learning
- preference learning
- adaptive memory
- optimization loops
- continual learning

### Example Systems
- RL systems
- adaptive agents
- self-reflective architectures

---

## 14. Models, Context & Inference

### Core Question
How are models and context managed?

### Includes
- model routing
- provider abstraction
- prompt architecture
- context assembly
- summarization
- token budgeting
- ensembles
- inference optimization
- speculative execution
- context compression

### Example Systems
- LiteLLM
- vLLM
- DSPy
- routing systems

---

## 15. Infrastructure, Protocols & State Architecture

### Core Question
What foundational systems support the architecture?

### Includes
- persistence
- queues
- distributed systems
- deployment
- Kubernetes
- event sourcing
- schemas
- MCP
- A2A
- OpenAPI
- internal state models
- caching
- resource management
- cost controls

### Example Systems
- Kubernetes
- Redis
- MCP ecosystems
- event-driven architectures

---

# Intended Next Steps

The next phase of the Bricolage project is:

1. Define subcategories beneath each top-level category.
2. Identify major open-source repositories relevant to each category.
3. Map architectural primitives to categories.
4. Build comparative matrices.
5. Identify state-of-the-art implementations.
6. Synthesize unified architectural patterns.
7. Produce canonical engineering specifications.
8. Implement a modular reference architecture.

---

# Project Direction

Bricolage is intended to become:

- a canonical synthesis architecture for agent systems
- a modular reference implementation
- an interoperability-oriented runtime architecture
- a codified body of agent systems engineering knowledge
- a continuously evolving research synthesis project

This taxonomy is the foundation of the entire project.
