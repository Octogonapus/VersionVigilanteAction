# VersionVigilanteAction

This actions runs [VersionVigilante.jl](https://github.com/bcbi/VersionVigilante.jl/) to check that your Julia package PRs contain appropriate version bumps.

## Example

In a file named `.github/workflows/VersionVigilante.yml`:

```yml
name: VersionVigilante

on:
  pull_request:
    branches:
      - main
    paths-ignore:
      - ".github/**"
      - "README.md"
      - "dev/**"

jobs:
  VersionVigilante:
    runs-on: ubuntu-latest
    permissions:
      contents: read
      pull-requests: write
    steps:
    - uses: Octogonapus/VersionVigilanteAction@main
```
