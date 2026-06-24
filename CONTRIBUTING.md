# Contributing to uBase

Thanks for your interest in contributing to uBase! This document explains how to submit packets, report issues, and get involved with the project.

---

## Ways to Contribute

### 1. Submit a New Packet

A packet is a self-contained `.ubase` file that adds a reusable feature to any Base44 app.

**To submit a new packet:**

1. Fork this repository
2. Create a new folder under `/packets/your-packet-name/`
3. Include the required files (see structure below)
4. Open a Pull Request with a clear description of what your packet does

**Required packet structure:**
```
/packets/your-packet-name/
├── meta.json        ← required
├── prompt.md        ← required
├── README.md        ← required
├── functions/       ← optional, backend .ts files
├── components/      ← optional, frontend .jsx files
└── entities/        ← optional, entity schema .json files
```

**meta.json format:**
```json
{
  "name": "Your Packet Name",
  "version": "1.0.0",
  "description": "What this packet does in one sentence",
  "author_name": "Your Name",
  "author_email": "you@example.com",
  "category": "UI | Auth | Payments | Email | Analytics | Utilities | Other",
  "tags": ["tag1", "tag2"],
  "price": 0
}
```

**prompt.md rules:**
- Must start with exactly these two lines:
  ```
  Please help me through this install process to enhance my app.
  
  Please read these instructions and build the feature into the current app.
  ```
- No title headers at the top
- No trust declaration blocks
- All backend code must use bracket notation (no dot notation)
- All functions must use arrow function syntax

---

### 2. Improve an Existing Packet

Found a bug or a way to make a packet better?

1. Fork the repo
2. Make your changes in the packet's folder under `/packets/`
3. Bump the version in `meta.json` (patch for fixes, minor for features)
4. Open a PR describing what you changed and why

---

### 3. Report an Issue

Open a [GitHub Issue](https://github.com/xBuildyTeam/ubase/issues) with:
- Which packet is affected
- What you expected to happen
- What actually happened
- Your Base44 app type (if relevant)

---

### 4. Suggest a Feature

Have an idea for a new packet type or standard improvement? Open an Issue with the `enhancement` label and describe your idea.

---

## Code Standards

All packet code must follow the uBase code standard:

- **Bracket notation only** — `obj["property"]` not `obj.property`
- **Arrow functions only** — `const fn = () => {}` not `function fn() {}`
- **No module-level fetch** — all external calls inside `Deno["serve"]()`
- **No dot notation in Deno globals** — `Deno["env"]["get"]()` not `Deno.env.get()`

---

## Review Process

1. Submit your PR
2. A maintainer will review within 7 days
3. Feedback will be left as PR comments
4. Once approved and merged, the packet becomes eligible for the marketplace

---

## Questions?

Reach out at **team@ubase.tech** or open a GitHub Discussion.
