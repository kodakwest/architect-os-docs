# 🧩 MCP Capabilities Matrix

## 🛠️ chrome-devtools-mcp
**Description:** High-fidelity browser automation and inspection toolset for Architect OS agents.

### 📊 Capability Report (Audit: 2026-04-27)
| Category | Tool | Description | Status |
| :--- | :--- | :--- | :--- |
| **Navigation** | `navigate_page` | Change URL, go back/forward, or reload. | ✅ Verified |
| **Navigation** | `new_page` | Open a new tab/context. | ✅ Verified |
| **Inspection** | `take_snapshot` | Accessibility tree-based text snapshot (uids). | 🛠️ Available |
| **Inspection** | `take_screenshot` | Visual capture of page/element. | 🛠️ Available |
| **Interaction** | `click` | Execute mouse click on element uid. | 🛠️ Available |
| **Interaction** | `fill` | Populate form inputs/textareas. | 🛠️ Available |
| **Performance** | `lighthouse_audit` | SEO, Accessibility, and Best Practices report. | 🛠️ Available |
| **Diagnostics** | `list_console_messages`| Retrieve console logs for debugging. | 🛠️ Available |

### 🚀 Usage in Architect OS
Agents can utilize these tools via the Shadow Orchestrator to perform real-time verification of generated UI components or to scrape technical documentation.

---
**Revision:** 1.0.0  
**Agent:** PrototypeBuilder-CodingAssistant  
**Last Updated:** 2026-04-27
