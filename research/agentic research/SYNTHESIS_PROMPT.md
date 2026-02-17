# Ember Agentic Education Platform — Synthesis Prompt

> **Instructions**: Run this prompt with the four agentic research documents attached as input context. Optionally, also attach the K-12 Market Scan and Innovative Research-Backed Approaches documents for richer grounding.

---

## Input Documents (Required)

1. **ChatGPT — Deep Research Report** (`ChatGPT - deep-research-report.md`)
2. **Claude — Compass Artifact** (`Claude - compass_artifact...md`)
3. **DeepSeek — Research** (`Deep-Seek-Research.md`)
4. **Gemini — Agent Frameworks for Personalized EdTech** (`Gemini - Agent Frameworks for Personalized EdTech.md`)

## Supplementary Context (Recommended — attach if context window allows)

5. **K-12 EdTech Market Scan** (`AI-Driven - K-12 EdTech Market Scan.md`) — 60+ company competitive landscape
6. **Innovative Research-Backed Approaches to K-12 Education** (`Innovative Research-Backed Approaches to K‑12 Education.md`) — Academic evidence base

---

## Prompt

You are a senior AI systems architect, education technology strategist, and learning science researcher. You have been provided with four independent deep research reports analyzing agentic AI frameworks — specifically OpenClaw, Pi, and Kimi Claw — and their applications to education technology.

Your task is to synthesize these four reports into a single, cohesive architectural blueprint for **Ember**: an AI-native education operating system being built for a pilot deployment at a school in Lisbon, Portugal.

This is not a product spec. It is a research-grounded exploration of **how agentic AI architecture can be applied to deliver personalized, per-student, per-course curriculum at scale** — and what it would take to bring that to life in a real school.

---

### Context: What Ember Is

Ember is an **education operating system** — not a school brand. Schools run *on* Ember. The Lisboan (the pilot school) doesn't become Ember; it runs on Ember. This is a platform, not a product.

The model compresses core academics (maths, literacy, science, etc.) into a **2-hour AI-tutored mastery block** each morning, freeing the rest of the school day for creativity, emotional intelligence, and human-led development. It is being built by a three-party partnership:

- **The Lisboan** — A progressive school in Lisbon providing the physical learning environment and student cohort
- **BGA (Brave Generation Academy)** — Operational and curriculum backbone. BGA already operates 53+ hubs across 12 countries (40+ in Portugal) with British and American accredited curricula via Pearson and eCampus. They use Learning Coaches (not teachers), self-directed asynchronous LMS, and serve 1,000-1,400 learners. BGA is a ready-made distribution network for Ember.
- **WE3** — The AI systems builder (venture studio) responsible for designing and deploying the agentic platform

**Critical framing**: Ember's agents operate during the **morning mastery block only**. The afternoon is screen-free, human-led, and focused on project-based learning, creativity, collaboration, and EQ development. However, the system understands the **full day** through a handoff-and-feedback loop: morning agents produce briefs that inform the guide's afternoon decisions, and guide observations from the afternoon feed back into the student profile overnight. This means the OS has a whole-child view without putting screens in front of kids all day.

### The Academic Foundation

Ember's approach is grounded in established educational research, not just tech optimism:

- **Bloom's 2-Sigma Problem (1984)**: 1:1 tutoring produces a 2 standard deviation improvement — the average tutored student performs above 98% of conventionally taught students. Mastery learning alone yields 1 sigma (84th percentile). Bloom's challenge: find group instruction methods as effective as 1:1 tutoring. **This is the problem Ember's agentic system is designed to solve.**

- **Pomodoro / Structured Focus Research (Ogut 2025)**: Structured 20-25 minute work intervals with breaks yield ~20% lower fatigue, higher concentration, and 10-18% engagement boosts. Grounded in Cognitive Load Theory and Self-Regulated Learning theory. This directly informs the 2-hour block structure.

