# Evidence guide: where proof lives in a reproduction package

<!--
THIS IS THE PART YOU WRITE (new this week: Unit 1 handed you this file
finished; the scaffolding fades). The skill uses this guide as its map:
for every kind of proof a rubric check names, this file says WHERE to
find it in a package and WHAT GOOD LOOKS LIKE when you do.

Under each family heading below, write:

- Where it lives: the exact places to look. In an eval bundle (which
  section of the package: the issue context, the repo-facts block, the
  claim comment, the repro report and its parts). In live mode (where
  on GitHub or in the draft: the issue thread, the repo's docs, the
  student's draft comment).
- What good looks like: one or two sentences someone else could apply.
  Prefer observable conditions ("the versions named match what the
  issue targets, or the difference is called out") over adjectives
  ("environment is thorough").

A rubric check whose evidence this guide cannot locate is a check
nobody else can execute; the rubric swap showed you what that feels
like. Write the map you wish your grader had.
-->

## Environment

<!-- Where the environment record lives, and what a sufficient one
looks like against the issue's stated target. -->

Where it lives

Eval mode: Look in the reproduction report for the environment/setup section, and compare it against the issue context and repo-facts block.

Live mode: Look at the issue thread for any required versions, operating systems, dependencies, commands, or setup assumptions, then compare those against the environment recorded in the student's draft or reproduction notes.

What good looks like

The environment record names the important versions, dependencies, platform, and setup conditions needed to reproduce the issue. These should match the environment targeted by the issue, or any differences should be explicitly called out so a reader can judge whether they might affect the result.

## Steps

<!-- Where the reproduction steps live, and what makes them followable
by a stranger, starting state to trigger. -->

Where it lives

Eval mode: Look in the reproduction report's steps or procedure section and compare the sequence against the issue description and any reproduction instructions included in the issue context.

Live mode: Look at the original issue body and thread for reproduction instructions, then compare them against the steps written in the student's draft report or comment.

What good looks like

The steps begin from a clear starting state and proceed in an order that another person could follow without guessing. They include the specific actions, commands, inputs, or navigation needed to reach the behavior being tested rather than skipping important setup or trigger steps.

## Behavior shown

<!-- Where the artifacts live (output excerpts, logs, screenshots),
and what it means for an artifact to show the issue's behavior rather
than an adjacent one. -->

Where it lives

Eval mode: Look at the reproduction report's evidence artifacts, including output excerpts, terminal logs, error messages, screenshots, test results, or other captured behavior. Compare these artifacts against the behavior described in the issue context.

Live mode: Look at any logs, screenshots, terminal output, test output, or other evidence included in the student's draft and compare it directly with the problem reported in the GitHub issue.

What good looks like

The evidence visibly demonstrates the behavior described by the issue, not merely a nearby error or a different failure. A reader should be able to connect the artifact to the issue's expected-versus-actual behavior without relying only on the student's interpretation.

## Honesty

<!-- Where claims and their backing meet: how to tell a report that
says exactly what happened (including an honest cannot-reproduce) from
one that claims more than its evidence shows. -->

Where it lives

Eval mode: Compare the claims made throughout the reproduction report with the environment record, steps, and attached evidence. Pay particular attention to the final reproduction result or conclusion.

Live mode: Compare the student's written claims in the draft comment or report against the commands they ran and the evidence they captured.

What good looks like

The report says only what the evidence supports. If the issue reproduces, it clearly states what was observed; if it does not reproduce, the report says so rather than forcing a positive result; and if the result is uncertain, partial, or affected by an environment difference, that limitation is explicitly stated.

## Comms

<!-- Where the words meet the repo: the claim comment against the
issue, the comments against the repo's stated templates and
contribution policy (including AI-use disclosure requirements), and
what specific-and-honest looks like next to boilerplate. -->

Where it lives

Eval mode: Look at the claim comment, the issue context, the reproduction report, and the repo-facts contribution-policy section. Check any repository-specific contribution templates, communication requirements, and AI-use disclosure rules included in the package.

Live mode: Compare the student's proposed GitHub comment against the issue thread, CONTRIBUTING.md, .github/ templates, PR or issue templates, dedicated AI policy files, and any contributor documentation linked by the repository.

What good looks like

The comment is specific to the actual issue and accurately summarizes what the student tested and observed rather than using generic boilerplate. It follows the repository's stated communication and contribution rules, includes required disclosures such as AI use when applicable, and does not claim that the issue is reproduced or understood more strongly than the evidence supports.