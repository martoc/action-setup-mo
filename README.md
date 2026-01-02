[![checks](https://github.com/martoc/action-setup-mo/actions/workflows/checks.yml/badge.svg?branch=main&event=push)](https://github.com/martoc/action-setup-mo/actions/workflows/checks.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

# action-setup-mo

A GitHub Action that installs [mo](https://github.com/tests-always-included/mo) (Mustache Templates in Bash) to your GitHub Actions runner. Mo is a pure bash implementation of Mustache templates.

## Features

- Installs mo v3.0.5 to `/usr/local/bin/`
- Makes `mo` command available for subsequent workflow steps
- Lightweight and fast installation

## Quick Start

```yaml
- name: Setup mustache template
  uses: martoc/action-setup-mo@v0
```

## Documentation

- [Usage Guide](./docs/USAGE.md) - Detailed usage instructions and examples
- [Code Style](./docs/CODESTYLE.md) - Code style guidelines for contributors

## Example

```yaml
- name: Setup mustache template
  uses: martoc/action-setup-mo@v0

- name: Process template
  run: |
    export NAME="World"
    echo "Hello {{NAME}}!" | mo
```

## Licence

This project is licenced under the MIT Licence - see the [LICENCE](LICENSE) file for details.
