# Embodied Agent Survey

A research repository for an ongoing survey on **Embodied Agent Technologies**.

This project studies how embodied agents integrate foundation models, reasoning, planning, physical action, memory, learning, and system-level mechanisms to interact with the physical world.

The repository is being developed as the literature base for a survey on embodied intelligent agents.

---

## Scope

We focus on **agent technologies for embodied intelligence**, rather than a specific robot platform or a single learning paradigm.

The survey is organized around five major technical dimensions:

1. **Foundation Models for Embodied Agents**
2. **Planning and Reasoning**
3. **Skills and Action Execution**
4. **Memory and Self-Evolution**
5. **Agentic Systems and Reliable Deployment**

The taxonomy is described in more detail in [`taxonomy.md`](taxonomy.md).

---

## Taxonomy

### 1. Foundation Models for Embodied Agents

Foundation models that provide general visual, linguistic, multimodal, and action-generation capabilities for embodied agents.

Subtopics:

* Vision-Language Models
* Vision-Language-Action Models
* Generalist Embodied Models

Representative seed papers:

* **OpenVLA: An Open-Source Vision-Language-Action Model**
* **π0: A Vision-Language-Action Flow Model for General Robot Control**
* **Vision-Language-Action Models for Robotics: A Survey**

---

### 2. Planning and Reasoning

Methods that enable embodied agents to understand goals, decompose complex tasks, generate plans, reason about the environment, and revise plans according to execution feedback.

Subtopics:

* Task Decomposition
* Language / VLM-based Planning
* Code-as-Policy
* Closed-loop Replanning

Representative seed papers:

* **DeCo: Task Decomposition and Skill Composition for Zero-Shot Long-Horizon Manipulation**
* **MoMaStage: Skill-State Graph Guided Planning and Closed-Loop Execution for Long-Horizon Indoor Mobile Manipulation**

---

### 3. Skills and Action Execution

Methods that connect high-level agent decisions with executable robot behaviors.

This category covers reusable robot skills, skill composition, tool use, VLA-based action generation, manipulation, mobile manipulation, and whole-body control.

Subtopics:

* Skill Learning
* Skill Retrieval and Composition
* VLA-based Execution
* Mobile and Whole-Body Manipulation

Representative seed papers:

* **Compose by Focus: Scene-Graph Atomic Skills**
* **ExBody: Expressive Whole-Body Control**
* **HOVER: Whole-Body Controller**
* **HuMI: Whole-Body Manipulation**
* **Harness VLA: Memory-Guided Agentic Manipulation**

---

### 4. Memory and Self-Evolution

Methods that allow embodied agents to preserve experience across tasks and use previous interaction to improve future behavior.

Subtopics:

* Short- and Long-Term Memory
* Experience Reuse
* Continual Learning
* Skill and Agent Self-Evolution

Representative seed papers:

* **LRLL: Lifelong Robot Library Learning**
* **RoboMemory**
* **LEGION: Preserving and Combining Knowledge in Robotic Lifelong Reinforcement Learning**
* **Long-Term Memory for VLA-Based Agents in Open-World Task Execution**

---

### 5. Agentic Systems and Reliable Deployment

System-level approaches for integrating models, planning, skills, memory, robot interfaces, monitoring, verification, recovery, and generalization into reliable embodied agents.

Subtopics:

* Agent Architecture and Orchestration
* Monitoring and Failure Recovery
* Safety and Verification
* Generalization and Sim2Real
* Benchmarks and Evaluation

Representative seed papers:

* **RoboOS: A Hierarchical Embodied Framework for Cross-Embodiment and Multi-Agent Collaboration**
* **ROSClaw: A Hierarchical Semantic-Physical Framework for Heterogeneous Multi-Agent Collaboration**
* **Regression Test Selection for Updated Capability Modules in Compositional ML Systems via Atomic-Quality Probes**
* **ClutterDexGrasp**
* **Zero-Shot Dexterous Force Grasping**
* **AdaClearGrasp**

---

## Paper Matrix

All collected papers are maintained in [`paper_matrix.xlsx`](paper_matrix.xlsx).

Each paper is assigned:

* a primary category;
* a subcategory;
* a short description of the research problem;
* its core technical idea;
* an importance level;
* a reading status;
* relevant paper and code links.

The paper matrix is used as the main literature database for the survey.

---

## Reading Strategy

Papers are divided into three levels according to their importance to the survey:

**A — Core Paper**

Representative or influential work that forms an important node in the technical development of embodied agents. These papers should be read carefully.

**B — Supporting Paper**

Relevant work that supports a technical branch, comparison, or development trend. These papers are mainly read through the abstract, introduction, main figures, experiments, and conclusion.

**C — Background Paper**

Useful for background, terminology, supplementary evidence, or broad literature coverage. These papers do not require detailed reading unless needed during writing.

---

## Survey Writing Goal

The objective is not to summarize papers one by one.

Instead, the survey aims to identify:

* major technical paradigms;
* the evolution of embodied agent technologies;
* relationships between different research directions;
* representative systems and methods;
* remaining limitations and open challenges.

For each technical direction, we aim to answer:

> What problem was initially addressed?

> Why were earlier approaches insufficient?

> What new capability did later methods introduce?

> How did the research direction evolve?

> What problems remain unsolved?

---

## Current Sources

The initial literature pool is built from:

* the project advisor's seed-paper list;
* the previous EmbodiedClaw paper collection;
* recent representative work such as Harness VLA;
* later literature expansion through surveys, references, citation tracing, and academic databases.

---

## Status

This repository is under active construction.

Current work:

* [ ] Consolidate existing seed papers
* [ ] Build the master paper matrix
* [ ] Refine the taxonomy using collected literature
* [ ] Expand the literature pool to 100+ papers
* [ ] Identify the development trajectory within each research direction
* [ ] Prepare figures and tables for the final survey
