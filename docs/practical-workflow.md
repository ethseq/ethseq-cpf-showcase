# What this could look like in a real workflow

## Planned external case: ski / 3D perception

This is an illustrative planned external workflow. It is **not** a completed customer deployment, a completed external validation, or a reported performance result.

Imagine a ski-perception system that performs well on some samples but fails on others. A team may suspect that occlusion is involved, but that suspicion alone does not establish that occlusion caused the failures.

| Stage | Example activity | What can be claimed at this stage |
| --- | --- | --- |
| Baseline | Measure current recognition or 3D-pose success on a defined evaluation set. | The current baseline measurement. |
| Bounded test space | Define which occlusion patterns and interventions are in scope. | A testable question, not a cause. |
| Candidate discovery | Let CPF identify and score concrete candidates within the allowed inputs. | A candidate to test, not attribution. |
| Candidate freeze | Freeze the selected candidate before the final experiment. | A precommitted test target. |
| Controlled intervention | Test whether that occlusion factor changes behavior; use reverse and unrelated control conditions when applicable. | Evidence for SUPPORTED, FAIL, or ABSTAIN. |
| Decision | If attribution is supported, decide whether to add targeted data, modify a model, or change the system. | A more grounded engineering decision. |
| Retraining and evaluation | Keep the training recipe controlled and evaluate on an untouched held-out test set. | A performance change only if a real experiment demonstrates it. |

## Why this matters

The useful output is not merely “the model made an error.” The team gets a testable answer to a narrower question:

> Was this factor actually responsible for the observed failure?

If attribution is supported, the team has evidence for why a targeted data, model, or system intervention may be worth testing. If attribution fails or CPF abstains, the team has evidence not to overcommit to that explanation.

CPF does not make the downstream decision automatically, and it does not imply that a retraining step will improve a metric. Improvement must be demonstrated separately on an untouched held-out test set.

## What an external validation can test

An external partner can bring its own task, model, data, and environment. Together, the work can test whether the same evidence-first attribution procedure produces a supported result, a failed result, or an abstention under that partner’s real conditions.

See [Collaboration](collaboration.md) for the proposed collaboration format.
