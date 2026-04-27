# 🗺️ Projects & Context Hub (Intersession Memory)

This board serves as our persistent memory across coding sessions. It tracks the state of the workspace, current objectives, and infrastructure context.

## 📌 Active Macro-Goals
- [ ] **Architect OS:** Finalize multi-agent orchestration flows in the Control Plane.
- [ ] **AgentFlow (Beta):** Build custom rules engine and authentication injection templates.
- [ ] **Knowledge Management:** Implement direct synchronization pipeline between generated agent artifacts and local Obsidian vault.

## 📋 Kanban Board

### 📝 To Do (Next Actions)
- [ ] Provide the absolute path to the local Obsidian vault so the Agent can build the sync script.
- [ ] Implement "History Preview" tooltips/modals for more detailed metadata without navigating.

### 🚧 In Progress
- [ ] **Organization Phase:** Refining Workspace isolation and session migration tools.

### ✅ Done
- [x] **Architect OS:** Successfully rebranded from AgentFlow to Architect OS.
- [x] **Architect OS:** Implemented **Workspace Core Architecture** with Sidebar selector.
- [x] **Architect OS:** Added **History Starring** (Gold Standard tagging).
- [x] **Architect OS:** Redesigned **Unified History Console** with time-based grouping.
- [x] **Architect OS:** Implemented **Session Previews** (last 3 messages stored as metadata).
- [x] **Architect OS:** Fixed Chat History persistence across reloads and proper session spawning.
- [x] **Architect OS:** Verified "Save to Vault" export is working natively with Obsidian.
- [x] **Documentation:** Updated API Reference and Project Board for v3.0.0 (Organizational Evolution).

## 🏗️ Infrastructure & Environment State

| Service | Status | Port/Details | Notes |
| :--- | :--- | :--- | :--- |
| **LM Studio** | ✅ Active | `192.168.50.98:1234` | Shadow Agent host. Qwen 2.5 7B extraction. |
| **Architect OS** | 🛠️ Development | `127.0.0.1:3000` | Workspaces & History Evolution live. |
| **OpenRouter** | ✅ Active | `API Layer` | Primary/Shadow provider for Gemini/Claude models. |

## 📁 Workspace Directory Map
* **`agentflow/`**: Vite-based Architect OS / prompt engineering workbench. (See: [ROADMAP.md](./docs/ROADMAP.md), [API_REFERENCE.md](./docs/API_REFERENCE.md), [MCP_CAPABILITIES.md](./docs/MCP_CAPABILITIES.md))
* **`OpenWebUI/genui-chat-app/`**: Next.js Generative UI chat application.

## 🛠️ Maintenance & Prompt Governance
- **Backup Before Edit:** Whenever a core system prompt is modified, the previous version must be archived.
- **Quality Regression Testing:** Any prompt change impacting output structure MUST be followed by a request for a "Gold Standard" test.
- **Organization:** Chats are now partitioned by Workspace. Default is "General".

---
> **Agent Handoff Protocol:** Updated 2026-04-27. Infrastructure stabilized. Organization Roadmap (Phase 1) complete.
