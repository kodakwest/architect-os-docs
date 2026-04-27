# Architect OS (Reference Index)
 
This document serves as the master roadmap and reference index for **Architect OS**. It outlines the architectural decisions, core modules, and upcoming development phases for the AI Operating System.
 
---
 
## 🏛️ 1. Architecture & Blueprinting
*Reference: The Local-First Graph RAG Agent System*
 
We have elected to build the **Local-First Graph** to ensure ultimate privacy and deep integration with the local Obsidian vault.
*   **Two-Shot Pipeline:** Separates high-fidelity Markdown generation (Primary Model) from deterministic JSON extraction (Shadow Agent).
*   **Control Plane Engine:** Real-time orchestration state managed via Zustand.
*   **Primary Brain:** Gemini 1.5 Pro / 2.0 Pro or Claude 3.5 Sonnet (via OpenRouter).
*   **Shadow Agent:** Local LM Studio (Qwen 2.5) with `gemini-2.5-flash-lite` fallback for structural healing.
*   **Knowledge Base:** Direct file-system integration with the Obsidian Vault.
 
---
 
## 🚀 2. Core Modules (Architect OS)
 
Architect OS acts as the high-performance development environment and control panel for the entire agent lifecycle.
 
### 1. The Architecture Chat (Conceptualization)
The entry point for generating and refining agent constraints.
*   **Features:** Generates System Prompts, Skills Trees, and **Control Plane Config Sync**.
*   **Status:** ✅ Active. Sync logic for `[ORCHESTRATION_CONFIG]` live. **System Prompt Editor** built into Settings.
*   **Governance:** Adheres to the **Prompt Governance Protocol** (Archive-Verify-Retry).
 
### 2. Control Plane (Orchestration Hub)
The real-time visualization and nerve center of the OS.
*   **Features:** Dynamic node mapping, intent classification, and real-time config updates from the Chat.
*   **Status:** ✅ Active. Synchronized with Architect Chat via the Shadow Agent pipeline.
 
### 3. AgentFlow (Beta) (Developer Tools)
The granular workbench for custom extensions.
*   **Features:** Build custom pipelines, rules engines, and code injections to extend the Control Plane.
*   **Status:** ✅ Active (Beta). **Chat History persistence** and session spawning implemented.
 
### 4. Knowledge Hub (RAG Engine)
The bridge between the generative playground and persistent memory.
*   **Features:** Connects directly to the local Obsidian Vault.
*   **Status:** ✅ Active. "Save to Vault" verified working natively with write-verify verification.
 
---
 
## 🤖 3. Key Agent Personas
 
### The Prompt Synthesizer
*   **Role:** An elite AI Prompt Engineering agent operating as a backend engine.
*   **Mechanism:** Receives a structured JSON payload from the React UI and dynamically compiles a highly optimized System Prompt.
 
### TechDoc-Agent
*   **Role:** Elite Technical Documentation Specialist.
*   **Mechanism:** Ingests code artifacts and synthesizes MDX documentation via deterministic state-machine workflow.
 
### Shadow Extraction Agent
*   **Role:** Structural Healer.
*   **Mechanism:** Background agent tasked with extracting valid JSON from primary model outputs when the direct match fails.
 
---
 
## 📋 4. Immediate Action Items
- [x] **Rebranding:** Finalize shift from AgentFlow to Architect OS.
- [x] **Pipeline:** Implement Two-Shot Pipeline (Markdown -> JSON extraction).
- [x] **Governance:** Formalize Prompt Governance Protocol.
- [x] **Stability:** Tame local Qwen models (Stop strings & Thinking mode disabled).
- [ ] **Feature:** Build the slider/toggle React UI for the Prompt Synthesizer parameters.
- [ ] **Integration:** Define the exact tool access list for the agents (e.g., `Read_File`, `Write_File`, `Search_ChromaDB`).
- [ ] **Documentation:** Finalize high-fidelity API Reference for the Orchestration Engine (v2.0).
