# 🏛️ Architect OS: The AI Systems Architecture Workbench

![Architect OS Hero](public/architect_os_hero.png)

Architect OS is a professional-grade AI development environment designed to bridge the gap between architectural conceptualization and local knowledge management. It provides a high-fidelity playground for designing, visualizing, and orchestrating complex multi-agent systems.

---

## 🚀 Core Architecture: The Two-Shot Pipeline

Architect OS leverages a unique **Two-Shot Pipeline** framework to ensure both creative depth and structural integrity:

1.  **Primary Model (Creative Generation)**: Generates high-fidelity Markdown containing agent designs, SOPs, and skill trees. (e.g., Gemini 1.5 Pro, Claude 3.5 Sonnet).
2.  **Shadow Agent (Structural Healing)**: A background subagent that monitors the primary output. If a valid `[ORCHESTRATION_CONFIG]` is missing or malformed, the Shadow Agent automatically extracts and repairs the structured JSON.

---

## 🛠️ Key Features

### 📂 Workspaces & Organizational Logic
Group your architectural sessions into logical project boundaries. 
- **Workspace Isolation**: Keep different projects separated and focused.
- **Session migration**: Move sessions between workspaces as your project evolves.

### ⭐ Gold Standard Starring
Build your own library of "Gold Standard" designs. 
- **One-click Starring**: Mark high-quality outputs for instant retrieval.
- **Filtered History**: Quickly access your best work from the Unified History Console.

### 🕒 Unified History Console
A redesigned history management pane with:
- **Time-based Grouping**: Organize sessions by date and priority.
- **Session Previews**: Hover or view snippets of the last 3 messages for instant UI insights without full navigation.

### 🔗 Knowledge Hub (Vault Sync)
Connect your local **Obsidian** vault directly via the File System Access API.
- **Native Write-Verify**: Every export includes a verification loop to ensure the data was written correctly to your vault.
- **Local-First**: Your architectural data remains local and private.

### 🧠 Dual Inference & Model Agnostic
- **Cloud Providers**: Native support for Google Gemini (1.5/2.5) and OpenRouter (Claude, GPT).
- **Local Inference**: Deep integration with **LM Studio** (Qwen 2.5) for local structural healing and privacy-conscious tasks.

---

## 🛡️ Prompt Governance Protocol

To maintain architectural stability, Architect OS enforces a strict governance protocol:
1.  **Archiving**: Automatic backup of core system prompts before any modification.
2.  **Verification**: Prompt updates trigger a "Gold Standard" verification request to ensure no regression in output quality.
3.  **Regression Check**: Instant roll-back capability if Markdown depth or JSON structure is compromised.

---

## 🧩 Extensibility & MCP
Architect OS is fully compatible with the **Model Context Protocol (MCP)**, allowing agents to access local tools for:
- **Browser Automation**: `chrome-devtools-mcp` for real-time verification and scraping.
- **File System Access**: Direct manipulation of local documentation and source code.
- **Custom Tooling**: Easily inject your own MCP servers to extend the OS capabilities.

---

## 📊 Orchestration Schema (v3.0.0)
The engine parses structured JSON configurations wrapped in `[ORCHESTRATION_CONFIG]` tags.

```json
{
  "nodes": [
    {
      "id": "string",
      "type": "agent | prompt | condition",
      "data": { "name": "string", "role": "string", "systemPrompt": "string" }
    }
  ],
  "metadata": {
    "workspaceId": "string",
    "isStarred": "boolean",
    "version": 3.0
  }
}
```

---

**Status**: Alpha / Active Development  
**Agent**: TechDoc-Agent  
**Revision**: 3.0.0  
**Last Updated**: 2026-04-27
