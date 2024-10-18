# Sentry Release Buildkite Plugin

A Buildkite plugin for creating a release in Sentry

## Options

These are all the options available to configure this plugin's behaviour.

### Required

#### `org` (string)

The Sentry organisation.

#### `project` (string)

The Sentry project.

### Optional

#### `environment` (string)

The environment of the release.  
Default: `production`

#### `source-maps-artifact` (string)

The name or pattern of a Buildkite artifact to download and use as source maps for the release.  
Default: `""`

## Examples

Create a release in Sentry:

```yaml
steps:
  - label: ":sentry: Create release in Sentry"
    plugins:
      - jradtilbrook/sentry-release#v1.0:
          org: atlantica
          project: website
```

## 📜 License

The package is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).
