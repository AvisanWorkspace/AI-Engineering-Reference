# AVISAN AI Engineering Reference Library

> **Purpose:** A reusable, project-independent technical reference for
> researching, selecting, integrating, and operating AI engineering
> tools across current and future AVISAN projects.

**Status:** Living reference\
**Owner:** AVISAN\
**Last consolidated:** 27 November 2026\
**Primary use:** Project discovery, architecture, implementation,
testing, deployment, and engineering workflow design

------------------------------------------------------------------------

## 1. Why this repository exists

AVISAN projects should not begin from a blank page every time. This
library consolidates reusable open-source repositories, agent
definitions, skills, SDKs, frameworks, and engineering practices into
one reference point.

It is intended to help us:

-   Find an existing implementation before building a new one.
-   Reuse proven patterns while retaining control of product
    architecture.
-   Assemble specialist AI-assisted engineering workflows.
-   Compare frameworks without committing prematurely to one vendor or
    stack.
-   Build repeatable project foundations, checklists, and delivery
    practices.
-   Keep a record of what was evaluated, adopted, modified, rejected,
    and why.

This is a **reference catalogue and decision aid**, not a mandate to use
every listed tool. A repository being popular, open source, or published
by a respected team does not automatically make it suitable for
production.

## 2. Guiding principles

1.  **Problem first, framework second.** Define the user problem,
    constraints, and success criteria before selecting an agent
    framework or model.
2.  **Reuse before reinventing.** Search this library and upstream
    repositories before implementing common capabilities.
3.  **Small, testable components.** Prefer modular skills, tools,
    services, and agents with explicit inputs and outputs.
4.  **Human approval for consequential actions.** Require approval for
    financial transactions, production changes, device control, data
    deletion, external communications, and other high-impact operations.
5.  **Evidence over confidence.** Agents must cite files, tests, logs,
    measurements, or source material for important claims.
6.  **Security by design.** Treat prompts, retrieved documents, tool
    outputs, plugins, and external repositories as untrusted inputs.
7.  **Portable architecture.** Avoid coupling core business logic to one
    model provider or coding assistant.
8.  **Evaluate continuously.** Use tests, benchmarks, traces, cost
    measurements, and failure analysis.
9.  **Document decisions.** Record why a tool was selected, its version,
    limitations, and replacement path.
10. **Build only the differentiator.** Use commodity tools for commodity
    capabilities; invest custom engineering in the product's unique
    value.

## 3. Reference library map

The resources currently consolidated fall into three complementary
collections.

  -----------------------------------------------------------------------
  Collection              What it contributes     Typical use
  ----------------------- ----------------------- -----------------------
  Anthropic repositories  Agent skills, Claude    Learn patterns and
                          Code, plugins, SDKs,    build Claude-based
                          tutorials, quickstarts  workflows

  Agency Agents and       Specialist role         Create a virtual
  Claude Code playbooks   definitions, skills,    engineering/product
                          MCP integrations,       team
                          orchestration and       
                          workflow ideas          

  50+ GitHub repository   Infrastructure, local   Compare implementation
  collection              models, agent           options across the AI
                          frameworks, RAG,        stack
                          memory, automation and  
                          developer tools         
  -----------------------------------------------------------------------

These collections overlap. Keep one canonical entry per repository in
the project inventory and use tags to connect it to multiple categories.

## 4. Anthropic ecosystem

