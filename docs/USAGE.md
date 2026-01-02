# Usage

## Overview

This GitHub Action installs [mo](https://github.com/tests-always-included/mo) (Mustache Templates in Bash) to your GitHub Actions runner. Mo is a pure bash implementation of Mustache templates.

## Quick Start

```yaml
- name: Setup mustache template
  uses: martoc/action-setup-mo@v0
```

## Example Workflow

```yaml
name: Process Templates

on:
  push:
    branches:
      - main

jobs:
  template:
    runs-on: ubuntu-24.04
    steps:
      - uses: actions/checkout@v4

      - name: Setup mustache template
        uses: martoc/action-setup-mo@v0

      - name: Process template
        run: |
          export NAME="World"
          echo "Hello {{NAME}}!" | mo
```

## What Gets Installed

- `mo` version 3.0.5 is downloaded and installed to `/usr/local/bin/`
- The `mo` command becomes available for subsequent steps in your workflow

## Notes

- The action requires `curl` to be available on the runner (included by default on GitHub-hosted runners)
- The tool is installed system-wide and persists for the duration of the workflow job
