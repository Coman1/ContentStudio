# Aviva IWR — Knowledge Studio · POC Demos

Interactive proof-of-concept demos for the **Aviva Investments, Wealth & Retirement (IWR) Knowledge Studio** — a platform for ingesting, curating, evaluating and distributing operational knowledge for both AI agents and human handlers.

> **These are design and concept demos.** No real data, no live systems, no Aviva infrastructure. Everything runs locally in your browser — no server, no account, no install needed.

---

## 🚀 Quick start — two ways to open the demos

### Option 1 — GitHub Pages (recommended, no setup)

If this repository has GitHub Pages enabled, visit:

```
https://<your-github-username>.github.io/aviva-knowledge-studio/
```

The landing page links to both demos.

### Option 2 — Run locally

```bash
git clone https://github.com/<your-github-username>/aviva-knowledge-studio.git
cd aviva-knowledge-studio
```

Then open either HTML file directly in your browser:

```
knowledge-ingestion-tool.html   ← Demo 1
knowledge-studio.html           ← Demo 2
```

No build step, no dependencies, no server. Pure HTML/CSS/JS.

---

## 📁 What's in this repo

| File | Description |
|------|-------------|
| `index.html` | Landing page — links to both demos with context |
| `knowledge-ingestion-tool.html` | Demo 1 — Knowledge Ingestion Tool MVP |
| `knowledge-studio.html` | Demo 2 — Full Knowledge Studio |
| `README.md` | This file |

---

## 🔍 Demo 1 — Knowledge Ingestion Tool

The ingestion tool is the **foundation layer** — it connects to existing knowledge sources, extracts and normalises content, and stores it as the single source of truth for agents and published pages.

**What you can explore:**

- **Dashboard** — live alerts from the evaluation pipeline, knowledge health by domain, pending approvals
- **Ingestion** — connected SharePoint sources, PDF and Word upload, live pipeline log, add a new source
- **Knowledge store** — all knowledge files with domain, version, sensitivity and eval status
- **Editor** — WYSIWYG editing with version history, linked agent warnings, and Arize AX trace panel
- **Evaluations** — golden dataset Q&A, failing eval detail, Arize experiment push
- **Arize AX** — tracing, guardrails, monitor alerts, experiments, annotation queue
- **Access & RBAC** — role and permission management, Entra ID SSO
- **Audit log** — immutable activity record with export

**Demo story:** A GAD rate change in a pensions knowledge file has caused an accuracy failure in the evaluation suite. The publish gate is blocking the update. Follow the trail from the dashboard alert → ingestion → knowledge store → editor → evaluations → Arize → audit log.

---

## 🏗️ Demo 2 — Knowledge Studio

The studio expands the platform into a full **content environment** — where knowledge is not just stored but curated, trained from, and continuously improved.

**What you can explore:**

- **Dashboard** — all studio activity in one place, knowledge gaps, certification progress
- **Ingestion** — same ingestion pipeline as Demo 1, embedded in the studio
- **Knowledge store + Editor** — with AI conflict detection badge and training module links
- **Curation studio** — knowledge gap queue (from Arize failures), conflict detection, freshness scores, readability scoring
- **Training builder** — module cards with progress, AI assessment bank, conversation simulator
- **Certifications** — Pensions certification pathway, handler status, learning analytics
- **Agent lab** — prompt playground with chunk retrieval inspector, A/B testing, agent configuration, guardrail builder
- **Evaluations** — same eval suite, now connected to training and curation
- **Arize AX** — full observability panel
- **Published pages** — human-readable guide preview
- **Reviews & sign-off** — structured review workflow, SME portal, compliance export
- **Access & RBAC**, **Audit log**

**Demo story:** The same GAD rate conflict runs through every layer — dashboard alert → curation conflict detection → editor → training module sync warning → agent lab retrieval inspector → evaluations → Arize → compliance export.

---

## 🎨 Design

Built to Aviva ION design system standards using the **Investments, Wealth & Retirement** colour palette:

| Token | Hex | Usage |
|-------|-----|-------|
| Navy | `#191D64` | Primary brand, headers, buttons |
| Yellow | `#FFD900` | Accent, CTAs, stat highlights |
| Dark teal | `#00596B` | Secondary brand, active states |
| Light teal | `#CDEBEE` | Surface, domain pills |
| Arize purple | `#6C47FF` | Arize AX integration panels |

---

## 📋 Background

These demos were built to support the **IWR AI workstream** product development process — specifically the Content and Accuracy project within the Ada (Aviva Digital Assistant) programme.

They illustrate the requirements set out in:
- *Knowledge Ingestion Tool — MVP Requirements v0.2*
- *Knowledge Studio — Content Studio MVP Requirements v0.1*

### Platform scope (IWR MVP)
- **Pensions** — drawdown, annual allowance, LTA, MPAA, vulnerable customers
- **Wealth** — ISA limits, portfolio rebalancing, adviser suitability
- **Health & Protection** — Phase 3, subject to Compliance confirmation

### Technology illustrated (not prescribed)
The demos illustrate capabilities. Technology choices for the actual build are defined separately in the architecture documentation.

---

## ⚠️ Important notes

- All data in these demos is **fictional** — no real customer, colleague, or Aviva data is used
- These demos are for **internal stakeholder communication and concept validation** only
- They do not represent committed product decisions or confirmed technology choices
- Arize AX panels illustrate the planned integration approach — not a live connection

---

## 🔗 Related

- [Arize AI — Generative AI observability](https://arize.com/generative-ai/)
- [Aviva ION Design System](https://standards.aviva.com)
