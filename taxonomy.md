# Taxonomy of Embodied Agent Technologies

## 1. Organizing Principle

This survey focuses on **Embodied Agent Technologies**.

An embodied agent is not defined by a particular robot embodiment, such as a robotic arm, mobile robot, dexterous hand, or humanoid robot. It is also not defined by a single learning method such as reinforcement learning, imitation learning, or Vision-Language-Action modeling.

Instead, we organize the literature according to the major technical capabilities required to build an embodied agent.

The taxonomy therefore follows five complementary dimensions:

1. **Foundation Models for Embodied Agents**
2. **Planning and Reasoning**
3. **Skills and Action Execution**
4. **Memory and Self-Evolution**
5. **Agentic Systems and Reliable Deployment**

These dimensions describe different research questions within an embodied agent system.

A single paper may contribute to multiple dimensions. Therefore, every paper is assigned one **Primary Category**, while additional contributions are recorded using secondary tags in the paper matrix.

---

# 2. Foundation Models for Embodied Agents

## Core Question

**What general perception, language, reasoning, and action capabilities are provided by the underlying model?**

This category focuses on foundation models that provide reusable capabilities for embodied agents.

## 2.1 Vision-Language Models

Research on models that jointly process visual observations and natural language.

Relevant topics include:

* visual-language understanding;
* visual grounding;
* instruction understanding;
* multimodal reasoning.

## 2.2 Vision-Language-Action Models

Models that extend vision-language understanding toward robot actions.

Relevant topics include:

* Vision-Language-Action models;
* generalist robot policies;
* action tokenization;
* continuous action generation;
* cross-task robot control.

Representative examples include OpenVLA and π0.

## 2.3 Generalist Embodied Models

Models designed to support multiple tasks, environments, robot embodiments, or interaction settings.

The emphasis is on general-purpose embodied capabilities rather than a single manipulation task.

## Boundary

A paper belongs primarily to this category when its main contribution is a **foundation or generalist model**.

If a paper mainly studies how an agent plans around or calls an existing VLA, it should normally be classified under Planning, Skills, or Agentic Systems instead.

---

# 3. Planning and Reasoning

## Core Question

**Given a goal and the current environment state, what should the embodied agent do next?**

This category studies high-level decision making.

## 3.1 Task Decomposition

Methods that transform a complex task into smaller subgoals, stages, or atomic tasks.

Typical problems include:

* long-horizon task decomposition;
* hierarchical task representations;
* subgoal generation;
* dependency modeling.

## 3.2 Language- and VLM-Based Planning

Methods that use LLMs, VLMs, or other foundation models to generate or update robot plans.

Typical problems include:

* semantic planning;
* language-conditioned planning;
* visual reasoning;
* affordance-aware decision making.

## 3.3 Code-as-Policy

Methods that represent robot plans or actions using executable code, programs, or structured tool calls.

The main question is how high-level model reasoning can be converted into executable procedures.

## 3.4 Closed-Loop Replanning

Methods that revise decisions according to execution results and environmental feedback.

The general evolution is:

**Plan → Execute → Observe → Evaluate → Replan**

This is particularly important for long-horizon embodied tasks, where a single planning error can propagate through later actions.

## Boundary

A paper belongs primarily to this category when its major contribution concerns **goal interpretation, decomposition, planning, reasoning, or replanning**.

If its main contribution is the physical skill or low-level robot policy itself, it belongs under Skills and Action Execution.

---

# 4. Skills and Action Execution

## Core Question

**How does an embodied agent convert a high-level decision into executable physical behavior?**

This category connects agent intelligence with physical interaction.

## 4.1 Skill Learning

Methods for learning reusable robot behaviors from demonstrations, reinforcement learning, interaction, or other forms of experience.

Examples include:

* grasping skills;
* manipulation skills;
* navigation skills;
* reusable motion primitives.

## 4.2 Skill Retrieval and Composition

Methods that select, retrieve, sequence, or combine previously acquired skills.

Typical research questions include:

* how skills are represented;
* how suitable skills are selected;
* how atomic skills are composed;
* how transitions between skills are handled.

## 4.3 VLA-Based Execution

Research in which Vision-Language-Action models or similar learned policies serve as action executors within a larger embodied system.

This subsection is different from Section 2.2.

Section 2.2 focuses on the **VLA model itself**.

Section 4.3 focuses on **how an agent uses a VLA to execute tasks**.

Harness VLA is a representative example of this distinction.

## 4.4 Mobile and Whole-Body Manipulation

Research connecting embodied-agent decisions with physical control of mobile manipulators or humanoid robots.

