# Governed Evidence Search

Retrieval-augmented search over a synthetic clinical trial protocol corpus, with governance built in from the start: deterministic retrieval first, an optional grounded and cited AI synthesis second, and the exact model context one click away.

**[Live demo](https://governed-evidence-search.vercel.app)** — works immediately with the built-in deterministic retrieval, no setup required. Adding the AI-synthesized, cited answer on top needs your own LLM API key — any OpenAI-compatible API (OpenAI, OpenRouter, Groq, Together, or a local Llama server) or an Anthropic-style API. The key is used client-side only and is never stored or sent anywhere except the endpoint you choose. Please use fictional/sample data only.

## Who it's for

Clinical development, medical affairs, and real-world-evidence teams evaluating how to put generative AI on top of protocol and evidence libraries safely.

## Why it matters

Most AI search demos hide the important part: what got retrieved, why, and whether the model actually used it. In a regulated evidence setting, a tool nobody can audit is a tool nobody can trust with a real decision. This tool makes every step visible: what was retrieved, why, and exactly what the model was given, so an answer can be checked rather than trusted.

## What it does

- Ask a question in plain language, or click an example, and see the ranked protocols with match scores and matched terms
- Get a deterministic, no-model readout of the retrieved records
- Optionally add your own LLM API key — OpenAI-compatible (including Llama models) or Anthropic-style, kept in browser memory only — for a grounded synthesis that cites protocol IDs and says when the excerpts aren't enough
- Inspect exactly what was sent to the model

## Product decisions that mattered more than the model

1. **Retrieval before generation** — the pipeline is fixed by code, not chosen by the model
2. **Data minimization** — the model only ever sees the few excerpts retrieval selected
3. **Works without AI** — the deterministic path is useful on its own, so the AI layer is additive

## Built with

- HTML, CSS, JavaScript (single-file prototype, no framework, no build step)
- Any LLM API, provider-agnostic: OpenAI-compatible or Anthropic-style (optional, called from the browser with a user-supplied key)

## Run locally

Open `index.html` in any browser — no install needed.

## Status

This is a prototype built to explore a problem space, using fictional/synthetic data — not a finished product and not connected to any organization's real systems. Built by [Jane Natividad](https://github.com/jane-natividad) — see more at [jane-natividad.github.io](https://jane-natividad.github.io).
