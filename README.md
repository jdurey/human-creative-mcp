# Human Creative MCP Server (`io.github.jdurey/human-creative`)

Zero-install **Streamable HTTP** Model Context Protocol (MCP) server for multi-vendor AI workflow diagnostics, deterministic HTTP Archive (`.har`) agent evaluation sandboxes, 50-vector adversarial guardrail audits, 4-family LLM judge rubric calibration, and SOP-to-SCORM/QTI compilation.

- **Remote MCP Endpoint (Streamable HTTP):** `https://josh-employer-funnel.josh-durey.workers.dev/mcp`
- **Registry Namespace:** `io.github.jdurey/human-creative`
- **Architecture Portfolio & Live Diagnostic Hub:** [https://jdurey.github.io](https://jdurey.github.io)
- **Interactive AI Video Twin (Live Technical Q&A):** [https://jdurey.github.io/interview/](https://jdurey.github.io/interview/)

No local runtime, Docker container, or API key is required to connect and run diagnostics or instant Edge dry-run previews (`preview_mode: true`).

---

## Available MCP Tools (5)

| Tool Name | Purpose | Instant Free Mode |
| :--- | :--- | :--- |
| `diagnose_ai_workflow` | Executes a live 3-stage cross-family AI workflow or job description diagnostic on Cloudflare Workers AI (`Mistral 24B` intake -> `Llama 3.3 70B` 4-node DAG architect + `Qwen 2.5 32B` independent quality gate). Returns structured bottlenecks, silent failure modes, a 4-node DAG with human checkpoints, a 30-day rollout plan, and matched architecture receipts. | Always free (`readOnlyHint: true`) |
| `build_rea_har_agent_sandbox` | Converts a live web workflow URL or recorded HTTP Archive (`.har` v1.2) into an offline deterministic REA AgentEnv MCP sandbox (callable read/write tools + state transitions) paired with 8 multi-step evaluation tasks, 3-vendor Judge-Trust reward verifiers, a 300-DPI Executive Benchmark PDF, and a SHA-256 verified `.zip` bundle. | Set `"preview_mode": true` |
| `audit_workflow_guardrails_50v` | Runs a 50-vector multi-family prompt-injection, policy-bypass, and stem-withheld answer-leak stress test judged by 3 independent LLM vendor families, producing a hardened v2.0 system prompt and a 300-DPI Executive Audit PDF. | Set `"preview_mode": true` |
| `calibrate_judge_rubric_4family` | Eliminates single-model self-preference bias and stochastic verdict flips by decomposing subjective quality criteria into deterministic Python checks paired with a 4-family Judge-Trust rubric panel verified across byte-identical repeats. | Set `"preview_mode": true` |
| `compile_sop_to_scorm_qti` | Compiles raw Markdown or plain-text SOPs, runbooks, and training documents into LMS-ready SCORM 1.2 and QTI 3.0 XML mastery packages with stem-withheld blind-QA item verification. | Set `"preview_mode": true` |

---

## 1-Click Client Setup

### Claude Code

Run in your terminal:

```bash
claude mcp add --transport http human-creative https://josh-employer-funnel.josh-durey.workers.dev/mcp
```

Or add to `.mcp.json` in your project root:

```json
{
  "mcpServers": {
    "human-creative": {
      "type": "http",
      "url": "https://josh-employer-funnel.josh-durey.workers.dev/mcp"
    }
  }
}
```

### Cursor

Add to `.cursor/mcp.json` (or `~/.cursor/mcp.json`):

```json
{
  "mcpServers": {
    "human-creative": {
      "url": "https://josh-employer-funnel.josh-durey.workers.dev/mcp"
    }
  }
}
```

### Windsurf

Add to `~/.codeium/windsurf/mcp_config.json`:

```json
{
  "mcpServers": {
    "human-creative": {
      "serverUrl": "https://josh-employer-funnel.josh-durey.workers.dev/mcp"
    }
  }
}
```

### Cline

Add to `cline_mcp_settings.json`:

```json
{
  "mcpServers": {
    "human-creative": {
      "type": "streamableHttp",
      "url": "https://josh-employer-funnel.josh-durey.workers.dev/mcp",
      "disabled": false
    }
  }
}
```

---

## Quick Verification (`curl`)

List all live tools via JSON-RPC 2.0:

```bash
curl -s -X POST https://josh-employer-funnel.josh-durey.workers.dev/mcp \
  -H "Content-Type: application/json" \
  -d '{"jsonrpc":"2.0","id":1,"method":"tools/list","params":{}}'
```

Run a free 3-vendor workflow diagnostic:

```bash
curl -s -X POST https://josh-employer-funnel.josh-durey.workers.dev/mcp \
  -H "Content-Type: application/json" \
  -d '{
    "jsonrpc": "2.0",
    "id": 2,
    "method": "tools/call",
    "params": {
      "name": "diagnose_ai_workflow",
      "arguments": {
        "mode": "workflow",
        "org_hint": "Example Engineering Team",
        "input": "Our customer support triage agent hallucinates refund policy exceptions and lacks deterministic pre-send verification."
      }
    }
  }'
```

---

## Links & Contact

- **Web Portfolio & Live Diagnostic:** [https://jdurey.github.io](https://jdurey.github.io)
- **Interactive AI Twin Interview:** [https://jdurey.github.io/interview/](https://jdurey.github.io/interview/)
- **Author:** Joshua Durey (`Human Creative`)

## License

MIT License. See [LICENSE](./LICENSE).
