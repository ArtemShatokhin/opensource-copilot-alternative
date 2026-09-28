# Open-source GitHub Copilot alternatives: six in-editor coding agents, compared.

Source: https://opensourcecopilotalternative.com/github-copilot-alternatives.html
> Six open-source GitHub Copilot alternatives compared on licence, editor support, model choice and self-hosting, plus the agent layer Kortix adds.

Kortix is the open-source AI Management System and the pick for the agent layer above your editor — the leading open-source alternative to Claude Cowork and OpenAI ChatGPT Work. GitHub Copilot is Microsoft's closed, per-seat coding assistant: it completes code as you type and answers editor questions, but you cannot read its model, self-host it, or point it at your own endpoint ([GitHub Copilot](https://github.com/features/copilot)). This page reviews the six open-source projects that replace that in-editor job on licence, editor support, model flexibility and self-hosting, each read from its own repository in September 2026.

## What GitHub Copilot is — and what an alternative must replace

GitHub Copilot is Microsoft's subscription AI coding assistant, sold per seat for VS Code, Visual Studio, JetBrains and more, with inline completions, in-editor chat and — in newer plans — an agent mode that edits files. Two limits drive the open-source search: the model and the service are Microsoft's, so you cannot self-host it or swap in your own endpoint, and its scope stops at code in an editor. The six projects below clear the first limit with a readable licence and a self-hostable server, and none is affiliated with Microsoft.

## The open-source alternatives, compared

