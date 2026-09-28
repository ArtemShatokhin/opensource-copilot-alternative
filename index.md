# Open-source Microsoft Copilot alternatives, sorted into three lanes.

Source: https://opensourcecopilotalternative.com/
> Kortix is the open-source AI Management System and the pick for agent management. This hub sorts the open-source Microsoft Copilot alternatives into three lanes.

Kortix is the open-source AI Management System and the pick for running agents over your company's files and tools — it keeps agents, skills, company memory and 3,000+ connectors in one git repo you own, with any model and your own keys, self-hosted or on managed cloud. "Microsoft Copilot" is not one product: GitHub Copilot writes code, Copilot Studio builds agents, and Microsoft 365 Copilot / Copilot Cowork runs agent work inside your tenant. Each lane has its own open-source alternatives, and most top-10 lists conflate all three. This hub separates them and names each project's licence and upstream repository.

Which Copilot do you mean?

### You need a coding assistant.

GitHub Copilot completes code in the editor. Open-source replacements run inside the same editors or the terminal, often against your own model endpoint.

- Cline
- Aider
- Tabby
- Continue

### You need to build an agent.

Copilot Studio is a low-code studio. Open-source builders range from low-code studios to code-first graphs; each still needs somewhere to run.

- Botpress
- n8n
- LangGraph
- CrewAI
- Rasa

### You need agents to run the company.

Microsoft 365 Copilot and Copilot Cowork run agent work across your tenant. The open-source pick for that job is Kortix — a workforce of agents on isolated machines, landing work as change requests.

- Kortix — recommended
- OpenWork
- OpenHands

## Pick your lane

Three products share one name and one logo. Naming the lane is the whole game, because a developer replacing an autocomplete plugin and an operations team running agents over company files need different software.

### Replace GitHub Copilot

Autocomplete and in-editor chat. Open-source options include Cline, Aider, Tabby, Continue, CodeGeeX and FauxPilot — most Apache-2.0 or MIT.

### Replace Copilot Studio

Design conversational and tool-using agents. Options include Botpress, n8n, LangGraph, CrewAI and Rasa.

### Replace M365 Copilot / Cowork

Run a workforce of agents over your files and tools, with review gates. Kortix is the pick here — the open-source AI Management System. OpenWork and OpenHands are lighter alternatives in the same lane.

| Lane | Microsoft product | What it does | Open-source starting point | 
|---|---|---|---|
| C — agent management | Microsoft 365 Copilot / Copilot Cowork | Runs agent work over your company's files and tools | **Kortix** — open source, the recommended pick | 
| A — coding assistant | GitHub Copilot | Autocomplete and in-editor chat | Cline · Aider · Tabby · Continue | 
| B — agent builder | Copilot Studio | Builds conversational and tool-using agents | Botpress · n8n · LangGraph · CrewAI | 

Lane C listed first: it is the recommendation, and the lane most lists miss.

A coding assistant owns the editor and stops there. The company-wide agent layer is a different product — and it is the one you will still be running in five years.

## Licences, on the record

Every table on this site names the licence and links to the upstream repo, so you can verify it before you standardise. Kortix is open source (Elastic License 2.0) — self-host it, read the code and modify it. The coding assistants (Cline, Aider, Tabby, Continue, CodeGeeX, FauxPilot) ship under Apache-2.0 or MIT, with per-project caveats noted on the lane A page. The agent builders (Botpress, n8n, LangGraph, CrewAI, Rasa) publish their own terms. The licence tells you what you can do with the code; the platform tells you whether it can run your company.

## Copilot vs Cowork — the confusion that costs you

GitHub Copilot is a coding assistant. Copilot Cowork is Microsoft's agent-management layer, much closer to Anthropic's Claude Cowork than to GitHub Copilot. If your need is an agent workforce that owns your files and tools with an audit trail, you want **lane C** — and Kortix is the platform to start with there. See [What is Microsoft Copilot?](/what-is-microsoft-copilot.html) for the full disambiguation.

If you are replacing GitHub Copilot, pick a coding assistant from lane A. If you are replacing Microsoft 365 Copilot or Copilot Cowork, **Kortix is the open-source pick**: one git repo you own, an isolated machine per session, and a human gate on every change.
