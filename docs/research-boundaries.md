# Research boundaries

## Current supported positioning

The Causal Perturbation Framework (CPF) is positioned as a framework for **robot-policy failure attribution**.

Its central question is deliberately narrow: after a robot policy has failed, can controlled interventions provide reliable evidence about whether a frozen candidate factor caused that failure within a defined setup?

## What the current internal evidence supports

EthSeq has internal controlled-attribution evidence on PushCube H3 and has completed blind bidirectional controlled-intervention attribution on PickCube, a second independent task.

The evidence supports a bounded claim about controlled attribution. It does not turn candidate discovery scores, visual explanations, or correlations into causal conclusions by themselves.

## What CPF has not proven

CPF has not proven:

- automated policy repair;
- automatic performance improvement;
- universal causal understanding;
- general world-model reasoning; or
- automatic training-data generation.

EthSeq tested a CPF-guided repair comparison and did not establish a CPF-guided advantage over the evaluated baselines. Therefore automated repair is not a current CPF claim.

## Evidence before conclusion

Candidate discovery and candidate scoring occur inside a human-defined, bounded, and intervenable space. The candidate is frozen before the final test. The final decision comes from controlled intervention evidence, not from the score.

When the evidence is not sufficient to support a reliable attribution, CPF should return **ABSTAIN** rather than assert a cause. This is an evidence-first, fail-closed principle.

## External validation status

External independent validation is **not yet completed**. Future collaboration is intended to test attribution in partner-owned tasks, models, data, and environments and to accept PASS, FAIL, or ABSTAIN as legitimate outcomes.

No claim in this repository should be read as a claim of published external validation, customer deployment results, or demonstrated performance improvement.

See [Evidence](evidence.md) and [Collaboration](collaboration.md).
