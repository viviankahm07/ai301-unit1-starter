# Voice guide: how I talk upstream

<!--
THIS IS THE PART YOU WRITE (new this week). Live mode reads this file
before any comment of yours goes out the door; eval mode ignores it
entirely, because your voice is yours and carries no gold labels.

This is not etiquette. "Be polite and concise" is advice for everyone
and therefore rules for no one. Write rules YOU need, in your own
words, each one concrete enough that the skill can hold a draft
against it and say which rule it breaks.

Three sections. Fill all three.
-->

## Who I am in threads

<!-- 2-3 lines. Who is talking when you comment on an issue: your
experience level stated plainly, what you are doing in this repo, what
readers can expect from you. This is the register your rules protect. -->

I am a student contributor learning how to work in established open-source codebases. I try to understand the issue and existing implementation before commenting, and I am transparent when I am still investigating something. Readers can expect me to be specific, concise, and respectful of maintainers' time.

## Rules I write by

<!-- 3-5 rules, drafted from the lecture's slide-12 moment. Each rule
needs a wrong/right pair from your own hand: one line you might
actually have written that breaks the rule, and the line you would
post instead. The pair is what makes a rule executable; a rule without
one is a wish.

Format each rule like this:

### Rule: <short name>

<The rule, one or two sentences.>

- Wrong: "<a line that breaks it>"
- Right: "<the line to post instead>"
-->

### Rule: Be specific about what I know

I separate what I verified from what I am assuming or still investigating. I do not present guesses as confirmed facts.

- Wrong: "The problem is definitely caused by the health check query."
- Right: "It looks like the health check query may be causing this; I am going to trace the execution path to confirm."

### Rule: Say what I actually did

When giving an update, I describe the concrete code, test, or behavior I checked instead of using vague progress language.

- Wrong: "I looked into this and I think I have a fix."
- Right: "I reproduced the error locally and traced it to the raw `SELECT 1` query in `api/routes/health.py`."

### Rule: Ask focused questions

Before asking a maintainer for help, I investigate what I can myself. If I still need clarification, I ask one specific question and explain what I have already checked.

- Wrong: "Can you explain what I should do for this issue?"
- Right: "I found that this endpoint currently uses a raw `SELECT 1`. Should the fix be limited to wrapping it with `sqlalchemy.text()`, or should the other raw SQL calls in this file be updated as well?"

### Rule: Do not overclaim ownership or certainty

I do not promise outcomes, timelines, or fixes before I know I can deliver them. I describe what I plan to try without implying that the solution is already settled.

- Wrong: "I'll have this fixed and a PR up tonight."
- Right: "I'd like to work on this. I'll first reproduce the issue and confirm the expected change before opening a PR."

### Rule: Keep comments useful and concise

Every comment should either provide new information, ask a necessary question, or give a meaningful progress update. I avoid filler and explanations that do not help move the issue forward.

- Wrong: "Thanks for the information! This makes a lot of sense and I am excited to work on it. I will take a look and see what I can figure out."
- Right: "Thanks for the clarification. I'll reproduce the issue and check how the existing health endpoint constructs the query."


## Things I never post

<!-- A short list. Promises you cannot keep, tones you refuse,
shortcuts you know you reach for when tired. The skill quotes this
list back at you when a draft crosses it. -->

- Promises about when I will finish a fix or open a PR unless I am certain I can meet them.
- Claims that something is definitely the cause before I have verified it.
- Vague updates like "still working on it" without saying what I checked or learned.
- Questions I could answer by reading the issue, repository, or existing documentation first.
- Overly apologetic or overly enthusiastic filler that distracts from the technical discussion.
- Language that makes me sound like a maintainer or expert when I am still learning the codebase.