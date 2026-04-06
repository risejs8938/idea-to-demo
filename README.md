# idea-to-demo

A Codex skill for Product PMs who want to skip heavy PRDs and move faster from feature idea or backlog concept to a clear, demoable artifact.

This skill helps with:

- discussing a feature idea, backlog idea, or small prototype concept clearly
- asking a short set of essential framing questions
- cutting scope hard
- producing the right artifacts for the size of the idea
- generating a strong Codex build prompt when the user wants to build now
- guiding deployment to Netlify or Vercel only after a demo exists

## Core Outputs

- `DEMO_BRIEF.md`
- `LOGIC_DOC.md`
- `BUILD_PROMPT.md`
- `DEPLOY_GUIDE.md`

Primary outputs:

- `LOGIC_DOC.md`

Supporting outputs:

- `DEMO_BRIEF.md`
- `BUILD_PROMPT.md`
- `DEPLOY_GUIDE.md`

The skill should decide which files are needed based on the size and stage of the idea. Small ideas should not be forced through the full set.

## Install

```text
Install this skill:
https://github.com/risejs8938/idea-to-demo
```

## Launch

Short version:

```text
Use $idea-to-demo on this idea.
```

Full version:

```text
Use $idea-to-demo to help me think through this feature or product idea, challenge weak framing, cut scope hard, create the right logic/doc artifacts, and then ask me if I want to build it now.
```
