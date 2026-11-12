# How AI screening interviews work

Short background for the practice. The general part describes common formats. The rules part is
Aethel's, because Aethel publishes its scoring rules; other tools use their own rules, and many do
not publish them.

## What an AI interviewer asks

Formats differ by tool and by company. Before you start, read the candidate guide or ask the
recruiter which one you will get:

- **A conversation about your past work.** The interviewer asks about a project, an incident or a
  decision, then follows up: why that way, what else you considered, how you knew it worked. This
  practice is this kind.
- **A coding exercise in the browser.** You write or fix code in an editor, sometimes while
  explaining it.
- **A system design discussion.** You describe how you would build something and defend your
  choices when the requirements change.
- **Recorded answers to fixed questions.** Nobody follows up, so each answer has to carry its own
  context and its own result.

Whatever the format, developer questions keep coming back to the same themes: something you built
or owned and what made it hard; a bug, outage or failed release from the first sign to the fix; a
trade-off between speed, reliability, cost and how easy the code is to change; how a system grew;
testing and review when the deadline is close; explaining a technical risk to someone who is not
an engineer; disagreeing with a teammate, a reviewer or a product manager.

Follow-up questions are where depth shows. A good AI interviewer keeps asking about the case you
chose, so pick cases you know well enough to answer "why" three times.

## What it looks for

Most interviews look for the same signals a careful interviewer would:

- **A specific case.** One project, one incident, one decision, with enough context to place it:
  the product, the scale, the size of the team.
- **Your own part.** What you did, said with "I", kept apart from what the team did.
- **Reasoning.** Why you chose it, what else you considered, and what risk you were guarding
  against.
- **A result someone could check.** A number, a before and after, or the person who confirmed it.
- **Honest limits.** What you did not know at the time, or what you would change now.

What rarely helps: a list of languages and frameworks with no decision behind it, the team's
results told as yours, and a textbook definition where the question asked about your experience.

## What "evidence" means: one published example

Aethel publishes how its interview is scored (https://aethel.pro/trust/ai). These rules describe
Aethel's interview only:

- Only the text of the answers is scored. Never the voice, accent, face, grammar or typing speed.
- A quote counts as evidence only if it is the candidate's exact words, found word for word in an
  answer, and at least 8 words long. An area with no valid quote is marked "Not enough evidence",
  which is not a low score.
- Every score shows the quotes it is based on.
- A reply under 8 words is not an answer. With fewer than 3 real answers, or under 60 words of
  answers in all, nothing is scored.
- Without a specific case, named with where it was and how big, an area is at most 60.
- An area scores 90 or more only when one of its quotes is complete and at least 20 words long.

The quick check in this skill only looks for signs of these things in your words. It is not a
score and it does not predict one.