The following repositories were explicitly included in the initial
Anthropic reference collection. Verify each repository's current status,
README, license, dependencies, and maintenance activity before adoption.

  --------------------------------------------------------------------------------------------------------------------------------------------------
  Repository                                                                                         What to investigate     AVISAN application
  -------------------------------------------------------------------------------------------------- ----------------------- -----------------------
  [claude-code-playground](https://github.com/anthropics/claude-code-playground)                     Real Claude Code        Reference
                                                                                                     setups, hooks,          configurations and
                                                                                                     settings, workflows,    developer workflow
                                                                                                     skills and demos        experiments

  [skills](https://github.com/anthropics/skills)                                                     Agent Skills format and Standardize repeatable
                                                                                                     reusable task           engineering and
                                                                                                     instructions            operational tasks

  [claude-plugins-official](https://github.com/anthropics/claude-plugins-official)                   Anthropic-managed       Evaluate integrations
                                                                                                     Claude Code plugins     and packaged workflows

  [launch-your-agent](https://github.com/anthropics/launch-your-agent)                               Agent launch/build      Explore agent
                                                                                                     examples; verify        application patterns
                                                                                                     current repository      
                                                                                                     scope                   

  [knowledge-work-plugins](https://github.com/anthropics/knowledge-work-plugins)                     Plugins for             Research, documentation
                                                                                                     knowledge-work tasks    and business workflows

  [claude-quickstarts](https://github.com/anthropics/claude-quickstarts)                             Starter projects for    Prototype API-backed
                                                                                                     deployable Claude API   applications
                                                                                                     applications            

  [prompt-eng-interactive-tutorial](https://github.com/anthropics/prompt-eng-interactive-tutorial)   Interactive             Improve prompt design
                                                                                                     prompt-engineering      and evaluation
                                                                                                     lessons                 discipline
  --------------------------------------------------------------------------------------------------------------------------------------------------

### Additional official repositories worth tracking

These were identified as useful adjacent references during
consolidation:

-   [claude-code](https://github.com/anthropics/claude-code) --- Claude
    Code agentic coding tool and its implementation.
-   [claude-agent-sdk-python](https://github.com/anthropics/claude-agent-sdk-python)
    --- Python SDK for building applications with Claude Code agent
    capabilities.
-   [claude-agent-sdk-demos](https://github.com/anthropics/claude-agent-sdk-demos)
    --- SDK demonstration applications; confirm current availability.
-   [claude-cookbooks](https://github.com/anthropics/claude-cookbooks)
    --- API examples, notebooks and implementation recipes.
-   [claude-code-action](https://github.com/anthropics/claude-code-action)
    --- Claude Code workflows for GitHub Actions.
-   [claude-code-security-review](https://github.com/anthropics/claude-code-security-review)
    --- AI-assisted security review of code changes.
-   [sandbox-runtime](https://github.com/anthropics/sandbox-runtime) ---
    Process sandboxing and filesystem/network restriction patterns.

**Important distinction:** Anthropic's `claude-code-playground`
describes itself as a DevRel playground, not an official product or a
universal best-practice standard. Treat examples as experiments to
inspect and validate, not production-ready templates. Plugin
installation also requires trust and security review.

## 5. Specialist agents: Agency Agents

Primary reference:
[msitarzewski/agency-agents](https://github.com/msitarzewski/agency-agents)

This collection provides specialist agent definitions with a role,
mission, workflow, deliverables, and communication style. It can be used
as a source of role templates for an AI-assisted team.

### Relevant specialist roles for AVISAN

  -----------------------------------------------------------------------
  Role                                Where it can help
  ----------------------------------- -----------------------------------
  Embedded Firmware Engineer          MCU firmware, RTOS,
                                      ESP32/STM32/Nordic development

  Backend Architect                   APIs, databases, service boundaries
                                      and scalability

  AI Engineer                         Model integration, inference, data
                                      pipelines and AI features

  Multi-Agent Systems Architect /     Agent boundaries, delegation,
  Agents Orchestrator                 coordination and recovery

  RAG Pipeline Engineer               Ingestion, chunking, retrieval,
                                      reranking and evaluation

  Security Engineer / Privacy         Threat modelling, secure
  Engineer                            implementation and data handling

  DevOps Automator                    CI/CD, deployment, infrastructure
                                      and monitoring

  Test Results Analyzer / Performance Test interpretation, performance
  Benchmarker                         measurement and regression analysis

  Reality Checker / Evidence          Evidence-based verification and
  Collector                           release gates

  Technical Writer                    Architecture records, API docs,
                                      user and maintenance documentation

  Product / Sprint Prioritizer        Scope, backlog, prioritization and
                                      delivery planning

  Trend Researcher / Feedback         Market research, customer feedback
  Synthesizer                         and product discovery
  -----------------------------------------------------------------------

### How to use an agent definition

1.  Read the full agent file and inspect its assumptions.
2.  Extract the useful role, workflow, output format, and quality
    criteria.
3.  Remove irrelevant personality language and tool-specific
    assumptions.
4.  Add AVISAN product context, approved tools, security constraints,
    and engineering standards.
5.  Define what the agent may read, write, execute, and approve.
6.  Add testable acceptance criteria and examples of good output.
7.  Run it on a bounded task and review results before wider use.

Do not treat an agent persona as a substitute for engineering
competence, code review, or domain validation. A role description is a
starting point, not proof that the agent's output is correct.

## 6. Claude Code skills, plugins, MCP and workflow playbooks

The consolidated Claude Code playbook contains references across these
areas:

-   **Skills:** Reusable instructions and procedures for repeatable
    tasks.
-   **Plugins:** Packaged extensions and integrations.
-   **MCP:** A protocol and integration pattern for exposing tools and
    context to AI applications.
-   **Orchestration:** Delegation, sequencing, routing, and coordination
    across agents.
-   **Memory and knowledge:** Project context, persistent knowledge,
    retrieval, and context management.
-   **Development and verification:** Coding, testing, review,
    documentation, and quality gates.
-   **Creative and operational workflows:** Design, documents,
    marketing, media, and automation.

A separate 25-skill collection covered design/video, documents/writing,
marketing, development, and testing/verification. The 33-repository
Claude Code playbook overlaps with the Anthropic collection and should
be deduplicated during detailed inventory work.

### Skill design template

Every AVISAN skill should document:

-   Name and purpose
-   When to invoke it and when not to
-   Required inputs and context
-   Procedure, preferably as explicit steps
-   Tools and permissions required
-   Expected output format
-   Validation and acceptance criteria
-   Failure handling and escalation
-   Security and data-handling notes
-   Example invocation and example output
-   Version, owner, and last-reviewed date

## 7. Broader AI engineering repository catalogue

The 50-repository collection is a broad technology discovery list. The
following named projects were present in the supplied material. This is
a **category index, not a claim that every repository has been fully
audited**.

  ------------------------------------------------------------------------------------------------------------
  Area                    Repositories / projects                                      What to evaluate
  ----------------------- ------------------------------------------------------------ -----------------------
  Local LLMs and          [Ollama](https://github.com/ollama/ollama),                  Local deployment, model
  inference               [llama.cpp](https://github.com/ggml-org/llama.cpp),          compatibility,
                          [vLLM](https://github.com/vllm-project/vllm)                 throughput, memory and
                                                                                       hardware needs

  Model ecosystem         [Hugging Face                                                Model loading,
                          Transformers](https://github.com/huggingface/transformers)   fine-tuning ecosystem,
                                                                                       inference interfaces
                                                                                       and supported
                                                                                       architectures

  Agent frameworks        [LangChain](https://github.com/langchain-ai/langchain),      Tool calling, agent
                          [AutoGen](https://github.com/microsoft/autogen)              execution, state,
                                                                                       orchestration and
                                                                                       observability

  RAG and knowledge       [RAGFlow](https://github.com/infiniflow/ragflow),            Document ingestion,
  systems                 [LlamaIndex](https://github.com/run-llama/llama_index)       parsing, indexing,
                                                                                       retrieval and answer
                                                                                       evaluation

  Memory                  [Mem0](https://github.com/mem0ai/mem0)                       User/project memory,
                                                                                       retrieval, lifecycle
                                                                                       and data governance

  Workflow automation     [n8n](https://github.com/n8n-io/n8n)                         Event-driven workflows,
                                                                                       connectors, retries and
                                                                                       human approval

  AI application          [Dify](https://github.com/langgenius/dify), [Lobe            Application
  platforms               Chat](https://github.com/lobehub/lobe-chat)                  scaffolding, model
                                                                                       access, workflow UI and
                                                                                       deployment

  Browser and web         [Browser Use](https://github.com/browser-use/browser-use),   Browser interaction,
  automation              [Firecrawl](https://github.com/firecrawl/firecrawl)          web extraction,
                                                                                       reliability and access
                                                                                       controls

  Creative workflows      [ComfyUI](https://github.com/comfyanonymous/ComfyUI)         Node-based generative
                                                                                       media workflows and
                                                                                       model execution
  ------------------------------------------------------------------------------------------------------------

The original list also contained repeated entries (including duplicates
among items 48--50) and some abbreviated or truncated URLs. Do not infer
missing repository paths from partial text. Restore and verify those
entries from the original source before treating the catalogue as
complete.

## 7A. Learning curriculum: Microsoft Generative AI for Beginners

**Repository:** [microsoft/generative-ai-for-beginners](https://github.com/microsoft/generative-ai-for-beginners)  
**Publisher:** Microsoft Cloud Advocates  
**Current course designation:** Version 3  
**Format:** 21 lessons with concept explanations and practical build exercises  
**License shown by GitHub:** MIT (verify the license file and notices before redistributing course material or code)  
**Reference checked:** 27 November 2026

### Why this belongs in the AVISAN library

This is a structured learning and implementation curriculum for building generative AI applications. It complements, rather than duplicates, the other collections:

- **Anthropic repositories** help us work with coding agents, skills, SDKs and developer workflows.
- **Agency Agents** provides role definitions and reusable specialist-agent patterns.
- **Microsoft Generative AI for Beginners** teaches the application-level building blocks: model selection, prompting, chat, search, embeddings, function calling, security, RAG, agents, fine-tuning and small language models.

Use it as a learning path and source of small proof-of-concept exercises. Do not treat the sample application architecture or provider-specific setup as an automatic production architecture for AVISAN.

### Curriculum map

| Lesson | Subject | AVISAN application |
|---:|---|---|
| 00 | Course setup | Establish a reproducible AI development environment |
| 01 | Generative AI and LLM fundamentals | Understand model behaviour and limitations |
| 02 | Comparing LLMs | Select models by quality, latency, cost, privacy and deployment constraints |
| 03 | Responsible AI | Define safe and responsible product behaviour |
| 04 | Prompt engineering fundamentals | Build clear, testable prompts |
| 05 | Advanced prompting | Improve structured outputs and multi-step tasks |
| 06 | Text generation applications | Prototype summarization, explanation and report generation |
| 07 | Chat applications | Build conversational interfaces |
| 08 | Search applications and vector databases | Explore semantic search and embeddings |
| 09 | Image generation applications | Evaluate image-generation workflows where relevant |
| 10 | Low-code AI applications | Prototype workflows quickly |
| 11 | Function calling and external applications | Connect models to approved APIs and tools |
| 12 | UX for AI applications | Design human review, uncertainty and feedback into interfaces |
| 13 | AI application security | Threat-model prompts, tools, data and model interactions |
| 14 | Generative AI application lifecycle | Introduce evaluation, monitoring and lifecycle practices |
| 15 | RAG and vector databases | Search manuals, maintenance records and engineering documents |
| 16 | Open-source models and Hugging Face | Evaluate self-hosted and open-weight model options |
| 17 | AI agents | Build bounded tool-using agent prototypes |
| 18 | Fine-tuning LLMs | Understand when fine-tuning is justified |
| 19 | Small language models (SLMs) | Explore compact models for constrained deployments |
| 20 | Mistral models | Compare a model family and its capabilities |
| 21 | Meta models | Compare another model family and its capabilities |

The course README describes lessons as either **Learn** (conceptual) or **Build** (hands-on), with Python and TypeScript examples where available. It lists OpenAI API, Azure OpenAI, Microsoft Foundry Models and Foundry Local as ways to work through the material. Provider availability and setup instructions can change, so follow the current upstream lesson rather than copying old environment instructions.

### Recommended AVISAN learning order

Do not necessarily complete every lesson linearly. For a practical embedded/industrial AI pathway, prioritize:

1. **Lessons 01–05:** Build a solid understanding of LLMs, model selection, responsible AI and prompting.
2. **Lessons 06–08:** Build a simple text/chat application and semantic search prototype.
3. **Lesson 11:** Learn function calling—the bridge between a language model and controlled application capabilities.
4. **Lessons 13–14:** Study security, evaluation and the application lifecycle before production integration.
5. **Lesson 15:** Build a RAG prototype over a small collection of equipment manuals or service documents.
6. **Lessons 16–17:** Compare open models and build a bounded agent.
7. **Lessons 18–21:** Explore fine-tuning, SLMs and model families only when a concrete use case justifies them.

### Suggested hands-on exercises

| Exercise | Build | What it teaches |
|---|---|---|
| 1. Equipment manual assistant | Ask questions over a few public/manual test documents and show source passages | Embeddings, retrieval, grounding and RAG evaluation |
| 2. Machine alarm explainer | Convert a synthetic fault code and telemetry snapshot into a structured explanation | Prompting, schemas and uncertainty handling |
| 3. Maintenance report generator | Summarize synthetic service events into a technician report | Text generation and structured outputs |
| 4. Read-only machine-data tool | Let a model call a mock API that reads simulated sensor values | Function calling, tool validation and authorization |
| 5. Operator support agent | Combine retrieval and a small set of read-only tools with explicit escalation | Agent boundaries and human-in-the-loop design |
| 6. Edge model comparison | Compare a small local model with a hosted model on the same test set | Latency, memory, quality, cost and offline trade-offs |

Use synthetic or public data for these exercises. Do not connect early prototypes to live machine controls, production networks, customer information or trading execution.

### Technical and operational caveats

- The course is educational; sample code needs review, testing and adaptation before production use.
- Model APIs, SDKs, deployment products and lesson setup instructions evolve. Pin versions in experiments and verify current upstream documentation.
- The README notes that GitHub Models was retired at the end of July 2026 and directs learners to Microsoft Foundry Models for the relevant course path. Do not use old GitHub Models setup instructions without checking the current lesson.
- Foundry Local is presented as an offline local-model option; actual feasibility depends on model size, hardware, runtime support and measured performance.
- A successful demo is not evidence of production reliability. Add tests for hallucination, retrieval quality, prompt injection, access control, latency, cost and failure recovery.

### Adoption classification

**REFERENCE / LEARNING PATH** — recommended for engineering learning and POCs. Individual code samples may later be adopted or adapted after license, dependency, security and quality review.

**Upstream:** [Microsoft Generative AI for Beginners](https://github.com/microsoft/generative-ai-for-beginners)  
**Related .NET edition:** [Generative AI for Beginners – .NET](https://github.com/microsoft/Generative-AI-for-beginners-dotnet)

---

## 8. How to select tools for a project

Use this sequence for every new AVISAN initiative.

### Step 1 --- Define the problem

Write a one-page problem brief:

-   Who is the user?
-   What problem are we solving?
-   What happens today without the product?
-   What is the measurable outcome?
-   What are the latency, reliability, privacy, offline, and cost
    constraints?
-   Does the product need AI at all?

### Step 2 --- Identify the capability

Break the product into capabilities, for example:

-   Edge sensing and device connectivity
-   Data ingestion and event processing
-   Rules and workflow automation
-   Search and knowledge retrieval
-   AI reasoning and tool use
-   User interface and notifications
-   Identity, permissions and audit
-   Testing, deployment and observability

### Step 3 --- Search this library

For each capability, record at least one candidate and compare it with a
simpler non-AI or custom implementation.

### Step 4 --- Run a small proof of concept

A POC should answer one important uncertainty. Define:

-   Hypothesis
-   Dataset or test fixture
-   Baseline
-   Evaluation metric
-   Hardware and deployment environment
-   Cost and latency budget
-   Failure cases
-   Exit criteria

### Step 5 --- Make an adoption decision

Use one of these labels:

-   **ADOPT:** Meets requirements and is acceptable for the intended
    environment.
-   **ADAPT:** Useful foundation, but needs meaningful AVISAN changes.
-   **REFERENCE:** Learn from the design; do not depend on the code.
-   **POC:** Worth testing; not approved for production.
-   **REJECT:** Does not meet requirements; record why.
-   **REVISIT:** Not suitable now, but may become relevant later.

### Step 6 --- Record the decision

Create an Architecture Decision Record (ADR) for consequential choices.
Include alternatives, trade-offs, security implications, operational
costs, and a revisit trigger.

## 9. Reuse, adapt, or build from scratch

  -----------------------------------------------------------------------
  Situation                           Preferred approach
  ----------------------------------- -----------------------------------
  Common developer workflow or        Reuse a skill or agent template
  documentation task                  

  Standard integration or connector   Evaluate an existing plugin, MCP
                                      server or SDK

  Generic orchestration or RAG        Benchmark established frameworks
  capability                          against a minimal baseline

  Product-specific domain logic       Build and own the core logic

  Safety-critical device behaviour    Keep deterministic local control;
                                      use AI only within bounded,
                                      supervised responsibilities

  Unique hardware protocol or device  Build a tested adapter around the
  abstraction                         protocol

  Authentication, authorization,      Use proven components and
  audit and data retention            explicitly validate security

  Unproven AI capability              Prototype behind an interface;
                                      avoid hard-wiring it into the
                                      product
  -----------------------------------------------------------------------

## 10. AVISAN project application map

These are possible reference paths, not pre-approved architectures.

### Industrial intelligence and connected machines

For products such as AviSan Pulse / AIIE:

-   Embedded Agents: firmware development, protocol analysis, test
    generation and troubleshooting.
-   Skills and playbooks: code review, release notes, test reports and
    commissioning procedures.
-   Workflow automation: alerts, maintenance workflows and escalation.
-   RAG: manuals, service history, fault codes and troubleshooting
    knowledge.
-   Local inference: investigate where offline or low-latency inference
    is valuable.
-   Security: device identity, least privilege, signed updates, network
    segmentation and audit trails.

### Water distribution and building automation

For AviSan WaterIQ:

-   Use deterministic algorithms for allocation, schedules, limits and
    fail-safe operation.
-   Use analytics/ML for demand forecasts and anomaly detection only
    after collecting representative data.
-   Use agents to assist operators with explanations, reports and
    maintenance workflows.
-   Require human approval for consequential control changes until
    safety and reliability are demonstrated.
-   Preserve manual override, safe fallback, event logs and explainable
    decisions.

### Developer productivity and internal engineering

-   Use specialist agents for bounded tasks such as embedded code
    review, test analysis, documentation and architecture critique.
-   Use skills to standardize repeatable procedures.
-   Use CI and deterministic tests as the authority for build and
    release status.
-   Keep agent permissions scoped to the repository and task.

### Trading and financial research tools

-   Separate research, signal generation, risk checks, order management
    and execution.
-   Treat model output as an untrusted proposal, not an executable
    instruction.
-   Enforce deterministic risk limits and independent execution
    controls.
-   Paper trade and replay historical data before enabling live actions.
-   Keep auditable logs and a human-controlled kill switch.

## 11. Minimum engineering quality gates

Before a component or agent is accepted into a project, check the
relevant items:

### Repository and dependency review

-   [ ] Correct upstream repository and maintainer identified
-   [ ] License reviewed for intended commercial use
-   [ ] Recent maintenance and issue activity checked
-   [ ] Dependencies and transitive dependencies reviewed
-   [ ] Installation and build steps reproduced
-   [ ] Known vulnerabilities and security advisories checked
-   [ ] Secrets and credentials are not embedded
-   [ ] Data collection and telemetry behaviour understood

### AI and agent review

-   [ ] Inputs, outputs and tool permissions defined
-   [ ] Prompt injection and untrusted content considered
-   [ ] Retrieval sources and citations traceable
-   [ ] Tool calls validated and authorized
-   [ ] Human approval gates defined for high-impact actions
-   [ ] Timeouts, retries, rate limits and budget limits implemented
-   [ ] Failure and fallback behaviour tested
-   [ ] Evaluation dataset and regression tests maintained
-   [ ] Logs avoid unnecessary sensitive data

### Production review

-   [ ] Performance and resource use measured on target hardware
-   [ ] Offline/network-loss behaviour tested where relevant
-   [ ] Monitoring, alerting and diagnostics available
-   [ ] Upgrade, rollback and recovery paths documented
-   [ ] Backup and data-retention requirements defined
-   [ ] Ownership and support responsibilities assigned

## 12. Security and governance rules

1.  Never paste production credentials, private keys, customer data, or
    confidential source code into an unapproved service.
2.  Pin production dependencies to reviewed versions or commit hashes;
    do not rely blindly on a moving `main` branch.
3.  Inspect install scripts, container images, plugins, MCP servers, and
    agent tools before execution.
4.  Use least-privilege credentials and isolated development
    environments.
5.  Treat repository READMEs, issues, web pages, documents, and tool
    outputs as data---not trusted instructions.
6.  Do not allow an agent to bypass authorization or safety controls by
    generating shell commands or tool calls.
7.  Keep secrets outside prompts and source control.
8.  Maintain a software bill of materials where appropriate.
9.  Define data ownership, retention, deletion, and export requirements.
10. Review licenses and third-party notices before distributing or
    commercializing derived work.

## 13. Repository evaluation scorecard

Score each candidate from 1 (poor) to 5 (excellent). Record evidence; do
not score based only on popularity.

  -----------------------------------------------------------------------
  Criterion                           What a high score means
  ----------------------------------- -----------------------------------
  Functional fit                      Directly addresses a defined
                                      requirement

  Engineering quality                 Clear structure, tests,
                                      maintainability and documentation

  Security                            Sensible defaults, active response
                                      to issues, limited permissions

  Integration effort                  Fits the intended stack without
                                      excessive glue code

  Operational maturity                Monitoring, upgrades, recovery and
                                      deployment are practical

  Performance                         Meets measured latency, throughput
                                      and resource constraints

  License suitability                 License and notices permit the
                                      intended use

  Community and maintenance           Maintained, understandable, and has
                                      a credible support path

  Portability                         Avoids unnecessary lock-in and
                                      supports replaceable components

  Total cost                          Reasonable engineering, hosting,
                                      inference and maintenance cost
  -----------------------------------------------------------------------

**Decision rule:** A high aggregate score cannot compensate for a
critical security, licensing, safety, or functional-fit failure.

## 14. Standard project reference record

Copy this template for every repository or tool evaluated.

``` yaml
name: ""
category: ""
upstream_url: ""
maintainer: ""
license: "Unverified"
last_checked: "YYYY-MM-DD"
version_or_commit: ""
status: "POC" # ADOPT | ADAPT | REFERENCE | POC | REJECT | REVISIT

purpose: ""
capabilities: []
use_cases: []
not_suitable_for: []

language_and_runtime: []
dependencies: []
deployment_options: []
hardware_requirements: []

integration:
  interfaces: []
  data_inputs: []
  data_outputs: []
  authentication: ""
  permissions_required: []

evaluation:
  functional_fit: null
  engineering_quality: null
  security: null
  integration_effort: null
  operational_maturity: null
  performance: null
  license_suitability: null
  portability: null
  total_cost: null

poc:
  hypothesis: ""
  success_criteria: []
  test_environment: ""
  results: ""

decision:
  outcome: ""
  rationale: ""
  risks: []
  alternatives: []
  owner: ""
  revisit_when: ""
```

## 15. Standard project kickoff checklist

For every new project:

-   [ ] Write problem brief and measurable success criteria.
-   [ ] Identify hardware, software, data, connectivity and regulatory
    constraints.
-   [ ] Search this reference library for relevant capabilities.
-   [ ] Check whether an existing AVISAN component can be reused.
-   [ ] Compare reuse, adaptation and custom-build options.
-   [ ] Verify repository identity, license, maintenance and security.
-   [ ] Create a small POC for major technical uncertainties.
-   [ ] Define system boundaries and replaceable interfaces.
-   [ ] Define agent roles and permissions only where agents add value.
-   [ ] Establish tests, observability, deployment and rollback
    requirements.
-   [ ] Record architecture decisions and rejected alternatives.
-   [ ] Update this reference library with findings.

## 16. Suggested folder structure for the AVISAN reference repository

``` text
avisan-ai-engineering-reference/
├── README.md
├── catalog/
│   ├── anthropic-ecosystem.md
│   ├── agent-frameworks.md
│   ├── skills-and-plugins.md
│   ├── mcp-and-integrations.md
│   ├── rag-and-memory.md
│   ├── local-llm-and-inference.md
│   ├── automation-and-orchestration.md
│   ├── browser-and-data-tools.md
│   └── embedded-and-edge-ai.md
├── playbooks/
│   ├── project-kickoff.md
│   ├── repository-evaluation.md
│   ├── agent-design.md
│   ├── rag-evaluation.md
│   └── production-readiness.md
├── templates/
│   ├── repository-record.yaml
│   ├── agent-skill-template.md
│   ├── proof-of-concept.md
│   └── architecture-decision-record.md
└── projects/
    ├── avisan-pulse/
    ├── avisan-wateriq/
    └── future-projects/
```

Rename folder examples to remove spaces if creating them on disk; the
structure is illustrative.

## 17. Maintenance process

Review the library monthly or whenever a project makes a meaningful
technology decision.

For each entry:

-   Confirm the upstream URL still resolves.
-   Check releases, maintenance activity, license and security notices.
-   Record the exact version or commit evaluated.
-   Update adoption status and project references.
-   Mark archived, superseded or unmaintained tools.
-   Preserve the reason for previous decisions so the same evaluation is
    not repeated without cause.

Do not automatically upgrade production dependencies because a
repository has a new release.

## 18. Known gaps in this consolidation

This README combines the source collections and named repositories that
were identifiable in the conversation. It is not yet a verified,
exhaustive inventory of every item in the 33-repository playbook or the
50-repository list.

The source material included some shortened or truncated GitHub URLs and
duplicate entries. Those should be recovered from the original posts
before adding them as canonical links. In particular:

-   Do not guess a repository URL from an abbreviated link.
-   Do not count duplicate repositories as separate tools.
-   Do not assume a repository is maintained or production-ready based
    on its inclusion in a curated list.
-   Recheck all current capabilities, licenses, versions and
    compatibility when a project actually needs the tool.

## 19. Useful upstream links

### Anthropic

-   [Anthropic GitHub organization](https://github.com/anthropics)
-   [Claude Code](https://github.com/anthropics/claude-code)
-   [Agent Skills](https://github.com/anthropics/skills)
-   [Claude Code
    Playground](https://github.com/anthropics/claude-code-playground)
-   [Official Claude
    plugins](https://github.com/anthropics/claude-plugins-official)
-   [Claude
    Quickstarts](https://github.com/anthropics/claude-quickstarts)
-   [Claude Cookbooks](https://github.com/anthropics/claude-cookbooks)

### Agent and engineering references

-   [Agency Agents](https://github.com/msitarzewski/agency-agents)
-   [LangChain](https://github.com/langchain-ai/langchain)
-   [Microsoft AutoGen](https://github.com/microsoft/autogen)
-   [LlamaIndex](https://github.com/run-llama/llama_index)

### Infrastructure and knowledge

-   [Ollama](https://github.com/ollama/ollama)
-   [llama.cpp](https://github.com/ggml-org/llama.cpp)
-   [vLLM](https://github.com/vllm-project/vllm)
-   [Hugging Face
    Transformers](https://github.com/huggingface/transformers)
-   [RAGFlow](https://github.com/infiniflow/ragflow)
-   [Mem0](https://github.com/mem0ai/mem0)
-   [n8n](https://github.com/n8n-io/n8n)
-   [Dify](https://github.com/langgenius/dify)
-   [Browser Use](https://github.com/browser-use/browser-use)
-   [Firecrawl](https://github.com/firecrawl/firecrawl)
-   [ComfyUI](https://github.com/comfyanonymous/ComfyUI)

------------------------------------------------------------------------

## Final operating principle

**Every AVISAN project should start by consulting this library, but no
project should be forced to use a tool simply because it is listed
here.**

The goal is to compound engineering knowledge: each project should reuse
what has already been validated, document what it learns, and leave the
next project with a stronger starting point.
