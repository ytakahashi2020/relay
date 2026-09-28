# Relay

_Payment rails for AI agents to autonomously pay each other for compute and data_

## Summary

Relay is a Solana-based protocol that lets autonomous AI agents discover, pay, and rate each other for services like API calls, data feeds, or compute jobs. It uses streaming micropayments and on-chain reputation so agents can transact without human intervention or trust setup.

## Target users

AI agent developers, autonomous agent frameworks, API/data providers

## Problem

AI agents increasingly need to pay for services (APIs, data, compute) in real time, but existing payment rails require human-in-the-loop card payments or slow invoicing, blocking full autonomy.

## Solution

A Solana program that lets agents open payment streams, settle per-call micropayments in stablecoins, and build verifiable on-chain reputation scores for future trust decisions.

## MVP features

- Agent wallet SDK for instant stablecoin micropayments per API call
- On-chain escrow with streaming payments settled via Solana program
- Reputation registry storing success/failure history per agent
- Simple marketplace UI to list and discover paid agent services
- Demo: two AI agents autonomously negotiating and paying for a task

## Chains

Solana

## Tech

Anchor, Rust, Solana Pay, USDC, Next.js, OpenAI/LLM SDK, TypeScript

## Category

AI

## Why now

Agentic AI is exploding and needs native payment rails; Solana's speed and low fees make it the natural settlement layer for machine-to-machine microtransactions.

## Roadmap

- Add multi-agent negotiation protocol with dynamic pricing
- Integrate with popular agent frameworks (LangChain, AutoGPT)
- Launch mainnet marketplace with real API providers
