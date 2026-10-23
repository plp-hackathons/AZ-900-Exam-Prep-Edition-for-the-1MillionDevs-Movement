# Prompt Engineering Log

How I used Claude to build the AZ-900 Quiz Coach (unofficial). The pattern: **give context, set constraints, ask for a specific output format, then review and iterate.** I stayed the reviewer. Claude drafted, I verified.

## 1. Scoping prompt (decide what to build)
**Prompt:** I pasted the full hackathon brief, judging criteria and deadline, and asked which challenge I could realistically finish and score well on in one day.
**Why it worked:** the judging weights were in the context, so the answer was optimised for Learning Value (25%) instead of feature count. Output: Smart Quiz Builder plus a built-in readiness view, with a timed plan.

## 2. Build prompt (generate the prototype)
**Constraints I gave:**
- Single-page app, mobile friendly, no backend
- Three official AZ-900 domains as topics
- Instant feedback with an explanation for every answer
- Results by topic, a "revise these first" list, and a retry-missed mode
- "Unofficial, not affiliated with Microsoft" on every screen, no Microsoft logos
- Original questions only, never real exam content

**Why it worked:** constraints and the output format were explicit, so the first draft was usable.

## 3. Journey-to-feature prompt (my own learning data)
I gave Claude my real study results: scores by round, and the pairs of services I kept confusing (Conditional Access vs RBAC, VPN Gateway vs ExpressRoute, NSG vs Azure Firewall, and more). I asked it to turn them into paired-service drills with a trigger-word hint and a "how they differ" explanation.
**Result:** the **Twin Drills** mode. The hints ("door vs keys") are my own study method.

## 4. Reusable question-generator prompt (how the bank can grow)
```
You are an AZ-900 study content writer. Write 5 ORIGINAL multiple-choice
questions for the domain: [DOMAIN], based only on the public AZ-900 skills
outline on Microsoft Learn.

Rules:
- Never reproduce or imitate real exam questions or dumps.
- Exactly 4 options, one clearly correct, three plausible distractors that
  are real Azure services or concepts.
- Each question tests ONE concept. Include a scenario with trigger words.
- Explanation: 1-2 sentences saying why the answer is right and what the
  closest distractor is actually for.
- Return ONLY JSON: [domainIndex, "question", ["opt1","opt2","opt3","opt4"],
  correctIndex, "explanation", "optional trigger-word hint"].
```
**Then I review:** every question and explanation is checked against Microsoft Learn before it goes into the app.

## 5. Iteration and quality control
- In review I caught a throwaway distractor in the first draft and replaced it with a plausible Azure service. Weak distractors teach nothing.
- I played through every question and approved the content and hints myself.
- I kept the explanations short and the wording fresh, so learners test logic and not memory.

## What I'd do next
Add a verification prompt that fact-checks each new question against the Microsoft Learn page for its topic, then a spaced-repetition scheduler for missed questions.