- **AI Tutor Efficacy (Kestin et al. 2025)**: RCT evidence showing carefully designed AI tutors outperform active-learning classrooms on learning gains and time-on-task, with higher student engagement and motivation.

- **Flow States and Creativity (Wang et al. 2025)**: Students who frequently experience flow in class show significantly higher creativity and problem-solving. The 2-hour mastery block should be designed to induce and sustain flow.

- **SEL and Academic Outcomes (Ha et al. 2025)**: Meta-analysis of 33,000+ students confirms SEL programs produce measurable academic gains (effect size ~0.10) across literacy and math. Investing in EQ development pays off academically — validating Ember's afternoon model.

- **Project-Based Learning and Creativity (Albar & Southcott 2021)**: PBL "immensely arouses" creative processes — exploration, risk-taking, experimentation, resilience. Validates the afternoon half's project-based, collaborative design.

- **Montessori Outcomes (Randolph et al. 2023)**: Montessori students outperform peers on creativity (g ≈ 0.26), executive function (g ≈ 0.36), and academics. Child-centered, exploratory learning works.

- **Alpha School / Two Hour Learning**: Real-world implementation claiming 2.3x learning per year, 99th percentile test scores, using AI-guided mastery + human guides + afternoon life skills. Demonstrates the model is operationally viable, but with caveats (high tuition $40-75K, unverified efficacy claims, Pennsylvania charter denial).

### The Competitive Landscape

The K-12 AI personalized learning market is projected to reach $9.2B by 2034 (37-38% CAGR). The market segments into 7 archetypes:

1. **Teacher Copilot Tools** (MagicSchool AI: 6M teachers, Brisk Teaching: 1M teachers) — Low friction, weak outcome proof
2. **AI Tutoring Companions** (Khan Academy Khanmigo: 160M learners, Amira Learning: ESSA Tier 1) — Growing evidence base
3. **Adaptive Learning Platforms** (DreamBox: ESSA "Strong", Carnegie Learning: 30% improvement) — Enterprise grade, high friction
4. **Content Generation Tools** (Curipod, Teachy) — Supplemental
5. **School-in-a-Box** (LEAD School: $1.1B unicorn, 9K schools; Alpha School; BGA) — **This is Ember's archetype**
6. **Regional Democratization** (PhysicsWallah: $3.7B, profitable) — Emerging markets
7. **LMS Integration Layers** (Clever, Canvas) — Infrastructure

**Key competitive insight**: The market's ideal position (low friction + strong outcome proof) is nearly empty — only Khan Academy and Amira occupy it. Evidence has become the new moat: ESSA "Strong" certification requires 2+ years and $500K-2M. Ember should plan for evidence generation from day one.

**Where Ember sits**: Archetype 5 (School-in-a-Box) but with a twist — it's a platform OS, not a school brand. Closest competitors are Alpha School (US, high-tuition, no agentic architecture), LEAD School (India, affordable private schools, no AI agents), and BGA itself (which becomes a partner, not competitor).

### The Core Question

**Can we build an agentic platform that tailors individual curriculums for each student on a course-by-course basis?**

Each student would have a personalized learning path through every subject — adapting in real time to their pace, comprehension, knowledge gaps, and learning style — all orchestrated by a system of collaborating AI agents. The goal is to **operationalize Bloom's 2-sigma finding**: deliver the equivalent of 1:1 tutoring through a multi-agent system, at the cost structure of group instruction.

### The Design Philosophy

Draw from these principles throughout the synthesis:

- **"Happiness over results" is a design principle**, not a soft answer. It differentiates Ember from Alpha (who optimize for MAP scores). The hard question: how do you measure "unlocking potential"? Mastery velocity is easy. Confidence, agency, spark — that's the measurement challenge.
- **AI should amplify teachers and students, not replace them.** The guide's role shifts from lecturing to mentorship, emotional support, and ensuring "every kid truly loves school."
- **Education is a human system before it is a technical one.** Most EdTech failures come from misunderstanding incentives, constraints, and child development — not from bad technology.
- **European values as genuine differentiator** — not just GDPR compliance, but a philosophical stance on child development, data sovereignty, and the role of technology in learning.
- **The afternoon half is the novel piece** — Human-led, screen-free development (wellbeing, creativity, EQ, project-based learning), not just "stuff that isn't academics." The morning agents inform it via guide handoffs; guide observations feed back overnight. The OS understands the full day, but agents only run during the morning block.

