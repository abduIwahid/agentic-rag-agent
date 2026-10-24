# Agentic RAG Agent — Q&A with Reasoning

Ask questions over web sources and watch the agent work: it searches its knowledge base, reasons step by step about what it found, and answers with sources cited. This is Retrieval-Augmented Generation (RAG) with the thinking left visible — not a black box.

## What it does

- Add any web pages as knowledge sources from the sidebar — articles, documentation, course pages
- Every answer is grounded in those sources, with the retrieval reasoning shown
- Semantic vector search (LanceDB) finds the relevant passages, Gemini reasons over them
- Runs entirely on one free Google API key — the chat model and the embeddings are both Gemini

## Tech stack

- **Streamlit** — web UI
- **Agno** — agent framework with ReasoningTools
- **Google Gemini 2.5 Flash** — answer model
- **Gemini Embedding (gemini-embedding-001) + LanceDB** — vector knowledge base

## Run it locally

```bash
pip install -r requirements.txt
streamlit run rag_agent.py
```

Paste your Google API key (free from Google AI Studio) in the app, add a few source URLs, and start asking.

## Where I use it

This pattern powers document Q&A over my class course materials — the same approach behind the AI assistant in [Study Hub](https://fa24-bai.vercel.app), my study platform for the FA24-BAI cohort: students ask a question and get an answer drawn from the actual lecture files, with the source named.

## Author

**Abdul Wahid** — AI/ML Developer
[Portfolio](https://www.abdulwahid.me) · [GitHub](https://github.com/abduIwahid) · [LinkedIn](https://www.linkedin.com/in/abdu1wahid)

## Credits

Adapted from a template in the [awesome-llm-apps](https://github.com/Shubhamsaboo/awesome-llm-apps) collection by Shubham Saboo, and reworked to run fully on Gemini (embeddings included) instead of requiring an OpenAI key. Licensed under Apache-2.0 — see [LICENSE](LICENSE).
