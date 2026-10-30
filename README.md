# Governed Evidence Search

Searches trial protocols and shows its work at every step, with optional AI answers that cite their sources.

**[Try the live demo](https://governed-evidence-search.vercel.app)**. It works straight away with no setup. To try the AI step, paste your own LLM API key. It works with any OpenAI compatible API (OpenAI, OpenRouter, Groq, Together, or Llama running on your own machine) or an Anthropic style API. Your key stays in your browser and is only sent to the endpoint you choose. Please use fictional or sample data only.

## Why I built it

Every AI search demo I saw skipped the part a regulated team cares about most: what was retrieved, and whether the answer actually used it. So I started from that end, built the scaffolding first, and made every step visible.

## The problem

Most AI search demos hide the important part: what was retrieved, why, and whether the model actually used it. In a regulated setting, a tool nobody can audit is a tool nobody can trust.

## What I built

A search tool over 12 made up trial protocols. It finds the best matches itself with no AI and no setup. If you add your own key, it writes a short answer using only those excerpts, cites a protocol for every statement, and shows exactly what the model was given.

## Who it's for

Clinical development, medical affairs and real world evidence teams exploring how to use generative AI safely.

## What it does

- Ask a plain language question and see ranked protocols with match scores
- Get a readout of the matches with no model involved
- Optionally add your own key for a grounded, cited answer
- See exactly what was sent to the model

## Decisions that shaped it

1. **Retrieval comes first:** the code decides each step, so the process is predictable.
2. **The model sees very little:** only the few excerpts that matched are shared.
3. **Useful on its own:** the search works without AI, which makes the AI step a bonus.

## Key takeaway

The model is the easy, swappable part. The real work is everything around it.

## Built with

- HTML, CSS and JavaScript in a single file
- Any LLM API (optional, bring your own key)

## Run it locally

Open `index.html` in any browser. There's nothing to install.

## About this project

This is a working prototype I built to explore a real problem space. It uses illustrative, fictional data and isn't connected to any organisation's systems. You can find more of my work at [jane-natividad.github.io](https://jane-natividad.github.io).

Built by [Jane Natividad](https://github.com/jane-natividad).
