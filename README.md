# upm-registry

The master list of areezkhan79's reusable Unity packages, consumed by the
[Package Hub](https://github.com/areezkhan79/upm-package-hub) Editor tool.

## Adding a new package

After publishing a new package repo (with at least one git tag), add an entry
to `registry.json`:

```json
{
  "name": "com.areezkhan79.<module>",
  "displayName": "<Human readable name>",
  "description": "<One line description>",
  "repoUrl": "https://github.com/areezkhan79/<repo>.git"
}
```

`name` must exactly match the `name` field in that package's own `package.json`.
Available versions are **not** listed here — Package Hub fetches them live from
each repo's git tags, so you never need to update this file when you cut a new
release, only when you add a brand-new package.
