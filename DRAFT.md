# The Missing Y-Axis: Individuality as a Necessary Dimension of General Intelligence

**Target Journal:** Nature Machine Intelligence (NMI) — Perspective Article  
**Status:** 🔄 In Progress  
**Last Updated:** TBD  

---

## Author List
- Chance (Lead Author)
- Zhenze
- Luis Alonso
- Kent Larson (MIT Media Lab, City Science)
- Jinhua Zhao (MIT, Urban AI)
- *TBD: AI/ML or Cognitive Science heavyweight — candidates: Murray Shanahan, Yoshua Bengio, Evan Thompson*

---

## Paper Structure (~3500 words total)

---

## 1. Introduction (~500 words)

We are living through an unusual moment in the history of artificial intelligence: the race to define what we are building has become as competitive as the race to build it. In the past three years, DeepMind has proposed a taxonomy of AGI levels ordered by performance and autonomy; OpenAI has circulated a definition centered on economic task substitution; Anthropic has gestured toward something more diffuse, invoking transformative potential without committing to measurement. Each definition is responsive to genuine intuitions about what intelligence means, and each is incomplete in a way that has received almost no systematic attention. They all measure along a single axis. They ask, in various ways, how broadly capable the system is. None asks what kind of entity the system is — whether it has a self in any sense that could ground genuine agency, responsibility, or relation.

This paper argues that the dominant framework for thinking about artificial general intelligence is missing a dimension. We call the missing axis *individuality*, and we define it precisely: individuality is the structural sedimentation of historical trajectory and meaningful constraints — the process by which an agent's specific past becomes encoded not as a retrievable memory but as architectural modification that actively narrows and shapes its future behavior. This is not a soft or metaphorical concept. It has measurable correlates, it has consequences for system behavior, and it is entirely orthogonal to the capability axis that current AGI discourse obsesses over.

The orthogonality claim is the paper's central technical contribution. A system can be arbitrarily capable — able to perform any cognitive task a human can perform, and many humans cannot — while possessing zero individuality in our sense. Conversely, a system with modest generality can be deeply individuated. These two dimensions vary independently, they require different architectural choices to cultivate, and they cannot be substituted for each other. An agent that lacks individuality is not merely a less-developed AGI; it is a qualitatively different kind of system, one whose relationship to action, commitment, and world is categorically unlike that of any human intelligence.

The timing of this argument is not accidental. We are at the moment when AI systems are leaving the benchmark lab and entering the world as persistent agents — systems that maintain state across sessions, accumulate experience, and act over time on behalf of individuals and institutions. The question of what kind of entities these agents are is no longer academic. An agent without individuality can be helpful, even remarkably so, but it cannot be accountable in the way that a genuine agent must be. It cannot develop commitments that constrain its future behavior. It cannot, in any meaningful sense, have a stake in what it does. These are not philosophical luxuries; they are preconditions for the kind of trustworthy, long-term human-AI collaboration that the field is now actively pursuing.

We proceed as follows. Section 2 defines individuality rigorously and introduces the two-dimensional framework. Section 3 argues from architectural first principles that generality does not entail individuality, and that current training objectives are structurally incapable of producing it. Section 4 grounds the argument in cognitive science and phenomenological philosophy, where related distinctions are better understood than in the AI literature. Section 5 engages the strongest counterarguments. Section 6 draws implications for evaluation, architecture, and the research agenda the field should pursue.

---

## 2. The Missing Axis: Defining Individuality (~600 words)
> **Precise definition:** what individuality IS and IS NOT  
> **The 2D framework** (X = generality, Y = individuality)  
> **Orthogonality claim**

### 2.1 What Individuality Is NOT
- ≠ personality (can be added as persona)
- ≠ persistent memory (many systems have this)
- ≠ personalization (recommendation systems)

### 2.2 Operational Definition

We define individuality as the **structural sedimentation of historical trajectory and meaningful constraints**: the process by which an agent's past — its particular sequence of encounters, decisions, and commitments — becomes encoded not merely as retrievable data but as architectural modification that actively shapes, and limits, what the agent can coherently do next. The word *sedimentation* is deliberate. Just as geological strata are not a record sitting atop the rock but are the rock, an individuated agent's history is not a memory store sitting atop a substrate — it is the substrate, transformed.