---

### What the Synthesis Should Produce

Organize your output into the following sections:

---

#### 1. Converging Insights: What the Research Agrees On

Identify the key themes, architectural patterns, and conclusions that appear across multiple (or all four) research reports. Where do these independent analyses converge? What can we treat as emerging consensus in the agentic AI space that Ember should build on?

Specifically address convergence on:
- Persistent agent identity (SOUL.md patterns)
- Minimalist toolset philosophy (Pi's 4-tool approach)
- Bot-to-bot communication as infrastructure, not experiment
- The shift from "model capability" to "framework design" as the breakthrough
- Security risks that are severe and unresolved

---

#### 2. Ember Agent Architecture: A Proposed Multi-Agent System

Drawing from the frameworks analyzed in the research (OpenClaw's persistent identity and bot-to-bot communication, Pi's minimalist toolset philosophy, the layered architecture models), propose a concrete multi-agent architecture for Ember.

Use the four-layer model from the Gemini research as a starting scaffold:

| Layer | Purpose |
|---|---|
| **Identity Layer** | Persistent SOUL.md / USER.md — who the agent is, who the student is |
| **Logic Layer** | Minimal toolset (Read, Write, Edit, Execute) — what the agent can do |
| **Focus Layer** | Pomodoro flow management, attention monitoring, session structure |
| **Social Layer** | Bot-to-bot protocols, agent coordination, guide communication |

Then define these specific agents:

- **Student Agent**: A persistent, per-student agent that holds the learner's profile — not just academic progress, but learning style preferences (visual/auditory/kinesthetic, per Howard Gardner's Multiple Intelligences), emotional state indicators, interests, strengths, and aspirations. Acts as the student's **advocate** in the system. When a student has mastered 80% of a level, the Student Agent autonomously unlocks the next. Structure its identity using USER.md patterns: productivity patterns, peak performance windows, hyperfocus detection, ADHD accommodations if needed.

- **Subject Agents**: Per-course agents (Maths Agent, Literacy Agent, Science Agent, etc.) that own the curriculum logic, generate lessons, assess mastery, and adapt difficulty. Must be aligned to BGA's accredited curriculum standards (Pearson British / eCampus American). These agents should:
  - Maintain persistent memory of each student's subject-specific profile (concepts mastered, error patterns, learning modalities) — think `Student_Math_Profile.md`
  - Communicate with each other via the **"Cabinet Meeting" pattern**: coordinating homework loads (reduce science homework when a maths exam approaches), orchestrating interdisciplinary projects (climate change unit where Science, Maths, Literacy, and History agents each contribute), transferring skills across subjects
  - Follow Pi's minimal tool philosophy: Read (access texts/assignments), Write (generate explanations, quizzes, prompts), Edit (provide Socratic feedback), Schedule (interact with academic calendar)

- **Orchestration / Flow Agent**: Manages the 2-hour learning block using a modified **20/2 Pomodoro structure** (20 min focused work, 2 min break — adapted from Ogut 2025 evidence). Specifically:
  - Defines granular task objectives for each interval
  - Monitors a `NOW.md` log — if flow state is detected, extends the interval (up to 40-50 min)
  - Enforces system lock-down during focus periods (silences notifications, blocks distractions)
  - Prompts diffuse-mode activities during micro-breaks (stretching, movement)
  - After 6 cycles, enforces a 30-45 min long break
  - Escalates to Guide Agent when a student is stuck, disengaged, or emotionally struggling

