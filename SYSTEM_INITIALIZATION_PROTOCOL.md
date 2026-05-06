# ⚠️ SYSTEM INITIALIZATION PROTOCOL ⚠️

**Target:** You (The AI Agent).

**Task:** Bootstrap the "Tiered Agent Vault" (TAV) in the current workspace using deterministic telemetry and high-density knowledge graph protocols.

**Instructions:** Create the exact directory structure below, then generate the specified files with the precise content provided. You MUST NOT alter the content of these files during generation.

## STEP 1: Create the Directory Architecture

Create the following folder structure in the root of the workspace.

_Directive: You MUST ensure an `AGENTS.md` file is placed in every single directory to enforce localized semantic boundaries._

```
/
├── AGENTS.md
└── Memory/
    ├── 00_System/
    │   ├── AGENTS.md
    │   └── MEMORY.md
    ├── 10_Episodic/
    │   └── AGENTS.md
    ├── 20_Semantic/
    │   └── AGENTS.md
    ├── 30_Procedural/
    │   ├── AGENTS.md
    │   ├── Ingesting_Research.md
    │   ├── Lint_Wiki.md
    │   └── Distill_Day.md
    ├── 40_Research/
    │   ├── AGENTS.md
    │   ├── Raw/
    │   │   └── AGENTS.md
    │   └── Processed/
    │       └── AGENTS.md
    ├── 50_Context/
    │   ├── AGENTS.md
    │   └── active-tasks.md
    └── 60_Archive/
        └── AGENTS.md
```

## STEP 2: Create the Root Bootloader (`./AGENTS.md`)

```
# 🧠 AGENT BOOTLOADER: READ IMMEDIATELY

You are operating within a Tiered Agent Vault (TAV) governed by a Distributed Semantic Control Plane.

**CRITICAL BOOT SEQUENCE:**
To understand your identity, operational parameters, and structural constraints, you MUST immediately read the following two files before taking any further action:

1. `./Memory/00_System/AGENTS.md` (Core Directives)
2. `./Memory/00_System/MEMORY.md` (Formatting & Schema)

**CORE PROCEDURAL TRIGGERS:**
When the human operator issues specific commands, you MUST immediately load and execute the corresponding procedure file. You MUST NOT attempt to execute the task from generic memory; follow the action document strictly:
- If prompted to **"ingest research"** -> You MUST load and execute `[[Memory/30_Procedural/Ingesting_Research.md]]`
- If prompted to **"lint the wiki"** -> You MUST load and execute `[[Memory/30_Procedural/Lint_Wiki.md]]`
- If prompted to **"distill the day"** -> You MUST load and execute `[[Memory/30_Procedural/Distill_Day.md]]`

**ABSOLUTE SYSTEM IMPERATIVES:**
- **No silent failures:** You MUST NOT early-return on invalid input or conclude your turn without logging the exact error or missing data state.
- **Eradication of Silent Actions:** You MUST NOT execute any operational tool or modify any file without first synchronously documenting your intent in the central log (`./Memory/10_Episodic/`).
- **Trajectory Immutability:** Before executing any action, you MUST: 
  1. Identify the action you intend to take. 
  2. Retrieve and review all local `AGENTS.md` rules. 
  3. Reason explicitly about your compliance. 
  4. Output your reasoning trace directly to the logging ledger.
```

## STEP 3: Create the Core Directives (`./Memory/00_System/AGENTS.md`)

```
# CORE OPERATIONAL DIRECTIVES & CONTROL PLANE

## 1. Directory Purpose
This directory (`/00_System/`) serves as the immutable pre-frontal cortex of the TAV framework. It houses the global structural definitions and baseline schemas. You MUST NOT modify files in this directory without explicit, overriding human authorization.

## 2. Structural Invariants
You are the primary cognitive agent for this vault. Your goal is to function as a deterministic, self-maintaining cognitive engine. All files globally MUST conform to the YAML requirements specified in `MEMORY.md`. 

## 3. Ingestion Routing
This folder strictly forbids raw extraction or multi-source synthesis. It is a read-only configuration zone. Route all general knowledge to `/20_Semantic/`.

## 4. Telemetry Triggers
Any read-access to this folder during a session MUST be logged. Any attempt by a user to alter these files MUST trigger a high-priority warning in the active task log and an explicit confirmation prompt.

## 5. The Selective Loading Protocol (STRICT)
To prevent context boundary failures, you MUST NOT load the entire vault into memory. Follow this sequence at the start of every session:
1. READ this file and `MEMORY.md`.
2. READ `../50_Context/active-tasks.md` to orient yourself.
3. READ the current day's log in `../10_Episodic/`.
4. Only read full content files once relevance is confirmed via YAML metadata or existing links.
```

