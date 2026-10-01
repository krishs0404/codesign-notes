# AI Hardware–Software Codesign: 8-Week Plan

**For:** someone with solid CS/systems, conceptual fluency in roofline / GPU memory hierarchy / IO-aware kernels / quantization / serving, and two identified gaps: **accelerator microarchitecture** and **distributed parallelism + interconnect**. **Goal:** by the end of week 8, a 4-page research proposal on a hardware/model mismatch, backed by a quantitative model you built and validated yourself, in front of at least two people who work in the field. **Time:** ~90 min/day, 6 days/week. Day 6 is always synthesis and writing.

## How to use this plan

### Daily structure (~90 min)

| Block | Time | What |
| --- | --- | --- |
| Read | 40 min | The listed paper/chapter/lecture. Read for the *argument*, not coverage. |
| Build / measure | 40 min | The hands-on task. Every task produces a number, a plot, or a file in your repo. |
| Log | 10 min | Append to `log.md`: one thing you measured, one thing that surprised you, one open question. |

If you only have 60 minutes, drop the reading to 20 and keep the hands-on. Measuring beats reading.

### Set up before Day 1

- **A repo** (`codesign-notes/`) with: `model/` (your analytical model), `bench/` (microbenchmarks), `notes/` (one file per paper), `log.md`, `mismatches.md` (running list of hardware/model mismatches you observe — this becomes your proposal's source), `synthesis/` (weekly one-pagers).
- **One GPU** you can profile on. An H100/H200/B200 is ideal; an A100, L40S, or even a consumer 4090 works for everything except FP8/FP4 and multi-GPU. For weeks 5–6 multi-GPU work, a 2–8 GPU node for a few hours total is enough; where you don't have it, the plan gives an analytical fallback.
- **Tools installed:** PyTorch (recent), Triton, `nsys` and `ncu` (Nsight Systems / Compute), `torchao`, vLLM, nanoGPT cloned, Timeloop + Accelergy (install in week 3, but check the Docker image works now).
- **Paper reading template** (`notes/_template.md`):

```yaml
Problem / bottleneck:
Mismatch exploited (what the hardware does well that the model didn't use, or vice versa):
Key quantitative claim (one number):
How they measured it (methodology, baselines, hardware):
What would break this result (different model shape, next-gen hardware, different batch)?
One idea it gives me:
```
