# AI interview practice

A skill for your coding agent that runs a practice AI screening interview for developers.
It asks real interview questions for your role and level, one at a time, checks each answer with
simple published word rules that quote your own words back, and asks a follow-up about your case.
English and Spanish.

Use it before an AI screening interview: the kind where an AI interviewer asks about your past
work and a written result is made from your answers, as platforms such as Mercor and micro1 run
them. This skill is not affiliated with any of them and does not have their questions. It
practises the general format: one real case, what you did yourself, why, and how it turned out.

Roles: backend, frontend, full-stack, data and ML, DevOps and SRE, mobile. Levels: junior,
mid-level, senior. The full question bank is readable here:
[English](skills/ai-interview-practice/references/questions-en.md) and
[Spanish](skills/ai-interview-practice/references/questions-es.md).

## Install

### Claude Code

As a plugin, from this repository:

```
/plugin marketplace add DPWonder/ai-interview-practice
/plugin install ai-interview-practice@aethel-practice
```

Or from your shell: `claude plugin marketplace add DPWonder/ai-interview-practice`, then
`claude plugin install ai-interview-practice@aethel-practice`.

Or as a personal skill, without the plugin system:

```
git clone https://github.com/DPWonder/ai-interview-practice.git
mkdir -p ~/.claude/skills
cp -R ai-interview-practice/skills/ai-interview-practice ~/.claude/skills/
```

Then ask for it in plain words, for example "run a mock AI screening interview with me, backend,
senior". As a plugin you can also start it with `/ai-interview-practice:ai-interview-practice`; as
a personal skill, with `/ai-interview-practice`.

### Other agents

With the open `skills` installer, which copies the skill into the folder your agent reads:

```
npx skills add DPWonder/ai-interview-practice
```

Or copy the folder `skills/ai-interview-practice` by hand:

- Codex: `~/.agents/skills/` (all projects) or `.agents/skills/` in a repository.
- Cursor: `~/.cursor/skills/` or `~/.agents/skills/` (all projects), or `.cursor/skills/` or
  `.agents/skills/` in a project.
- Any agent that reads SKILL.md files: put the folder wherever it looks for skills.

## Example session

This is an example, shortened. The answers are made up.

```
You:    Mock AI interview please: backend, mid-level, English.
Agent:  Question 1 of 4
        Walk me through an outage or a serious bug you helped resolve, from the first
        alert to the fix. What did you check first, and why?
You:    Last March our checkout API started timing out at lunch, with about 2,000
        requests a minute. I traced the slow calls to one query that scanned the whole
        orders table. I added an index instead of a cache, because a cache would have
        shown stale prices and the index fixed the cause. After that, p95 latency went
        from 900 ms to 120 ms and the timeouts stopped.
Agent:  Quick check (not a score)
        - Counts as an answer: 67 words.
        - A real example. Spotted: "Last March our checkout API started timing out..."
        - What you did yourself. Spotted: "I traced the slow calls to one query..."
        - Why you chose it. Spotted: "I added an index instead of a cache, because..."
        - How it turned out. Spotted: "After that, p95 latency went from 900 ms to 120 ms..."
        - Your longest sentence has 22 words, long enough to back a top score.
        - Try this: be ready to go one layer deeper: one option you rejected and why.
        Follow-up: You chose an index over a cache. How did you check the index would
        not slow down writes to the orders table?
```

## What it does

- Asks 4 questions for your role and level, one at a time, and waits for each answer. Type or
  dictate.
- After each answer, runs a quick check: does it count as an answer, and are there signs of a
  real example, what you did yourself, why you chose it, and how it turned out. It quotes your
  exact words for each sign it finds and says plainly what is missing, with one "try this" line.
- Asks one follow-up question about the case you told, as an AI interviewer would.
- Ends with what showed up in every answer, what never did, and two things to practise.

## What it does not do

- It does not score you. The check looks for signs in your words, not their meaning, so it can be
  wrong both ways. No number it shows is a score.
- It does not pretend to be a person or any company's interviewer. It is your own agent, running
  a practice.
- It does not invent facts about you or rewrite your answers into things you did not say.
- It sends nothing to Aethel. Your answers stay in your agent's chat, like anything else you
  type there.
- It does not cover coding exercises, algorithm puzzles or system design whiteboards.

## Who made it

Made by the Aethel team. Aethel is operated by HackerX, Inc. We built this, so weigh it with that
in mind.

The questions and the check rules come from Aethel's free practice. At the end of a session the
skill mentions, once, that a real AI screening interview is usually spoken, and that you can try
Aethel's free AI video interview, about 15 minutes, where the interviewer is an AI and says so and
you see your transcript and scores first. Free practice:
https://aethel.pro/practice?ref=gh-skill

## Licence

The skill is MIT licensed (see [LICENSE](LICENSE)). The question text in
`skills/ai-interview-practice/references/questions-en.md` and `questions-es.md` is licensed
[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) (see [LICENSE-questions.md](LICENSE-questions.md)): reuse it with
credit to Aethel.
