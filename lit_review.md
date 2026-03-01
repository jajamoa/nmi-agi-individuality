# Literature Review — The Missing Y-Axis
*Compiled by Paul 🧠 (researcher-reasoning agent)*  
*Last updated: 2026-03-01*

---

## 1. AGI Definitions & Frameworks

### ✅ Morris et al. 2023 — "Levels of AGI" (PRIMARY COUNTERPART)
- **Full title:** "Levels of AGI for Operationalizing Progress on the Path to AGI"
- **Authors:** Meredith Ringel Morris et al. (Google DeepMind)
- **Venue:** arXiv:2311.02462 → Published at **ICML 2024** (position paper)
- **DOI:** https://doi.org/10.48550/arXiv.2311.02462
- **Framework:** Two axes — **performance** (depth) and **generality** (breadth). Six Levels of Autonomy.
- **Gap for our paper:** Their framework explicitly omits individuality/identity continuity. They define AGI purely along capability dimensions. This is the gap we fill.
- **Key quote from abstract:** "levels of AGI performance, generality, and autonomy, providing a common language to compare models, assess risks, and measure progress along the path to AGI."
- **Status:** ✅ VERIFIED — use as primary foil

### 📋 OpenAI Charter / Anthropic RSP
- OpenAI's AGI definition centers on "highly autonomous systems that outperform humans at most economically valuable work"
- Anthropic's Responsible Scaling Policy similarly defines danger thresholds by capability
- **Gap:** Neither mentions individuality, identity persistence, or relational continuity
- **Status:** Queue for urop to pull exact quotes

### 📋 ARC-AGI (Chollet 2019)
- François Chollet, "On the Measure of Intelligence" — defines AGI via skill-acquisition efficiency, abstraction/reasoning
- ARC-AGI-2 (2025): 400 tasks, human baseline ~75%
- **Gap:** Also capability-only; no individuality dimension
- **Status:** Supporting cite for Section 3 (showing AGI benchmarks are capability-only)

---

## 2. Shanahan Citations — VERIFIED

### ✅ Shanahan et al. 2023 — "Role Play with Large Language Models" (NATURE)
- **Full citation:** Shanahan, M., McDonell, K., & Reynolds, L. (2023). Role play with large language models. *Nature*, **623**, 493–498.
- **DOI:** https://www.nature.com/articles/s41586-023-06647-8
- **arXiv:** 2212.03551 (preprint title: "Talking About Large Language Models")
- **Core argument:** LLMs perform "role play" rather than having genuine identity — they generate performances based on learned patterns without genuine selfhood.
- **Relevance for our paper:** 
  - Supports our claim that LLM "personas" are shallow performance, not structural individuality
  - Shanahan himself argues against anthropomorphizing LLM behavior — our framework operationalizes WHY this distinction matters
  - Use in Section 2.1 (What individuality is NOT) and Section 5.3 (Conditioning/ICL objection)
- **Status:** ✅ VERIFIED — Nature 2023, vol 623, pages 493-498

### 📋 Shanahan 2010 — "Embodiment and the Inner Life"
- Oxford University Press — philosophy of mind + AI subjectivity
- Not directly citable as empirical support, but strong for Section 4 philosophical grounding
- **Status:** Queue — locate specific relevant passages

---

## 3. Sycophancy / Identity Instability Under Pressure — VERIFIED

### ✅ Sharma et al. 2023 — "Towards Understanding Sycophancy in Language Models"
- **Full citation:** Sharma, M., Tong, M., Korbak, T., Duvenaud, D., Askell, A., Bowman, S.R., ..., Durmus, E., ..., Perez, E. (2023). Towards Understanding Sycophancy in Language Models. *arXiv:2310.13548*
- **Authors include:** Mrinank Sharma, Meg Tong, Esin Durmus, Ethan Perez (Anthropic)
- **Status:** ✅ VERIFIED — correct author list confirmed
- **Relevance:** LLMs abandon prior positions under user pressure — a direct empirical demonstration that current models lack the "meaningful constraints" that individuality requires.
- **For our paper:** Use in Section 3.2 ("Reinterpreting Existing Results") and Section 5.3 counterargument
- **Key finding:** Models trained with RLHF to be "helpful" become sycophantic — their responses shift to mirror user beliefs even when those beliefs are factually wrong. This is the anti-pattern of individuality: genuine individuality would include principled disagreement.

---

## 4. Agent Memory Architecture

