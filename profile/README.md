# revitbridge

**An intent bridge between designers and AI for Autodesk Revit.**
It turns a designer's brief into a confirmed task spec, runs it inside Revit, and verifies the result. Model-agnostic: bring your own Claude, OpenAI-compatible or local model.

设计师意图与 AI 之间的桥：把一句话的需求变成每个参数都有出处、经设计师确认的任务规格，在 Revit 中执行并验证结果。

Pick your door:

## 1. Designer (设计师) — use it inside Revit

1. Install the Revit add-in with one PowerShell line (Revit 2020, 2021, 2023-2026; every installed year gets its own install): see [revit-bridge-addin → Install](https://github.com/revitbridge/revit-bridge-addin#install).
2. In Revit, click **Revit MCP Switch** on the ribbon.
3. Open the demo host and pair: see [revit-bridge-web → Install](https://github.com/revitbridge/revit-bridge-web#install).

## 2. Claude user (Claude 用户) — Claude Code / Claude Desktop

1. Install the add-in (step 1 above).
2. In Claude Code: `/plugin marketplace add revitbridge/revit-bridge` then `/plugin install revit-bridge@revit-bridge`.
   Claude Desktop or any MCP client: `uvx revit-bridge`, see [revit-bridge → Install](https://github.com/revitbridge/revit-bridge#install).
3. Describe what you want built. Claude reads the project snapshot, asks only what it cannot know, and executes after you confirm the spec.

## 3. Developer (开发者) — build on it or self-host

1. `uvx revit-bridge` is the MCP server; `pip install revit-bridge` gives you the Python API. Docs: [revit-bridge → Use](https://github.com/revitbridge/revit-bridge#use).
2. Self-host the demo web app: `docker compose up`, see [revit-bridge-web → Install](https://github.com/revitbridge/revit-bridge-web#install).
3. Optional Revit API reference for weaker models (data set: Revit 2026 only): `uvx revit-api-docs`, see [revit-api-docs](https://github.com/revitbridge/revit-api-docs#install).

## Repositories

| Repo | What it is |
|---|---|
| [revit-bridge](https://github.com/revitbridge/revit-bridge) | Python package, MCP server, Claude Code plugin and marketplace |
| [revit-bridge-addin](https://github.com/revitbridge/revit-bridge-addin) | Revit add-in (C#), installer, releases |
| [revit-bridge-web](https://github.com/revitbridge/revit-bridge-web) | Deploy-anywhere demo host (`docker compose up`) |
| [revit-api-docs](https://github.com/revitbridge/revit-api-docs) | Optional Revit API reference MCP server |

All public code is MIT licensed. The Revit add-in is a fork of [mcp-servers-for-revit](https://github.com/mcp-servers-for-revit/mcp-servers-for-revit).
