# [[VANITY]].

**Stack:** LangGraph (LangChain), scikit-learn, Python, Streamlit, FAISS/Chroma, Pydantic, LangSmith (optional), Docker

> Goal: Build an AI system that ingests documentation (PDF/HTML/Markdown), answers questions, and **makes decisions** (e.g., classify requests as compliant/non-compliant, route to teams, suggest actions) with an auditable rationale and UI.

---

- [ ] 0) Milestones & Deliverables
- [ ]  **M1: Ingestion & RAG prototype** (doc upload ➜ chunking ➜ embeddings ➜ retrieval ➜ LLM answer with citations)
- [ ]  **M2: Decision module v1** (scikit-learn classifier/regressor + thresholds + justification)
- [ ]  **M3: LangGraph orchestration** (state, nodes, conditional edges, persistence, tracing)
- [ ]  **M4: Streamlit UI** (upload, KB management, chat, decisions, dashboards)
- [ ]  **M5: Evaluation & Benchmarks** (IR@k, answer faithfulness, decision accuracy, latency)
- [ ]  **M6: Packaging & Deployment** (Docker, .env secrets, one-click run, demo script)

- [ ] 1) Project Setup
- [ ]  Create repo: `ai-doc-decider/`
- [ ]  Python 3.11+ venv/conda
- [ ]  Requirements file(s): `requirements.txt` / `pyproject.toml`
- [ ]  Dev tooling: pre-commit, ruff/flake8, black, pytest, mypy (optional)
- [ ]  Secrets via `.env` + `pydantic-settings`
- [ ]  GitHub Actions (lint/tests) + badges

**Suggested structure**

```
ai-doc-decider/
├─ app/
│  ├─ ui/               # Streamlit pages
│  ├─ graphs/           # LangGraph definitions
│  ├─ models/           # sklearn pipelines, persistence
│  ├─ retrievers/       # chunking, embeddings, vector stores
│  ├─ tools/            # web, math, file, custom tools
│  ├─ schemas/          # Pydantic state & outputs
│  ├─ evaluators/       # metrics for RAG & decisions
│  ├─ config.py
│  └─ main.py           # entrypoints
├─ data/
│  ├─ raw/              # original docs
│  ├─ processed/        # text/cleaned/chunks
│  └─ vectorstore/      # FAISS/Chroma index
├─ notebooks/
├─ tests/
├─ .env.example
├─ requirements.txt / pyproject.toml
└─ Dockerfile
```

---

- [ ] ## 2) Internal Mechanism (Backend)

- [ ] ### 2.1 State & Schemas (LangGraph)

- [ ]  Define **State** (TypedDict/Pydantic):
    
    - [ ]  `user_query`, `context_docs`, `retrieval_metadata`
        
    - [ ]  `decision_request` (structured), `decision_result` (class/score), `rationale`
        
    - [ ]  `trace` (node logs), `errors` (list), `timings`
        
- [ ]  Define **Output Schemas** (Pydantic) for: Answer, Decision, Evidence, Metadata
    

- [ ] ### 2.2 Document Ingestion

- [ ]  Loaders: PDF (pymupdf/pdfminer), HTML (BeautifulSoup/trafilatura), Markdown/Docs folders
    
- [ ]  Normalize to text + metadata (source, page, section, URL)
    
- [ ]  Cleaning: unicode fix, boilerplate removal, de-dup, table extraction (optional)
    
- [ ]  Chunking strategies (choose one):
    
    - [ ]  Fixed-size tokens with overlap (e.g., 800/150)
        
    - [ ]  Semantic/sentence-boundary chunking (e.g., `nltk`/`spacy`)
        
- [ ]  Embeddings: **Open-source** (e5/mxbai/Instructor) or **API** (OpenAI/Anthropic/Google)
    
- [ ]  Vector store: **FAISS** (local, fast) or **Chroma** (easy, metadata-rich)
    
- [ ]  Index build + persist (`/data/vectorstore/`)
    

- [ ] ### 2.3 Retrieval (RAG)

- [ ]  Implement retriever (k, filters, MMR, hybrid BM25+vectors)
    
- [ ]  Citation packaging: doc snippets + page/URL references
    
- [ ]  Guardrails: domain filter, max-tokens, de-dup, source diversity
    

- [ ] ### 2.4 Decision Module (scikit-learn)

- [ ]  Label schema: define decision types (e.g., **Approve / Flag / Reject**)
    
- [ ]  Feature sets:
    
    - [ ]  Text-only: TF-IDF / character n-grams / embeddings
        
    - [ ]  RAG features: retrieved evidence counts, similarity scores
        
    - [ ]  Heuristics: keyword hits, policy rules
        
