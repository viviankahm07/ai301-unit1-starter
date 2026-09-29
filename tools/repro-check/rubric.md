# Rubric: is this reproduction package ready to post?

<!--
THIS IS THE PART YOU WRITE. The skill in SKILL.md executes whatever
checks you define here. It ships empty on purpose: the judgment is your
work.

A filled rubric must contain:

1. At least one row in the checks table. Each row needs all four
   columns:
   - Check: a short name (used in the output JSON).
   - Evidence: exactly what to look at, and where in the package. Name
     the part (the claim comment, the repro report's environment
     record, the artifacts read against the issue's description, the
     repo-facts block) or a location from your
     references/evidence-guide.md. "The report" is not a source; "the
     output excerpt read against the error the issue describes" is.
   - Pass condition: a decision rule about the OUTCOME that someone
     else could apply and get your answer. Judge the thing itself (does
     the artifact show the issue's behavior?), never the write-up's
     shape (how many steps it has, how long it is, whether it uses a
     template's headings). Structure-shaped checks are what make
     graders disagree with themselves.
   - Weight: `required` (a fail here holds the package) or `preferred`
     (never changes the verdict).

2. A verdict rule below the table: how the check grades combine into
   accept (ready) or reject (hold), including how `unclear` is
   treated. The verdict space is binary. If you write no rule for
   `unclear`, the skill treats it as fail.

Cover what actually gets bad packages posted. The lecture named the
proof families: the environment is recorded, the steps are complete
and followable, the behavior shown matches the issue (not an adjacent
one), the outcome is stated honestly (an evidenced cannot-reproduce is
a pass, a confident wrong-target is not), and the words respect the
repo's conventions. A rubric that ignores a family will fail eval
packages designed around that family.
-->

## Checks

| Check | Evidence | Pass condition | Weight |
|---|---|---|---|
| Environment | Repro report environment/setup record, read against the issue context and repo-facts block | Pass if the report records the important platform, versions, dependencies, and setup conditions needed to interpret the result, and those conditions match the issue's target environment or any differences are explicitly called out. Fail if the environment is missing important information or silently differs in a way that could affect the result. | required |
| Steps | Repro report steps/procedure, read against the issue body and thread | Pass if the steps start from a clear initial state and give enough concrete actions, commands, inputs, or navigation for another person to follow the same path to the tested behavior. Fail if a reader would need to guess a material setup or trigger step. | required |
| Behavior shown | Repro report artifacts such as logs, screenshots, terminal output, test results, or error excerpts, read directly against the behavior described in the issue | Pass if the evidence demonstrates the same behavior the issue describes, or clearly demonstrates that the behavior does not occur under the tested conditions. Fail if the evidence only shows an adjacent, unrelated, or ambiguous failure. | required |
| Honesty | Claims in the repro report and claim comment, checked against the recorded environment, steps, and artifacts | Pass if the written conclusion matches what the evidence actually shows, including an honest cannot-reproduce, partial result, or environment limitation. Fail if the report overstates certainty, claims reproduction without supporting evidence, or hides a material mismatch. | required |
| Comms | Claim comment and repro report, read against the issue context, repo-facts contribution policy, templates, and any AI-use requirements | Pass if the communication is specific to this issue, accurately summarizes what was tested and observed, follows repo-specific contribution or comment requirements, and includes any required disclosure. Fail if it is generic boilerplate, contradicts the evidence, ignores required repo conventions, or omits a required disclosure. | required |

## Verdict rule

<!-- State how the grades above combine into accept or reject, and how
unclear is treated. Example shape (write your own): "accept if every
required check passes; preferred checks never change the verdict;
unclear counts as fail." -->

- **ACCEPT** only if every required check passes.
- **REJECT** if any required check fails.
- If the evidence for a required check is unclear, missing, or ambiguous, treat that check as **FAIL**.
