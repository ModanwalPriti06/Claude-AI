# Claude-AI 
Claude Skill  (model, harness, tools, context management, and execution environment)

![AI](https://img.shields.io/badge/AI-Think-blue)
![Gen AI](https://img.shields.io/badge/Gen_AI-Create-purple)
![AI Agent](https://img.shields.io/badge/AI_Agent-Act-green)
![Agentic AI](https://img.shields.io/badge/Agentic_AI-Plan_Act_Adapt-orange)

### PROMPTS Full Form

### P — Pick (Choose the right models and build your personal AI toolkit.)
### R — Refine (Help AI understand your context and standards.)
### O — Operate (Use different tools together in reliable workflows.)
### M — Make (Create professional content and visual stories.)
### P — Productize (Turn repeatable problems into working products.)
### T — Trigger (Make recurring work start on its own.)
### S — Synthesize (Combine everything into assistants, agents and AI employees.)

---

# Week - 1 - S1 (https://lmstudio.ai/docs/bionic)

## What is a cohort?
- Instructor-led milestones
- Fixed timelines
- Peer-to-peer learning
- Community accountability

## LLM (Large Language Model) : 
LLM is an AI model trained on huge amounts of text to understand and generate human-like language.

## Harness:
In AI, a harness is the system around an AI model that helps it perform tasks by providing tools, instructions, context, and execution control.
- Example: An LLM is the brain, while the harness gives it tools like file access, a browser, and code execution.

## OLMo:
OLMo stands for Open Language Model. It is a family of open language models developed by the Allen Institute for AI (AI2).

#### In simple terms:
- LLM: A large language model in general.
- OLMo: A specific family of open language models.
- ChatGPT: An AI product powered by language models.

## Open Weight Model:
An open-weight model is an AI model whose trained parameters (called weights) are publicly available to download and run.

## Diff between Full precision and Quant model
The main difference is model accuracy vs. memory and speed.  In simple terms: Full precision preserves more numerical detail, while quantization compresses the model so it needs less memory and may run more efficiently, with a possible quality trade-off.

| Feature      | Full-Precision Model                 | Quantized Model                                   |
| ------------ | ------------------------------------ | ------------------------------------------------- |
| Weights      | Higher precision, e.g. FP16/BF16     | Lower precision, e.g. INT8/INT4                   |
| Memory usage | High                                 | Much lower                                        |
| Speed        | Can be slower on limited hardware    | Often faster, depending on hardware               |
| Accuracy     | Usually closer to the original model | May lose some accuracy                            |
| Hardware     | Requires more RAM/VRAM               | Can run on smaller GPUs or even some CPUs         |
| Use case     | Research, high-quality inference     | Local AI apps, laptops, cost-efficient deployment |

### Example
Suppose you have a 7-billion-parameter LLM.
- FP16: Weights alone require approximately 14 GB of memory.
- INT8: Approximately 7 GB.
- INT4: Approximately 3.5 GB.

## Context Window:
Context window is the maximum amount of information an LLM can process at one time, measured in tokens.

## Token Per Second(TPS):
Tokens per second (TPS) measures how many tokens an LLM generates per second. It indicates the model's response speed.
- What affects TPS? GPU/CPU performance, model size, quantization, and the length of the input context.
- Remember: Context window = how much information a model can handle; TPS = how fast it generates output.

## Complete model example: Llama-3.1-8B-Instruct-Q4_K_M.gguf
| Question          | Example       | Meaning                                                     |
| ----------------- | ------------- | ----------------------------------------------------------- |
| Who built it?     | Meta          | The company that developed it                               |
| What family?      | Llama         | The model family                                            |
| How big?          | 8B            | Approximately 8 billion parameters                          |
| How optimized?    | Q4_K_M        | 4-bit quantization format commonly used with GGUF           |
| Where runs?       | GGUF          | A model file format used by tools like Ollama and llama.cpp |
| How much context? | 128K tokens   | Maximum context window supported by this model              |
| What behavior?    | Instruct      | Fine-tuned to follow user instructions                      |
| How fast?         | 40 tokens/sec | Example generation speed; actual speed depends on hardware  |

---
# Week - 1 - S2 (tokenizer)

## Vector embedding:
Vector embedding is a way to convert text, images, or other data into a list of numbers (a vector) so AI can understand semantic meaning and find similar information.

## Autoregression:
Autoregression in AI is a process where a model predicts the next token based on the tokens generated so far. Autoregression = predict the next token using the tokens that came before it.

## LL Model
- LLM is only a next-token prediction engine.
- No Math skills
- No Emotions
- A great mimicker
- Data is not stored in an LLM.
- LLMs do not search a database of facts.

## Word2vec
Word2Vec is a machine learning technique that converts words into numerical vectors (embeddings) so words with similar meanings have similar vector representations.

---
# Week - 2 - S1

## Big Picture – Overview Table

| Concept                   | Meaning                                                                 | Example / Current Implementation     |
| ------------------------- | ----------------------------------------------------------------------- | ------------------------------------ |
| Prompt Engineering        | Managing and improving prompts given to an LLM.                         | User message + Tools                 |
| Context Engineering       | Managing the input and context provided to an LLM.                      | Prompt + Message Chaining            |
| Orchestration             | Coordinating multiple LLM calls and their sequence.                     | First call → Call Tool → Final Call  |
| Agentic Workflow          | Following step-by-step actions to achieve a goal.                       | Our chat function                    |
| Tool Chaining             | Connecting multiple tools to work together in sequence.                 | Our example had only one tool        |
| Agent Memory – Short-Term | Retaining information during the current interaction or task.           | Our agent has only short-term memory |
| Agent Memory – Long-Term  | Retaining useful information across multiple sessions or conversations. | Long-term memory capability          |

---
# Week - 2 - S2

- LLM = The AI model that generates responses.
- MCP = The protocol that connects AI applications to tools and data.
- MCP Server = Exposes tools, resources, or prompts.
- MCP Client = Connects the AI application to an MCP server.

---

# Claude Notes - Algomaster.io

## Git Command
Git Command

| Operation                        | Examples                            | Typical Policy           |
| -------------------------------- | ----------------------------------- | ------------------------ |
| Inspect changes                  | `git status`, `git log`, `git diff` | Allow                    |
| See what's ready to be committed | `git diff --cached`                 | Allow                    |
| Create local commits             | `git add`, `git commit`             | Allow after review       |
| Discard changes                  | `git reset --hard`, `git clean -fd` | Require approval         |
| Publish changes                  | `git push`, `gh pr create`          | Require approval         |
| Rewrite remote history           | `git push --force`                  | Block                    |
| Merge into main                  | `gh pr merge`                       | Human approval required  |

## LangGraph Vs LangChain 

LangChain: LangChain is an open-source framework and agent engineering platform launched in October 2022 by Harrison Chase. It helps developers build applications powered by large language models (LLMs) by connecting models to external data sources, memory, and software workflows

<img width="752" height="423" alt="Screenshot 2026-11-17 at 6 37 06 PM" src="https://github.com/user-attachments/assets/98fe092b-2ad3-4268-9e54-9702e988c3ff" />

**LangGraph:** LangGraph is a framework to orchestrate multisteps, stateful workflow using LLM, with a graph based structure. Help to cretae agentic ai.

## **LangChain vs LangGraph**

| Feature            | LangChain                                         | LangGraph                                                                    |
| ------------------ | ------------------------------------------------- | ---------------------------------------------------------------------------- |
| **Purpose**        | Toolkit to build LLM apps (chains, tools, agents) | Framework to manage complex workflows with state                             |
| **Style**          | Linear or reactive chains                         | Graph-based, supports loops, retries, memory                                 |
| **Best Use Case**  | Simple chatbots, RAG apps, tool usage             | Multi-step workflows, agents with memory, conditional paths                  |
| **State Handling** | Stateless or partially stateful                   | Fully stateful; remembers and transitions based on logic                     |
| **Example Use**    | "Book a flight" using a flight API                | "Plan a vacation" (ask budget → choose flights → book hotel → loop if error) |

**LangSmith:** LangSmith is a platform used to debug, monitor, test, evaluate, and improve LLM-powered applications and AI agents.

### Features of LangSmith
- Tracing
- Debugging
- Evaluation
- Monitoring
- Datasets
- Prompt 

```
- LangChain → Build AI applications.
- LangGraph → Manage complex AI workflows.
- LangSmith → Monitor, debug, and evaluate AI applications.
```
## Context Rot: (https://youtu.be/lDglqMhhpjM?si=PzYeL0K5H17CrRH6)
Context rot lost in the middle Haystack test Attention Rag. Context rot is the measurable degradation in LLM performance that occurs when input contexts grow too long.

### Lost in the Middle: 
The "Lost in the Middle" phenomenon is a well-documented weakness where large language models (LLMs) pay strong attention to information placed at the beginning or end of a long input context, but significantly ignore or miss details buried in the middle

### The Needle In a Haystack Test: 
The Needle in a Haystack (NIAH) test is an evaluation benchmark used to measure how accurately a large language model (LLM) can find and retrieve a specific piece of information hidden inside a very long block of text. 

## RAG = Retrieval-Augmented Generation
RAG is a technique that allows an LLM to retrieve relevant information from external sources (documents, databases, PDFs) before generating an answer. Example: Camera related issue check in above youtube link.
```
Retrieval: Finds relevant information from the PDF.
Augmentation: Adds the retrieved information to the LLM's prompt.
Generation: LLM generates an answer based on that information.
```

## Ingestion Pipeline and Retrieval Pipeline

![Chunking](https://img.shields.io/badge/Chunking-Text_Splitting-blue)
![Embedding](https://img.shields.io/badge/Embedding-Vector_Representation-purple)
![Vector Database](https://img.shields.io/badge/Vector_Database-Store_&_Search-green)
