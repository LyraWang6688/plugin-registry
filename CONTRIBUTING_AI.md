# AI Contribution Protocol

This file defines the required rules for any AI system modifying the plugin registry.

## Mandatory Read Order

Before making changes:

1. Read `CONTRIBUTING_AI.md`.
2. Read `registry.yaml`.
3. Inspect the relevant provider record before editing it.

## What Belongs Here

Register external tools that provide capabilities to AI systems, including:

- plugins
- connectors
- MCP servers
- external APIs used as tools
- authenticated application integrations

Do not store reusable workflow instructions here; those belong in the Skill Lifecycle Hub.

## Provider Structure

Each provider should use:

```text
providers/<provider-name>/README.md
```

Use lowercase kebab-case for provider identifiers.

## Registry Fields

A plugin record should capture, when known:

- `name`
- `provider`
- `status`
- `auth`
- `capabilities`
- `permissions`
- `provider_path`
- `notes`

Do not invent unknown permissions or authentication methods.

## Status Values

Use:

- `available`
- `limited`
- `disabled`
- `unknown`

## Contribution Workflow

1. Check whether the plugin or provider already exists.
2. Inspect the current record.
3. Add or update only verified information.
4. Update `registry.yaml`.
5. Update the provider README when details change.
6. Use a clear commit message.

## Commit Message Convention

```text
feat(plugin): add <plugin-name>
update(plugin): update <plugin-name>
fix(plugin): correct <plugin-name>
chore(registry): update plugin registry
```

## Safety Rules

Do not:

- store secrets, API keys, access tokens, cookies, or credentials
- claim permissions that have not been verified
- duplicate the same provider under multiple identifiers without a reason
- mix plugin records with skill definitions
- change unrelated files