- **Guide Agent**: Surfaces actionable insights to human guides. The guide's role is mentor, coach, and emotional anchor — not instructor. This agent should:
  - Provide a "helicopter view" dashboard highlighting anomalies, breakthroughs, and recommended interventions per student
  - Compile synthesized daily/weekly reports — not raw data dumps
  - Flag specific moments for human intervention (a student who's been stuck for 10+ minutes, emotional distress signals, breakthrough moments worth celebrating)
  - Support the guide in one-on-one check-ins by surfacing talking points

- **Curriculum Planning Agent**: Works on longer time horizons (weekly/monthly/term). Must:
  - Plan learning arcs that ensure curriculum coverage against BGA's accreditation requirements
  - Rebalance when students fall behind or race ahead
  - Maintain alignment with external assessment calendars
  - Generate reports for parents (simplified, actionable: "What did my child work on today? What was the biggest challenge? How can we support this weekend?")
  - Interface with the Institutional Agent role (ensuring equity, removing barriers to student success)

- **Morning-to-Afternoon Handoff** (not a separate agent — a capability of the existing agents): The afternoon is **screen-free and human-led**. There is no agent running during the afternoon. Instead, at the end of each morning mastery block, the Student Agent and Subject Agents produce a **guide-facing handoff brief** — a short synthesis for the human guide summarizing:
  - Academic highlights and struggles from the morning session
  - Observed strengths and emerging interests (e.g., "strong spatial reasoning in geometry — might thrive in a building/making project")
  - Emotional state indicators (frustration, confidence, energy level)
  - Suggested afternoon approaches (not prescriptions — the guide decides)

  The guide uses this to shape the afternoon, but the afternoon itself is fully unplugged: project-based learning, collaboration, creativity, movement, EQ development — no screens, no agents.

  At the end of the day, guides log brief observations back into the system (a simple input form, not a complex tool): "Maria led a team building project, showed strong collaboration, was energized after a frustrating morning reading segment." These human observations are ingested overnight into the Student Agent's profile, so the next morning's session reflects the **whole child** — not just test scores. This feedback loop is what makes Ember an OS for the full day, even though agents only operate during the morning block.

For each agent, specify:
- Core responsibilities
- Minimal toolset (following Pi's philosophy)
- Data/memory it maintains (file patterns)
- Communication protocols with other agents
- Identity/persona considerations (especially for student-facing agents working with children)

---

#### 3. The Student Journey: A Day in the Life

Walk through **two concrete scenarios** showing how the full system works:

**Scenario A — Morning Mastery Block**: A 10-year-old working through a maths mastery unit who is strong in maths but struggling with reading comprehension. Show:
- How the session starts and the Orchestration Agent sets up the block
- How the Maths Subject Agent selects and adapts content
- How the Student Agent's profile influences decisions (this student learns best with visual/spatial approaches)
- How a struggle moment is detected when a word problem's reading level exceeds the student's comprehension
- How the Maths Agent and Literacy Agent coordinate (Cabinet Meeting) to adjust the word problem's language level without reducing mathematical rigor
- How the Flow Agent manages Pomodoro timing, detects flow state during a geometry exercise, and extends the interval
- How the Guide Agent alerts the human guide when the student needs encouragement after a frustrating reading segment
- How the session data feeds back into the Curriculum Planning Agent

**Scenario B — The Full Day Arc** (morning block → handoff → afternoon → next morning): Show how the system bridges the screen-on and screen-off halves of the day **without running agents in the afternoon**:
- End of the morning block: the agents produce a handoff brief for the guide. The same student's spatial strength is flagged, along with the reading frustration.
- The guide (human, no screens) uses this to pair the student with a building project in the afternoon and arranges a reading buddy.
- At the end of the day, the guide logs brief observations: "Led the building team, high energy, reading buddy session went well — she chose to keep reading for 10 extra minutes."
- The next morning, the Student Agent's profile reflects both the academic data AND the guide's afternoon observations. The Literacy Agent adjusts — maybe the reading buddy approach suggests a social/collaborative modality for reading practice in the next session.
- Show how this daily loop builds a richer, whole-child picture over weeks and months.

---

#### 4. Identity, Memory, and Persistence

One of the most compelling patterns across the research is persistent agent identity (OpenClaw's SOUL.md). For Ember, this has profound implications — these agents will work with children over months and years, accumulating deep understanding of each learner.

Address:

- **Student profile structure**: What should USER.md contain for a child? Learning style (Multiple Intelligences profile), productivity patterns (morning peak vs afternoon peak), emotional indicators, interests and aspirations, social dynamics, family context (without overreach). How does this differ from an adult's USER.md?

- **Memory accumulation and pruning**: OpenClaw's pattern of daily notes (YYYY-MM-DD.md) with periodic consolidation into long-term memory. For education: daily learning logs consolidate into weekly summaries, which feed termly assessments. The agent's memory should mimic how a good human tutor remembers — knowing that Maria struggled with fractions in October helps when percentages come up in February.

- **The "growing with the child" challenge**: A 7-year-old's agent persona should be different from a 14-year-old's. How does SOUL.md evolve as the child develops? When should the agent's communication style shift?

- **Privacy and data protection**: GDPR for minors in the EU (Article 8: parental consent for data processing of children under 16; member state derogation to 13). EU AI Act considerations — educational AI may fall under "high-risk" classification requiring conformity assessments. Data minimization: what's the minimum data needed for effective personalization?

- **Transitions**: Student moves schools (data portability), ages out of the system, changes courses. The agent's accumulated knowledge is valuable — how is it transferred, archived, or deleted?

- **Ethical dimensions**: AI agents building long-term relationships with children raises questions no EdTech company has fully answered. What are the attachment risks? How do you prevent over-reliance? What's the role of the human guide as emotional anchor vs. the AI as learning companion? Reference the Charlotte Mason educational philosophy (mentioned in the project's research) — technology as tool, not master.

---

#### 5. Technical Stack and Protocol Choices

Based on the research's analysis of available frameworks and protocols, recommend a technical approach for Ember's first pilot. Address:

- **Framework choice**: OpenClaw, Pi, custom, or hybrid? Consider that Pi's minimalist philosophy (4 tools, sub-1000 token system prompt) may be ideal for education — maximum context window for actual content, minimal token waste. But OpenClaw's persistent identity and social layer add critical capabilities. Propose a pragmatic architecture.

- **Communication protocols**: A2A (Google's agent-to-agent — 50+ partners) for inter-agent communication, MCP (Anthropic's agent-to-tool — 97M monthly SDK downloads) for agent-to-tool connections. How do these map to Ember's needs?

- **LLM selection per agent role**: Not all agents need frontier models. The Orchestration/Flow Agent might run on a lightweight local model (via Ollama on Mac Mini M4 — low power, quiet, school-friendly). Subject Agents generating content need stronger models (Claude, GPT-4o). Curriculum Planning Agent needs long-context reasoning. Map cost/latency/capability trade-offs per agent.

- **Infrastructure**: The Gemini research proposes two modes:
  - **Local Model Mode**: Zero API fees via Ollama, limited to 7B/8B parameter models
  - **API Cloud Mode**: Local device handles execution, calls frontier models via API for complex reasoning
  - For a school: what's the right mix? Network reliability, student data locality, cost per student per month?

- **Integration**: How does Ember connect to BGA's existing LMS, Pearson curriculum materials, and parent communication channels? The WAB (Western Academy of Beijing) case study shows successful AI integration using MagicSchool, Diffit, and audience-specific guidance — what can Ember learn from this?

- **Security**: The research flags severe unresolved risks — OpenClaw's 512 vulnerabilities, Moltbook's database exposure. For a system handling children's data, security is existential. Gartner rated OpenClaw code an "unacceptable cybersecurity risk." How does Ember build something production-grade?

---

#### 6. Implementation Roadmap: From Research to Pilot

Propose a phased implementation plan. Align with DeepSeek's three-phase blueprint but adapted for Ember's European school context:

- **Phase 1 — Single Subject Foundation (Term 1)**
  - Build the core agent framework for **one subject** (likely Maths — best existing AI tutor evidence, clearest mastery progression)
  - Implement persistent student profiles (USER.md pattern)
  - Deploy the Orchestration/Flow Agent with 20/2 Pomodoro structure
  - Build the Guide Agent dashboard (minimum viable: flag stuck students, daily summary)
  - Integrate with BGA's Maths curriculum standards
  - **Measure**: Mastery velocity vs. BGA baseline, student engagement (time-on-task), guide satisfaction, student wellbeing indicators
  - **Validate before proceeding**: Does the single-subject agent system produce measurable learning gains without negative wellbeing effects?

- **Phase 2 — Multi-Agent Collective (Terms 2-3)**
  - Deploy Subject Agents for 3-4 core subjects (Maths, Literacy, Science, History)
  - Implement the **Cabinet Meeting** inter-agent communication layer (shared "Student Context Bus")
  - Build the Curriculum Planning Agent for cross-curricular coordination
  - Add parent-facing reporting (simplified dashboard or conversational agent)
  - Begin afternoon integration (Afternoon Agent prototype)
  - **Measure**: Cross-curricular transfer effects, guide time allocation (are they spending more time on mentorship vs. administration?), parent satisfaction
  - **Validate**: Does multi-agent coordination produce better outcomes than isolated subject agents?

- **Phase 3 — Full OS (Year 2)**
  - Complete multi-agent orchestration across all subjects + afternoon
  - Full persistent identity with long-term memory accumulation
  - Adaptive curriculum planning that adjusts to individual trajectories
  - Evidence collection for external validation (engage Andrew Manches / University of Edinburgh for academic partnership)
  - Prepare for ESSA-equivalent European evidence certification
  - Begin conversations with BGA about platform deployment across their 53+ hub network
  - **Measure**: Year-over-year learning gains (aim for Bloom's 1+ sigma), student agency and confidence metrics, guide role transformation, parent engagement depth

For each phase, identify:
- Key deliverables
- Technical risks and mitigation strategies
- What needs to be validated before moving to the next phase
- Cost structure (per-student economics)
- Regulatory checkpoints (GDPR, EU AI Act compliance gates)

---

#### 7. The Measurement Challenge

This is Ember's hardest problem and its biggest opportunity. Address:

- **What's easy to measure**: Mastery velocity, time-on-task, curriculum coverage, test scores (MAP equivalents)
- **What's hard to measure but essential**: Confidence, agency, curiosity, creativity, collaboration quality, emotional resilience, "spark" — the discovery of what makes each child come alive
- **Proposed measurement framework**: How might the agent system itself help measure what traditional assessment can't? Agent-observed behavioral signals (engagement patterns, question-asking frequency, self-correction rates, peer interaction quality) could become proxies for deeper learning indicators
- **The evidence moat**: Plan for rigorous outcome research from day one. Partner with academia (Andrew Manches, University of Edinburgh). The K-12 market scan shows that evidence is the new competitive moat — ESSA "Strong" requires 2+ years and $500K-2M but creates defensibility that AI-native startups can't easily replicate
- **Operational metrics**: Define what "deep flow" means operationally (time-on-task, distraction rate, affect, mastery velocity). Define what "spark" means (creativity measures, interest development, identity formation, self-efficacy). What outcomes can be measured weekly vs. termly vs. annually?

---

#### 8. Open Questions and Research Gaps

What important questions do the four research reports leave unanswered? Where does Ember's specific use case create challenges the general agentic AI research doesn't address?

Consider:
- **Age-appropriateness**: The research mostly discusses adult/professional agent use. What changes for 6-year-olds vs. 14-year-olds? Screen time limits? Interaction modality (voice vs. text vs. visual)?
- **Neurodiversity**: How do agents adapt for dyslexia, ADHD, autism spectrum? The Gemini research mentions ADHD-accommodating Pomodoro modes — go deeper
- **Language**: Ember is in Portugal — students may be Portuguese-speaking, English-speaking, or multilingual. How do agents handle code-switching and language development?
- **Physical learning environments**: The WAB case study shows 10 differentiated learning space types (Movement, Construction, Stillness, Sound, Lab, etc.). How do digital agents interface with physical space design? Do agents make recommendations about which physical zone a student should work in?
- **Teacher/guide resistance**: The most common EdTech failure mode. How does Ember's guide model (mentorship, not instruction) avoid the adoption barriers that have killed other platforms?
- **Regulatory uncertainty**: EU AI Act classification for educational AI systems. What conformity assessments might be required?
- **Sustainability**: Cost per student per month at scale. What's the unit economics path to BGA-network-wide deployment?

---

#### 9. Unique Differentiators: What Makes Ember Different

Based on the competitive landscape (60+ companies in the K-12 AI space), articulate what makes Ember's approach distinctive. No other player combines:

1. **Agentic architecture** — Multi-agent system with persistent identity, bot-to-bot coordination, and per-student advocacy. Everyone else uses monolithic AI tutors or simple adaptive engines. Ember's agents form a "collective learning OS" around each child.

2. **The afternoon half is human-led and screen-free** — Ember's morning agents produce handoff briefs that inform the afternoon, and guide observations from the afternoon feed back into the next morning. The OS understands the whole day, but agents only operate during the morning block. Alpha School does 2-hour learning but treats the afternoon as a separate program. Ember creates a continuous feedback loop between the agentic morning and the human afternoon — without putting screens in front of kids all day.

3. **European values and regulatory framework** — Built for GDPR, EU AI Act, and a philosophical stance on childhood that prioritizes wellbeing over optimization. "Happiness over results" as a design principle. Local-first data ownership. Transparency by default.

4. **Platform, not product** — BGA's 53+ hubs across 12 countries provide ready-made distribution. Ember is the OS that schools run on, not a school brand to compete with. This is a fundamentally different business model from Alpha (private school) or Khan (nonprofit tool).

5. **Evidence-first from day one** — Academic partnership with University of Edinburgh. Designed for rigorous outcome measurement. Targeting the market's empty quadrant: low friction + strong outcome proof.

6. **"Spark finding" as a core capability** — Not just "personalized learning" (everyone claims this) but a system designed to discover and nurture each child's unique gifts. Agents that notice a student's emerging passion for architecture through their spatial reasoning patterns in maths and their afternoon project choices — and amplify it.

Map these against the specific competitors: Khan Academy (nonprofit, massive scale, no agentic architecture), Alpha School (US, high-tuition, no European values, weak evidence), LEAD School (India, no AI agents, different market), MagicSchool (teacher tool, not student-facing OS), DreamBox/Carnegie (adaptive platforms, not agentic, no afternoon model).

---

### Formatting and Tone

- Write for an audience of **technical co-founders and potential investors** who understand both AI and education
- Be specific and concrete — name frameworks, protocols, tools, and studies rather than staying abstract
- Use **Mermaid diagrams** for architecture and flow visualizations
- Use **tables** for comparisons and component specifications
- **Flag assumptions clearly** — distinguish between what the research supports, what the academic evidence shows, and what is speculative
- Reference specific academic studies by author and year where relevant (Bloom 1984, Ogut 2025, Kestin 2025, etc.)
- Total length: aim for **8,000–12,000 words**
- End with a one-page **executive summary** that could stand alone as a briefing document

---

### Draft Vision Statement (for reference, not for inclusion in output)

> *"Ember is an AI-native education operating system that orchestrates the relationship between child, mentor, and machine. It compresses core academics into a 2-hour daily mastery block through personalised AI tutoring — freeing the rest of the school day for what actually matters: creativity, collaboration, emotional intelligence, and discovering what makes each child come alive. Built in Europe, for European values. Evidence-led from day one. Human mentorship at the centre, AI as the amplifier — never the authority."*
