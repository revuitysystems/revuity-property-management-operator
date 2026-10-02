# Changelog

## Unreleased

- Added `displayName` to the manifest and `SUBMISSION.md` for the directory submission. Switched the README icon to Markdown image syntax. No change to plugin behavior.
- Added plugin icon assets (`assets/icon.png` and 512, 256, 128 pixel versions), an `icon` manifest field for the Anthropic directory listing, and a README icon section. No change to plugin behavior.

## 1.0.0 — Initial public release

- Initial public release of Property Management Operator as a standalone plugin repository.
- Added the `property-management-operator` plugin with the `property-operations` skill covering intake and triage, maintenance workflow, vendor coordination, lease and renewal workflow, delinquency workflow, and operating reviews.
- Includes a source hierarchy, an emergency-concern escalation rule, and a fair-housing and screening boundary.
- Includes explicit authorization boundaries for legal notices, fees, payment arrangements, spending, collections, filings, and lease commitments.
- Added a GitHub Actions workflow that validates the manifest, semantic version, skill frontmatter, and required documentation.

### Verification

Package validation runs in GitHub Actions. This release has not been installed or exercised in a user's Claude runtime by its authors; smoke-test the plugin in your own Claude environment after installing it.
