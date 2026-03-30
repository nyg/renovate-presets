# renovate-presets

My Renovate presets.

## Presets

### `default` (`github>nyg/renovate-presets`)

The default preset. Extends `config:best-practices` and adds:

- Minor and patch updates are grouped, scheduled monthly, and automerged.
- Lock file maintenance is automerged.
- A `minimumReleaseAge` of 3 days is applied to all updates (stability wait).
- Vulnerability alerts are automerged immediately (no stability wait).

### `default2` (`github>nyg/renovate-presets:default2`)

Extends `default` with one change: **lock file maintenance PRs are not subject to the `minimumReleaseAge` / stability-days waiting period** and will automerge as soon as all checks pass.

Use this preset if you want lock file maintenance PRs to automerge without waiting on `renovate/stability-days`.

```json
{
  "extends": ["github>nyg/renovate-presets:default2"]
}
```
