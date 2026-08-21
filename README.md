# Christian Hartmann

**Senior Software Engineer & Architect** · [Hartmann Softwareengineering](https://www.hartmann-softwareengineering.de)

I design and build systems that have to survive a few years in production, mainly with Java and Spring on the backend, React and TypeScript on the frontend, Python wherever it's the shorter path. Most of my professional work happens behind NDAs, so what you'll find here are the side projects: small, sharp tools that solve exactly one problem, properly.
A lot of what I build in public comes out of a second life: I'm an active member of a volunteer fire department. That's where the requirements come from, not from a market analysis.

Currently working my way into **AI Engineering**, meaning less prompt tinkering, more building things that hold up outside a demo.

---

## Currently building

### [ResQ Ready](https://www.resqready.de) - mandatory-training platform for fire departments
Managing UVV, respiratory protection and vehicle briefings digitally: create, assign, prove. Readiness score for the commander, approval workflow for instructors, audit-ready reports. Multi-tenant, mobile-first, hosted in Germany.
*Status: closed beta with pilot departments.*

### [Sketchury](https://www.sketchury.de) - animated whiteboard videos for online courses
SaaS that lets course creators produce whiteboard-style explainer videos, drawn path by path, with a tracking hand, without any animation skills. Script-first, chapters, multilingual, LMS export. Deliberately built for teaching rather than generic marketing clips.
*Status: MVP feature-complete, beta release imminent.*

The interesting constraint in Sketchury: the animation engine runs both in the browser preview and inside the server-side Remotion renderer. So it's headless by design — no React, no DOM except through injected adapters — with the UI layer only ever touching the public engine API. Everything else follows from that one boundary.

---

## AI Engineering, in practice

Sketchury doubles as my working laboratory for AI engineering. A real product with real constraints, which turns out to be a much better teacher than a tutorial:

- **Agents that write the video.** Scripts and complete storyboards generated end to end, then handed to the engine as structured data. Exposed as a Claude Code skill over bearer-authenticated API keys, which makes the product itself agent-addressable.
- **Synthetic narration.** Voiceover generation via text-to-speech APIs, timed against the scene script and its subtitles.
- **Agentic features inside a web frontend.** The unglamorous half: streaming, partial results, failure states, and giving the user somewhere to intervene when the model gets it wrong.
- **Agentic coding itself.** Building a monorepo of this size largely with coding agents, and paying close attention to where they genuinely accelerate the work and where they quietly don't. My [`skills`](https://github.com/ChristianHartmann/skills) repo is the other side of that: tooling to make agents better at the parts they're weakest at.

---

## Open source

**[skills](https://github.com/ChristianHartmann/skills)** · Python
Agent Skills for coding agents. `ui-variants` turns a UI design question into side-by-side, clickable variants. Built from your app's actual CSS, not a generic mockup.

**[centerline](https://github.com/ChristianHartmann/centerline)** · Python
Single-stroke pen paths from any outline font. Computes the exact medial axis of the glyph's Bézier contours instead of rasterizing first, then prunes it, fits splines and splits the result into strokes.

**[CBRNBuddy](https://github.com/ChristianHartmann/CBRNBuddy)** · TypeScript
Offline hazmat assistant for firefighters. Detects orange ADR placards with an on-device YOLO model, identifies the substance and shows the immediate measures. Android, German UI, no network required.

**[urkunden-editor](https://github.com/ChristianHartmann/urkunden-editor)** · JavaScript
Fill certificates from templates, export as PDF, print - including batches from a participant list. Runs offline and without an account; templates and styling are configurable per club.

---

## Stack

| | |
|---|---|
| **Backend** | Java · Spring Boot · Python · Postgres · RabbitMQ · Kafka |
| **Frontend** | React · TypeScript |
| **Architecture** | Domain-driven design, service boundaries, long-lived systems |
| **Exploring** | AI Engineering - agents, on-device models, LLM-backed tooling |

---

## Get in touch

- Website — [hartmann-softwareengineering.de](https://www.hartmann-softwareengineering.de)
- Open to conversations about architecture, JVM systems and where AI actually earns its place in them.

<!--
**ChristianHartmann/ChristianHartmann** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
