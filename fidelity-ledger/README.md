# Fidelity ledger

Maintainer evidence lives here. Ordinary domain dialogue loads the root skill and relevant references only.

## Current records

- [source-manifest.json](source-manifest.json): eight source identities, hashes, corrected chapter counts, extraction outcomes, budgets, and publication exclusions.
- [coverage-inventory.json](coverage-inventory.json): retained arguments and omissions, including chapter dispositions for the Guide and both new Heschel works.
- [coverage-audit.md](coverage-audit.md): original audits plus two additional spans per Heschel book, counterexamples, and limits.
- [heschel-reading-ledger.json](heschel-reading-ledger.json): incremental bounded reading, audit questions, and emitted-token bounds. Two clipped outputs are marked; actual model consumption was not metered.
- [reading-ledger.json](reading-ledger.json) and [reading-report.json](reading-report.json): historical six-book reading records, unchanged by this expansion.
- [synthesis-and-attribution.md](synthesis-and-attribution.md): adopted subject priorities, settled conflicts, and the distinction between the guide's voice and its sources.
- [acceptance-suite.json](acceptance-suite.json): original frozen eight-scenario suite, preserved byte-for-byte.
- [spiritual-guide-acceptance-suite.json](spiritual-guide-acceptance-suite.json): eight additional frozen scenarios for the redesigned guide, defined before semantic reading of the new complete books and the rewritten core, after the user brief and publisher opening excerpts had been read.
- [acceptance-results.json](acceptance-results.json) and [spiritual-guide-acceptance-results.json](spiritual-guide-acceptance-results.json): current runtime identity and explicit unrun status. No fabricated transcripts, grades, or provider usage.
- [editorial-review.md](editorial-review.md): same-author inspection, distinct from behavioral evidence.
- [validation.json](validation.json), [scan-core.json](scan-core.json), [scan-references.json](scan-references.json), [quick-validation.txt](quick-validation.txt), [verification.json](verification.json), and [suite-validation.json](suite-validation.json): actual mechanical checks for the revised layout.
- [history/companion-v1/](history/companion-v1/): preserved earlier maintainer evidence. Historic hashes and counts describe that earlier artifact, not this revision.

## Reproduce checks

Using the Books-to-Skill-Refs tool repository, run:

```sh
python3 tools/validate_library.py /path/to/Jewish-Spiritual-Guide --layout published-repo --json
python3 tools/scan_generated_skill.py /path/to/Jewish-Spiritual-Guide/SKILL.md --strict --json
python3 tools/scan_generated_skill.py /path/to/Jewish-Spiritual-Guide/references --strict --json
```

Section budgets are targets, not floors. References are not padded to meet a target. Extraction does not establish semantic reading of all lines. Emitted-token bounds are not billing data. Private source paths and raw books are excluded from publication.

Controlled evaluation requires actual independent contexts, a selected model with identical settings for baseline, core-only, and relevant-reference conditions, retrieval traces, separate grading, and reported usage where available. Until run, structural passes establish neither behavioral superiority nor full acceptance.