Topics include:

* mobile manipulation;
* whole-body control;
* loco-manipulation;
* coordinated locomotion and manipulation.

## Boundary

A paper belongs primarily to this category when its main contribution is about **skills, robot policies, action generation, or physical execution**.

---

# 5. Memory and Self-Evolution

## Core Question

**How can an embodied agent preserve experience and improve across tasks?**

A capable embodied agent should not treat every task as an isolated episode.

## 5.1 Short- and Long-Term Memory

Mechanisms for storing information about:

* observations;
* task states;
* previous actions;
* successful trajectories;
* failures;
* environmental knowledge.

## 5.2 Experience Reuse

Methods that retrieve previous experiences to improve current decision making.

The key transition is from simply storing history to making stored experience useful for future tasks.

## 5.3 Continual Learning

Methods that allow robot agents to acquire new knowledge or skills while retaining previously learned capabilities.

Important problems include:

* catastrophic forgetting;
* lifelong robot learning;
* continual skill acquisition;
* knowledge transfer across tasks.

## 5.4 Skill and Agent Self-Evolution

Methods that allow an agent to modify its skills, memory, tools, policies, or other components through accumulated experience.

A useful conceptual trajectory is:

**Task Experience
→ Memory
→ Experience Reuse
→ Continual Learning
→ Persistent Self-Improvement**

## Boundary

A paper belongs primarily to this category when **experience across tasks changes future agent behavior**.

Temporary feedback used only for replanning within one task is normally classified under Planning or Reliability instead.

---

# 6. Agentic Systems and Reliable Deployment

## Core Question

**How can models, reasoning, skills, memory, and robot interfaces operate together as a reliable embodied-agent system?**

This category focuses on system-level integration and deployment.

## 6.1 Agent Architecture and Orchestration

Research on the overall architecture connecting:

* foundation models;
* planners;
* skills;
* tools;
* memory;
* robot middleware;
* multiple agents or robot platforms.

Examples include hierarchical embodied-agent architectures and ROS-based agent interfaces.

## 6.2 Monitoring and Failure Recovery

Mechanisms for detecting failures during execution and recovering from them.

Typical problems include:

* execution monitoring;
* progress estimation;
* failure detection;
* retry strategies;
* reset and recovery;
* closed-loop correction.

## 6.3 Safety and Verification

Methods that determine whether proposed actions or system behaviors satisfy correctness and safety constraints.

Relevant topics include:

* action verification;
* permission control;
* runtime guards;
* safety monitoring;
* regression testing.

## 6.4 Generalization and Sim2Real

Methods that allow embodied agents to operate beyond their original training distribution.

Relevant topics include:

* zero-shot generalization;
* unseen-object manipulation;
* cross-environment transfer;
* cross-embodiment transfer;
* simulation-to-real transfer.

## 6.5 Benchmarks and Evaluation

Benchmarks and evaluation frameworks for measuring embodied-agent capabilities.

Important evaluation dimensions include:

* task success;
* long-horizon completion;
* generalization;
* robustness;
* failure recovery;
* efficiency;
* safety.

## Boundary

A paper belongs primarily to this category when its contribution concerns **system integration, reliability, deployment, evaluation, or transfer**, rather than one isolated model component.

---

# 7. Multi-Category Papers

Many embodied-agent papers span several categories.

For example, a system may contain:

* a VLM for perception;
* an LLM planner;
* a skill library;
* long-term memory;
* a failure-recovery loop.

Such a paper should **not** be copied into several categories.

Instead:

* assign one **Primary Category** according to its main contribution;
* record other relevant dimensions as **Tags** in `paper_matrix.xlsx`.

Example:

**Harness VLA**

Primary Category:

`3. Skills and Action Execution`

Subcategory:

`3.3 VLA-Based Execution`

Tags:

`VLA; Agent Harness; Memory; Long-Horizon Manipulation; Failure Recovery; Reliability`

---

# 8. How the Taxonomy Will Be Refined

This taxonomy is an initial organizational framework rather than a fixed final conclusion.

As the literature pool expands, especially after collecting 100+ papers, subcategories may be merged, divided, or renamed according to the actual structure of the research field.

However, taxonomy changes should be driven by evidence from the literature rather than by individual papers.

The final survey should use the taxonomy not merely to group papers, but to reveal the **technical evolution within each research direction**.

For each subsection, we aim to identify:

**early problem formulation
→ representative solution
→ limitation
→ subsequent improvement
→ current frontier**

This development trajectory will form the main narrative of the final survey.
