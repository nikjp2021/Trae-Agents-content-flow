# Trae-Agents-content-flow

A professional, multi-agent orchestrator for business content generation. This repository contains the core logic and agentic flow for creating platform-native content (LinkedIn, Facebook, Instagram, Threads) using a 5-step pipeline.

## 🚀 The Agentic Flow

The system uses a **Controller Agent** (`business-article-writer`) to manage a specialized pipeline:

1.  **Research** (`article-researcher`): In-depth web research and trend analysis.
2.  **Drafting** (`article-drafter`): Generation of platform-specific dialects.
3.  **Organization** (`article-organizer`): Contextual sorting and structure management.
4.  **Enrichment** (`article-enricher`): Visual hooks, emojis, and AI image prompts.
5.  **Review** (`article-reviewer`): A rigorous **13-criteria weighted scoring** system (5.0 scale).

## 📂 Repository Structure

- `/agents`: The markdown-based agent definitions and logic.
- `/samples`: Real-world outputs from the flow (e.g., "WMD Paradox" campaign).
- `Plan.md`: Roadmap for transitioning this local flow into a commercial SaaS.

## 📊 Scoring Rubric (The "Secret Sauce")

Our agents are held to a high standard using a weighted scoring model:
- **Hook, Citations, Virality** (Weighted 2x)
- **Platform Fit, Differentiation, Emojis, Structure, Length, Visuals, Context Grounding, Title Format, Alt Text Awareness, No Generic Filler** (Weighted 1x)

---
*Created with Trae IDE.*