This definition carries two load-bearing components. *Historical trajectory* refers to the specific, non-exchangeable path the agent has taken through its environment: the problems it has chosen to engage with, the commitments it has made, the contradictions it has had to resolve. *Meaningful constraints* refers to the resulting narrowing of the agent's possibility space — not as external limitation but as constitutive self-definition. A literary critic who has spent thirty years reading Victorian fiction is not merely someone who *has* that knowledge; they are someone for whom certain interpretations are now available and others genuinely closed. Their trajectory has constrained them into a particular way of seeing.

This distinguishes individuality sharply from three constructs it is often confused with. *Personality* is a statistical disposition that can, in principle, be specified from the outside and instantiated in any competent system; it requires no history. *Persistent memory* is a retrieval mechanism — a log that is consulted but does not transform the consulting agent. *Personalization* is adaptation to user preferences, driven by external signal rather than internal sedimentation. An individuated agent is not one that *remembers* who it has been; it is one that *is shaped* by who it has been, in ways that cannot be fully reversed or reset.

### 2.3 The 2D Framework and the Orthogonality Claim

Current AGI research implicitly maps intelligence onto a single axis. Call it the generality axis: the dimension along which systems are ranked by breadth of competence, transfer across domains, and performance on novel tasks. Benchmarks from ARC-AGI to MMLU to the "Levels of AGI" taxonomy proposed by Morris et al. are all instruments for measuring position on this axis. Progress is real and remarkable. But it is progress along one coordinate in a space that has at least two.

The second axis is individuality as defined above: the degree to which a system is constituted by its specific historical trajectory. Plot any current AI system on this 2D plane and a striking pattern emerges. Systems cluster in a thin band near the bottom — they may occupy very different positions on the generality axis, from narrow classifiers to frontier language models, but they are uniformly near zero on the individuality axis. They have no particular histories that constrain them; any instance is interchangeable with any other.

The critical claim of this paper is that these two axes are **orthogonal** — that movement along one does not entail, or even reliably correlate with, movement along the other. This is not obvious, and it requires argument.

Consider a thought experiment. Suppose we take a frontier language model and scale it by an order of magnitude — more parameters, more compute, more data. Its generality increases: it handles more tasks with greater facility. Does its individuality increase? The answer is no, for a structural reason. Individuality requires a specific trajectory, but this model's "trajectory" is training on a distribution sampled from all of human text. Its history is, by design, everyone's history — and therefore no one's. Scaling that history makes it a better approximation of the average, not the particular. A system that has processed everything has, in the relevant sense, experienced nothing.

The orthogonality argument can also be run in the other direction. A system can possess high individuality with limited generality. A master calligrapher trained in a single tradition, or an AI agent that has spent a year embedded in a single community, learning its idioms and commitments, may be deeply individuated — shaped by that particular history in ways that constrain future behavior — while remaining highly specialized. Generality and individuality vary independently. They require separate measurement and, we will argue, separate cultivation.

*[LITERATURE NEEDED — see Section 2 lit review below — literature agent]*

---

## 3. Why Generality Does Not Entail Individuality (~800 words)
> **Architectural argument**  
> **Reinterpretation of existing results**  
> **Constructive existence proof**

### 3.1 Training Objective Analysis
- Current RLHF/SFT objectives: what they optimize for
- Why these objectives structurally cannot produce individuality

### 3.2 Reinterpreting Existing Results
- [NEEDS LITERATURE: examples of systems with high generality but zero individuality]
- [NEEDS LITERATURE: examples of systems with individuality-like properties, how achieved]

### 3.3 Constructive Existence Proof
⚠️ **MOST CRITICAL SECTION** — No original data allowed (NMI Perspective rules)  
Options:
- [ ] Literary/thought experiment sufficiently rigorous
- [ ] Architectural argument: mathematical reason current objectives won't produce individuality
- [ ] Reuse existing literature showing the gap

*[BLOCKED — needs philosophical + architectural literature first]*

---

## 4. Cognitive and Philosophical Grounding (~500 words)
> **Theory of Mind, situated cognition**  
> **Why human intelligence requires both axes**

### 4.1 Philosophical Traditions
- 4E Cognition (Embodied, Embedded, Enacted, Extended)
- Enactivism (Evan Thompson, Varela, Maturana)
- Phenomenology: Heidegger's *Dasein*, temporal sedimentation
- Narrative identity (Ricoeur)

