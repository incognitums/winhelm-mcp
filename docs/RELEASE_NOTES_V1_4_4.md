# WinHelm v1.4.4 — Release Notes

**Release date:** 2026-11-19
**Type:** documentation patch published so the npm page shows the current README.

## Why this release exists

npm renders the README from the published tarball, and metadata for a published version
cannot be edited afterwards. v1.4.3 was published before its README was updated, so the
npm page kept showing "Product Status: v1.4.2". v1.4.4 republishes the same code with
the corrected documentation.

## Changed (docs only)

- README now reports **v1.4.4** as the current status/identity and links the v1.4.4
  release notes.
- `/health` example shows `"version": "1.4.4"`.
- npm page now matches the repository README.

## Unchanged

- No source, tool, schema, gateway, or security change.
- Canonical MCP surface remains **56 tools**.

## Upgrade

```sh
npm install -g winhelm-mcp@1.4.4
```

No configuration or migration steps.

## Links

- npm: https://www.npmjs.com/package/winhelm-mcp
- Repository: https://github.com/incognitums/winhelm-mcp
- Changelog: [`CHANGELOG.md`](../CHANGELOG.md)