- [ ]  Pipelines: `Pipeline([TfidfVectorizer, Classifier])`
    
- [ ]  Models to try: LogisticRegression, LinearSVC, RandomForest, Calibrated NB
    
- [ ]  Multi-label (if needed): OneVsRestClassifier
    
- [ ]  Calibration: Platt/Isotonic for probability thresholds
    
- [ ]  Persistence: `joblib.dump`/`load`
    

- [ ] ### 2.5 Orchestration (LangGraph)

- [ ]  Build a `StateGraph`
    
- [ ]  Nodes:
    
    - [ ]  **classify_intent** (query ➜ Q&A vs Decision vs KB management)
        
    - [ ]  **retrieve_context** (RAG)
        
    - [ ]  **answer_with_citations** (LLM + templates + schema)
        
    - [ ]  **make_decision** (sklearn pipeline + thresholds)
        
    - [ ]  **explain_decision** (LLM turns features/evidence → rationale)
        
    - [ ]  **fallback_or_handoff** (human-in-the-loop / escalate)
        
    - [ ]  **log_and_persist** (traces, metrics, state checkpoint)
        
- [ ]  Conditional edges: route based on intent/confidence/guardrails
    
- [ ]  Streaming/interrupts (optional): ask user for missing info
    
- [ ]  Persistence: save checkpoints for replay/analysis
    
- [ ]  Tracing: LangSmith (optional) for node-level spans
    

- [ ] ### 2.6 Tooling (optional but useful)

- [ ]  Web search retriever
    
- [ ]  Math/code tool for calculations
    
- [ ]  Policy rule engine (simple YAML rules checked pre/post decision)
    
- [ ]  PII scrubber / redaction for uploads
    

- [ ] ---

- [ ] ## 3) Evaluation & Datasets

- [ ]  **Build a supervision set**:
    
    - [ ]  Sample 150–500 queries from your target domain
        
    - [ ]  Label expected answers and **decisions** + evidence (cite doc IDs/pages)
        
- [ ]  **IR metrics**: Recall@k, MRR
    
- [ ]  **Answer quality**: faithfulness (source-grounded), completeness, style
    
- [ ]  **Decision metrics**: Accuracy, F1, AUROC, calibration curves, confusion matrix
    
- [ ]  **Latency**: P50/P95 end-to-end, per-node timings
    
- [ ]  **Ablations**: chunk size, k, model choices
    

- [ ] ---

- [ ] ## 4) Streamlit UI (Python)

- [ ]  Multipage app: `Home`, `Knowledge Base`, `Chat/Decisions`, `Analytics`, `Admin`
    
- [ ]  **Home**: system description, quick start
    
- [ ]  **Knowledge Base**:
    
    - [ ]  Upload PDFs/URLs/Markdown
        
    - [ ]  Show ingestion status, chunk counts, index size
        
    - [ ]  Rebuild index, purge sources, filter by tags
        
- [ ]  **Chat/Decisions**:
    
    - [ ]  Chat area with history (Session State)
        
    - [ ]  Toggle: _Ask_ vs _Request Decision_
        
    - [ ]  Output: Answer, **Decision** (class + probability), **Rationale**, **Citations**
        
    - [ ]  Expose thresholds & what‑if sliders (see live decision boundary)
        
- [ ]  **Analytics**:
    
    - [ ]  Upload eval set → run benchmark → show metrics (tables/plots)
        
    - [ ]  Confusion matrix, PR/ROC curves, latency plots
        
- [ ]  **Admin**:
    
    - [ ]  API keys, model selection, safety toggles
        
    - [ ]  Export/import vector store & sklearn model
        

- [ ] **UI behaviors**
- [ ]  Use `st.session_state` for chat, KB selections, thresholds
- [ ]  Cache heavy ops (`@st.cache_data` for data, `@st.cache_resource` for models)
- [ ]  Progress + status spinners for ingestion and eval runs

- [ ]  5) Implementation Tasklists (Step-by-Step)

- [ ]  5.1 Environment & Config
- [ ]  Create venv, install deps (langchain, langgraph, scikit-learn, pydantic, streamlit, faiss-cpu or chromadb, sentence-transformers / chosen embedding lib, bs4, pymupdf)
- [ ]  Implement `app/config.py` (settings from `.env`)
- [ ]  Add logging with `logging` + JSON formatter

