# setup-shfmt action

easy way to install [shfmt](https://github.com/mvdan/sh) in your GitHub Actions
workflows.

```yaml
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@9c091bb21b7c1c1d1991bb908d89e4e9dddfe3e0  # v7.0.0
      - uses: pcrockett/setup-shfmt@LATEST_RELEASE_TAG
```

if you don't want to use the default version of shfmt that comes with this action, you
can specify your own version and checksum:

```yaml
- uses: pcrockett/setup-shfmt@LATEST_RELEASE_TAG
  with:
    version: '3.13.1'
    checksum: 'fb096c5d1ac6beabbdbaa2874d025badb03ee07929f0c9ff67563ce8c75398b1'
```

**recommended:** run [pinact](https://github.com/suzuki-shunsuke/pinact) to pin your
actions to a specific release. don't worry, if you're using Dependabot, Renovate, etc.,
they will update your pins correctly for you.

```bash
pinact run --update
```
