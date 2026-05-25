# SASS-CONTENT: Commercial SaaS Roadmap

## **Product Vision**
Transform the local `business-article-writer` agentic flow into a multi-tenant SaaS platform that automates high-quality, platform-native business content creation.

---

## **Core Engine Architecture**
The platform will utilize the 5-step agentic pipeline currently running locally:
1.  **Research** (`article-researcher`): Web-search and trend analysis.
2.  **Drafting** (`article-drafter`): Generation of platform-specific dialects.
3.  **Organization** (`article-organizer`): Contextual sorting and structure.
4.  **Enrichment** (`article-enricher`): Emojis, hooks, and AI image prompts.
5.  **Review** (`article-reviewer`): 9-criteria weighted scoring (5.0 scale) with auto-fix loops.

---

## **Technical Stack**
- **Frontend:** Next.js (React) for a responsive, dashboard-style UI.
- **Backend:** FastAPI (Python) for high-performance agent orchestration.
- **State Management:** LangGraph to manage the agentic flow and feedback loops.
- **Database:** Supabase (PostgreSQL) for multi-tenant data, user auth, and scoring history.
- **AI Models:** GPT-4o / Claude 3.5 Sonnet (for reasoning) + DALL-E 3 / Midjourney (for enrichment).

---

## **Development Roadmap**

### **Phase 1: Foundation (API & Data)**
- Design the **Database Schema** in Supabase to handle users, teams, and article history.
- Build the **FastAPI wrappers** for the existing local agents.
- Implement **Multi-tenant isolation** to ensure data security.

### **Phase 2: Agentic Orchestration**
- Port the current flow to **LangGraph** for better state persistence.
- Refine the **9-Criteria Reviewer** to provide JSON-structured feedback for the frontend.
- Implement the **Auto-Fix Loop** (if score < 4.0, trigger automatic drafting retry).

### **Phase 3: User Experience**
- Build the **Next.js Dashboard** to visualize the pipeline progress.
- Create an **Editor Interface** where users can see scores and manually override AI suggestions.
- Add **Export/Post** functionality for LinkedIn, FB, Threads, and Instagram.

---

## **Scoring Rubric (The "Secret Sauce")**
The platform will differentiate itself via the **9-criteria weighted rubric**:
- **Weighted 2x:** Hook, Citations, Virality.
- **Weighted 1x:** Platform Fit, Differentiation, Emojis, Structure, Length, Visuals.
- **Formula:** `Points = (H×2 + C×2 + V×2 + T×1 + D×1 + E×1 + S×1 + L×1 + F×1)`
- **Final Score:** `(Points ÷ 60) × 5.0`

---

## **Next Steps**
When we resume, we will begin with **Phase 1: Database Schema Design** in Supabase to track multi-tenant article storage and scoring history.
