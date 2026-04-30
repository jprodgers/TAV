The Tiered Agent Vault (TAV) is an open-source framework built to solve the fundamental challenges of AI context management and state persistence. Standard transformer architectures are susceptible to "context rot" as input volumes increase, leading to a degradation in reasoning and retrieval accuracy. TAV mitigates these constraints by replacing flat context windows with a hierarchical memory system relying on localized Markdown files within a strict, predictable directory structure.

Designed to integrate seamlessly with the Obsidian knowledge management ecosystem, TAV allows an AI to maintain its own structured, human-editable documentation.

### Core Features

- **Tiered Memory Architecture:** Organizes knowledge across Episodic, Semantic, Procedural, and Archival tiers to ensure the agent only loads relevant information.
    
- **Context Window Optimization:** By paging data across these tiers, the system keeps the agent operating efficiently within the "Goldilocks zone" of its context window.
    
- **Automated Maintenance Cycles:** Enforces strict "write-manage-read" loops and a "heartbeat" distillation process to periodically convert raw episodic logs into durable, long-term semantic knowledge.
    
- **Obsidian-Native Syntax:** Leverages dense cross-linking via wikilinks, strict YAML frontmatter, and callouts to build a navigable, interlinked knowledge graph.
    
- **Dual-Layered Governance:** Utilizes a root `AGENTS.md` file as the primary source of truth, establishing boundaries and directing the agent toward detailed schemas within the system directory.