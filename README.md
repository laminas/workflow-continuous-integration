# Laminas Reusuable Continuous Integration Workflow

This repository contains a reusable workflow describing the Laminas Project continuous integration.


## Usage

To use the CI workflow:

```yaml
# In a package repository, in the file .github/workflows/continuous-integration.yml:
name: "Continuous Integration"

on:
  pull_request:
  push:
    branches:
    tags:

jobs:
  ci:
    uses: laminas/workflow-continuous-integration/.github/workflows/continuous-integration.yml@1.x
```

## Available references

GitHub recommends when using reusable workflows that you specify a reference to ensure stability.
This package defines a release branch per stable version, as well as tags.
Generally speaking, a release branch will only receive:

- Bugfixes
- New opt-in features (including optional inputs, and new outputs)

Since they will not receive backwards incompatible changes, you can pin to them.

We also provide tags.
Tags are immutable, and can be trusted without issue; however, your project will not benefit from updates without first changing the reference in your workflow.

### Current branches

- 1.x

### Tags

Please see the [releases page](/laminas/workflow-continuous-integration/releases) for a complete list.
