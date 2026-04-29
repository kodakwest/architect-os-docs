# 🏛️ Architect OS: The AI Systems Architecture Workbench

![Architect OS Hero](public/architect_os_hero.png)

Architect OS is a professional-grade AI development environment designed to bridge the gap between architectural conceptualization and local knowledge management. It provides a high-fidelity playground for designing, visualizing, and orchestrating complex multi-agent systems.

---

## 🚀 Core Architecture: The Two-Shot Pipeline

Architect OS leverages a unique **Two-Shot Pipeline** framework to ensure both creative depth and structural integrity:

1.  **Primary Model (Creative Generation)**: Generates high-fidelity Markdown containing agent designs, SOPs, and skill trees. (e.g., Gemini 1.5 Pro, Claude 3.5 Sonnet).
2.  **Shadow Agent (Structural Healing)**: A background subagent that monitors the primary output. If a valid `[ORCHESTRATION_CONFIG]` is missing or malformed, the Shadow Agent automatically extracts and repairs the structured JSON.

---

## 🛠️ Key Features (v3.2.0 Stable)

### 🧪 Prompt Workbench (Iteration Engine)
The core evolution hub for AI prompt engineering.
- **Iteration Mode**: Evolve existing "Gold Standard" designs through recursive natural language refinement.
- **Scratch Mode**: A sandboxed playground for rapid system/user prompt validation.
- **Native Versioning**: Auto-incrementing version control (v1, v2, v3) for architectural artifacts.

### 📂 Workspaces & Organizational Logic
Group your architectural sessions into logical project boundaries. 
- **Workspace Isolation**: Keep different projects separated and focused.
- **Session Previews**: Metadata-rich session tracking with previews for the last 3 messages.
- **Gold Standard Starring**: Mark high-quality designs for instant retrieval and filtering.

### 🔗 Knowledge Hub (Vault Sync)
Connect your local **Obsidian** vault directly via the File System Access API.
- **Native Write-Verify**: Every export includes a verification loop to ensure data integrity.
- **Local-First**: Your architectural data remains local and private.

---

## 🛡️ Prompt Governance Protocol

To maintain architectural stability, Architect OS enforces a strict governance protocol:
1.  **Archiving**: Automatic backup of core system prompts before any modification.
2.  **Verification**: Prompt updates trigger a "Gold Standard" verification request.
3.  **Regression Check**: Instant roll-back capability if Markdown depth or JSON structure is compromised.

---

**Status**: Stable / v3.2.0 "Workbench Evolution"  
**Agent**: TechDoc-Agent  
**Revision**: 3.2.0  
**Last Updated**: 2026-04-28
