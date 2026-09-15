# Fidelity ledger

These are maintainer records. Ordinary domain dialogue loads the root skill and relevant references only.

- [source-manifest.json](source-manifest.json): six source identities, hashes, section counts, extraction outcome, budgets, and publication exclusions.
- [coverage-inventory.json](coverage-inventory.json): retained sections, dropped material, and a complete disposition list for the Guide's 178 chapters.
- [coverage-audit.md](coverage-audit.md): two additional spans per source, changed qualifications, and limitations.
- [reading-ledger.json](reading-ledger.json) and [reading-report.json](reading-report.json): bounded reads, overlap, emitted-token upper bounds, and unknown actual consumption. Some tool outputs were clipped; neither exact reading coverage nor precise provider usage is claimed.
- [synthesis-and-attribution.md](synthesis-and-attribution.md): source distinctions and the companion's own design commitments.
- [acceptance-suite.json](acceptance-suite.json): eight frozen scenarios, defined after conversion/metadata inspection and before semantic source reading; four development and four final.
- [acceptance-results.json](acceptance-results.json): explicitly **unrun**, with suite/runtime hashes. No fabricated responses, grades, or provider usage.
- [editorial-review.md](editorial-review.md): same-author design review, distinct from behavioral evidence.
- [validation.json](validation.json): actual structural validator result.
- [scan-core.json](scan-core.json) and [scan-references.json](scan-references.json): separate strict instruction-boundary scans.
- [quick-validation.txt](quick-validation.txt): Agent Skills frontmatter validation.
- [verification.json](verification.json): links, reference count, source-locator bounds, hashes, and symlink checks.

## Reproduce mechanical checks

With the Books-to-Skill-Refs tool repository available, run its tools against this repository path:

```sh
python3 tools/validate_library.py /path/to/Jewish-Study-Companion --layout published-repo --json
python3 tools/scan_generated_skill.py /path/to/Jewish-Study-Companion/SKILL.md --strict --json
python3 tools/scan_generated_skill.py /path/to/Jewish-Study-Companion/references --strict --json
```

`reading-report.json` uses the metatool's reading-audit calculation with renamed fields because emitted-token bounds are not actual read counts. Do not use its estimates as provider billing data. The section budget is a target, not a floor; shorter references were not padded. No local paths to the source books are published.

Controlled behavioral evaluation must use actual independent contexts, the same selected model/settings across baseline, core-only and full-reference conditions, retrieval traces, separate grading, and provider-reported usage where available. Until then, the suite's existence and the structural pass establish neither improvement nor full behavioral acceptance.
