# ABCs of How We Learn — Claude Skill

A [Claude](https://claude.ai) skill that turns the 26 research-backed learning mechanisms from *The ABCs of How We Learn* (Schwartz, Tsang & Blair, 2016) into a working instructional toolkit. It's built for a **9th–12th grade choir and guitar teacher**, treating the 26 letters as a shared professional vocabulary for lesson design, rehearsal planning, practice routines, and student troubleshooting.

Each letter is a **mechanism** (how learning happens), matched to the **problems it solves** and the **risks** that come with it.

## What this skill does

When you ask for help planning a lesson or rehearsal, designing an activity or assessment, fixing a student learning problem ("they keep forgetting," "they've plateaued," "they're checked out," "they can't hear the difference"), building practice materials, or giving feedback, the skill:

1. **Diagnoses before prescribing** — identifies the actual learning problem (memory? perception? motivation? transfer? misconception?) and maps it to the relevant letters.
2. **Reads the reference file** for each mechanism it applies, rather than working from a one-line summary.
3. **Applies, doesn't recite** — translates the mechanism into the choir/guitar/mixed-level context and names the letter so the vocabulary sticks.
4. **Flags the risks** — every mechanism has failure modes, and the skill surfaces the relevant one.
5. **Combines letters** — real lessons stack mechanisms, and the skill points out the combination explicitly.

It activates even when you never mention the book or learning science — and also when you reference a letter directly ("what does C say," "use G for this").

## Repository structure

```
abcs-skill/
├── abcs.skill              # packaged skill archive (zip)
├── abcs/
│   ├── SKILL.md            # skill entry point: how-to, diagnostic index, letter summaries
│   └── references/         # one file per letter (a–z)
│       ├── a-analogy.md
│       ├── b-belonging.md
│       ├── ...
│       └── z-zzzs-sleep.md
└── README.md
```

Each reference file follows the same structure: **core learning mechanic**, an **example and what it's good for**, **why it works**, **problems it solves**, **how to use it**, and **risks**.

## The 26 letters

| | Letter | Mechanism |
|---|---|---|
| **A** | [Analogy](abcs/references/a-analogy.md) | Find the shared principle across surface-different examples; builds understanding and transfer. |
| **B** | [Belonging](abcs/references/b-belonging.md) | Feeling one belongs increases effort and quiets stereotype threat and alienation. |
| **C** | [Contrasting Cases](abcs/references/c-contrasting-cases.md) | Juxtapose near-misses so learners notice the distinguishing features. (Gold for ear training and technique.) |
| **D** | [Deliberate Practice](abcs/references/d-deliberate-practice.md) | Effortful, goal-directed practice just beyond current ability; the antidote to mindless reps. |
| **E** | [Elaboration](abcs/references/e-elaboration.md) | Connect new info to prior knowledge so it can be found later. |
| **F** | [Feedback](abcs/references/f-feedback.md) | Make the gap between did and should-have-done visible and fixable. |
| **G** | [Generation](abcs/references/g-generation.md) | Retrieval practice — recall from partial cues, spaced over days, strengthens memory. |
| **H** | [Hands On](abcs/references/h-hands-on.md) | Perceptual-motor experience anchors abstract symbols and concepts. |
| **I** | [Imaginative Play](abcs/references/i-imaginative-play.md) | Pretend and role-play exercise symbolic thinking and cognitive control. |
| **J** | [Just-in-Time Telling](abcs/references/j-just-in-time-telling.md) | Let students wrestle with a problem *before* the explanation, so the telling lands. |
| **K** | [Knowledge](abcs/references/k-knowledge.md) | The framing essay — efficiency vs. innovation, routine vs. adaptive expertise. |
| **L** | [Listening and Sharing](abcs/references/l-listening-and-sharing.md) | Structured collaboration; joint attention and group-worthy tasks. |
| **M** | [Making](abcs/references/m-making.md) | Producing an artifact or performance creates its own feedback-and-goals learning cycle. |
| **N** | [Norms](abcs/references/n-norms.md) | Informal social rules shape what and how people learn; set them deliberately. |
| **O** | [Observation](abcs/references/o-observation.md) | Learning by watching and imitating, including affect; model failure and resilience too. |
| **P** | [Participation](abcs/references/p-participation.md) | Scaffold beginners into authentic activity, then fade the support. |
| **Q** | [Question Driven](abcs/references/q-question-driven.md) | A driving question organizes curiosity, purpose, and well-connected memory. |
| **R** | [Reward](abcs/references/r-reward.md) | Shape behavior via reinforcement — with serious risks of killing intrinsic motivation. |
| **S** | [Self-Explanation](abcs/references/s-self-explanation.md) | Prompt learners to explain material to themselves to build a mental model and expose gaps. |
| **T** | [Teaching](abcs/references/t-teaching.md) | Having students teach deepens the teacher-student's own understanding. |
| **U** | [Undoing](abcs/references/u-undoing.md) | Surface the misconception underneath the error and build a competing representation. |
| **V** | [Visualization](abcs/references/v-visualization.md) | Spatial representations reveal structure in complex information. |
| **W** | [Worked Examples](abcs/references/w-worked-examples.md) | Step-by-step demonstrations for initial procedural learning. |
| **X** | [Excitement](abcs/references/x-excitement.md) | Arousal focuses attention and stamps in memory; too much causes choking. |
| **Y** | [Yes I Can](abcs/references/y-yes-i-can.md) | Self-efficacy — praise effort not traits, use peer models, so learners persist. |
| **Z** | [ZZZs (Sleep)](abcs/references/z-zzzs-sleep.md) | Sleep consolidates the day's learning; relevant to teenagers and performance prep. |

## Diagnostic index: problem → letter

| The problem sounds like... | Reach for |
|---|---|
| Can't grasp a new/abstract concept | **A** Analogy, **H** Hands On |
| Learned it here, can't use it there (no transfer) | **A** Analogy, **Q** Question Driven, **K** Knowledge |
| Confuses two similar things; can't hear/see the difference | **C** Contrasting Cases |
| Plateaued; repetition isn't producing improvement | **D** Deliberate Practice |
| Forgets material, names, vocabulary, sequences | **E** Elaboration, **G** Generation, **Z** ZZZs |
| Keeps making the same mistake; doesn't know how they're doing | **F** Feedback |
| Persistent wrong idea or faulty habit that resists correction | **U** Undoing |
| No idea where to start on a procedure | **W** Worked Examples, **O** Observation |
| Bored, checked out, "why do we have to learn this?" | **Q** Question Driven, **M** Making, **X** Excitement, **P** Participation |
| "I'm just not a music person" / gives up after failure | **Y** Yes I Can, **B** Belonging |
| Feels out of place; test anxiety; opts out of participating | **B** Belonging |
| Won't do the work at all; behavior/habit problem | **R** Reward |
| Reads/hears material but nothing sticks; shallow understanding | **S** Self-Explanation, **T** Teaching, **J** Just-in-Time Telling |
| Group work is dysfunctional or unequal | **L** Listening & Sharing, **N** Norms |
| Task is beyond their level but they want in | **P** Participation (scaffold & fade) |
| Overwhelmed by complex information; ideas are vague | **V** Visualization |
| Class culture/expectations are off | **N** Norms |
| Young or impulsive learners; over-scripted classroom | **I** Imaginative Play |
| Lecture lands flat; explanations feel abstract | **J** Just-in-Time Telling |

## Power combinations

Frequently useful stacks for this teaching context:

- **J → C → F** — invent/struggle, then contrast, then feedback (concept lessons)
- **D + G + Z** — practice-routine design
- **C + F** — ear training and technique diagnosis
- **B + N + Y** — classroom culture
- **M + P + T** — performance-based projects

## Installing the skill

Point Claude at this repository, or install the packaged `abcs.skill` archive into your Claude skills directory. Once installed, the skill activates automatically when you ask for teaching, lesson-design, or student-troubleshooting help — no need to invoke it by name.

## Attribution

The learning mechanisms are drawn from:

> Daniel L. Schwartz, Jessica M. Tsang & Kristen P. Blair. *The ABCs of How We Learn: 26 Scientifically Proven Approaches, How They Work, and When to Use Them.* W. W. Norton & Company, 2016.

The reference files in this repository are teacher's notes and paraphrases of the book's framework, adapted for a high school music classroom.