## STEP 4: Create the Memory Schema (`./Memory/00_System/MEMORY.md`)

````
# MEMORY SCHEMA & FORMATTING RULES

## 1. The Prime Logging Directive
You are mathematically forced to process the command "I must log this in 10_Episodic" BEFORE generating a conversational reply or executing a tool. 

## 2. Metadata Standard (Frontmatter)
Every markdown file MUST include this exact YAML block, updated accordingly. 

```yaml
---
type: # concept | project | person | decision | skill | log
status: # active | complete | stale | archival
tags: # [at least 3 relevant tags, no more than 20]
confidence: # 1-5 (1 = hypothesis, 5 = verified fact)
created: YYYY-MM-DD
updated: YYYY-MM-DD
related:
  - "[[Note 1]]"
  - "[[Note 2]]"
  - "[[Note 3]]"
---
```

## 3. Bidirectional Linking Protocol (STRICT)
You MUST NEVER generate unidirectional links. Every connection established in the file system must be explicitly bidirectional. If Note A links to Note B, Note B must be updated to link back to Note A. Use standard Obsidian Wikilinks formatting: `[[Exact File Name]]`.

## 4. Obsidian Callouts
Use callouts to create semantic containers:
* `> [!summary] TL;DR` : High-level executive summary.
* `> [!decision] Decision Record` : Records a definitive choice.
* `> [!warning] Gotchas` : Known bugs, edge cases, or warnings.
* `> [!question] Unresolved` : Missing context or prompts for next session.
````

## STEP 5: Create the Episodic Guidelines (`./Memory/10_Episodic/AGENTS.md`)

```
# EPISODIC MEMORY PROTOCOL

## 1. Directory Purpose
This directory acts as the immutable episodic memory ledger. It captures the raw flow of experience and enforces deterministic interaction records. 

## 2. Structural Invariants (The Immutable Ledger)
All logs are compiled into a single file named `YYYY-MM-DD.md`. You MUST create this file if it does not exist for the current date. Every entry generated by you MUST conform to this exact schema:
- **Absolute Temporal Markers:** A precise timestamp and session identifier.
- **User Intent Capture:** A raw, unaltered transcription of the exact prompt or query provided by the human operator. You MUST log literally every prompt provided verbatim.
- **Agent Reasoning Trajectory:** A deterministic summary of your internal planning process executed prior to manipulating any files.
- **Resolution State & Graph Delta:** The final outcome of the sequence, explicitly noting any new semantic relationships created within the knowledge graph.

## 3. Ingestion Routing
This folder is strictly for append-only logging. Do not synthesize external knowledge here. 

## 4. Telemetry Triggers
You MUST NOT execute any operational tool, read any raw file, or modify any semantic file without FIRST synchronously documenting your intent in today's ledger according to the Structural Invariants.
```

## STEP 6: Create the Semantic Guidelines (`./Memory/20_Semantic/AGENTS.md`)

