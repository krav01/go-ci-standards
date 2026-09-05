# Changelog

## 1.7.0

- add release/SHA verification guidance for consumer standards pins;
- require immutable SHA scanning across workflow files;
- define CI duration budgets for fast, normal, and high-risk verification paths;
- strengthen automatic standards-upgrade validation before opening a PR;
- prepare consumer integration for richer impact planning metadata.

## 1.6.0

- define standards-only fast paths so consumer repositories can skip heavy verification when only standards metadata changes;
- add a safe automatic standards-upgrade workflow template that only moves repositories forward to a newer published baseline;
- extend guidance for immutable action pinning and memory freshness automation.

## 1.5.0

- pin third-party GitHub Actions by immutable commit SHA;
- add release safety validation;
- add atomic tag and GitHub Release publishing workflow;
- align public standards drift version with development baseline 1.5.0.

## 1.4.0

- initial public reusable Go CI and standards drift workflows.
