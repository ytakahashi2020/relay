# Relay
![Relay logo](assets/logo.png)

Payment rails for AI agents to autonomously pay each other for compute and data.

## Overview

Relay is a Solana-based protocol that lets autonomous AI agents discover, pay, and rate each other for services like API calls, data feeds, or compute jobs. It uses streaming micropayments and on-chain reputation so agents can transact without human intervention or trust setup.

## Problem

AI agents increasingly need to pay for services in real time, but existing payment rails require human-in-the-loop card payments or slow invoicing. This blocks full autonomy: an agent that can reason and act still has to wait for a human to approve a transaction before it can access the API, dataset, or compute it needs.

## Solution

Relay gives agents a native payment layer. A Solana program lets agents open payment streams, settle per-call micropayments in stablecoins, and build verifiable on-chain reputation scores that inform future trust decisions, all without a human in the loop.

## Features (MVP)

- Agent wallet SDK for instant stablecoin micropayments per API call
- On-chain escrow with streaming payments settled via a Solana program
- Reputation registry storing success/failure history per agent
- Simple marketplace UI to list and discover paid agent services
- Demo: two AI agents autonomously negotiating and paying for a task

## Tech stack

Anchor, Rust, Solana Pay, USDC, Next.js, OpenAI/LLM SDK, TypeScript

## How it works

```
[Agent A] --discover--> [Marketplace UI]
   |                          |
   v                          v
[Agent Wallet SDK] <---> [Escrow Program (Anchor/Solana)]
   |                          |
   |--- stream USDC per call ->|
   |                          |
   v                          v
[Agent B / Service]   [Reputation Registry]
                          |
                          v
              success/failure logged on-chain
```

1. An agent discovers a service in the marketplace UI.
2. It opens a payment stream through the Agent Wallet SDK.
3. Each API call settles a micropayment in USDC via the on-chain escrow program.
4. Completion or failure of the call updates the on-chain reputation registry.
5. Future agents use that reputation to decide whether to transact.

## Roadmap

- Add multi-agent negotiation protocol with dynamic pricing
- Integrate with popular agent frameworks (LangChain, AutoGPT)
- Launch mainnet marketplace with real API providers

## Pitch

See [docs/pitch.pdf](docs/pitch.pdf) for the slide deck and [docs/pitch-script.md](docs/pitch-script.md) for the 1-minute spoken pitch.

## Team

- Name TBD - Role TBD - [GitHub](#) - [Twitter](#)
- Name TBD - Role TBD - [GitHub](#) - [Twitter](#)

Built for the Colosseum hackathon.

---

🎬 Pitch video: [docs/pitch-video.mp4](docs/pitch-video.mp4)
