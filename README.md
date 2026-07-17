# Atlas Fleet: Vault Graph Workbench

Atlas Fleet is a public-safe workbench for turning markdown-style vault notes into an interactive agent-routing graph.

The original idea came from organizing a private AI-agent / second-brain setup. This repo does not include private notes, credentials, server details, school records, health records, or personal files. It ships with synthetic sample notes so the architecture can be reviewed safely.

## Features

- Parses bundled sample markdown notes
- Extracts `[[wiki links]]` into graph edges
- Extracts `#tags` into filters and categories
- Renders an interactive graph with clickable nodes
- Supports cluster, ring, and column layouts
- Includes search, graph filters, and a node inspector
- Generates an approval-style task queue from parsed notes
- Exports the parsed graph as JSON
- Runs as one static HTML file

## Why It Exists

AI-agent systems get hard to reason about once notes, routing rules, safety gates, and specialists all live in different places. Atlas Fleet turns that structure into a visible map:

1. Notes describe tools, agents, hubs, and guardrails.
2. Wiki links become graph edges.
3. Tags classify nodes as hubs, agents, tools, or approval guards.
4. The queue shows which work is automatic and which needs review.

## Technical Notes

- No framework
- No backend
- No build step
- No external APIs
- No private data
- Graph geometry is calculated directly in JavaScript
- Edges are DOM elements rotated with CSS transforms

## Run

Open `index.html` in a browser.

Live preview:
https://raw.githack.com/unnholy/public-vault-graph-demo/main/index.html

