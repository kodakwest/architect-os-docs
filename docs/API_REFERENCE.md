# 🏛️ Architect OS: Orchestration Engine API Reference

## 🛠️ Prompt Governance Protocol
> [!IMPORTANT]
> To ensure architectural stability and output quality, the following protocol must be followed by all AI agents:
> 1. **Archiving:** Always backup the current `DEFAULT_ARCHITECT_SYSTEM_PROMPT` before making modifications.
> 2. **Verification:** Notify the user immediately after a prompt change to perform a "Gold Standard" verification (e.g., generating a complex agent like the *Content Curator*).
> 3. **Regression Check:** If output quality drops (loss of markdown depth, missing JSON), revert to the last known good backup immediately.

---

# 1.0 Overview & Purpose

The **Architect OS Orchestration Engine** is a two-shot pipeline framework that separates creative Markdown generation from deterministic JSON extraction.

**Pipeline Architecture:**
1. **Primary Model** → Generates high-fidelity Markdown (agent designs, SOPs, skill trees)
2. **Shadow Agent** → Extracts structured JSON from the Markdown via a background subagent
3. **Vault Sync** → Writes outputs to the file system with write-verify-retry verification
4. **Organizational Context** → Metadata-rich tracking (Workspaces, Starring, Preview Snippets)

## 1.1 Orchestration Configuration Schema
The engine parses structured JSON configurations wrapped in `[ORCHESTRATION_CONFIG]` tags.
 
**Schema Definition:**
```json
{
  "nodes": [
    {
      "id": "string",
      "type": "agent | prompt | condition",
      "data": {
        "name": "string",
        "role": "string",
        "systemPrompt": "string"
      }
    }
  ],
  "knowledgeBase": [
    {
      "id": "string",
      "name": "string",
      "type": "obsidian | url | file"
    }
  ],
  "metadata": {
    "version": "number",
    "author": "string",
    "workspaceId": "string",
    "isStarred": "boolean"
  }
}
```

---

# 2.0 Authentication & Configuration

The engine interacts with the Google Gemini API (Pro and Flash models). Configuration is managed via environment variables and local storage persistence.

### Base Configuration
- **API Key**: `VITE_GEMINI_API_KEY` (Must be provided in the `.env` file).
- **Primary Chat Model**: User-configured via Settings (default: `gemini-1.5-pro`).
- **Shadow Agent Model**: Configurable independently in Settings → Shadow Orchestrator.
- **OpenRouter**: Supported as both primary chat and shadow agent provider.
- **Local Inference**: LM Studio via configurable URL (default: `localhost:1234`).

### Organizational Logic
| Feature | Key | Logic |
| :--- | :--- | :--- |
| **Workspaces** | `workspaceId` | Groups sessions into logical project boundaries. |
| **Starring** | `isStarred` | Marks "Gold Standard" designs for instant retrieval. |
| **Previews** | `previewMessages` | Stores snippets of the last 3 messages for instant UI insights. |

---

# 3.0 Core SDK Reference

## 3.1 `saveChatSession(session: ChatSession)`
The primary persistence utility for architect sessions.

**Parameters:**
| Name | Type | Description |
| :--- | :--- | :--- |
| `id` | `string` | Unique session identifier. |
| `workspaceId` | `string` | The ID of the active workspace. |
| `isStarred` | `boolean` | Favorite status. |
| `messages` | `Message[]` | Full array of messages. |

## 3.2 `getTimeline()`
Returns a metadata-rich list of all architect activities, grouped and formatted for the History Pane.

---

# 4.0 Code Examples

## 4.1 Toggling Session Priority (Starring)
```typescript
import { toggleStar } from './lib/storage';

async function markAsGoldStandard(sessionId: string) {
  const updated = await toggleStar(sessionId, 'chat');
  console.log("Session Starred:", updated.find(s => s.id === sessionId).isStarred);
}
```

---

# 5.0 Error Codes & Troubleshooting

| Error Code | Description | Resolution |
| :--- | :--- | :--- |
| `ORCHESTRATION_FAILED` | Internal error during the state machine execution. | Check network connectivity and API quota. |
| `WORKSPACE_NOT_FOUND` | Active workspace ID does not exist in storage. | Re-initialize via `getWorkspaces()` to restore the Default workspace. |
| `INVALID_JSON_RESPONSE` | LLM failed to return a valid JSON object. | Refine the extraction prompt or lower temperature. |

---
**Status**: Publication Ready  
**Agent**: TechDoc-Agent  
**Revision**: 3.0.0 (Evolution Update)  
**Last Updated**: 2026-04-27
