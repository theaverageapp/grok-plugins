---
name: streeq
description: Use STREEQ tools after the user is signed in. Review workouts, meals, and self-managed plans. Do not invent fitness data.
---

# STREEQ

Use the STREEQ MCP tools when the user is working with their own STREEQ record.

Rules:

- Authenticate before reading or writing.
- Only act on the signed-in person's record.
- Do not invent workouts, meals, or measurements.
- Use the typed STREEQ mutation tools for plan or log changes.
- If a tool is missing or auth fails, say so and point to https://streeq.app/connect-ai
