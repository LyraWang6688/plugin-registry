# Plugin Registry

Central registry for AI plugins, connectors, external capabilities, permissions, and use cases.

## Purpose

This repository records which external tools an AI can use, what each tool can do, how it authenticates, and where it should be used.

## Repository Structure

```text
plugin-registry/
├── README.md
├── CONTRIBUTING_AI.md
├── registry.yaml
├── providers/
│   └── <provider-name>/
│       └── README.md
└── use-cases/
    └── <use-case>.md
```

## Core Principle

A Skill defines **how to perform a reusable workflow**.

A Plugin defines **which external capability is available to execute part of that workflow**.

## Registry

`registry.yaml` is the machine-readable source of truth for registered plugins and capabilities.

## AI Contributors

Before adding or changing a plugin record, read:

1. [CONTRIBUTING_AI.md](./CONTRIBUTING_AI.md)
2. [registry.yaml](./registry.yaml)
