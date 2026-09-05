# Go CI Standards

Public reusable GitHub Actions workflows for Go repositories.

This repository intentionally contains only safe, generic CI automation. Private engineering rules, project memory, decisions, and project-specific context remain in `krav01/dev-standards`.

## Reusable Go CI

Call `.github/workflows/go-ci.yml` from a consumer repository and pin it to an immutable commit SHA or release tag.

Supported controls:
- module tidiness check;
- `go build ./...`;
- shuffled tests;
- optional `golangci-lint`;
- optional `govulncheck`;
- optional race detector.

Project-specific integration tests, migrations, Docker smoke tests, release validation, CodeQL, dependency review, and domain invariants remain the responsibility of the consuming repository.

## Security model

- read-only `contents` permission;
- checkout credentials are not persisted;
- no secrets are required;
- no project data is uploaded;
- no write operations are performed in consumer repositories.

## Versioning

Consumers must not depend on `@main` for behavior-changing CI. Pin to an immutable commit SHA or reviewed release tag.
