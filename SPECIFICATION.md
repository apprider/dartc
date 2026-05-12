# DARTC Protocol v0.2

**Distributed Agent Real-Time Communication**  
*Real-time signed transport for the open agent ecosystem*  
**MIT Licensed** • **Neutral Governance (Proposed)** • **May 2026**

---

### The Missing Layer in the Agent Stack

A2A (Agent2Agent) and MCP (Model Context Protocol) are rapidly becoming the standard for **semantic interoperability** and **tool access**.  

**What’s still missing?**  
A production-grade, low-latency, signed **real-time transport layer** that works across browsers, edge, and servers — with graceful fallback and strong security guarantees.

**DARTC fills that gap.**

---

### What is DARTC?

DARTC is an open, signed, topic-multiplexed message envelope designed as the **real-time transport binding** for A2A (and other agent protocols).

It runs over **WebRTC DataChannels** (peer-to-peer) with **WebSocket relay fallback**, delivering:
- Sub-100ms latency for streaming
- End-to-end signing (Ed25519)
- Replay protection
- Native support for long-running tasks and deltas

---

### Key Capabilities

| Feature                    | Benefit                                      |
|---------------------------|----------------------------------------------|
| **WebRTC + WS Fallback**  | True P2P when possible, reliable everywhere  |
| **Signed Envelopes**      | Ed25519 over canonical JSON — tamper-proof   |
| **Topic Multiplexing**    | `a2a.*`, `dartc.*`, `gemmapod.*`, custom     |
| **Streaming Native**      | `stream`, `chunk_id`, `is_final` metadata    |
| **Acknowledgements**      | `requires_ack` + `dartc.ack` for reliability |
| **Browser + Daemon Ready**| Reference impl in progress (browser shim + origin daemon) |

---

### Perfect Complement to A2A & MCP

- **A2A** = Semantic layer (Agent Cards, tasks, messages)  
- **MCP** = Tool & data access layer  
- **DARTC** = **Real-time transport layer**

DARTC topics beginning with `a2a.` carry full A2A objects in the `a2a` field while adding real-time delivery metadata. It is explicitly designed to become an **official A2A transport binding**.

---

### Current Status (v0.2 – Implementation Draft)

- Full protocol specification published  
- Envelope, canonicalization, signing, and topic model defined  
- Reference implementation roadmap:  
  1. Shared `@gemmapod/dartc` TypeScript package  
  2. Browser WebRTC client  
  3. Origin daemon with signature verification  
  4. A2A Agent Card + streaming integration  

**Seeking:** Neutral home under **Linux Foundation / Agentic AI Foundation (AAIF)** and foundational sponsors.

---

### Why Companies Should Support DARTC

- Completes the open agent stack (A2A + MCP + DARTC)  
- Enables low-latency, browser-native, and enterprise-grade real-time agents  
- Strong security model aligned with A2A’s “secure by default” principle  
- 100% MIT + vendor-neutral governance

---

### Get Involved

**Review the Spec**  
https://github.com/[your-org]/dartc (or dartc.org)

**Propose as Official A2A Binding**  
Open issue on https://github.com/a2aproject/A2A

**Become a Foundational Sponsor**  
Contact: [your-email] • LinkedIn: [your-profile]

**Join the Community**  
GitHub Discussions • MCP Dev Summit 2026

---

**DARTC** — *The real-time glue for the next generation of interoperable AI agents.*

*Proposed by the GemmaPod Project • Now seeking neutral governance and ecosystem partners*