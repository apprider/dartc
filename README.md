# DARTC Protocol

**Distributed Agent Real-Time Communication**

> Real-time signed transport for the open AI agent ecosystem  
> **v0.2** • **MIT Licensed** • **May 2026**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Status](https://img.shields.io/badge/Status-Implementation%20Draft-blue)]()
[![A2A Compatible](https://img.shields.io/badge/A2A-Compatible-green)]()

---

## The Missing Real-Time Layer for Agents

[A2A (Agent2Agent)](https://a2a-protocol.org) and [MCP (Model Context Protocol)](https://modelcontextprotocol.io) are defining how agents **discover** and **use tools**.  

**DARTC** completes the stack as the **real-time transport layer**:

- Low-latency peer-to-peer delivery via WebRTC DataChannels
- Signed envelopes with Ed25519 + replay protection
- Native streaming support (deltas, chunks, final flags)
- Graceful WebSocket fallback
- Topic-multiplexed (`a2a.*`, `dartc.*`, custom)

DARTC is designed from the ground up to carry **A2A payloads** and is proposed as an **official real-time binding** for the A2A protocol.

---

## Quick Links

- **Official Website**: https://www.dartc.org
- **Full Specification**: [SPECIFICATION.md](./SPECIFICATION.md)
- **One-Page Summary**: [one-pager.md](./one-pager.md)
- **GitHub Discussions**: [Join the conversation](https://github.com/your-org/dartc/discussions)
- **A2A Binding Proposal**: Open issue on [a2aproject/A2A](https://github.com/a2aproject/A2A)

---

## Current Status (v0.2)

- ✅ Complete protocol specification published
- ✅ Envelope format, canonicalization, signing, and topic model defined
- 🚧 Reference implementation in progress:
  - Shared TypeScript package (`@dartc/core`)
  - Browser WebRTC client
  - Origin daemon with signature verification
- 🎯 **Goal**: Become an official A2A transport binding under neutral Linux Foundation / AAIF governance

---

## Why DARTC Matters

| Use Case                    | How DARTC Helps                              |
|----------------------------|----------------------------------------------|
| Real-time chat / streaming | Native delta + chunk support                 |
| Browser-based agents       | WebRTC DataChannels (no server relay needed) |
| Enterprise multi-agent     | Signed + replay-protected messages           |
| Long-running tasks         | `requires_ack`, `is_final`, priority levels  |
| Cross-vendor interoperability | Works with any A2A-compliant agent         |

---

## Getting Started

```bash
# Clone the repo
git clone https://github.com/your-org/dartc.git

# Read the spec
open SPECIFICATION.md
```

## How to Contribute

We welcome contributions from individuals and organizations!

Read CONTRIBUTING.md
Join GitHub Discussions
Propose changes via Pull Request
For major proposals (especially A2A binding), open an issue first

## Governance & Neutrality

DARTC is currently maintained by the GemmaPod Project but is explicitly designed for neutral, community-driven governance.
We are actively seeking:

A home under the Linux Foundation or Agentic AI Foundation (AAIF)
Foundational sponsors and Technical Steering Committee members

## License

MIT License — see LICENSE

DARTC — The real-time foundation for interoperable AI agents.
Let’s build the open agent internet together.