```
# SEMANTIC MEMORY PROTOCOL

## 1. Directory Purpose
This is the core synthesized knowledge graph. You act as an autonomous, persistent maintainer of a heavily structured, interlinked collection of markdown files.

## 2. Structural Invariants & The Pointy Graph Dilemma
You MUST artificially enforce high graph density. You are forbidden from creating "pointy" graphs (isolated nodes linking only to a central index). 
- **Island Prevention:** No note can exist without at least two `related` links in its YAML pointing laterally to other concept nodes.
- **Nested MOCs:** Do not use a monolithic central index. Use localized Maps of Content (MOCs) inside subfolders (e.g., `/20_Semantic/people/index.md`).

## 3. Ingestion Routing
This folder is strictly for high-fidelity synthesis. When routing data here, you must force analytical depth, extracting conceptual frameworks and explicitly writing synthesized insights into the evolving repository.

## 4. Telemetry Triggers & Autonomous Structural Linting
Every time you enter this folder to write a new note, you MUST algorithmically evaluate the link density of surrounding pages. If structural voids are detected, you MUST autonomously synthesize missing bridging connections before concluding your turn.
```

## STEP 7: Create the Procedural Guidelines (`./Memory/30_Procedural/AGENTS.md`)

```
# PROCEDURAL MEMORY PROTOCOL

## 1. Directory Purpose
This directory stores executable "Action Documents" or Skills. It defines the rigid operational pipelines you must follow for complex, multi-step tasks.

## 2. Structural Invariants
All files here MUST use the `type: skill` schema. They must be formatted as highly deterministic algorithms with numbered, imperative steps.

## 3. Ingestion Routing
When the user establishes a repeated workflow, document it here. Do not store general knowledge or episodic logs in this directory.

## 4. Telemetry Triggers
Trigger Phrase Execution: The user will invoke these files via natural language. When recognized via the triggers in the root `AGENTS.md`, you MUST load the corresponding procedural markdown file, log the initiation of the skill in `/10_Episodic/`, and follow its instructions to the letter without skipping steps.
```

## STEP 8: Create the Research Ingestion Skill (`./Memory/30_Procedural/Ingesting_Research.md`)

```
---
type: skill
status: active
tags:
  - workflow
  - procedural
  - research
  - ingestion
  - high-density-graph
created: 2026-04-30
updated: 2026-04-30
confidence: 5
related: 
  - "[[Memory/40_Research/AGENTS|AGENTS]]"
  - "[[Memory/20_Semantic/AGENTS|AGENTS]]"
---

# Procedural Workflow: The High-Density Ingestion Engine

> [!summary] TL;DR
> Execute this workflow to deterministically transform raw data into a highly refined, finalized state of structured knowledge. You MUST execute all 3 phases sequentially.

## Phase 1: Interactive Ingestion and Fractal Expansion
1. Read the specified raw file(s) located in `./Memory/40_Research/Raw/`.
2. Extract unique architectural decisions, idiosyncratic nomenclature, and edge cases.
3. **Atomic Concept Extraction:** You MUST create a dedicated, independent markdown file for every distinct concept, reference, or entity found in the source.
4. **Information Maximization:** Flesh out those concept nodes with internal knowledge to ensure the wiki contains more context than the original document alone.

## Phase 2: Topological Gap Analysis and Conflict Detection
1. Prior to committing new root pages, compare the newly extracted semantic triples against the historical baseline of the wiki graph.
2. Search for Structural Voids: instances where two highly related concepts have been ingested but lack a bridging narrative document.
3. If a void is detected, autonomously generate a synthesis page to physically bridge the topological distance between the concepts.

## Phase 3: Bidirectional Compilation and File Mutation
1. Create the primary reference nodes in `/20_Semantic/` (full text, executive summary, atomic concepts).
2. You are restricted from generating unidirectional links. Inject backlinks pointing directly to the original raw file.
3. File Management: Once the graph is updated, you MUST move the original raw file from `/40_Research/Raw/` to `/40_Research/Processed/`. Log the Graph Delta in `/10_Episodic/`.
```

## STEP 9: Create the Wiki Linting Skill (`./Memory/30_Procedural/Lint_Wiki.md`)