- [ ] 5.2 Schemas & State
- [ ]  Define `AppState` (Pydantic) with fields in §2.1
- [ ]  Define output models: `Answer`, `Decision`, `Evidence`
- [ ]  Create templates for prompts with structured outputs
- [ ]  5.3 Ingestion Pipeline
- [ ]  Implement `loaders` (PDF/HTML/MD)
- [ ]  Text cleaning + metadata enrichment
- [ ]  Chunker (token-aware)
- [ ]  Embed + index build (FAISS/Chroma)
- [ ]  CLI: `python -m app.retrievers.build_index --src data/raw --out data/vectorstore`
-
- [ ] 5.4 Retrieval & Answering
- [ ]  `retrieve_context(state)` node
- [ ]  `answer_with_citations(state)` node (LLM call, max new tokens, stopwords guard)
- [ ]  Source block builder (quote snippets, page links)

- [ ] 5.5 Decision Module
- [ ]  Create labeled CSV: `data/labels/decisions.csv` (text, label, meta)
- [ ]  Build sklearn pipelines (TF-IDF → classifier)
- [ ]  Train, cross-validate, pick model, calibrate probabilities
- [ ]  Persist with `joblib` and load in app
- [ ]  `make_decision(state)` node to call pipeline, return class/prob

- [ ] 5.6 LangGraph Orchestration
- [ ]  Define `StateGraph`
- [ ]  Add nodes: intent ➜ retrieve ➜ answer/decision ➜ explain ➜ log
- [ ]  Add conditional edges (confidence thresholds / guardrails)
- [ ]  Add persistence/checkpointing (SQLite or file-based)
- [ ]  Add tracing (LangSmith) and error handling

- [ ]  5.7 Streamlit UI
- [ ] Boilerplate multipage app scaffolding
- [ ]  Page: **Knowledge Base** (upload + index rebuild)
- [ ]  Page: **Chat/Decisions** with sidebar controls (k, thresholds, model)
- [ ]  Page: **Analytics** (run eval, show metrics)
- [ ]  Theme, branding, and help tooltips
- [ ] ### 5.8 Evaluation & Reporting
- [ ]  Script `app/evaluators/run_eval.py`
- [ ]  Metrics tables + plots saved to `reports/`
- [ ]  Add downloadable CSV/JSON of results from Streamlit
- [ ] ### 5.9 Packaging & Deployment
- [ ]  Dockerfile with CPU build (include `faiss-cpu`)
- [ ]  Healthcheck endpoint (optional `fastapi` stub) or Streamlit share
- [ ]  Makefile: `make build`, `make run`
- [ ]  Demo dataset + scripted scenario `scripts/demo.sh`
- [ ] ## 6) Tech Choices & Notes
- [ ]  **Vector store**: Start with **FAISS** for local speed; Chroma is ok if you want easy metadata ops
- [ ]  **Embeddings**: choose one model and stick to it for consistent indices
- [ ]  **LLM**: Any provider or local (Ollama) — keep abstraction layer so you can switch
- [ ]  **Determinism**: use temperature=0 for decisions; enable retries & timeouts
- [ ]  **Explainability**: show evidence chunks + decision probability + concise rationale
- [ ]  **Safety**: file type allowlist; size caps; PII scan; rate limits; content filters

---

## 7) Example Prompts & Outputs (Skeletons)

-  **Answer prompt**: “You are a documentation assistant. Cite sources as [DocName p.12]. Use only provided context. If missing, say you don’t know.”
-  **Decision rationale prompt**: “Given features and retrieved evidence, explain in 2–3 sentences why the decision class=X at probability=P, citing chunks.”

---

## 8) Timeline (suggested)

- [ ]  Week 1: Setup, ingestion, embeddings, vector store
- [ ]  Week 2: RAG QA with citations + eval v0
- [ ]  Week 3: Decision dataset & sklearn baseline
- [ ]  Week 4: LangGraph orchestration + persistence
- [ ]  Week 5: Streamlit UI
- [ ]  Week 6: Evaluation, ablations, polish
---

## 9) Success Criteria (acceptance)

-  Upload docs and build index without errors (< 5 min for 200 docs)
-  Top‑k retrieval recall ≥ 0.8 on eval set
-  Decision F1 ≥ target (set domain-specific)
-  UI shows answer, decision, rationale, and citations consistently
-  Reproducible run: `docker run -p 8501:8501 app`
---

## 10) Nice-to-Haves

-  Hybrid retrieval (BM25 + vectors)
-  Semantic routing (LLM decides which policy/doc set to use)
-  Knowledge graph extraction for cross‑doc rules
-  Active learning loop: add difficult cases to training set from UI feedback
-  Multi-tenant KBs (separate indexes by project)
---

### Quick Next Actions (today)

-  Initialize repo & tooling
-  Implement ingestion + vector store build
-  Train a tiny sklearn baseline on a toy labeled set
-  Wire a minimal LangGraph with 3 nodes: intent → retrieve → answer
-  Spin up Streamlit page: upload & simple chat with citations