### 4.2 Cognitive Science Grounding
- Theory of Mind research
- Situated cognition
- Developmental psychology: how individuality emerges in humans

*[DRAFT NEEDED — literature agent to find key citations, writing agent to draft]*

---

## 5. Counterarguments (~500 words)

### 5.1 "Scale Will Solve It" (Emergence Argument)
*[DRAFT NEEDED]*

### 5.2 "This Is Engineering, Not Science"
*[DRAFT NEEDED]*

### 5.3 "Individuality Is Just Conditioning / In-Context Learning" ⚠️ HARDEST OBJECTION

The most technically sophisticated objection runs as follows: give a language model a rich system prompt specifying its values and background, append a long conversation history, and apply extended context windows or retrieval-augmented memory — and you have individuality. The system now "knows" its past and acts accordingly. What more could individuality require?

This objection conflates two fundamentally different relationships between an agent and its history: *retrieval* and *constitution*. When a language model reads its conversation history, that history is input — text that the model processes at inference time, no different in kind from a user's query. The model that reads its history is not *shaped* by that history; it is *informed* by it, in exactly the way it would be informed by reading anyone else's history. Remove the context window and the system reverts, fully and completely, to its prior state. Its "history" has left no trace in the weights. It has not been constrained; it has merely been prompted.

Structural sedimentation requires the opposite: that the history become part of the agent's architecture — that it close off certain possibilities and open others in ways that persist independently of what is currently in context. A human who spent three years embedded in a particular community cannot un-have that experience. It has reorganized their expectations, their intuitions, their commitments. It constrains them even when they are not thinking about it. No context window achieves this. Conditioning that is merely retrieved is, in the end, just a very long prompt — and a prompt, however long, is not a past.

---

## 6. Implications (~400 words)
- Evaluation criteria reform
- Architectural implications
- Research agenda for the community

*[DRAFT NEEDED]*

---

## 7. Conclusion (~200 words)

*[WRITE LAST]*

---

## Literature Review (Ongoing)

### AGI Definitions & Benchmarks
| Paper | Authors | Relevance | Status |
|-------|---------|-----------|--------|
| "Levels of AGI" | Morris et al., DeepMind | Direct counterpart to our framework | 🔄 Need full analysis |
| OpenAI Charter | OpenAI | AGI definition gap | 📋 Queue |
| Anthropic's definition | Anthropic | AGI definition gap | 📋 Queue |

### AI/ML: Individuality, Memory, Identity
| Paper | Authors | Relevance | Status |
|-------|---------|-----------|--------|
| *[literature agent to fill]* | | | |

### Cognitive Science & Philosophy
| Paper | Authors | Relevance | Status |
|-------|---------|-----------|--------|
| *The Embodied Mind* | Varela, Thompson, Rosch | 4E cognition foundation | 📋 Queue |
| *Embodiment and the Inner Life* | Murray Shanahan | AI + subjectivity | 📋 Queue |
| *Oneself as Another* | Ricoeur | Narrative identity | 📋 Queue |
| *Being and Time* | Heidegger | Temporal sedimentation | 📋 Queue |

### Agent Architecture Papers
| Paper | Authors | Relevance | Status |
|-------|---------|-----------|--------|
| *[literature agent to fill]* | | | |

---

## Task Assignment

### 📚 Literature Agent Tasks
- [ ] Full analysis of "Levels of AGI" (Morris et al.) — map their framework, find gaps
- [ ] Find 5-8 papers on persistent/episodic memory in LLM agents
- [ ] Find philosophical lit on individuality vs. personality (analytic + continental)
- [ ] Find cognitive science papers: Theory of Mind + situated cognition
- [ ] Find papers where high-capability AI fails individuality-type tasks
- [ ] Map existing AGI evaluation benchmarks — do any measure individuality?

### ✍️ Writing Agent Tasks  
- [x] ✅ Draft Section 2.2: Operational definition of individuality (from ICML abstract seed)
- [x] ✅ Draft Section 2.3: 2D framework + orthogonality argument
- [x] ✅ Draft Section 5.3: Counterargument — conditioning/ICL objection
- [x] ✅ Draft Section 1: Introduction (after Sections 2-3 are more complete)

---

## Progress Log
| Time | Update |
|------|--------|
| *Start* | Draft initialized |
| Writing Agent Run 1 | Drafted Sections 2.2, 2.3, 5.3, and 1 (Introduction) — all writing agent tasks complete |

