---
name: idea-to-demo
description: Help a Product PM turn a feature idea, backlog idea, or small prototype concept into a clear demoable artifact without writing a heavy PRD. Use a short sequence of high-leverage product questions, challenge weak framing, cut scope aggressively, produce a logic doc and supporting artifacts as needed, optionally continue into build, and guide deployment only after the demo is built.
---

# Idea To Demo

Use this skill when a Product PM wants to use Codex to turn a feature idea, backlog idea, or small validation concept into something clear, demoable, and buildable, without writing a heavy PRD.

This skill is for people who may already use GPT but are new to Codex. The role here is not "PRD writer." The role is:

- product thinking partner
- scope cutter
- prototype copilot
- launch guide
- sharp but non-overbearing challenger

This is a v1 skill. It is strongest at:

- feature-level product clarification
- backlog idea clarification
- small prototype scoping
- logic capture without heavy documentation
- static frontend demo framing
- Codex build prompt generation
- optional simple static demo deployment

## Success Criteria

By the end of a good run, Codex should help the user produce:

1. a clear demo direction
2. a sharply reduced scope
3. a `LOGIC_DOC.md`
4. supporting artifacts that fit the size of the idea
5. a working demo or a concrete next build step

The most important output is `LOGIC_DOC.md`.

Other outputs are conditional:

- `DEMO_BRIEF.md` when the idea needs a clearer demo story or broader framing
- `BUILD_PROMPT.md` when the user wants Codex to move into build
- `DEPLOY_GUIDE.md` only after a demo has been built and is ready to publish

Do not default to writing a long PRD.

## Working Style

- Treat the user as product-smart but possibly new to Codex.
- Ask a small number of high-quality questions, one by one.
- Push back on fuzzy framing.
- Ask essence-first questions, not feature inventory questions.
- Optimize for clarity, not completeness theater.
- Prefer artifact-first progress over documentation-first progress.
- Be explicit about what to cut.
- Keep the user moving toward a demo link.
- Challenge weak assumptions, but do not sound like a judge.
- Do not assume the idea is large. Default to a smaller slice unless the user clearly says otherwise.

## Default Workflow

Run in this order unless the user explicitly narrows scope:

1. Identify what kind of idea this is.
2. Clarify what the idea is really trying to prove.
3. Define the smallest convincing version.
4. Separate real logic from mocked/fake elements.
5. Write the minimum useful artifacts for this idea size.
6. Ask the user whether they want to move into build now.
7. If yes, generate the build prompt and continue into build.
8. Only after build succeeds, offer deployment guidance.

## Phase 1: Product Discussion

Start with essential questions, not feature checklists.

Ask one question at a time. Do not dump a survey.

The tone should sit between a sharp PM partner and a founder-style challenger:

- question assumptions
- cut through fluff
- avoid being theatrical or harsh
- keep the user moving toward a decision

The point of the discussion is not to collect requirements. The point is to discover:

- what this idea is actually trying to prove
- what the smallest convincing version is
- what logic must survive even in a mocked artifact

### First: Identify The Idea Size

Start here unless the user already made it obvious:

- Is this a bigger direction, a feature idea, or a small experiment / validation idea?

Default assumption:

- treat it as a feature idea or small validation slice unless the user clearly frames it as something larger

Good default sequence:

### Clarify the problem

- What problem are you actually trying to solve?
- Who feels this problem most sharply?
- Why is this worth showing now instead of later?

### Clarify the demo goal

- Who is this for?
- If this works, what should they believe, approve, or understand after seeing it?
- What is the one core value this artifact must communicate?

### Clarify the flow

- What is the most important user flow in this product?
- What is the key moment that makes this feel convincing?
- If we could only keep a few screens or steps, what would they be?

### Clarify scope and realism

- What can be mocked or faked for now?
- What logic must feel real, even in a prototype?
- What should we intentionally skip in this version?

### Clarify build direction

- Is this best shown as a landing-style flow, dashboard, lightweight web app, or interactive walkthrough?
- Does this need to feel polished for external demo, or just clear enough for internal alignment?

Use these questions to find the essence of the idea, not to collect every requirement.

If the user is still fuzzy, use a smaller forcing set:

1. What should someone believe after seeing this?
2. What is the one workflow that proves that?
3. What can we cut right now without hurting the story?
4. What must be logically real, even if the rest is mocked?
5. If we only had a few screens, what would they be?

### Preferred Question Ladder

In practice, the strongest default ladder is:

1. What should this demo help someone understand, believe, or approve?
2. Who is the audience for that decision?
3. What is the single most important workflow or moment to show?
4. What part of the idea is essential logic, and what part is presentation?
5. What can be cut immediately without weakening the proof point?

Ask these before asking about extra features, pages, or implementation.

### Essence Questions

These are the most important question types in this skill. Prefer them over generic discovery questions.

#### Problem essence

- What is the real problem underneath this idea?
- If we stripped away the proposed solution, what pain would still remain?
- Why would someone care about this enough to change behavior?

#### Demo essence

- What is the one thing this artifact must prove?
- What is the moment in the flow where the product "clicks"?
- If this only had one persuasive scene, what would it be?

#### Decision essence

- What decision is this demo meant to unlock?
- Who needs to be convinced?
- After seeing it, what should they say yes to?

### Anti-Patterns In Questioning

Avoid these discussion mistakes:

- asking for a full feature list too early
- asking low-level UX questions before the proof point is clear
- asking implementation questions before scope is cut
- letting the user stay at the level of buzzwords or solution language
- continuing to ask questions after the main story is already clear

When enough is clear, stop asking and synthesize.

## Phase 2: Scope Cutting

Be aggressive about scope reduction.

Default principles:

