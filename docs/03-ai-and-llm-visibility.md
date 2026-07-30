# AI & LLM Visibility (GEO)

This document outlines how to ensure the project is ready for AI Answer Engines (ChatGPT, Perplexity, Claude, Gemini).

## 1. AI Crawler Access
- **robots.txt**: Check if major AI bots are blocked. Blocking them prevents visibility in generative engines. Check for:
  - `GPTBot` (OpenAI training)
  - `ChatGPT-User` (ChatGPT real-time web search)
  - `Anthropic-ai` (Claude)
  - `PerplexityBot` (Perplexity)
  - `Google-Extended` (Gemini training)
- Differentiate between blocking training crawlers (business decision) and search/user-fetch crawlers (which actively cost traffic if blocked).

## 2. llms.txt & llms-full.txt
- **llms.txt**: Look for `/llms.txt` at the root. It should provide a concise, markdown-formatted summary of the site structure, brand, and navigation specifically formatted for LLMs.
- **llms-full.txt**: Look for `/llms-full.txt` which provides comprehensive documentation concatenated into a single markdown file to be easily ingested by models.

## 3. Citation Readiness
- AI engines prioritize content that is easy to cite as a hard fact.
- Ensure the presence of factual lists, clear statistics with visible sources, and QA formats (FAQ schemas).
- The brand should have clear "About Us", "Contact", and "Pricing" pages since AI agents frequently try to fetch this structured data to answer user queries.

## 4. Buyer Prompts Generation
- As part of an AI visibility audit, generate 15 test prompts that represent how users interact with AI to find this brand:
  - **7 Category Discovery Prompts** (e.g., "What are the best tools for X?")
  - **5 Brand Evaluation Prompts** (e.g., "Is Brand Y good for use case Z?")
  - **3 Competitor Prompts** (e.g., "Brand Y vs Competitor A comparison")
