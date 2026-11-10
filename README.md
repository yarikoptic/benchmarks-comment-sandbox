# benchmarks-comment-sandbox

Throwaway sandbox to test, before proposing it to datalad/datalad, how the
benchmark comparison gets reported to PRs, including PRs from forks.

- `.github/workflows/benchmarks-comment.yml` and `tools/ci/benchmark-report.py`
  are verbatim copies from the datalad branch `claude/stoic-goldberg-nlfsda`.
- `.github/workflows/benchmarks.yml` is datalad's "Benchmarks" workflow with
  the asv setup and run replaced by a stub: it takes the real `asv compare
  --split` output (and notes, if any) of the scenario named in the file
  `scenario` from `fixtures/<scenario>/`.  All steps from "Summarize" on are
  verbatim.

A PR selects a scenario by changing the content of `scenario` to one of
`slower`, `nochange` or `notes`.

Scenario F2: PR from a fork without significant changes.
