# Devlog Draft

I rebuilt this into **Atlas Fleet**, a public-safe vault graph workbench for AI-agent systems.

The project parses markdown-style notes, extracts `[[wiki links]]` and `#tags`, and turns them into an interactive graph. The point is to show how a private second-brain / agent-fleet setup can be mapped without exposing the private vault itself.

What I built:

- Markdown note parser
- Wiki-link graph generator
- Tag-based graph filters
- Clickable node inspector
- Cluster, ring, and column graph layouts
- Search across notes, links, and tags
- Approval-style task queue generated from parsed notes
- JSON export
- Static single-file app with no backend

The privacy part matters: the real system this is inspired by has private notes and workflows, so the public version uses synthetic sample notes only. It shows the architecture without leaking personal data, credentials, server details, or private prompts.

The hardest part was turning the idea from “a pretty graph” into something closer to a real tool. The graph is now data-driven: edit the sample vault, click **Parse vault**, and the graph, filters, table, stats, inspector, and queue all update from the parsed notes.

Repo: https://github.com/unnholy/public-vault-graph-demo
Live preview: https://raw.githack.com/unnholy/public-vault-graph-demo/main/index.html

