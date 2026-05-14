# LangGraph Tutorial Series — Stateful AI Agents from Zero to Production

> A complete beginner-to-advanced tutorial series for building stateful,
> cyclical, and self-correcting AI agents using LangGraph and Google Gemini.
> If LangChain chains are roads, LangGraph is the full road network.

---

## Why LangGraph?

Most LLM tutorials teach you to build a chain:

```
prompt → llm → output_parser   (A → B → C, done)
```

That works for simple Q&A. But real-world AI agents need to:

- **Loop** — retry when the output isn't good enough
- **Branch** — take different paths based on what the LLM decides
- **Remember** — maintain state across multiple conversation turns
- **Pause** — wait for a human to approve before taking an action
- **Collaborate** — route tasks between multiple specialized agents

LangChain chains cannot do any of this. **LangGraph can.**

```
LangChain chain:   A → B → C → END                    (linear)

LangGraph graph:   A → B → [decide] → C → END          (branching)
                                  ↘ → A (retry loop)   (cyclic)
                                  ↘ → PAUSE → human → D (human-in-the-loop)
```


---
## Prerequisites

**You should know:** Python basics — functions, dicts, type hints.
**You don't need:** ML experience, a GPU, or a paid API key.

If you are brand new to LangChain and LLMs, start with the
[LangChain Fundamentals Series](https://github.com/YOUR_USERNAME/langchain-tutorials)
first — then come back here.

---

## Setup

### 1. Get a free Gemini API key

[aistudio.google.com](https://aistudio.google.com) → Create API key.
Free tier. No credit card needed.

### 2. Install

```bash
pip install langgraph langchain langchain-community \
            langchain-google-genai google-generativeai \
            wikipedia duckduckgo-search
```
---