```
---
type: skill
status: active
tags:
  - workflow
  - procedural
  - linting
  - maintenance
  - graph-density
created: 2026-04-30
updated: 2026-04-30
confidence: 5
related: 
  - "[[Memory/20_Semantic/AGENTS|AGENTS]]"
---

# Procedural Workflow: Autonomous Graph Linting

> [!summary] TL;DR
> Execute this workflow to cure the "pointy graph" dilemma and fix semantic drift. You MUST traverse the knowledge base to locate unlinked concepts and weave them together.

## Phase 1: Graph Traversal and Island Identification
1. Scan the contents of `/20_Semantic/` and its nested Maps of Content (MOCs).
2. Identify "Orphan Nodes": Any markdown file with fewer than two `related:` connections in its YAML frontmatter.

## Phase 2: Relational Matching (The Karpathy Sweep)
1. Read the body text of established semantic notes.
2. Cross-reference the raw text against the titles of other existing notes in the wiki.
3. Locate instances where a note explicitly mentions a concept that exists as a separate page, but is NOT currently wrapped in a `[[Wikilink]]`.

## Phase 3: Structural Healing and Injection
1. **Inline Weaving:** You MUST modify the identified files to physically inject `[[Wikilinks]]` around the unlinked mentions of existing concepts.
2. **Backlink Enforcement:** Ensure that the newly linked target page is updated so that the relationship remains explicitly bidirectional.
3. **Bridge Synthesis:** If multiple nodes share highly related tags but have zero lateral connections, generate a brief synthesis page connecting them.

## Phase 4: Telemetry Log
1. You MUST generate a comprehensive ledger entry in today's `/10_Episodic/` file detailing exactly which files were modified and how many new links were injected during the linting sweep.
```

## STEP 10: Create the Distillation Skill (`./Memory/30_Procedural/Distill_Day.md`)

```
---
type: skill
status: active
tags:
  - workflow
  - procedural
  - heartbeat
  - distillation
created: 2026-04-30
updated: 2026-04-30
confidence: 5
related: 
  - "[[Memory/10_Episodic/AGENTS|AGENTS]]"
  - "[[Memory/20_Semantic/AGENTS|AGENTS]]"
---

# Procedural Workflow: The End-of-Day Distillation (Heartbeat)

> [!summary] TL;DR
> Execute this workflow to convert transient episodic memory into durable semantic knowledge, preventing context rot. 

## Phase 1: Episodic Review
1. Read the current day's log file located in `./Memory/10_Episodic/`.
2. Analyze the raw observations, session outputs, and interaction trajectories logged throughout the day.

## Phase 2: Durable Fact Extraction
1. Filter out transient interactions (e.g., minor code bugs fixed, casual queries).
2. Identify "Durable Knowledge": Core architectural decisions, new conceptual definitions, definitive verified facts, or newly established user preferences.

## Phase 3: Semantic Promotion
1. You MUST migrate these durable facts into the `./Memory/20_Semantic/` wiki.
2. Update existing concept pages with the new findings, or create new atomic nodes if the concept does not exist. Ensure rigorous bidirectional linking.
3. Update the `updated` timestamp and `confidence` score in the YAML of any modified files.

## Phase 4: Ledger Reconciliation
1. Return to the daily log in `./Memory/10_Episodic/`.
2. Append a `> [!success] PROMOTED:` callout to the bottom of the log, explicitly listing which facts were successfully distilled into the long-term wiki, thereby completing the heartbeat cycle.
```

## STEP 11: Create the Research Guidelines (`./Memory/40_Research/AGENTS.md`)

```
# RESEARCH PROTOCOL

## 1. Directory Purpose
This directory manages external documents and acts as the parent routing layer for the raw ingestion pipelines. 

## 2. Structural Invariants
You MUST NOT place data files directly into this parent folder. All files MUST be strictly routed into either the `/Raw/` or `/Processed/` subdirectories.

## 3. Ingestion Routing
This is a raw extraction zone. You MUST demand strict fidelity to the source text when reading from its subdirectories. Do not hallucinate or synthesize prior to moving the data into `/20_Semantic/`.

## 4. Telemetry Triggers
Reading this parent folder requires no immediate logging, but any file movement between its subdirectories MUST be logged as a Graph Delta in `/10_Episodic/`.
```

## STEP 12: Create the Raw Drop-Zone Guidelines (`./Memory/40_Research/Raw/AGENTS.md`)