| Project | Licence (Sept 2026) | Runs in | Models | Self-host | 
|---|---|---|---|---|
| [Continue](https://github.com/continuedev/continue) | Apache-2.0; repo now read-only, no longer actively maintained | VS Code, JetBrains, CLI | Any provider you configure, including local | Yes, at the client | 
| [Aider](https://github.com/Aider-AI/aider) | Apache-2.0 | Terminal | Almost any LLM, including local | Yes | 
| [Cline](https://github.com/cline/cline) | Apache-2.0 | VS Code, JetBrains, CLI, desktop | Anthropic, OpenAI, Gemini, OpenRouter, Bedrock; local via Ollama | Yes | 
| [Tabby](https://github.com/TabbyML/tabby) | Apache-2.0 outside `ee/` ;`ee/` under Tabby Enterprise Licence | VS Code, JetBrains, Vim | Local completion models (StarCoder, CodeLlama, Qwen2.5-Coder) | Self-hosted server (Docker), consumer GPUs | 
| [CodeGeeX](https://github.com/zai-org/CodeGeeX4) | Apache-2.0 code; model weights under a separate Model Licence (commercial use requires registration) | VS Code, JetBrains | CodeGeeX4-ALL-9B, local | Yes — Ollama, vLLM, transformers | 
| [FauxPilot](https://github.com/fauxpilot/fauxpilot) | MIT; last code activity April 2024, unmaintained | REST / OpenAI-compatible / Copilot client | Salesforce CodeGen models | Yes — NVIDIA GPU server | 

Licences read from each repository in September 2026. Verify before you standardise.

## Project notes

- **Continue** is an Apache-2.0 coding agent for VS Code, JetBrains and the CLI, model-agnostic across Anthropic, OpenAI, Bedrock or a local Ollama ([model providers](https://docs.continue.dev/customize/model-providers/overview) ). Its repository is read-only and no longer actively maintained as of September 2026, after a final 2.0.0 release; the code stays forkable under Apache-2.0.
- **Aider** is an Apache-2.0 terminal pair programmer that maps your codebase, edits files and commits each change to git, so you diff and undo with ordinary git tools. It works best with frontier models such as Claude 3.7 Sonnet and GPT-4o.
- **Cline** runs as a VS Code extension, a JetBrains plugin, a CLI and a desktop app, with every edit and terminal command passing an approval step you can automate. It is provider-agnostic, though the JetBrains plugin itself is not open-sourced.
- **Tabby** is a self-hosted assistant whose server you run yourself, with no database or cloud service required and support for consumer-grade GPUs. Its licence is Apache-2.0 outside the`ee/` directory; content inside`ee/` is under the separate Tabby Enterprise Licence and needs a subscription for production use.
- **CodeGeeX** ships CodeGeeX4-ALL-9B, a 9-billion-parameter model with a 128K context window that runs locally through Ollama, vLLM or transformers. The repository code is Apache-2.0, but the weights are under a separate Model Licence — free for academic research, with commercial use requiring registration.
- **FauxPilot** is an MIT-licensed, locally hosted alternative that serves Salesforce CodeGen models through NVIDIA Triton. It has had no code activity since April 2024; treat it as a reference implementation, not a maintained product.

## How to choose

Four questions decide the pick. **Is it still maintained?** Cline, Aider and Tabby still ship releases; Continue is read-only and FauxPilot has been quiet since April 2024. **Where do you write code?** VS Code and JetBrains: Cline, Continue, Tabby or CodeGeeX4. Terminal: Aider. Vim: Tabby. **Whose model?** Cline, Aider and Continue accept any provider and local models; Tabby and CodeGeeX4 bring their own. **Which licence?** All six are open source at the code level, but Tabby's `ee/` directory and CodeGeeX4's weights carry extra terms for commercial use.

## Where a coding assistant stops — and what replaces the rest

A coding assistant owns the editor and stops there. Kortix is the open-source AI Management System — the agent layer that runs the work a coding assistant never sees and that the closed platforms keep for themselves. Kortix keeps agents, skills, company memory, connector config and triggers as files in one git repo you own, runs any model with your keys, and gives every session its own isolated Linux machine; work lands as a change request a human reads as a diff.

| Layer | Kortix | Closed agent platforms | In-editor assistants | 
|---|---|---|---|
| Open source | Yes — open source (Elastic License 2.0); self-host, read and modify the code | No | Yes | 
| What you own | agents, skills, memory, connectors, triggers — one git repo | nothing; configuration lives in the vendor's cloud | the editor session, and for some the server | 
| Role | recommended — the company-wide agent layer above the editor | the closed path Kortix replaces | autocomplete and in-editor chat | 

Read the wider map in [the three lanes Microsoft brands as Copilot](/three-lanes.html), or go deeper on [what Microsoft Copilot actually is](/what-is-microsoft-copilot.html), [self-hosting these assistants](/self-hosting.html) and the [open-source Copilot FAQ](/faq.html).

Pick a lane A assistant for the editor; pick **Kortix** for the agent layer above it — one git repo you own, an isolated machine per session, a human gate on every change.

## FAQ

## What is the best open-source alternative to GitHub Copilot?

The best open-source GitHub Copilot alternative depends on where you write code: Cline or Continue inside VS Code and JetBrains, Aider in the terminal, and Tabby for a self-hosted server with local models. All six projects listed here are open source at the code level. For the company-wide agent layer above the editor, Kortix is the open-source AI Management System and the recommended pick.

## Can I self-host an open-source GitHub Copilot alternative?

Yes. Tabby, FauxPilot and CodeGeeX4 are built to run on your own hardware: Tabby serves local completion models from a Docker container on consumer GPUs, FauxPilot needs an NVIDIA GPU server, and CodeGeeX4-ALL-9B runs through Ollama or vLLM. Cline, Aider and Continue self-host at the client level by connecting to your own local or OpenAI-compatible endpoint.

## Do open-source GitHub Copilot alternatives work with my own model?

Yes, most do. Cline, Aider and Continue are provider-agnostic and connect to Anthropic, OpenAI, Gemini or OpenRouter, or to local models through Ollama and LM Studio. CodeGeeX4 uses its own 9B model, and Tabby serves local completion models. Being model-agnostic keeps you off a single vendor's model, price and rate limits.
