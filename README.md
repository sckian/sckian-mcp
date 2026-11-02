# Sckian MCP Server

**Your job search, inside your agent.**

Sckian matches new job offers to your profile every day. Connect the Sckian MCP server and your agent can read your matches and applications and help you choose where to apply, in Claude, ChatGPT, Gemini, Grok or any MCP client.

```
https://sckian.com/mcp
```

- **Transport:** Streamable HTTP (remote, nothing to install)
- **Auth:** OAuth. Sign in with your Sckian account, no API keys
- **Registry:** `com.sckian/sckian` on the [official MCP Registry](https://registry.modelcontextprotocol.io)
- **Pricing:** free to start, no credit card required

## Connect

| Client | How |
|---|---|
| **Claude** | Settings → Connectors → Add custom connector → paste `https://sckian.com/mcp` |
| **ChatGPT** | Settings → Connectors → Create → paste `https://sckian.com/mcp` |
| **Gemini / Grok / others** | Add a remote MCP server with URL `https://sckian.com/mcp` |

The first time you use it, your client opens a Sckian sign-in page. Approve access and you're done.

## Ask things like

- "Any new remote backend roles for me this week?"
- "What does this job ask for, and how does my tailored resume read?"
- "Where do my applications stand?"
- "How well does my resume fit this job for ATS?"

## Tools

| Tool | What it does | Access |
|---|---|---|
| `get_profile` | Your profile, with a stable id | Read |
| `get_plan` | Your plan and the credits you have left | Read |
| `list_matches` | The jobs matched to you, with scores | Read |
| `get_job` | One job in full, with its apply link | Read |
| `list_bookmarks` | The jobs you saved | Read |
| `list_applications` | Your applications and their status | Read |
| `get_application` | One application, with its documents | Read |
| `get_document` | A tailored resume or cover letter, as text | Read |
| `get_document_link` | A PDF download link, valid five minutes | Read |
| `score_ats` | How well an application's resume fits its job | Read |
| `save_job` / `unsave_job` | Save or remove a job | Write |
| `prepare_application` | Prepare an application with its documents, after you confirm | Write |
| `update_profile` | Change job title, summary and links | Write |
| `update_preferences` | Change job types, remote work, categories, minimum salary | Write |

## Privacy & safety

- Read and write permissions are separate OAuth scopes (`profile:read`, `jobs:read`, `applications:read`, `jobs:write`, `applications:write`, `profile:write`, `preferences:write`).
- Disconnect anytime from your client's connector settings.
