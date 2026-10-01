# AI Hardware–Software Codesign

An eight-week learning and research project focused on accelerator microarchitecture and distributed parallelism + interconnect.

**Goal:** Produce a four-page research proposal on a hardware/model mismatch, backed by a quantitative model built and validated here, and share it with at least two people working in the field.

**Schedule:** Approximately 90 minutes per day, six days per week. Day 6 is for synthesis and writing.

Start with [the plan](PLAN.md), copy [the paper-reading template](notes/_template.md) for each paper, and record each session in [log.md](log.md).

## Repository layout

| Path | Purpose |
| --- | --- |
| `model/` | Analytical models and validation |
| `bench/` | Microbenchmarks and measurement scripts |
| `notes/` | One reading note per paper |
| `log.md` | Daily measurements, surprises, and questions |
| `mismatches.md` | Observed hardware/model mismatches and supporting evidence |
| `synthesis/` | Weekly one-page summaries and the final proposal |

The supplied plan currently covers the introduction, daily routine, and setup. Detailed week-by-week tasks have not yet been supplied. GPU tools and third-party projects are setup items; they are not installed or vendored by this repository.
