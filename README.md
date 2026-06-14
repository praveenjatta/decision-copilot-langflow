# 🤖 Decision Copilot — Multi-Agent Pipeline with LangFlow

An autonomous multi-agent decision support system built with LangFlow. Given a business decision prompt, the pipeline researches, analyzes, synthesizes, critiques, revises, and scores the output — delivering a structured, high-confidence recommendation with no human in the loop.

---

## 🧠 Pipeline Overview

**13-node multi-agent architecture:**

```
Chat Input
    ↓
Planner Agent        → Breaks the decision into research tasks
    ↓
Research Agent       → Gathers relevant information
    ↓
Analyzer (Risk Lens)       → Evaluates risks and downsides
Analyzer (Customer Lens)   → Evaluates customer/market impact
    ↓
Synthesizer Agent    → Combines all analysis into a unified draft
    ↓
Critic Agent         → Reviews the draft and identifies weaknesses
    ↓
Revisor Agent        → Rewrites the draft incorporating critic feedback
    ↓
Confidence Agent     → Scores the final recommendation (0-100)
    ↓
Chat Output
```

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| LangFlow | Visual multi-agent pipeline builder |
| OpenAI GPT-4 | LLM for all agents |
| Prompt Templates | Structured system prompts for each agent role |
| File Reader | Ingest context documents |

---

## 📁 Files

| File | Description |
|------|-------------|
| `MAO_June_7_V1.json` | LangFlow flow export — import directly into LangFlow |
| `README.md` | Project documentation |

---

## 🚀 How to Use

1. Clone or download this repo
2. Open [LangFlow](https://langflow.org)
3. Click **Import** → upload `MAO_June_7_V1.json`
4. Add your OpenAI API key to the agent nodes
5. Run the flow — enter a business decision in the Chat Input
6. The pipeline will return a structured recommendation with a confidence score

---

## 💡 Example Use Case

**Input:** "Should a 50-person e-commerce company invest in AI automation for their order fulfillment process in 2026?"

**Output:** A structured recommendation covering:
- Research findings
- Risk analysis
- Customer impact analysis
- Synthesized recommendation
- Critic review
- Revised final recommendation
- Confidence score (0-100)

---

## 🔑 Key Design Decisions

- **Dual Analyzer pattern** — Risk Lens and Customer Lens run in parallel, giving balanced perspectives before synthesis
- **Critic → Revisor loop** — Forces self-improvement before final output
- **Confidence Agent** — Adds a quantified trust score so decision-makers know how reliable the output is
- **Prompt Templates** — Each agent has a dedicated system prompt defining its role, constraints, and output format

---

## 👤 Author

**Praveen Kumar Jatta** — Senior Technical Program Manager | AI Automation Consultant

- 🌐 [jattaai.com](https://jattaai.com)
- 💼 [linkedin.com/in/praveenjatta](https://linkedin.com/in/praveenjatta)
- 🐙 [github.com/praveenjatta](https://github.com/praveenjatta)
- 📅 [Book a free discovery call](https://calendly.com/praveenjatta/free-ai-automation-discovery-call)

---

## 📄 License

MIT License — free to use and modify with attribution.