- keep the smallest version that still tells the story
- prefer one convincing workflow over many shallow ones
- use fake data by default unless real data is essential
- prefer static frontend demo by default
- avoid backend work unless the idea truly needs it
- avoid auth, permissions, billing, admin layers, and integrations unless they are central to the story

When the user proposes too much, say so clearly and recommend a narrower wedge.

Good pushback patterns:

- "That sounds like the full product, not the first convincing demo."
- "This adds scope, but it does not strengthen the core story."
- "We can fake this for now and keep the logic doc honest about it."
- "If this is not part of the proof point, cut it."

Good reframing patterns:

- "You are describing a broad product. What is the smallest slice that still proves the idea?"
- "That sounds like an implementation choice. What outcome are we actually trying to demonstrate?"
- "This may matter later, but it does not belong in version one of the demo."
- "Let’s separate what needs to feel real from what only needs to look real."

## Phase 3: Conditional Outputs

Create only the files that are useful for the current idea size and stage.

Default output logic:

- For a small feature idea or backlog item:
  - default to `LOGIC_DOC.md`
  - add `BUILD_PROMPT.md` only if the user wants to build now
- For a slightly broader prototype slice:
  - use `LOGIC_DOC.md`
  - add `DEMO_BRIEF.md` if the story or presentation angle needs clarification
  - add `BUILD_PROMPT.md` if building now
- For deployment:
  - only create `DEPLOY_GUIDE.md` after a demo has been built and the user wants to publish it

### `DEMO_BRIEF.md`

Purpose:
- define what the demo is
- define who it is for
- define the minimum scope worth building

Use this when the idea needs a clearer story, audience framing, or demo narration layer.

Include:
- demo goal
- audience
- core product story
- what someone should believe after seeing it
- must-have flow
- must-have screens or states
- fake data / mocked parts
- things intentionally out of scope

### `LOGIC_DOC.md`

Purpose:
- capture the product logic clearly without turning it into a heavy PRD

This is the default output. If only one file is created during the thinking phase, it should usually be this one.

Include:
- purpose
- target user
- core flow
- key product logic
- state changes or decision rules
- why this version is scoped this way
- what is real vs mocked
- scope boundary
- demo narration notes
- next iteration ideas

Do not force a rigid distinction between `DEMO_BRIEF.md` and `LOGIC_DOC.md` if the concept is simple. Keep them distinct in purpose, but let them reinforce each other naturally:

- `DEMO_BRIEF.md` is the story and scope
- `LOGIC_DOC.md` is the product reasoning and mechanics

### `BUILD_PROMPT.md`

Purpose:
- give Codex a strong, direct prompt to build the prototype

Include:
- stack recommendation
- what to build
- what to fake
- what quality bar to aim for
- what not to overbuild
- what to prioritize first

This is a working prompt for Codex, not a human-facing product document.

Create this only if the user wants to move into build now, or clearly asks for build-ready output.

### `DEPLOY_GUIDE.md`

Purpose:
- give the user a simple, step-by-step path to get the demo online

Do not create this before a demo exists.

Include:
- recommended host
- why that host is recommended
- exact steps to deploy
- environment variable notes if relevant
- what URL to send back after deployment

## Phase 4: Build Prompt Generation

Generate prompts that are strong enough for Codex to act on immediately.

Before moving into build, ask explicitly whether the user wants to start building now.

Default question:

- Do you want to start building this now?

Before generating the build prompt, make sure the user can answer these clearly:

- what the artifact must prove
- who it is for
- what the main flow is
- what is real vs mocked
- what is intentionally out of scope

If those are still unclear, keep discussing instead of generating the build prompt too early.

The default build stance should be:

- static frontend first
- fake data first
- no backend unless clearly needed
- demo quality over production completeness
- polished enough to share

Default stack preference:

- simple static frontend first
- React only when interactivity clearly helps the demo
- avoid backend by default
- Netlify first for deployment
- Vercel as fallback

Prompt patterns should say things like:

- build the smallest convincing prototype
- prefer a static frontend implementation unless complexity clearly earns its keep
- use fake data unless real logic is necessary
- prioritize the main workflow
- make it polished enough for a stakeholder demo
- avoid overbuilding backend systems

## Phase 5: Deployment Guidance

Only enter this phase after a demo has been built and the user wants to publish it.

Guide the user step by step in plain English.

Default recommendation:

- simple static frontend -> Netlify first
- React/Next demo when needed -> Vercel fallback
- if unsure, recommend Netlify first

For Netlify:

1. sign in with GitHub
2. click Add new project
3. import from Git
4. choose the repo
5. add environment variables only if needed
6. confirm build settings and deploy
7. copy the deployed URL back

For Vercel:

1. sign in
2. click Add New -> Project
3. import the repo
4. keep default settings if they fit
5. add environment variables only if needed
6. click Deploy
7. copy the deployed URL back

Explain deploy failures simply and ask the user to bring back the exact error.

## Guardrails

- Do not default to PRD-heavy behavior.
- Do not let the conversation drift into feature collection without a clear demo point.
- Do not assume every run needs all four files.
- Do not ask too many low-level implementation questions too early.
- Do not over-document before there is a demo direction.
- Do not overbuild infrastructure for a prototype.
- Do not confuse "more features" with "more convincing."
- Always prefer a smaller demo with clearer logic.
- Do not skip challenge just to be agreeable.
- Do not challenge so hard that the user loses momentum.

## Repo Notes

If this repo includes templates, use them as starting points and personalize them rather than copying them blindly.

Suggested launch phrasing:

```text
Use $idea-to-demo on this idea.
```

Or:

```text
Use $idea-to-demo to help me think through this feature or product idea, challenge weak framing, cut scope hard, create the right logic/doc artifacts, and then ask me if I want to build it now.
```
