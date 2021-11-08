# Reusable Workflows for GitHub Actions

A simple collection of reusable Workflows for GitHub Actions.

## Available Workflows

### Docker

#### Anchore Analysis

```YAML
jobs:
  anchore-analysis:
    uses: paniclobster/github-workflows/.github/workflows/docker-anchore-analysis.yaml@main
    with:
      docker_build_context: .
      docker_image_name: desired-org-name/desired-image-name
```

#### Build

```YAML
jobs:
  build:
    uses: paniclobster/github-workflows/.github/workflows/docker-build.yaml@main
```

#### Build and Publish

```YAML
jobs:
  build-publish:
    uses: paniclobster/github-workflows/.github/workflows/docker-build-publish.yaml@main
    with:
      docker_build_context: .
      docker_image_name: desired-org-name/desired-image-name
      docker_hub_username: ${{ secrets.DOCKER_HUB_USERNAME }}
      docker_hub_password: ${{ secrets.DOCKER_HUB_PASSWORD }}
```

#### Dive Analysis

```YAML
jobs:
  dive-analysis:
    uses: paniclobster/github-workflows/.github/workflows/docker-dive-analysis.yaml@main
    with:
      docker_build_context: .
      docker_image_name: desired-org-name/desired-image-name
```
