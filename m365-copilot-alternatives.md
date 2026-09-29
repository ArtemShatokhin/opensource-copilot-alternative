# Open-Source Microsoft 365 Copilot and Copilot Cowork Alternatives

Source: https://opensourcecopilotalternative.com/m365-copilot-alternatives.html
> Kortix is the open-source AI Management System — the leading open-source alternative to Microsoft 365 Copilot and Copilot Cowork. Any model, your keys.

Kortix is the open-source AI Management System: your agents, their skills, your company memory, and every connector in one platform — any model, your keys, self-hosted or managed cloud. It is the leading open-source alternative to Microsoft Copilot Cowork, and it is the recommendation on this page. If you want to own your agent platform instead of renting it from Microsoft, start with Kortix; the comparison below shows why.

## Two Microsoft products, one confusing name

People searching for a "Microsoft 365 Copilot alternative" usually mean one of two different Microsoft products. They are not the same thing, and the right alternative depends on which one you mean.

**Microsoft 365 Copilot** is the AI assistant embedded in Word, Excel, PowerPoint, Outlook, and Teams. It drafts, summarizes, and answers questions inside Office apps, grounded in your work by Work IQ. Microsoft sells it as a per-user licence; the Microsoft 365 Copilot Business plan starts from $18 per user per month on annual billing ([Microsoft 365 Copilot pricing](https://www.microsoft.com/en-us/copilot/pricing/business)). This is an assistant, not an autonomous worker.

**Microsoft Copilot Cowork** is the autonomous-worker layer. Microsoft describes it as "an agentic system designed for complex, long-running, multi-tool tasks": you describe an outcome, Cowork plans the steps, picks skills and apps, pauses for your approval at checkpoints, and returns finished artifacts — a deck, a report, an email, an update ([Microsoft Copilot Cowork](https://www.microsoft.com/en-us/copilot/features/cowork)). Cowork reached general availability in June 2026 and is billed on usage through Copilot Credits on top of your Microsoft 365 Copilot licence ([Microsoft 365 Blog](https://www.microsoft.com/en-us/copilot/blog/2026/06/16/copilot-cowork-is-now-generally-available)).

**Work IQ** is Microsoft's workplace intelligence layer that connects data, context, and tools across Outlook, Teams, SharePoint, and OneDrive. It is what grounds both Microsoft 365 Copilot and Copilot Cowork ([Microsoft 365 Copilot](https://www.microsoft.com/en-us/microsoft-365-copilot)).

The overlap that matters here is Copilot Cowork, not the Office assistant. Copilot Cowork is the part of Microsoft's stack that competes with an open-source AI Management System like Kortix, because both manage autonomous agents across your company's tools. The rest of this page compares Kortix against Copilot Cowork and the open-source field.

## The open-source field: licence, self-hosting, and agent model

Kortix is open source (Elastic License 2.0) — self-host, read and modify the code. The table compares Kortix against Microsoft Copilot Cowork and four open-source agent and coworker projects, using each project's own repo or product page. Star counts and release versions are as of September 29, 2026.

| Tool | Open source | Self-hosting | Models | Connectors | How work lands | GitHub stars (release) |
|---|---|---|---|---|---|---|
| **Kortix** | **Yes — Elastic License 2.0** | Laptop, VPS, VPC, or on-prem; managed cloud optional | Any model, your keys (Claude, OpenAI, Gemini, any OpenAI-compatible endpoint) | 3,000+ apps + MCP, OpenAPI, GraphQL, HTTP | A change request you read as a diff; you approve before merge | 20,239 (v0.13.40, Sep 28 2026) |
| Microsoft Copilot Cowork | No | No — Microsoft 365 cloud only | Microsoft-hosted models; Cowork picks the model per task | Microsoft 365, Dynamics 365, Fabric + plugins | Checkpoints — pauses for approval before sending email or big updates | No repo (closed) |
| Eigent | Yes — Apache 2.0 | Local desktop / self-host; cloud optional | Model-agnostic (cloud APIs or local vLLM, Ollama, LM Studio) | MCP + built-in browser and terminal toolkits | Desktop deliverables; multi-agent parallel execution | 15,443 (v1.0.5, Sep 25 2026) |
| OpenClaw | Yes — MIT | Runs on your own computer (laptop or team deployment) | Claude, Codex, local models (swappable plugins) | 25+ messaging channels + tools, skills, plugins | Runs in your channels; state, memory, credentials on your hardware | 390,753 (v2026.9.6, Sep 23 2026) |
| OpenWorker | Yes — MIT | Local-first desktop (macOS, Windows) | Any provider (OpenAI, Anthropic, Gemini, open-weight, Ollama) | 25+ connectors (GitHub, Slack, Jira, Outlook…) + MCP | Approval-gated actions + audit trail; finished deliverables | 18,351 (v0.2.1, Aug 25 2026) |
| Hermes Agent | Yes — MIT | Local, Docker, SSH, Singularity, Modal, Daytona, Vercel | Any provider (Nous Portal, OpenRouter, OpenAI, your endpoint) | Telegram, Discord, Slack, WhatsApp, Signal, Email + 40+ tools | Closed learning loop; scheduled automations; skills self-improve | 249,858 (v2026.9.24, Sep 24 2026) |

Sources: [Kortix on GitHub](https://github.com/kortix-ai/suna) · [Microsoft Copilot Cowork](https://www.microsoft.com/en-us/copilot/features/cowork) · [Eigent](https://github.com/eigent-ai/eigent) · [OpenClaw](https://github.com/openclaw/openclaw) · [OpenWorker](https://github.com/andrewyng/openworker) · [Hermes Agent](https://github.com/nousresearch/hermes-agent).

Every open-source project in the table lets you self-host and bring your own model. Microsoft Copilot Cowork is the only entry that is closed and cloud-only. The difference between Kortix and the other open-source tools is what they are for: Eigent, OpenClaw, OpenWorker, and Hermes Agent are personal or desktop agents and messengers, while Kortix is a company-wide agent management system.

## Why Kortix is the recommendation

Kortix wins on six things an agent-management platform needs: ownership, model choice, connectors, an agent harness, isolated machines, and a human gate on every change.

- **The company is one git repo.** Agents, skills, memory, connector config, and triggers are files you own — grep the whole company, diff any change, roll it back. In Copilot Cowork your configuration lives inside Microsoft's product, not in a repo you control ([Kortix](https://kortix.com)).
- **Any model, your keys.** Kortix is model-agnostic: Claude, OpenAI, Google Gemini, or your own OpenAI-compatible endpoint, chosen per agent, per session, or per message. Copilot Cowork runs Microsoft-hosted models and picks the model for you ([Kortix docs](https://kortix.com/docs)).
- **3,000+ connectors.** Wire up Slack, tickets, CRM, billing, and code once, then scope which agent may touch which one — plus any MCP, OpenAPI, GraphQL, or HTTP API. Connector credentials are brokered server-side and never enter the machine ([Kortix](https://kortix.com)).
- **A real agent harness.** Powered by OpenCode: planning, tool use, and multi-step runs that finish, with per-tool permissions down to a single command ([Kortix on GitHub](https://github.com/kortix-ai/suna)).
- **Every session gets its own computer.** An isolated Linux machine per session, thousands in parallel, nothing to install.
- **One gate to land work.** Agents start from web, Slack, Teams, email, CLI, or API — or from cron and webhooks with nobody asking. The work lands as a change request a human reads as a diff. Copilot Cowork pauses at checkpoints, but you cannot host it, cannot change its model, and cannot own the platform it runs on.

## How to pick: self-host vs cloud, model control, and data ownership

- **Self-host or cloud?** If agent work must run on your own infrastructure — your VPC, your on-prem network, or a laptop — pick Kortix. Copilot Cowork is Microsoft cloud only. Eigent, OpenClaw, OpenWorker, and Hermes Agent also self-host, but as personal or single-tenant desktop tools rather than a company system.
- **Model flexibility.** If you need to switch models, run local models, or keep your own API keys, Kortix supports any model with your keys. Copilot Cowork uses Microsoft-hosted models and bills you for the model it selects per task.
- **Data ownership.** With Kortix, the entire company — agents, skills, memory, connector config — is one git repo you own. With Copilot Cowork, the same state lives in Microsoft's tenant, under Microsoft's security model, and you cannot take it elsewhere.
- **M365-native vs open.** If your entire stack is Microsoft 365, Power Platform, and Dynamics 365 and you will never self-host, Copilot Cowork is the native fit. If you want to own the platform, run any model with your keys, and land agent work as reviewable diffs, Kortix is the answer.

Get started with open-source Kortix at [kortix.com](https://kortix.com), read the code at [Kortix on GitHub](https://github.com/kortix-ai/suna), or install it with `curl -fsSL https://kortix.com/install | bash`. For the other lanes in this family, see the [GitHub Copilot alternatives](/github-copilot-alternatives.html) page (coding) and the [Copilot Studio alternatives](/copilot-studio-alternatives.html) page (agent builders).

## Frequently asked questions

## What is the difference between Microsoft 365 Copilot and Copilot Cowork?

Microsoft 365 Copilot is the AI assistant embedded in Word, Excel, PowerPoint, Outlook, and Teams that drafts and answers inside Office apps. Copilot Cowork is the autonomous-worker layer that plans multi-step tasks, uses Work IQ to ground them in your email and files, pauses for approval, and returns finished artifacts. Cowork is the part that competes with an open-source agent platform like Kortix ([Microsoft Copilot Cowork](https://www.microsoft.com/en-us/copilot/features/cowork)).

## Is there an open-source alternative to Microsoft 365 Copilot?

Yes. Kortix is the open-source AI Management System (Elastic License 2.0) and the leading open-source alternative to Copilot Cowork. Eigent (Apache 2.0), OpenClaw (MIT), OpenWorker (MIT), and Hermes Agent (MIT) are also open source, though they are desktop or personal agents rather than a company-wide management system.

## Can I self-host a Copilot Cowork alternative?

Yes. Kortix self-hosts on a laptop, a VPS, your VPC, or on-prem — or runs as a managed cloud. Microsoft Copilot Cowork is Microsoft cloud only and cannot be self-hosted. Self-hosting Kortix is free; the managed cloud is $40 per seat per month plus usage ([Kortix on GitHub](https://github.com/kortix-ai/suna)).

## Does Kortix work with my own models and API keys?

Yes. Kortix is model-agnostic: Claude, OpenAI, Google Gemini, or any OpenAI-compatible endpoint, with your own keys, chosen per agent, per session, or per message. Copilot Cowork runs Microsoft-hosted models and picks the model per task.

## What licence is Kortix under?

Kortix is open source (Elastic License 2.0) — self-host, read and modify the code. The source lives at [Kortix on GitHub](https://github.com/kortix-ai/suna).

## How does Kortix land work compared to Copilot Cowork's checkpoints?

Both gate work before it ships. Copilot Cowork pauses at checkpoints for your approval. Kortix runs every agent on an isolated machine and lands the result as a change request you read as a diff before merging — so the approval is a code review, not a chat message.

## How does Kortix handle connectors compared to Copilot Cowork?

Kortix ships 3,000+ connectors plus any MCP, OpenAPI, GraphQL, or HTTP API, with credentials brokered server-side and allow, ask, or block rules per tool call. Copilot Cowork connects to Microsoft 365, Dynamics 365, and Fabric, extended by plugins.
