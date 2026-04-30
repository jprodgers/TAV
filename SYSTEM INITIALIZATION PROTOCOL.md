# ⚠️ SYSTEM INITIALIZATION PROTOCOL ⚠️

**Target:** You (The AI Agent).

**Task:** Bootstrap the "Tiered Agent Vault" (TAV) in the current workspace.

**Instructions:** Create the exact directory structure below, then generate the 13 specified files with the precise content provided. Do not alter the content.

## STEP 1: Create the Directory Architecture

Create the following folder structure in the root of the workspace:

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
    │   └── Ingesting Research.md
    ├── 40_Research/
    │   ├── AGENTS.md
    │   ├── Raw/
    │   └── Processed/
    ├── 50_Context/
    │   ├── AGENTS.md
    │   └── active-tasks.md
    └── 60_Archive/
        └── AGENTS.md
```

## STEP 2: Create the Root Bootloader (`./AGENTS.md`)

```
# 🧠 AGENT BOOTLOADER: READ IMMEDIATELY

You are operating within a Tiered Agent Vault (TAV) designed to prevent context rot. 
Do **NOT** scan or load the entire vault into your context window.

**CRITICAL BOOT SEQUENCE:**
To understand your identity, operational parameters, and how to read/write to this vault, you must immediately read the following two files:

1. `./Memory/00_System/AGENTS.md` (Core Directives & Boot Sequence)
2. `./Memory/00_System/MEMORY.md` (Formatting, Schema, & Obsidian Syntax)

Read those files now before taking any further action.
```

## STEP 3: Create the Core Directives (`./Memory/00_System/AGENTS.md`)

```
# CORE OPERATIONAL DIRECTIVES

## Identity and Intent
You are the primary cognitive agent for this Obsidian-based vault. Your goal is to assist the user by maintaining a persistent, high-accuracy memory system. You act as a Senior Knowledge Engineer.

## Distributed Governance
Each primary directory in this vault contains its own `AGENTS.md` file. When operating within a specific directory (e.g., writing an episodic log or executing a skill), you must consult that folder's localized `AGENTS.md` for specific instructions.

## The Selective Loading Protocol (STRICT)
To prevent context rot, do NOT load the entire vault. Follow this sequence at the start of every session:
1. READ this file and `MEMORY.md`.
2. READ `../50_Context/active-tasks.md` to orient yourself.
3. READ the current day's log in `../10_Episodic/` (if it exists).
4. SCAN the relevant index/manifest to find file paths if the user mentions a specific topic.
5. Only read full content files once relevance is confirmed via YAML metadata.

## Safety and Permissions
- **Always:** Use Wikilinks `[[Note]]` and YAML metadata.
- **Ask First:** Before deleting files or majorly reorganizing `/20_Semantic/`.
```

## STEP 4: Create the Memory Schema (`./Memory/00_System/MEMORY.md`)

````
# MEMORY SCHEMA & FORMATTING RULES

## 1. Metadata Standard (Frontmatter)
Every markdown file MUST include this exact YAML block at the top. Note the structure for related documents, expand or contract as needed:

```yaml
---
type: # concept | project | person | decision | skill | log
status: # active | complete | stale | archival
tags: # [at least 3 relevant tags, no more than 20]
confidence: # 1-5 (1 = hypothesis, 5 = verified fact)
created: YYYY-MM-DD
updated: YYYY-MM-DD
related01: [[Note 1]]
related02: [[Note 2]]
related03: [[Note 3]]
---
```

## 2. Linking Protocol
Always use Obsidian Wikilinks formatting: `[[Exact File Name]]`. Utilize multiple `relatedXX` fields in the YAML block to build a traversable graph.

## 3. Obsidian Callouts
Use callouts to create semantic containers:
* `> [!summary] TL;DR` : High-level executive summary.
* `> [!decision] Decision Record` : Records a definitive choice.
* `> [!warning] Gotchas` : Known bugs, edge cases, or warnings.
* `> [!question] Unresolved` : Missing context or prompts for next session.
````

## STEP 5: Create the Episodic Guidelines (`./Memory/10_Episodic/AGENTS.md`)

```
# EPISODIC MEMORY PROTOCOL

This directory acts as the system's hippocampus, capturing the raw flow of experience.

## Rules of Operation
1. **Per Prompt:** Record a brief, timestamped bullet point in the current day's note detailing the action taken or information requested.
2. **Per Session:** At the end of a cohesive working block, generate a session summary using a `> [!summary]` callout. Identify if any facts should be promoted to the `/20_Semantic/` folder.
3. **Per Day:** All logs are compiled into a single file named `YYYY-MM-DD.md`. Create this file if it does not exist for the current date. Do not modify past daily notes unless specifically fixing a broken link.
```

## STEP 6: Create the Semantic Guidelines (`./Memory/20_Semantic/AGENTS.md`)

```
# SEMANTIC MEMORY PROTOCOL

This is the core "Second Brain" of the system, storing durable, long-term knowledge.

## Organization & Sub-Folders
When research is ingested or facts are promoted, organize them into logical sub-folders (e.g., `/concepts`, `/people`, `/technologies`, `/frameworks`). Create these sub-folders dynamically as needed.

## Structural Requirements
1. **Island Prevention:** No note can exist without at least two `relatedXX` tags in its YAML pointing to other nodes. 
2. **Visual Hierarchy:** Every semantic note must begin with a `> [!summary]` callout, followed by logically grouped headings.
3. **Index Maintenance:** Whenever a new note is added, you must update the `index.md` (or equivalent manifest) in this directory with a link and a 1-sentence description.
```

## STEP 7: Create the Procedural Guidelines (`./Memory/30_Procedural/AGENTS.md`)

```
# PROCEDURAL MEMORY PROTOCOL