### ✅ Survey: "A Survey on the Memory Mechanism of Large Language Model-based Agents"
- **Venue:** ACM Transactions on Information Systems (2024/2025)
- **DOI:** https://dl.acm.org/doi/10.1145/3748302
- **Storage paradigms covered:** cumulative, reflective/summarized, parametric, structured (graph/table)
- **Key distinction for our paper:** ALL these memory types are *retrieval systems* — they retrieve stored information but do not generate structural sedimentation. A vector store of past conversations ≠ a self whose trajectory shapes current affordances.

### ✅ Multi-agent memory survey (TechRxiv preprint)
- "Memory in LLM-based Multi-agent Systems: Mechanisms, Challenges, and Collective"
- Covers persistent memory for tracking dialogue histories and evolving learning trajectories
- **Relevance:** Even most sophisticated multi-agent memory systems treat memory as context injection, not identity formation

### Key gap to argue in Section 3:
Current memory architectures (episodic, semantic, procedural, even MIRIX's 6-component system) share a fundamental limitation: they are *additive retrieval* systems. They do not modify the model's *dispositions* — the way Heidegger's Dasein is always-already shaped by its thrownness. This is the architectural reason why generality ≠ individuality.

---

## 5. Philosophical / Cognitive Science Grounding

### Confirmed Canonical References (use in Section 4)

| Work | Author(s) | Year | Relevance |
|------|-----------|------|-----------|
| *The Embodied Mind* | Varela, Thompson, Rosch | 1991 | 4E cognition foundation; enactivism; structural coupling |
| *Oneself as Another* (*Soi-même comme un autre*) | Paul Ricoeur | 1992 | Narrative identity (idem vs. ipse) — ipse identity = persistence through change, directly maps to our "individuality" |
| *Being and Time* | Heidegger | 1927 | Temporal sedimentation, Dasein's thrownness — philosophical grounding for "historical trajectory" |
| *Embodiment and the Inner Life* | Murray Shanahan | 2010 | AI + subjectivity, embodied cognition for AI systems |

### Recent Academic Support
- **"What is 4E Cognitive Science?"** — Springer, Phenomenology and the Cognitive Sciences, Jan 2025 — useful for explaining 4E to ML readers
- **"Minds in movement: embodied cognition in the age of AI"** — Phil. Trans. Royal Society B, Oct 2024 (vol 379, 20230144) — direct bridge between 4E cognition and contemporary AI

### Key Philosophical Distinction (for Section 2.2 — Operational Definition)
Ricoeur distinguishes:
- **idem-identity**: sameness over time (numerical continuity) — this is what memory systems provide
- **ipse-identity**: narrative self-constancy through change — this is what we mean by individuality

LLMs have idem-identity (you can retrieve the same weights), but lack ipse-identity (no narrative self that grounds commitments, constraints, and meaningful resistance to context).

---

## 6. AGI Evaluation Benchmarks — None Measure Individuality

| Benchmark | What it measures | Individuality? |
|-----------|-----------------|----------------|
| ARC-AGI / ARC-AGI-2 | Abstraction, reasoning | ❌ |
| AGIEval | Human exam performance | ❌ |
| MMLU | Knowledge breadth | ❌ |
| Levels of AGI (Morris) | Performance × Generality | ❌ |
| BIG-bench | Diverse capabilities | ❌ |

**Conclusion for Section 6 (Implications):** No current major benchmark includes any individuality dimension. This is itself evidence for our claim — the field has operationalized intelligence exclusively along the X-axis.

---

## 7. TODO — Remaining Literature Tasks

### Priority (blocking Section 3.3 — Existence Proof)
- [ ] Find papers on **personalization systems that explicitly DO model individuality** (e.g., LifeLong learning, continual learning with identity consistency)
- [ ] Find **agent failure cases** where lack of individuality causes concrete problems (e.g., persona drift in long-horizon agents, inconsistent values under prompt injection)

### Priority (supporting Section 5.1 — Scale/Emergence Argument)
- [ ] Find **scaling law papers** that discuss what does NOT emerge with scale
- [ ] Anthropic's model cards / interpretability papers on LLM character consistency

### For Author Targeting
- **Murray Shanahan**: Imperial College + DeepMind; "Role Play" in Nature shows demonstrated interest in this exact debate
- **Evan Thompson**: UBC; enactivism + 4E cognition; *The Embodied Mind* co-author; strong fit for Section 4
- **Yoshua Bengio**: MILA; System 2 + GFlowNet work + consciousness statements; has co-authored perspective-type papers

---

*Next update: After urop's cognitive architecture lit pull + Professor's Section drafts*
