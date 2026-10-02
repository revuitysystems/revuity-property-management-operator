# Property Management Operator

**A free Claude workflow plugin by [Revuity Systems](https://revuitysystems.com).**

![Property Management Operator plugin icon](assets/icon-128.png)

A free Claude plugin for recurring property-management coordination across resident requests, maintenance, vendors, inspections, lease events, delinquencies, and portfolio review. It helps property teams organize work, prepare communications, track dependencies, and surface exceptions without replacing legal, financial, or management authority.

- Plugin name: `property-management-operator`
- Skill: `/property-management-operator:property-operations`
- Version: 1.0.0
- License: MIT

## Plugin icon

The plugin icon ships in the assets folder in 512, 256, and 128 pixel versions. The manifest references it with the icon field, which Anthropic's directory reads for the plugin listing and Claude Code ignores at load time.

## Good for

- Resident request triage
- Maintenance coordination
- Vendor follow-up and briefs
- Inspection preparation
- Lease and renewal workflow
- Delinquency follow-up preparation
- Work-order aging review
- Property and portfolio operating reviews

## How it works

The plugin structures each item around the property or unit, requester, issue, urgency based on the policy you supply, access constraints, responsible party, next action, due date, and escalation condition. Maintenance work follows request, clarify, classify, assign, schedule, access, complete, verify, and close. It prepares vendor briefs and resident communication drafts while leaving approvals and regulated decisions with authorized people.

## Example requests

Once the plugin is loaded, ask in plain language or invoke the skill directly with `/property-management-operator:property-operations`.

- "Triage these new resident requests against our emergency and urgency policy and tell me which need an authorized person now."
- "Prepare a vendor brief for this work order with scope, location, access, and what we need back as completion evidence."
- "Build the renewal workflow for leases with notice dates in the next 90 days."
- "Summarize open work orders by age and repeat issues for the weekly property review."

You supply the information, either by pasting it in or through tools you have already connected to Claude. The plugin does not collect data of its own, does not call any Revuity service, and has no executable code.

## Authority and safety boundaries

The plugin drafts, organizes, compares, and recommends by default. It does not invent legal obligations, emergency classifications, lease terms, fees, or enforcement authority. For a possible immediate threat to life or safety such as fire, gas, or flooding, it surfaces the concern prominently and directs the authorized operator to the approved emergency procedure. It does not make or recommend tenant-selection, renewal, enforcement, accommodation, or service decisions based on protected characteristics, and it escalates possible fair-housing, accommodation, or retaliation questions to authorized policy or legal review. Legal notices, lease commitments, screening or denial, fees, payment arrangements, spending approval, collections, filings, access and security changes, and external sends with legal or financial consequence require explicit human authorization.

When something is missing, stale, or in conflict, the plugin is written to stop and say so rather than guess.

## Data handling

Share only the resident, property, and financial information a task needs, and use authoritative records for balances and dates. Avoid pasting passwords or unnecessary personal identifiers. Your own privacy and records obligations still apply to anything you share with Claude.

## Install

This repository is a single Claude plugin with its manifest at `.claude-plugin/plugin.json` and its skill at `skills/property-operations/SKILL.md`.

To try it locally, clone the repository and start Claude Code with the plugin directory:

```bash
git clone https://github.com/revuitysystems/revuity-property-management-operator.git
claude --plugin-dir ./revuity-property-management-operator
```

Then run `/reload-plugins` and confirm `/property-management-operator:property-operations` appears. To check the package without running it, use `claude plugin validate ./revuity-property-management-operator`.

## Validation

A GitHub Actions workflow in this repository checks the manifest, semantic version, skill frontmatter, and required documentation on every push and pull request. See `.github/workflows/validate.yml`. Passing validation shows the package is well formed. It does not replace testing the plugin in your own Claude environment against your own policies.

## Built by Revuity Systems

Revuity Systems is an Operations Systems company. These public workflow plugins are free operating tools designed to make real work easier while demonstrating how Revuity thinks about roles, workflows, responsibility, authority, exceptions, outcomes, and operating cadence.

When an organization later needs the workflow adapted to its own systems, policies, data, approvals, integrations, or operating model, Revuity may help design or build that larger system. You do not need to talk to anyone to use this plugin.

More at [revuitysystems.com](https://revuitysystems.com). Questions or security concerns: info@revuitysystems.com.

## Privacy

This plugin does not collect or store data itself. Revuity's privacy policy is at [revuitysystems.com/privacy](https://revuitysystems.com/privacy).

## License

MIT. See [LICENSE](LICENSE).
