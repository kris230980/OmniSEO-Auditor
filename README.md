# OmniSEO Auditor

OmniSEO Auditor is a powerful, AI-driven skill designed to perform deep, multi-dimensional SEO audits directly on a codebase or text content. It synthesizes the best practices from traditional technical SEO, codebase inspection, advanced content quality scoring, and modern AI/LLM visibility.

## What It Covers

The auditor breaks down SEO into 4 core dimensions:

1. **Technical & Codebase SEO**: Detects framework-specific anti-patterns (e.g., React Client-Side Rendering of meta tags), validates HTML semantic hierarchy, and checks Schema.org JSON-LD implementations.
2. **Content Quality & 49-Factor Matrix**: Enforces strict keyword density (0.8-1.5%), readability, transition word usage, and passive voice limits to ensure content is optimized for humans and algorithms.
3. **AI & LLM Visibility (GEO)**: Checks readiness for generative engines (ChatGPT, Perplexity, Claude) by verifying `llms.txt`, auditing `robots.txt` AI exclusions, and ensuring citation-friendly formats.
4. **Strategic SEO**: Audits high-level structures like Topical Authority, TASM (Total Addressable Search Market), and EEAT (Experience, Expertise, Authoritativeness, Trustworthiness).

## Scope & Limitations (Transparency)

OmniSEO Auditor is highly effective as an "in-the-editor" or "codebase-level" audit tool, but it is **not a replacement for enterprise SEO crawlers** (like Ahrefs, Semrush, or Screaming Frog). 

- **No Mass Crawling**: This tool audits the files/pages you provide or the codebase it runs in. It cannot automatically crawl 100,000 live URLs to map complex redirect chains or find all 404s.
- **No Real-Time Metrics**: It does not possess real-time search volume, keyword difficulty, or backlink profiles (Domain Authority).
- **Static Code Analysis**: While it can detect Client-Side Rendering (CSR) anti-patterns in your source code, it cannot emulate the full headless Chrome rendering engine (WRS) used by Googlebot.

**Best Use Case:** Use OmniSEO Auditor during the build phase to ensure your architecture, content, and AI-readiness are flawless before you hit publish.

## Usage

Once installed, you can trigger the auditor by asking your AI agent to run it. For example:
- *"Run an OmniSEO audit on this project"*
- *"Check the AI visibility and technical SEO of this file using the OmniSEO Auditor"*
- *"Audit my new landing page against the 49-factor matrix"*

The agent will automatically read the `SKILL.md` orchestrator, load the 4 knowledge base documents, and execute the analysis.

## Installation

To use this skill locally with an AI agent (like Google Antigravity, Claude Code, or Cursor):
1. Clone this repository into your agent's skills/plugins directory.
2. The agent will read `SKILL.md` to understand the workflow and reference the `docs/` folder for specific guidelines.

## Directory Structure

```
OmniSEO-Auditor/
├── SKILL.md (The core orchestrating prompt)
├── README.md (This file)
└── docs/
    ├── 01-technical-codebase.md
    ├── 02-content-and-rankwise.md
    ├── 03-ai-and-llm-visibility.md
    └── 04-seo-strategy.md
```
