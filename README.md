# renovate-config

libops' [Renovate Shareable Config Presets](https://docs.renovatebot.com/config-presets/#github)

LibOps-owned GitHub dependencies and container images stay on readable release
tags or branches. Renovate updates those refs, but does not replace them with
commit SHAs or image digests. External dependencies retain the upstream
best-practice digest-pinning policy.


## Usage

In the GitHub repo you want to have renovate manage updates for, add a `renovate.json5` file in the root of the repo with the contents

```
{
  $schema: 'https://docs.renovatebot.com/renovate-schema.json',
  extends: [
    'github>libops/renovate-config:default.json5',
  ],
}
```