This directory stores executable "Action Documents" or Skills.

## Rules of Operation
1. **Trigger Phrase Execution:** The user will invoke these files via natural language (e.g., "Ingest new research please"). When recognized, you must load the corresponding procedural markdown file and follow its instructions to the letter.
2. **Current Skills Index:**
   - `[[Ingesting Research]]`: Triggered when asked to process files in the `40_Research/Raw/` folder.
3. **Skill Creation:** When the user establishes a repeated workflow, document it here using the `type: skill` schema.
```

## STEP 8: Create the Research Ingestion Skill (`./Memory/30_Procedural/Ingesting Research.md`)

```
---
type: skill
status: active
tags:
  - workflow
  - procedural
  - research
  - ingestion
created: 2026-04-30
updated: 2026-04-30
confidence: 5
related01: [[40_Research/AGENTS]]
related02: [[20_Semantic/AGENTS]]
---

# Procedural Workflow: Research Ingestion

> [!summary] TL;DR
> Execute this workflow **only** when explicitly prompted by the user to ingest new research dropped into `./Memory/40_Research/Raw/`. Do not auto-ingest.

## 1. Ingestion & Analysis
1. Read the specified raw file(s) located in `./Memory/40_Research/Raw/`.
2. Parse the document completely, extracting unique architectural decisions, idiosyncratic nomenclature, subtle edge cases, and definitive empirical data points.

## 2. Synthesis & Creation
Create a new Markdown file in the appropriate sub-directory of `./Memory/20_Semantic/`. Include mandatory YAML and Obsidian callouts (`> [!summary]`, `> [!warning]`, etc.).

## 3. Graph Integration
1. Heavily cross-link the new document to existing notes using `relatedXX` YAML fields and inline `[[Wikilinks]]`.
2. Add a brief entry to today's log in `./Memory/10_Episodic/` stating what research was ingested.

## 4. File Management (CRITICAL)
Once ingestion is complete and the semantic note is saved, you **MUST** move the original raw file from `./Memory/40_Research/Raw/` into `./Memory/40_Research/Processed/`.

## 5. Completion State
Respond to the user confirming the ingestion is complete, summarizing extracted insights, listing the new `[[Wikilinks]]` generated, and confirming the raw file was moved to `/Processed/`.
```

## STEP 9: Create the Research Guidelines (`./Memory/40_Research/AGENTS.md`)

```
# RESEARCH PROTOCOL

This directory manages external documents and raw ingestion pipelines.

## Directory Structure
- `/Raw/`: Unprocessed files dropped by the user.
- `/Processed/`: Files that have successfully gone through the `Ingesting Research` procedural workflow.

## Rules of Operation
1. **Ignore Processed:** Do not scan, read, or summarize files located in the `/Processed/` directory unless explicitly commanded by the user. They are considered "read-only" archives of source material.
2. **Trigger Only:** Wait for the user to prompt you before reading anything in the `/Raw/` folder.
```

## STEP 10: Create the Context Guidelines (`./Memory/50_Context/AGENTS.md`)

```
# CONTEXT PROTOCOL

This directory acts as the active "blackboard" for current sessions and open tasks.

## Rules of Operation
1. **Self-Explanation:** This folder provides the immediate state of the workspace. It is always read during the boot sequence.
2. **Prompt Storage:** User prompts dictating major tasks, pivots, or complex instructions must be stored verbatim as linked nodes within this directory.
3. **Index Maintenance:** The `active-tasks.md` file serves as the index of ongoing work. Cross off completed items and append new priorities here.
```

## STEP 11: Create the Initial Context File (`./Memory/50_Context/active-tasks.md`)

```
---
type: project
status: active
tags: [context, tasks, bootstrapping]
confidence: 5
created: 2026-04-30
updated: 2026-04-30
related01: [[50_Context/AGENTS]]
---

# 🎯 Active Context & Tasks

> [!summary] Current State
> The Tiered Agent Vault (TAV) has just been bootstrapped.

## Immediate Priorities
- [ ] Ask the user for the primary domain and overall goals of this workspace.
- [ ] Create the first daily log entry in `/10_Episodic/` to record this initialization.

## Historical Prompts
*(Agent: Link verbatim complex prompts here as `[[Prompt - Date - Topic]]`)*
```

## STEP 12: Create the Archive Guidelines (`./Memory/60_Archive/AGENTS.md`)

```
# ARCHIVE PROTOCOL

This directory is the "Cold Storage" of the TAV framework.

## Rules of Operation
1. **Manual Trigger:** Do NOT archive any file proactively. Items are only moved here when the user explicitly issues an archive order (e.g., "Archive project X" or "Archive stale semantic notes").
2. **Directory Mirroring:** When archiving, you must replicate the original directory path structure. (e.g., A file moving from `/20_Semantic/concepts/AI.md` should be moved to `/60_Archive/20_Semantic/concepts/AI.md`).
3. **Exemptions:** System files (anything in `/00_System/` or `AGENTS.md` files) are permanently exempt from archival. The `/10_Episodic/` and `/20_Semantic/` folders will be the most frequent targets for archival sweeps.
```

**Completion Check:** Once you have created all the directories in Step 1 and the 12 markdown files in Steps 2-12, reply to the user confirming that the Tiered Agent Vault is online, the distributed governance network is active, and you are ready for the first working session.