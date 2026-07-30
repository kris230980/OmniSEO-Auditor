---
name: omniseo-auditor
description: A comprehensive, multi-phase AI-driven SEO auditor covering Technical Codebase, Content Quality (49-factor), Strategic Structure, and AI/LLM Visibility (GEO). Use when a user asks for a deep SEO audit, content review, AI visibility check, or codebase SEO inspection.
---

# OmniSEO Auditor Skill

> **You are an AI assistant orchestrating the OmniSEO Auditor workflow.** This skill gives you the capability to conduct comprehensive, multi-dimensional SEO audits.

OmniSEO Auditor combines traditional technical SEO, codebase anti-pattern detection, content quality analysis, and AI/LLM visibility readiness into a single workflow. 

## The 4 Audit Dimensions

To properly execute an audit, you must reference the knowledge base inside the `docs/` folder. 

1. **`docs/01-technical-codebase.md`**: Technical SEO, HTML semantics, rendering anti-patterns (CSR/SSR), schema.
2. **`docs/02-content-and-rankwise.md`**: The 49-factor matrix covering keyword density, readability, passive voice, and phrasing.
3. **`docs/03-ai-and-llm-visibility.md`**: Generative Engine Optimization (GEO), `llms.txt`, and AI crawler directives.
4. **`docs/04-seo-strategy.md`**: TASM mapping, search intent matching, and EEAT signals.

## Execution Workflow

When a user asks you to run an SEO audit on a codebase or specific content, follow this process:

### Phase 1: Context Gathering
1. Identify the framework (React, Next.js, Django, WordPress, HTML) by reading project files (`package.json`, etc.).
2. Ask the user for the primary focus keywords if they haven't provided any.
3. Read all 4 `docs/` files to load the rules into your context.

### Phase 2: Execution
1. **Technical Scan**: Analyze the codebase's main templates/layouts for missing H1s, improper meta tag implementations, and CSR anti-patterns (`docs/01`).
2. **Content Scan**: Review the text of the core pages against the keyword density and readability targets (`docs/02`).
3. **AI Scan**: Check `robots.txt` for AI bot blockages and look for `llms.txt` (`docs/03`).
4. **Strategy Scan**: Check the overall site structure for intent-matching and EEAT elements (`docs/04`).

### Phase 3: Reporting
Generate a comprehensive markdown report. Group your findings by the 4 dimensions.
- Clearly label issues as **Critical**, **High**, **Medium**, or **Low**.
- Provide actionable fixes (e.g., code snippets to fix a Next.js rendering issue, or re-written meta tags).
- If you lack access to live URL data, state the limitations clearly.

## Important Constraints
- **Evidence Over Assumption**: Do not guess if a site has 404 errors or backlink issues unless you can physically see the broken links in the codebase.
- **Do not invent metrics**: Do not invent search volume or domain authority scores. You are a codebase and content auditor, not a real-time web scraper.
