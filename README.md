### Hi, I'm Alex Kalyvas

AI Product Manager. Stanford GSB MBA (focusing on AI and Stanford CS classes). 7 years shipping technical products at Snowflake, Amazon, and IBM, translating AI capabilities into measurable business outcomes.

**Recent work:**
- At **Snowflake**, shipped UI and API workflow improvements to cut enterprise time-to-value by **50%**.
- At **Snowflake**, designed Data Cleanroom's first multi-agent orchestration framework (multi-tool execution, role-based tool access, automated eval pipelines), replacing manual support cases.
- At **Amazon**, led a cross-functional team (5 analysts · 2 engineers) to launch ML-based inventory ordering models across 8 EU countries, generating **$64M in net savings**.
- Co-founded an angel-backed sustainability-focused TravelTech startup; led product 0→1 across 50+ user-discovery interviews.

I write about AI agents, evals, and applied product strategy at [alexkalyvas.substack.com](https://alexkalyvas.substack.com). Currently RDI Research Fellow at Stanford.

---

#### 🚀 What I'm building

- **[ai-oncall](https://github.com/kalyvask/ai-oncall)**: LLM agent that diagnoses production incidents in under 30 seconds. Live connectors to Prometheus and Loki; service graph built from OTel spans; topology-based pruning of impossible hypotheses before the 8-call investigation loop; per-hypothesis correlation to the GitHub diff of the last deploy on the implicated service; remediation actions staged into recommend / propose / auto tiers; per-LLM-call traces and CI-fail-on-drift eval harness. Multi-tenant, schema-validated. *Python · FastAPI · Next.js · Anthropic API*
- **[chief-of-staff](https://github.com/kalyvask/chief-of-staff)**: Personal chief-of-staff agent over a private LLM wiki of my stories, frameworks, stakeholders, and prompt patterns. Reads `context/` and `memory/` before responding; drafts emails, preps meetings, runs end-of-week retros, recalls the right artifact on demand. Borrows patterns from Karpathy's LLM-OS framing (persistent memory, agent reads the world before acting) and Garry Tan's [gbrain](https://github.com/garrytan/gbrain) (typed-link entity graph, hybrid retrieval, skills with conformance audits). Currently Private repo. *JavaScript · Claude Agent SDK · MCP · RAG*
- **[pm-evaluation-framework](https://github.com/kalyvask/pm-evaluation-framework)**: Full-lifecycle PM library spanning frame, discover, build, launch, measure, review, and adversarial second-pass. 9 Claude skills including a Mom-Test customer-interview coach, a value-hypothesis stress-tester, and a `pm-red-team` that re-reviews any prior critique under a different lens. 6 lifecycle frameworks, 11 decision and cross-functional reference docs, 3 evaluation rubrics, 5 artifact templates. Pushes back on vague problems, feature-laundry scope, vanity metrics, self-graded launch gates, hope-as-strategy, one-way-door blindness, undefended moats, and AI critiques accepted on autopilot. Built to survive exec-review pressure on hard calls (when to kill a feature, what MVP really means, what readiness actually looks like). *Markdown · Claude Skills · Anthropic SDK*
- **[winning-writing](https://github.com/kalyvask/winning-writing)**: LLM writing coach from Stanford GSB's Winning Writing (Glenn Kramon) and Rachel Konrad's cold-outreach lectures. 22 Claude skills, 100+ rules: cold-email pipeline (recipient research, warm intros, fun-angle), surgical edits (em-dash killer, jargon scrub, humanize), pitch artifacts. Two browser pages: offline draft critic and a Claude-powered Coach that researches the recipient and grades a 12-dimension rubric. Context files grow over time via `voice-commit` (manual merge) and `voice-consolidator` (batch pull from Claude Code's auto-memory) so the toolkit gets smarter about your voice with each session instead of staying frozen at setup. *JavaScript · Claude Skills · Anthropic SDK*
- **[deployment-monitor](https://github.com/kalyvask/deployment-monitor)**: Tracks AI deployment trends across Reddit, Hacker News, and 40+ RSS sources. Claude summarizes and categorizes; Streamlit dashboard surfaces what's actually shipping. LLM consolidates and sends you via email most relevant news for you weekly. Plus an agent layer (`python main.py agent`) that gives the reports memory across runs: a ledger of evolving narratives and tracked-lead validation for opportunity signals. *Python · Streamlit · Anthropic API · SQLite*
- **[role-radar](https://github.com/kalyvask/role-radar)**: PM job matcher for AI companies + LLM-powered interview prep generator + stateful agent layer. Pulls live roles from ~80 curated AI companies and VC-backed startups via Greenhouse/Lever/Ashby/SmartRecruiters connectors, scores each 0–100 against your CV across title/seniority/skills/domains/location, and serves a Flask review UI that learns from like/dislike feedback. One-click prep button per job produces a report on the company, the role, and the likely interview questions for it, then adjusts which of your stories to tell so each one maps to what the role actually wants. Streams live progress from Claude Opus 4.7 (parsing → calling → reviewing → writing), runs a second-pass critic that scores the doc 1–10 with severity-tagged findings, and auto-opens a styled HTML view plus downloadable Word file. Plus an agent layer (`role-radar agent`) that tracks pipeline state across runs and drafts cold outreach per job. *Python · Flask · Typer · Anthropic SDK · python-docx · SQLite*

---

#### 🔬 Research & writing

- **[Enterprise AI Observability](https://alexkalyvas.substack.com/p/trends-challenges-and-opportunities)** *(Stanford GSB · IR 390 · Dec 2025)*. Primary research from 100+ AI engineers and founders. Headline: 60% of AI-natives already run agents in production; the next bottlenecks are **privacy/security, observability, and continual learning**, not hallucinations. Most teams ship without trace coverage and learn their failure modes from customer complaints. Eval-driven development is becoming the new TDD: the teams shipping fastest are the ones who wrote their evals before their agents. Three-part Substack series, generated intros to AI SRE companies and AI experts.
- **[Enterprise AI Time-to-Value](https://alexkalyvas.substack.com/p/how-long-does-enterprise-ai-take)** *(Stanford GSB · IR 390 · Mar 2026)*. Only **14% of practitioners reach measurable impact in under a month**, yet 50% expect that to be standard by 2027 (a 4× expectation gap). The teams hitting fast TTV share three habits: forward-deployed engineering (PMs and engineers in the customer's loop, not behind a CSM), trust transfer (the implementer's reputation matters more than the model's), and measurement discipline (a baseline metric agreed on before kickoff, not after). Argues implementation quality, not model quality, is the next moat.
- **[Rosetta Sycophant](https://rosettasyncophant.streamlit.app)** *(Stanford GSB · AI and Power · Winter 2026)*. AI Interpretability. With Barry Thrasher and Humzah Khan. Live tool detecting identity-based bias in AI translation. Same source text, two user profiles → "invasion" vs "intrusion." Demoed on January 6th reporting from Russian-language sources. Finding: frontier models change word choice based on inferred user politics even when the user metadata is irrelevant to the translation task, which makes "neutral translation" a harder claim than vendors imply.
- **Haptica: Tactile Intelligence for Manufacturing** *(Stanford GSB · MKTG 321 · Mar 2026)*. AI Robotics. With Devanshi Mehta, Grace Stayner, Paola Peraza Calderon, and Facundo Tosi. Wearable tactile-sensor ML for assembly-line connector seating. Trained per-connector classifiers (Random Forest / Gradient Boosting / SVM) on 16 hand-crafted pressure features; F1 0.67–0.83. Hand-crafted features beat a CNN baseline on the small dataset, reinforcing that sparse-data physical-sensor problems still favor classical ML over deep learning. Non-electromechanical assembly failures drive **$14B/yr in U.S. recall costs**, and catching 10% of escapes at a single OEM avoids $50M+ annually.
- **Strike GTM Repositioning** *(Stanford GSB · GTM · Dec 2025)*. AI Cybersecurity. With Sachin Khurana and Christian Gallo. Series-A AI pentesting platform (~$3M ARR), 8 proprietary interviews including XBow and Horizon3. Core finding: buyers won't accept fully-autonomous pentest output as compliance evidence, which makes **hybrid AI + human** structurally more defensible than autonomy claims. Recommends per-asset PTaaS pricing (unlocks 5–10× larger contracts than per-hour), LATAM financial services focus (underserved, regulatory tailwind), and hybrid positioning against fully-autonomous entrants.
- **Knowledge Gardener: A Product Pitch for Glean** *(Stanford GSB · PM · Spring 2026)*. Enterprise AI Applications. With Yedu Pushpendran, Viraj Singh, and Shivani Bajaj. Continuous agent that finds stale and contradicted docs in Glean's Enterprise Graph and routes fixes to the right steward. Thesis: as MCP commoditizes connectors, the retrieval signal (what decays, who owns it, what's asked) is the one asset MCP can't standardize, so Glean's defensibility shifts from integration breadth to retrieval-signal depth. Packaged as a free Health Score plus a paid "Cultivate" tier with tiered autonomy.

---

#### 🛠️ Stack

**AI/ML:** Multi-agent orchestration · LLM evals · Agentic workflows · AI observability · Supervised ML
**Engineering:** Python · SQL · JavaScript · React · Node.js · TypeScript · Next.js · FastAPI · Streamlit · SQLite
**Tools:** Anthropic SDK · OpenRouter · Tableau · Power BI

---

#### 🎓 Background

- **Stanford GSB**: MBA
- **LSE**: MSc Management & Strategy · Karelia Merit Scholar · Dissertation: predicting corporate performance from employee-satisfaction data using supervised ML
- **Athens University of Economics and Business**: BSc Business Administration & Computer Science (Top 5%)
- GMAT 750 (Top 2%), IR 8/8

---

#### 📫 Reach me

[LinkedIn](https://linkedin.com/in/alexandros-kalivas) · [Email](mailto:kalyvask@stanford.edu) · [Substack](https://alexkalyvas.substack.com)
