# Field Vision

**Reads the whole field. Plays for the goal. No wasted runs.**

Quick install — Claude Code: `/plugin marketplace add RtheNerd/field-vision` · Codex: `codex plugin marketplace add RtheNerd/field-vision` · Claude app and ChatGPT: see [Install](#install).

Tunnel vision is an AI agent staring at the ball — the task in front of it — while the game is lost: it forgets what the project is for, breaks premises it never looked up, and runs hard in directions nobody needed. Field Vision is a skill that keeps the whole field in view.

## Where it comes from

One user ran a real business with several AI agent sessions for five weeks: server operations, a document tool, exam-question generation, a news site, a company site and a game. In that time, seven agent sessions lost the user's trust and were replaced. None of them failed once, big. Each one piled up small failures.

We pulled every message in which the user got angry at an agent (596, grouping into 84 incidents) and classified each one together with the agent reply right before it. The top causes:

| Cause | Messages |
|---|---|
| Acted without knowing the deliverable's goal and basic premises | 101 |
| Stated things without checking ("done", "it's not there", "the cause is") | 88 |
| Had read the rules but did not apply them at the moment of acting | 82 |
| Excuses, caveats, piles of apologies and promises | 77 |

Two things were common to almost every case. First, what to do was already written down; the agents had read it. Second, the mistakes happened at the moment of acting, when trained habits took over. Those habits are to look busy, guess, hand options back, add a caveat and make excuses. The angrier the user got, the stronger the habits became.

So this skill does not add more rules. It sets **two governing principles** and **nine gates** at the moments an agent acts.

The principles:

1. Put first what the deliverable is for and which basic premises must never be compromised.
2. Papering over a problem lets it rot inside. Pull it out by the root.

The gates: taking on work, stating a fact, touching anything, asking the user, reporting "done", being corrected, failing twice, handing over, and listening.

It works with Claude, Claude Code, ChatGPT and Codex. The skill text is in English; agents answer in the user's language.

## Install

### Claude (claude.ai app)

1. Download `dist/field-vision.zip`.
2. Go to **Customize > Skills**, then **+ → Create skill → Upload a skill**, and upload the zip.
3. Claude Code signed in with the same Claude account picks up the skill automatically.

### Claude Code (plugin)

```
/plugin marketplace add RtheNerd/field-vision
/plugin install field-vision@rxai
```

### ChatGPT (personal plugin on your account)

1. Download `dist/field-vision-plugin.zip`.
2. In a ChatGPT chat, type **@** and choose **Plugin Creator**.
3. Upload the zip and say: "Save the field-vision folder in this zip as my personal plugin. Don't publish it."

### Codex CLI (marketplace)

```
codex plugin marketplace add RtheNerd/field-vision
codex plugin add field-vision@rxai
```

## Layout

```
.agents/plugins/marketplace.json      Codex / ChatGPT marketplace
.claude-plugin/marketplace.json       Claude Code marketplace
plugins/field-vision/
  plugin.json                         plugin manifest (with OpenAI display info)
  .codex-plugin/plugin.json           same manifest, Codex compatibility copy
  .claude-plugin/plugin.json          Claude Code manifest
  skills/field-vision/
    SKILL.md                          the skill
    references/patterns.md            failure types and 35 real scenes
    agents/openai.yaml                ChatGPT app display info
dist/field-vision.zip               for claude.ai upload
dist/field-vision-plugin.zip        for ChatGPT Plugin Creator upload
```

## Updating

The skill lives in one place: `plugins/field-vision/skills/field-vision/`. After editing:

- Bump `version` in the three manifests.
- Rebuild both zips:
  ```
  cd plugins/field-vision/skills && zip -qr ../../../dist/field-vision.zip field-vision -x 'field-vision/agents/*'
  cd ../.. && zip -qr ../dist/field-vision-plugin.zip field-vision -x 'field-vision/.claude-plugin/*'
  ```
- Re-upload the zips to claude.ai and ChatGPT.

Made by RXAI Creative. Released under the MIT License (see `LICENSE`).
