# uBase

**The open standard for packaging and sharing reusable features across Base44 apps.**

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Built for Base44](https://img.shields.io/badge/Built%20for-Base44-6366f1)](https://base44.com)
[![Marketplace](https://img.shields.io/badge/Marketplace-ubase.tech-0ea5e9)](https://ubase.tech)

---

## What is uBase?

uBase is an open standard for packaging and distributing reusable features as `.ubase` files — portable zip archives that any Base44 developer can install into their app in minutes.

Stop rebuilding the same things. Package it once, share it everywhere.

---

## What's a `.ubase` file?

A `.ubase` file is a zip archive containing everything needed to install a feature into any Base44 app:

```
my-feature.ubase
├── meta.json          ← name, version, author, category
├── prompt.md          ← AI install instructions for the Base44 builder
├── README.md          ← human-readable documentation
├── functions/
│   └── myFeature.ts  ← backend logic (Deno/TypeScript)
├── components/
│   └── MyWidget.jsx  ← frontend UI (React)
└── entities/
    └── MyEntity.json ← data schema
```

When dropped into the Base44 builder, the `prompt.md` guides the AI to install entities, deploy functions, and place components — automatically.

---

## Marketplace

Browse and install community packets at **[ubase.tech](https://ubase.tech)**.

---

## Contributing

We welcome contributions of all kinds:

- 📦 **Submit a new packet** — package a feature and publish it to the marketplace
- 🛠️ **Improve an existing packet** — fork, improve, and submit a PR
- 🐛 **Report issues** — open a GitHub Issue for bugs or broken installs
- 💡 **Suggest features** — propose new packet types or standard improvements

See [CONTRIBUTING.md](./CONTRIBUTING.md) to get started.

---

## Repository Structure

```
/packets          ← community-contributed packet source files
  /packet-name/
    meta.json
    prompt.md
    README.md
    functions/
    components/
    entities/
/docs             ← standard documentation and guides
/examples         ← example packets for reference
```

---

## Roadmap

See [ROADMAP.md](./ROADMAP.md) for planned features and the long-term vision.

---

## Join the Team

uBase is actively looking for contributors who love building on Base44. Whether you want to submit a single packet or become a core maintainer, there's a place for you here.

Reach out: **team@ubase.tech**

---

## License

MIT © [xBuildyTeam](https://github.com/xBuildyTeam)
