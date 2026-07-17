# Hermes Vault Fleet Dashboard

An interactive, public-safe dashboard for a private knowledge-vault and AI-agent routing architecture.

This is a sanitized version of a larger private vault/fleet design. It keeps the architecture, dashboard layout, graph interaction, agent roster, routing pipeline, and safety model, but uses sample data only.

## Problem

Large personal AI setups get messy fast: notes live in a vault, agents have different jobs, sensitive actions need approval, and it becomes hard to see what is connected to what. I wanted one dashboard that explains the whole system without exposing the private vault behind it.

## Features

- Overview cards for project scope
- Interactive graph generated from sample markdown notes
- Built-in parser for `[[wiki links]]` and `#tags`
- Search and graph filtering
- Clickable node inspector
- Agent role roster
- Multi-step routing pipeline
- Approval-band safety model
- Single-file static app
- No private notes, credentials, school records, health records, or local paths

## Technical details

- The graph is rendered with plain DOM nodes and calculated SVG-like edge lines using CSS transforms.
- The parser reads bundled sample markdown blocks, extracts wiki links and tags, and turns them into graph data.
- Search filters visible graph nodes by title, summary, and tags.
- Navigation tabs switch between overview, graph, agent roster, routing pipeline, and safety model.
- The right-side inspector updates from shared node data, so the graph and metadata stay in sync.
- The app is static and offline-capable: no backend, no database, no analytics, no external API calls.

## Privacy design

The original private system includes real notes, agent prompts, server setup notes, and personal workflows. This public repo does not include that material. The public dashboard uses representative sample nodes so the architecture is visible without leaking the actual vault.

## Why I built it

I wanted a way to show the structure of a growing AI-agent / knowledge-vault setup without exposing the private vault itself.

## Build log

- Built a first graph prototype with clickable sample nodes.
- Reworked it into a full dashboard after the first version looked too small.
- Added architecture tabs for agent roles, task routing, and approval gates.
- Added graph edges, filters, search, and an inspector panel.
- Added a sample markdown vault parser that rebuilds the graph from `[[links]]` and `#tags`.
- Sanitized all content so the repo can be public.

## Run

Open `index.html` in a browser.
