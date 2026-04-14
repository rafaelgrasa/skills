# inference.sh skills

AI agent skills for 250+ models via [inference.sh](https://inference.sh) CLI. Generate images, videos, call LLMs, search the web, and more.

![inference.sh](https://cloud.inference.sh/app/files/u/4mg21r6ta37mpaz6ktzwtt8krr/01kgvqa60jjrqa47j3g5s6ce6v.jpeg)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Esta fork — **Prospect 360 B2B** (instalar a partir daqui)

Este repositório (**[rafaelgrasa/skills](https://github.com/rafaelgrasa/skills)**) é um fork público de `inference-sh/skills` e inclui a skill extra **[prospect-360-b2b](tools/llm/prospect-360-b2b/)** (pesquisa de prospect e preparação de reuniões B2B).

**Quem entra nesta página e quer só esta skill:** no terminal, rode **nesta ordem**:

| Ordem | Comando |
|-------|---------|
| **1º** | `npx skills add rafaelgrasa/skills@prospect-360-b2b -g -y` |
| **2º** | `npx skills add inference-sh/skills@web-search -g -y` |

*(O 1º baixa **deste** GitHub; o 2º instala a dependência obrigatória `web-search`, que continua no repo oficial.)*

Documentação detalhada: **[tools/llm/prospect-360-b2b/README.md](tools/llm/prospect-360-b2b/README.md)**.

---

## Contents

- [Esta fork — Prospect 360 B2B](#esta-fork--prospect-360-b2b-instalar-a-partir-daqui)
- [Install as Claude Code Plugin](#claude-code-plugin)
- [Install as Skills](#install-as-skills)
- [CLI Setup](#cli-setup)
- [Available Skills](#available-skills)
- [Documentation](#documentation)

---

## Claude Code Plugin

Install all skills as a Claude Code plugin:

```bash
/plugin install inference-sh
```

Or add from GitHub:

```bash
/plugin marketplace add inference-sh/skills
/plugin install inference-sh@inference-sh-skills
```

After install, skills are available as `/inference-sh:flux-image`, `/inference-sh:google-veo`, etc.

---

## Install as Skills

### All Skills

```bash
npx skills add inference-sh/skills
```

### Specific Skills

**Prospect 360** a partir **deste fork** (use `rafaelgrasa/skills`, não `inference-sh`, até o PR ser merged no upstream):

```bash
npx skills add rafaelgrasa/skills@prospect-360-b2b -g -y
npx skills add inference-sh/skills@web-search -g -y
```

Outras skills (catálogo oficial):

```bash
npx skills add inference-sh/skills@flux-image
npx skills add inference-sh/skills@google-veo
npx skills add inference-sh/skills@llm-models
npx skills add inference-sh/skills@web-search
```

Depois de **prospect-360-b2b** existir no `inference-sh/skills`, o 1º comando poderá ser também `npx skills add inference-sh/skills@prospect-360-b2b -g -y`.

### Manual

```bash
cp -r tools/* ui/* sdk/* guides/* ~/.claude/skills/
```

---

## CLI Setup

> Requires inference.sh CLI (`infsh`). [Install instructions](https://raw.githubusercontent.com/inference-sh/skills/refs/heads/main/cli-install.md)

```bash
infsh login
```

Browse apps: `infsh app list`

---

## Available Skills

### Tools

| Skill | Description |
|-------|-------------|
| [ai-image-generation](tools/image/) | 50+ image models (FLUX, Gemini, Reve, etc.) |
| [ai-video-generation](tools/video/) | 40+ video models (Veo, Seedance, Wan, etc.) |
| [llm-models](tools/llm/) | Claude, Gemini, Kimi, GLM |
| [prospect-360-b2b](tools/llm/prospect-360-b2b/) | B2B prospect research & sales meeting prep |
| [web-search](tools/llm/) | Tavily, Exa search |
| [twitter-automation](tools/social/) | X/Twitter API |

### SDKs

| Skill | Description |
|-------|-------------|
| [javascript-sdk](sdk/javascript-sdk/) | JS/TS SDK with streaming, tools, React |
| [python-sdk](sdk/python-sdk/) | Python SDK with async, streaming |

### UI Components

| Skill | Description |
|-------|-------------|
| [agent-ui](ui/agent-ui/) | Full agent interface |
| [chat-ui](ui/chat-ui/) | Chat components |
| [tools-ui](ui/tools-ui/) | Tool call/result rendering |

### Guides

| Category | Topics |
|----------|--------|
| [prompting](guides/prompting/) | Prompt engineering, video prompts |
| [design](guides/design/) | Landing pages, thumbnails, logos |
| [video](guides/video/) | Storyboards, explainers, ads |
| [writing](guides/writing/) | Blogs, case studies, newsletters |
| [social](guides/social/) | LinkedIn, Twitter threads, carousels |
| [product](guides/product/) | Competitor analysis, personas, launches |

---

## Documentation

- [Getting Started](https://inference.sh/docs/getting-started/introduction)
- [Running Apps](https://inference.sh/docs/apps/running)
- [CLI Setup](https://inference.sh/docs/extend/cli-setup)
- [API & SDK](https://inference.sh/docs/api/overview)

**Links:** [Website](https://inference.sh) | [App Store](https://app.inference.sh) | [Docs](https://inference.sh/docs) | [Blog](https://inference.sh/blog)
