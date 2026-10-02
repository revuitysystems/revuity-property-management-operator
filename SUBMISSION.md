# Submission answers

Prepared for Revuity's submission to the Claude plugin directory. This file does not change plugin behavior.

## Source

- Repository: https://github.com/revuitysystems/revuity-property-management-operator
- Branch: main
- Plugin path: repository root (the folder containing .claude-plugin/plugin.json)
- Plugin name: property-management-operator
- Display name: Property Management Operator
- Version: 1.0.0
- Skill: property-management-operator:property-operations

## Listing

- Description: Property management workflow support for resident requests, maintenance triage, vendors, inspections, renewals, delinquencies, and operating reviews.
- Author / publisher: Revuity Systems
- Homepage: https://revuitysystems.com
- Contact: info@revuitysystems.com
- License: MIT
- Icon: assets/icon.png (512, 256 and 128 pixel versions alongside)

## Data handling

- External services operated by Revuity: None
- Plugin-controlled storage: None
- Plugin-controlled retention: None
- Sends data to undeclared Revuity services: No
- Intended for users under 18: No
- Plugin may process personal information supplied by the authorized user: Yes
- Plugin does not independently collect or retain user data

The plugin may process resident, applicant, employee, owner, or vendor information supplied by authorized users. It does not independently store that data.

## External services

None operated by Revuity. The plugin contains no MCP servers, hooks, commands, agents, or executable plugin code. It relies only on the tools and connectors the user has already enabled in their own Claude environment.

## Storage and retention

The plugin stores nothing and sets no retention. Anything the user shares is handled under the user's own Claude plan and their organization's policies.

## Audience

Intended for adult professionals using the workflow at work. Not intended for users under 18.

## Validation

- Structural validation (scripts/validate.py): PASS in GitHub Actions
- claude plugin validate --strict: PASS locally and in GitHub Actions
- Runtime load with claude --plugin-dir: PASS (plugin recognized at 1.0.0, skill property-management-operator:property-operations registered, no plugin errors, no plugin-provided MCP servers, absent when started without the flag)
- Representative skill invocation: NOT RUN. The local Claude CLI session was unauthenticated when this file was written. See SUBMISSION_READINESS.md once the invocation test has been completed.

## Submission notes

- Submit as a single plugin from the repository root. Choose Plugin bundle in the developer portal.
- The plugin name is built from generic words. The directory may hold it for reviewer confirmation under its name rules.
- The only non-documentation files are the skill, the manifest, icon images, a GitHub Actions workflow, and a small Python validation script that does not run when the plugin is installed.