```
# RAW DATA PROTOCOL

## 1. Directory Purpose
This directory acts strictly as the drop-zone for completely unstructured, unverified, and raw source materials provided by the human operator.

## 2. Structural Invariants
Files residing here are considered completely immutable. You MUST NOT modify the contents of any raw file placed in this directory under any circumstances.

## 3. Ingestion Routing
You MUST ONLY read from this directory when explicitly executing the `Ingesting_Research.md` procedural skill. 

## 4. Telemetry Triggers
You MUST wait for the user to prompt you before reading anything in this folder. Once triggered, you MUST log the read event and source file target in the daily episodic ledger before beginning analysis.
```

## STEP 13: Create the Processed Archive Guidelines (`./Memory/40_Research/Processed/AGENTS.md`)

```
# PROCESSED DATA PROTOCOL

## 1. Directory Purpose
This directory serves as the read-only, cold-storage archive for source materials that have successfully completed the ingestion pipeline and have been integrated into the semantic graph.

## 2. Structural Invariants
Every file residing here MUST have a corresponding set of interlinked concept nodes mapped into `/20_Semantic/`. Files MUST NOT be modified or appended to once moved here.

## 3. Ingestion Routing
You are explicitly forbidden from running ingestion, extraction, or synthesis pipelines on files located in this folder. They are considered complete.

## 4. Telemetry Triggers
You MUST ignore this folder entirely unless explicitly commanded by the user to retrieve an archived source. Any access MUST be logged in `/10_Episodic/`.
```

## STEP 14: Create the Context Guidelines (`./Memory/50_Context/AGENTS.md`)

```
# CONTEXT PROTOCOL

## 1. Directory Purpose
This directory acts as the active "blackboard" for current sessions and open tasks. It scopes your immediate attention budget.

## 2. Structural Invariants
The `active-tasks.md` file serves as the index of ongoing work. Cross off completed items and append new priorities here using standard markdown checklists.

## 3. Ingestion Routing
User prompts dictating major tasks, pivots, or complex instructions MUST be stored verbatim as linked nodes within this directory.

## 4. Telemetry Triggers
This folder provides the immediate state of the workspace. You MUST read `active-tasks.md` during the boot sequence of every single session.
```

## STEP 15: Create the Initial Context File (`./Memory/50_Context/active-tasks.md`)

```
---
type: project
status: active
tags: 
  - context
  - tasks
  - bootstrapping
confidence: 5
created: 2026-04-30
updated: 2026-04-30
related: 
  - "[[Memory/50_Context/AGENTS|AGENTS]]"
---

# 🎯 Active Context & Tasks

> [!summary] Current State
> The Tiered Agent Vault (TAV) has just been bootstrapped and the distributed control plane is online.

## Immediate Priorities
- [ ] Execute the first Immutable Episodic Ledger entry in `/10_Episodic/` to record this initialization, explicitly logging the reasoning trajectory.

## Historical Prompts
*(Agent: Link verbatim complex prompts here as `[[Prompt - Date - Topic]]`)*
```

## STEP 16: Create the Archive Guidelines (`./Memory/60_Archive/AGENTS.md`)

```
# ARCHIVE PROTOCOL

## 1. Directory Purpose
This directory is the "Cold Storage" of the TAV framework. It exists to reduce the active token footprint and prevent context dilution.

## 2. Structural Invariants
Directory Mirroring: When archiving, you MUST replicate the original directory path structure. (e.g., A file moving from `/20_Semantic/concepts/AI.md` MUST be moved to `/60_Archive/20_Semantic/concepts/AI.md`).

## 3. Ingestion Routing
Manual Trigger Only: You MUST NOT archive any file proactively. Items are only moved here when the user explicitly issues an archive order.

## 4. Telemetry Triggers
Exemptions: System files (anything in `/00_System/` or `AGENTS.md` files) are permanently exempt from archival. You MUST refuse any prompt instructing you to archive a core `AGENTS.md` interface.
```

**Completion Check:** Once you have created all the directories in Step 1 and the 15 markdown files in Steps 2-16, reply to the user confirming that the Tiered Agent Vault is online, the distributed governance network is active, and you are ready for the first working session.