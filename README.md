# AI-VMF: Vulnerability Management Framework for Autonomous AI Agents

**Status:** Early draft — work in progress   
**Author:** Rohan Kumar Sachdeva

---

## What this is

AI agents are being deployed in production environments without a standardized way to identify, classify, or track the vulnerabilities specific to them.

Existing frameworks like NIST AI RMF and FedRAMP provide governance-level guidance but were designed for deterministic software systems. They do not have answers for things like prompt injection through retrieved content, behavioral drift over time, cascading tool invocations, or credential exposure through an agent's output. I ran into this gap directly while working on vulnerability management and API security, and I haven't found a framework that addresses it systematically.

This repo is my attempt to build one.

---

## What I'm working toward

The goal is a structured framework covering:

- A vulnerability taxonomy specific to AI agent systems (not just LLM apps — agents with tool use, memory, and autonomous action)
- A risk scoring model that accounts for an agent's privilege level, tool access scope, and execution autonomy — because the same vulnerability has very different blast radius depending on what the agent can do
- A behavioral monitoring spec for detecting drift and anomalies at runtime
- A compliance mapping to NIST AI RMF, FedRAMP, and sector-specific standards
- A standardized disclosure format so findings can be shared across organizations

---

## Current state

- [ ] Vulnerability taxonomy — first draft in progress
- [ ] AAF (Autonomy Amplification Factor) scoring model — draft
- [ ] Behavioral monitoring architecture — notes only
- [ ] Compliance mapping — partial
- [ ] Disclosure schema — not started

The spec will be added to this repo in sections as I work through it. I'm also planning to submit the taxonomy to OWASP's LLM Top 10 working group once it's in reasonable shape.

---

## Why I'm doing this in the open

A few reasons. One is that this kind of framework only becomes useful if it reflects real-world deployment patterns, not just one person's threat model. Another is that standards contributions require public prior art. And frankly, working through this in public is a good forcing function for making the thinking rigorous.

If you work in AI security and have opinions about what belongs in the taxonomy, or what I'm getting wrong, open an issue. Early feedback is more useful than late feedback.

---

## Repo structure (planned)

```
/spec          ← the framework specification documents
/taxonomy      ← vulnerability catalog entries
/examples      ← example disclosure reports using the schema
/mappings      ← compliance mapping tables
```

---
