# Devlog Draft

I rebuilt my project into a public-safe dashboard for a private AI-agent / knowledge-vault system.

The hard part was not just making a graph. The hard part was showing the architecture of a real private setup without leaking personal notes, credentials, server details, school/health records, or private agent prompts. So I made a sanitized dashboard that keeps the useful structure and replaces private content with representative sample data.

What it includes:

- Interactive graph generated from sample markdown notes
- Built-in parser for `[[wiki links]]` and `#tags`
- Clickable node inspector
- Search and graph filters
- Agent role roster
- Task routing pipeline
- Approval-band safety model
- Static single-file HTML app

The dashboard models how a private second-brain system can route work between different AI agents: a front-door agent receives tasks, a command agent decomposes work, specialists handle research/security/building, and sensitive actions pass through approval gates.

The newest feature is the parser tab: it takes bundled sample markdown notes, extracts links and tags, shows the parsed table, then rebuilds the graph from that data. That makes the demo closer to the real idea: a vault graph should come from notes, not just hardcoded boxes.

I also added the privacy layer intentionally. The public app shows the system design, but it does not expose the actual private vault or any personal data.

Repo: https://github.com/unnholy/public-vault-graph-demo
Live preview: https://raw.githack.com/unnholy/public-vault-graph-demo/main/index.html
