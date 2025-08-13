# [[VANITY]], [[topics to cover]].
#toppriority 

> Goal: Learn how to design, build, and deploy AI agents with autonomy, planning, reasoning, memory, and interaction.

---

## 🟢 Phase 1: Foundations of Agency
- [ ] Understand what Agentic AI is
- [ ] Compare Agentic AI vs Prompt-based LLMs
- [ ] Learn types of agents: Reactive, Deliberative, Hybrid, Interactive
- [ ] Understand concepts of:
  - [ ] Perception → Decision → Action loop
  - [ ] Planning vs Policy
  - [ ] Tool use and self-reflection
- [ ] Study classic architectures: BDI (Belief-Desire-Intention), GOFAI
- [ ] Explore examples: AutoGPT, BabyAGI, ReAct, Voyager, Devin

---

## 🟡 Phase 2: LLM + Tool-Using Agents
- [ ] Review prompt engineering fundamentals
- [ ] Learn about tools: Search, Calculator, Code Interpreter, DB Access
- [ ] Implement a basic tool-using agent using:
  - [ ] LangChain agents
  - [ ] OpenAI Function Calling or Assistants API
- [ ] Understand memory types:
  - [ ] Short-term context memory
  - [ ] Long-term retrieval memory (vector stores)
- [ ] Add memory via tools like:
  - [ ] FAISS / Chroma
  - [ ] Weaviate / Pinecone

---

## 🟠 Phase 3: Agent Frameworks
- [ ] Install and set up:
  - [ ] LangChain (Python or JS)
  - [ ] CrewAI (agent collaboration)
  - [ ] AutoGen (multi-agent programming)
  - [ ] AutogenStudio or OpenAgents
- [ ] Build single-agent systems:
  - [ ] Research Assistant
  - [ ] Code Fixer
  - [ ] Web Searcher
- [ ] Design multi-agent setups:
  - [ ] Planner + Executor
  - [ ] Supervisor + Worker
- [ ] Explore self-asking and self-correcting agents

---

## 🔵 Phase 4: Reasoning and Planning
- [ ] Implement ReAct (Reason + Act) prompting
- [ ] Understand chain-of-thought vs tree-of-thought
- [ ] Use language models for:
  - [ ] Task decomposition
  - [ ] Tool selection
  - [ ] Reflection and planning
- [ ] Explore AutoGPT-like architectures:
  - [ ] Goal memory
  - [ ] Task queue
  - [ ] Feedback loop
- [ ] Evaluate Planning Libraries:
  - [ ] TaskWeaver
  - [ ] DSPy
  - [ ] Microsoft Semantic Kernel

---

## 🟣 Phase 5: Autonomy & Behavior Modeling
- [ ] Define internal agent states (goals, beliefs, plans)
- [ ] Model external environment interaction
- [ ] Learn agent behaviors using:
  - [ ] Finite-State Machines
  - [ ] Behavior Trees
  - [ ] Utility Functions
- [ ] Implement self-reflection prompts and improvement loops
- [ ] Study autonomy boundaries and failure cases

---

## 🟤 Phase 6: Agent Memory, Personality & Identity
- [ ] Build persistent memory with vector stores
- [ ] Use LLMs to reconstruct and retrieve knowledge
- [ ] Add agent profiles:
  - [ ] Role, tone, values
  - [ ] Skill list and limitations
- [ ] Model emotion, goals, and values
- [ ] Implement role-play agents using Guardrails or LangChain RunnableSequence

---

## 🧪 Phase 7: Evaluation & Safety
- [ ] Design evals for:
  - [ ] Task success rate
  - [ ] Tool usage correctness
  - [ ] Reflection loops
- [ ] Use tools like:
  - [ ] DeepEval
  - [ ] Ragas
  - [ ] Promptfoo
- [ ] Learn safety practices for:
  - [ ] Tool limits
  - [ ] System messages / guardrails
  - [ ] Rate limiting / memory clearance

---

## ⚙️ Phase 8: Deployment & API Integration
- [ ] Convert agent to API using FastAPI or Flask
- [ ] Add frontends using:
  - [ ] Streamlit
  - [ ] Gradio
  - [ ] Webhooks & Chat UIs
- [ ] Log interactions (LangSmith, Telemetry)
- [ ] Deploy using:
  - [ ] Docker
  - [ ] Cloud services (AWS/GCP/Render)
  - [ ] GitHub Actions for CI/CD

---

## 🧩 Phase 9: Real-World Projects
- [ ] 🛠️ Build a Multi-Agent Research Team (Planner + Coder + Summarizer)
- [ ] 🛠️ Create a Personal DevOps Agent (deploy & monitor apps)
- [ ] 🛠️ Implement a Multimodal AI Agent (text + vision tools)
- [ ] 🛠️ Build a Data Analysis Agent (csv, SQL, charting)
- [ ] 🛠️ Design a Knowledge Assistant (RAG + Memory + Reflection)

---

## 📚 Bonus: Tools, Papers & Further Reading
- [ ] **Key Papers**:
  - [ ] [ReAct (Reason + Act)](https://arxiv.org/abs/2210.03629)
  - [ ] [AutoGPT](https://github.com/Torantulino/Auto-GPT)
  - [ ] [Voyager](https://voyager.minedojo.org/)
  - [ ] [Generative Agents](https://arxiv.org/abs/2304.03442)
  - [ ] [HuggingGPT](https://arxiv.org/abs/2303.17580)
- [ ] **Awesome Lists**:
  - [ ] [awesome-LLM-agents](https://github.com/gojiteji/awesome-LLM-agents)
  - [ ] [LangChain Hub](https://smith.langchain.com/)
- [ ] **Books / Blogs**:
  - [ ] LangChain docs
  - [ ] OpenAI Function Calling & Assistants API docs
  - [ ] AutoGen & CrewAI tutorials
