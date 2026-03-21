# Git Version Action

This GitHub Action automates the process of determining and tagging the semantic version of your repository using [GitVersion](https://gitversion.net/). It is designed to work with any Git repository and supports custom configuration via a `gitversion.yml` file.

## Features

- Calculates semantic version based on your Git history and branching strategy
- Outputs version information for use in subsequent workflow steps
- Includes a default GitVersion config (GitHubFlow + Conventional Commits)
- Supports custom configuration via `gitversion-config` input
- Optionally generates AI-powered changelogs via GitHub Models API
- Optionally updates Terraform module version files
- Works with any GitHub workflow

## Requirements

`No Requirements`

## Inputs

| Name | Description | Required | Default |
| --- | --- | --- | --- |
| <a name="input_gitVersionConfigPath"></a> [gitVersionConfigPath](#input_gitVersionConfigPath) | Path to a custom `gitversion.yml`. If empty, uses the default config bundled with this action. | false | `''` |
| <a name="input_useChangeLogPromptDefaultConfig"></a> [useChangeLogPromptDefaultConfig](#input_useChangeLogPromptDefaultConfig) | Whether to use the default CHANGELOG prompt configuration | false | `'true'` |
| <a name="input_isTerraformModule"></a> [isTerraformModule](#input_isTerraformModule) | Whether the repository is a Terraform module | false | `'false'` |
| <a name="input_githubToken"></a> [githubToken](#input_githubToken) | GitHub PAT with `models:read` permission for AI changelog generation | false | `${{ github.token }}` |

## Outputs

| Name | Description |
| --- | --- |
| `majorVersion` | Major version number |
| `minorVersion` | Minor version number |
| `patchVersion` | Patch version number |
| `majorMinorVersion` | Major.Minor version |
| `majorMinorPatchVersion` | Major.Minor.Patch version |

## Usage

Here's an example of how to use this action in a GitHub Actions workflow:

```yaml
name: Tag Version

on:
  push:
    branches: [ main, dev ]
  pull_request:
    branches: [ main ]
  workflow_dispatch:

permissions:
  contents: write
  models: read

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
    - name: Checkout Step
      uses: actions/checkout@v6
      with:
        fetch-depth: 0
        fetch-tags: true
    
    - name: Generate semantic version and tag repository
      id: gitversion
      uses: mbasri-actions/gitversion@main
      with:
        isTerraformModule: 'true'
```

## Author

* [**Mohamed BASRI**](https://github.com/mbasri)

## License

This is free and unencumbered software released into the public domain. See the [LICENSE](./LICENSE) file for details.
