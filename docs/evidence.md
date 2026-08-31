# Evidence

## Scope of this page

This page reports the public experimental facts EthSeq is prepared to state about CPF. It contains no proprietary implementation or non-public research artifacts.

The evidence below is internal. External independent validation is not yet completed.

## PushCube H3: bidirectional controlled attribution

| Condition | Successful episodes | Role in the comparison |
| --- | ---: | --- |
| Noop | 20 / 20 | Successful reference condition |
| Forward intervention | 0 / 20 | Change only the frozen candidate in the successful condition |
| Placebo | 20 / 20 | Apply an unrelated control change |
| Full Failure | 0 / 20 | Failure reference condition |
| Reverse intervention | 20 / 20 | Restore only the frozen candidate in the failure condition |

Within the bounded PushCube H3 setup, this pattern supported attribution to the tested frozen candidate: changing it altered the observed policy behavior in the forward comparison, restoring it altered behavior in the reverse comparison, and the reported placebo control did not show the same effect.

### Candidate-discovery restriction

During PushCube H3 candidate discovery, CPF was allowed to use **only policy-crop RGB render difference**.

Candidate discovery was not allowed to use:

- rollout success;
- segmentation;
- object or goal ground-truth coordinates; or
- a CPF oracle.

After discovery, the selected candidate had to be frozen. It could not be reselected because a later intervention result failed.

These restrictions apply to candidate discovery. The final attribution decision was made from the controlled intervention evidence.

## PickCube: a second independent task

CPF completed **blind bidirectional controlled-intervention attribution** on PickCube, a second independent task. This is internal evidence that the controlled-attribution workflow can be tested across more than one task.

For PickCube candidate discovery, CPF was allowed to use only:

- RGB;
- proprioception; and
- policy output.

It was not allowed to use:

- segmentation;
- proxy-panel coordinates;
- oracle masks;
- actor pose; or
- repair outcome.

As with PushCube H3, candidate selection was frozen before the final experiment. The PickCube result is not a claim of external independent validation, automated repair, or performance improvement.

## Repair comparison and the resulting boundary

EthSeq also ran a CPF-guided repair comparison. The comparison did **not** demonstrate that CPF-guided repair outperformed the evaluated baselines.

That negative result matters. It is why CPF is not presented as an automated policy-repair system or as a demonstrated route to automatic performance improvement. The supported claim is narrower: controlled robot-policy failure attribution in the reported internal experiments.

## How to read this evidence

The PushCube and PickCube results are evidence for a bounded, controlled attribution workflow. They are not evidence for:

- universal causal understanding;
- general world-model reasoning;
- automatic training-data generation;
- automated policy repair; or
- automatic performance improvement.

For the complete claim boundary, see [Research boundaries](research-boundaries.md).
