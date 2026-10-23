# AZ-900 Quiz Coach (Unofficial)

> **Unofficial study tool.** Not affiliated with or endorsed by Microsoft. All questions are original and based on the public AZ-900 skills outline on Microsoft Learn. No real exam questions, no Microsoft logos.

Built for the **Vibe Coding Hackathon: AZ-900 Exam Prep Edition** (#1MillionDevs), theme *"Building Smarter Exam Prep Tools from Our Own Learning Journey."*
Challenge: **Practice & Assessment (Smart Quiz Builder)**, with a built-in **Readiness Tracker** view.

**Live prototype:** https://claude.ai/artifact/ViFD1NUKz6VLSTLjTcUBZU
**Demo video:** _add link_  |  **Pitch deck:** _add link_

## The problem (from my own AZ-900 journey)

I understood the concepts, but I kept losing marks on **"twin" services that sound alike**: Conditional Access vs RBAC, VPN Gateway vs ExpressRoute, NSG vs Azure Firewall, Advisor vs Service Health vs Resource Health, ACI vs AKS vs Functions. My scores swung from 80% down to 40% on a networking round, and only recovered once I started **learning services in pairs** and **drilling fresh wording after each miss**. Most practice tools only say "wrong". I wanted one that tells me *why*, and shows *which topic* to fix.

## What it does

- 36 original questions across the three official AZ-900 domains: Cloud Concepts, Azure Architecture & Services, Management & Governance
- **Instant feedback** on every answer with a clear "why this is right" explanation
- Options are shuffled on every attempt, so you test the logic and not your memory of the answer position
- **Readiness view:** score by topic, with a "Revise these first" list and the missed questions explained again
- **Retry missed questions** to drill weak spots
- **Twin Drills:** 12 paired-service questions (Conditional Access vs RBAC, VPN Gateway vs ExpressRoute, NSG vs Azure Firewall, and more) with a trigger-word hint and a "how they differ" explanation
- **Saved progress:** your per-topic accuracy persists on your device, with a "Drill my weak spots" button that rebuilds a quiz from the questions you keep missing
- Works on phones, supports light and dark mode

## Tech

Single-file HTML, CSS and vanilla JavaScript. No backend, no dependencies, so it loads instantly on low-bandwidth connections. Built with AI-assisted "vibe coding" using Claude.

## Run it

Open `index.html` in a browser, or enable GitHub Pages on this repo.

## Prompt engineering (how I used Claude)

1. **Scoping prompt:** I pasted the full hackathon brief and the deadline and asked for the best challenge to finish in one day. Result: Smart Quiz Builder plus a readiness view, with a timed plan.
2. **Build prompt:** asked for a single-page quiz with domain filter, instant explanations, per-topic results and a retry-missed mode, an unofficial label, and original questions only (no real exam content).
3. **Content-quality prompt:** every question must have one clearly correct answer, plausible distractors, and a short explanation that teaches the concept. I reviewed each one against Microsoft Learn.
4. **Learner-journey prompt:** I fed my own study results (scores and the pairs of services I confused) so the next version targets "twin" service confusion.

## Build log and tool choices (rapid prototyping)

1. **Scoping (first ~15 min):** gave Claude the full brief and the deadline, and chose one challenge (Smart Quiz Builder) plus a readiness view instead of building five half-tools.
2. **First working prototype:** one prompt produced a playable quiz with explanations and a topic score screen, published and shareable straight away.
3. **Pivot from my own data:** I reviewed my real AZ-900 score history and found my misses clustered on "twin" services, so I added **Twin Drills** with trigger-word hints.
4. **Progress tracking:** added saved per-topic readiness and a weak-spot drill, so the tool adapts to the learner.
5. **Docs and submission:** README, pitch deck (Canva) and demo video.

**Tools used:** Claude.ai (scoping, build, question drafting, README), GitHub and GitHub Pages (repo and hosting), Canva (pitch deck).
**Deliberate trade-off:** a single static file with browser storage, so there is no backend to break and it loads fast on low bandwidth. Supabase is the planned next step for cross-device progress and cohort leaderboards.

## Roadmap

- Expand Twin Drills to every confusing service family
- Supabase for cross-device progress and a cohort leaderboard
- Spaced repetition that resurfaces missed questions
- Swahili and African real-life explanations (for example, availability zones through the lens of M-Pesa uptime)
- Question bank expansion, then other certifications (AZ-104, AI-900, SC-900)

## Disclaimer

Practice scores here are not a prediction of exam results. Always use the official Microsoft Learn skills outline and practice assessments alongside this tool.
