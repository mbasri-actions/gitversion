# Git Version Action

This GitHub Action automates the process of determining and tagging the semantic version of your repository using [GitVersion](https://gitversion.net/). It is designed to work with any Git repository and supports custom configuration via a `gitversion.yml` file.

## Features

- Calculates semantic version based on your Git history and branching strategy
- Outputs version information for use in subsequent workflow steps
- Supports custom configuration via `gitversion.yml`
- Works with any GitHub workflow

## Requirements

`No Requirements`

## Inputs

| Name | Description | Required | Default |
| --- | --- | --- | --- |
| <a name="input_useDefaultConfig"></a> [useDefaultConfig](#input_useDefaultConfig) | Whether to use the default GitVersion configuration | false | `true` |
| <a name="input_configFilePath"></a> [configFilePath](#input_configFilePath) | Path to a custom GitVersion configuration file | false | `gitversion.yml` |

## Outputs

`No Outputs`

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

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
    - name: Checkout Step
      uses: actions/checkout@v4
      with:
        fetch-depth: 0
    - name: Tag the repo
      id: gitversion
      uses: mbasri-actions/gitversion@v1.0.0
```

## Author

* [**Mohamed BASRI**](https://github.com/mbasri)

## License

This is free and unencumbered software released into the public domain. See the [LICENSE](./LICENSE) file for details.
