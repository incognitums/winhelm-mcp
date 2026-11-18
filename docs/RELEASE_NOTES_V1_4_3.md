# WinHelm v1.4.3 — Release Notes

**Release date:** 2026-11-19
**Type:** metadata and test-robustness patch. No tool, schema, or runtime behaviour changes.

## Summary

v1.4.3 transfers project ownership metadata to the `incognitums` GitHub account and
removes an assumption in the integration tests that the runtime version is `1.4.2`.
The canonical MCP surface stays at **56 tools**.

## Changed

- **Project metadata → `incognitums`**
  - `package.json` (`author`, `repository`, `bugs`, `homepage`)
  - `manifest.json`, `server.json`, `public/.well-known/security.txt`
  - npm package page now points at `github.com/incognitums/winhelm-mcp`
- **Tests read the runtime version dynamically**
  - `test/integration/server.test.ts` uses `SERVER_VERSION` instead of the hardcoded
    `1.4.2`, so future version bumps no longer break the suite.

## Unchanged

- 56 canonical tools, Schema-v2 governance, dynamic profiles
- Approval UX, dashboard, gateway (`/mcp`, `/sse`), health endpoint shape
- All security posture defaults (conservative ingress, Manual service, no dangerous mode)

## Upgrade

```sh
npm install -g winhelm-mcp@1.4.3
```

No configuration or migration steps.

## Verification

- `npm test` — full suite green on the release candidate
- `package.json`, `package-lock.json`, `manifest.json`, `server.json` all report `1.4.3`
- npm publish verified: metadata on the registry points at `incognitums/winhelm-mcp`

## Links

- npm: https://www.npmjs.com/package/winhelm-mcp
- Repository: https://github.com/incognitums/winhelm-mcp
- Changelog: [`CHANGELOG.md`](../CHANGELOG.md)
