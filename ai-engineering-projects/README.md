# AI Engineering Projects

A collection of hands-on projects building applications across the modern LLM and AI-engineering stack — from single-model chatbots to multi-agent systems, retrieval-augmented generation, structured output, and open-source models. Each notebook is a self-contained, working implementation.

> These projects were built as practical implementations while developing my AI-engineering skills, using **current versions** of each library (several were updated from older tutorial patterns to the latest APIs — e.g. LangChain's `create_retrieval_chain`, the current Google GenAI SDK, and up-to-date agent frameworks).

---

## What's inside

Projects are grouped by the capability they demonstrate.

### Foundations — LLM apps & multimodal
| Project | What it does | Key tech |
|---|---|---|
| [`character-ai-chatbot`](notebooks/character-ai-chatbot.ipynb) | A configurable character chatbot with persona and memory | OpenAI API |
| [`vision-calorie-tracker`](notebooks/vision-calorie-tracker.ipynb) | Estimates calories from a **photo of food** using a vision model | OpenAI vision, PIL, base64 |
| [`adaptive-ai-tutor-gradio`](notebooks/adaptive-ai-tutor-gradio.ipynb) | A tutor that adapts explanations to the learner's level, with a web UI | OpenAI, Gradio |

### Multi-model
| Project | What it does | Key tech |
|---|---|---|
| [`multi-model-landing-page-generator`](notebooks/multi-model-landing-page-generator.ipynb) | Generates landing-page copy and compares output across **three providers** | OpenAI, Anthropic (Claude), Google (Gemini) |
| [`resume-ai-assistant-pydantic`](notebooks/resume-ai-assistant-pydantic.ipynb) | Tailors a resume to a job description and writes a cover letter, with **schema-validated structured output** | OpenAI, Gemini, Pydantic |

### Open-source models (HuggingFace)
| Project | What it does | Key tech |
|---|---|---|
| [`chat-with-documents-huggingface`](notebooks/chat-with-documents-huggingface.ipynb) | Chat over your own PDFs using **open-source LLMs** running locally | Transformers, HuggingFace, PyTorch, Gradio |
| [`reasoning-llms-and-leaderboards`](notebooks/reasoning-llms-and-leaderboards.ipynb) | Explores reasoning models, quantization, and benchmark leaderboards | Transformers, datasets, BitsAndBytes |

### Retrieval-augmented generation (RAG)
| Project | What it does | Key tech |
|---|---|---|
| [`rag-langchain-document-qa`](notebooks/rag-langchain-document-qa.ipynb) | Answers questions grounded in a document set via embeddings + retrieval | LangChain, ChromaDB, OpenAI embeddings |

### Agents & orchestration
| Project | What it does | Key tech |
|---|---|---|
| [`multi-agent-teams-autogen`](notebooks/multi-agent-teams-autogen.ipynb) | Multiple AI agents collaborating in a group chat to solve a task | AutoGen, multi-provider |
| [`agentic-workflows-langgraph`](notebooks/agentic-workflows-langgraph.ipynb) | A stateful agent graph with tools and web search | LangGraph, LangChain, Tavily |
| [`data-science-automation-crewai`](notebooks/data-science-automation-crewai.ipynb) | A crew of agents (planner/analyst/modeler) automating a data-science task | CrewAI, scikit-learn |
| [`ai-tutor-mcp-agents-sdk`](notebooks/ai-tutor-mcp-agents-sdk.ipynb) | An AI tutor built on the **Model Context Protocol** and the OpenAI Agents SDK | MCP, OpenAI Agents SDK, Gradio |

### Machine learning
| Project | What it does | Key tech |
|---|---|---|
| [`predictive-analytics-ml`](notebooks/predictive-analytics-ml.ipynb) | End-to-end regression: cleaning, features, models, evaluation | scikit-learn, pandas, matplotlib, seaborn |

---

## Tech & concepts covered

**Providers:** OpenAI · Anthropic (Claude) · Google (Gemini) · HuggingFace open-source models
**Frameworks:** LangChain · LangGraph · CrewAI · AutoGen · OpenAI Agents SDK · MCP
**Techniques:** RAG & vector search (ChromaDB) · structured output (Pydantic) · multi-agent orchestration · tool use & web search · vision/multimodal · quantization · Gradio UIs
**ML:** regression, feature engineering, model evaluation with scikit-learn

---

## Running the notebooks

Each notebook loads API keys from a `.env` file (they are never hard-coded).

```bash
# 1. Install Jupyter and per-notebook dependencies
pip install jupyter
#    each notebook installs its own libraries in the first cell

# 2. Create your .env from the example and add your keys
cp .env.example .env

# 3. Launch
jupyter notebook
```

You only need keys for the providers a given notebook uses (see the tables above). Not every notebook needs every key.

---

## A note on how these were built

These began as guided builds and were implemented by me from scratch, then **modernised** where the reference material used deprecated libraries — updating imports and API calls to current, working versions. They represent my hands-on practice across the AI-engineering stack. Where a project is developed further into a standalone, deployed application, it's noted in that notebook.

---

*Built by **Charity Umoren** — medical doctor transitioning into AI engineering.*
*[LinkedIn](https://www.linkedin.com/in/charityumoren/)*
