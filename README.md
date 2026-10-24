# AZ-900 Study Coach (Unofficial)

> **Unofficial study tool.** Not affiliated with or endorsed by Microsoft. All content is original and based on the public AZ-900 skills outline on Microsoft Learn. No real exam questions, no Microsoft logos.

Built for the **Vibe Coding Hackathon: AZ-900 Exam Prep Edition** (#1MillionDevs).

**Live prototype:** https://claude.ai/artifact/ViFD1NUKz6VLSTLjTcUBZU
**GitHub Pages:** https://github.com/plp-hackathons/AZ-900-Exam-Prep-Edition-for-the-1MillionDevs-Movement | **Demo video:** https://docs.google.com/videos/d/1dlszp_h8AUeYsIcqFyKG0Njhn4v1AkBkRMfoVSK6JnM/play?usp=sharing | **Pitch deck:** https://docs.google.com/videos/d/1dlszp_h8AUeYsIcqFyKG0Njhn4v1AkBkRMfoVSK6JnM/play?usp=sharing

## The problem (from my own AZ-900 journey)
I understood the concepts, but I kept losing marks on "twin" services that sound alike: Conditional Access vs RBAC, VPN Gateway vs ExpressRoute, NSG vs Azure Firewall, Advisor vs Service Health vs Resource Health. My scores swung from 80% down to 40% on a networking round, and only recovered once I learned services in pairs and drilled fresh wording after each miss.

## Choose how you revise
| Mode | What it is | Challenge it covers |
|---|---|---|
| **Smart Quiz** | 36 original questions, instant explanations, trigger-word hints, readiness by topic, retry weak questions | Practice and Assessment, Readiness Tracker |
| **Flashcard Coach** | Recall, reveal, rate (Got it / Hard / Missed it). Missed cards return in about 10 minutes, hard cards in 1 day, known cards at 1, 3, 7 and 14 day steps | Memory and Revision |
| **Study Buddy** | 8 concepts in simple words, with African real-life examples, a Kiswahili summary and a "do not mix up" note | Support |

Also: **Twin Drills** (12 paired-service questions), saved progress on your device, a light theme by default with a dark option, and no gradients. In v2, a **study planner** built with Bolt.new.

## Honest notes
- Study Buddy is written, curated content. It is **not** a live AI model yet (see roadmap).
- Flashcards use a simple Leitner-style schedule, a lightweight study heuristic and not a validated memory model.
- Progress is stored in your browser only. It does not sync across devices.
- Kiswahili summaries are short and should be reviewed by a fluent speaker. Content should be checked against the current Microsoft Learn study guide.
- Practice scores are not a prediction of exam results.

## Tech
Single-file HTML, CSS and vanilla JavaScript. No backend, no dependencies, no runtime network calls, so it loads quickly on low bandwidth. Built with AI-assisted vibe coding (Claude, plus Bolt.new for the v2 planner).

## Run it
Open `index.html` in a browser, or enable GitHub Pages.

## Roadmap
- Live AI Study Buddy through a server-side function (API key never in the browser), restricted to AZ-900 topics
- Supabase accounts and cross-device sync
- More cards in every mode, each checked against Microsoft Learn
- More Kiswahili and other local-language explanations
- Other certifications (AI-900, SC-900, AZ-104)

See `PROMPTS.md` for how I used prompts to build and iterate.
