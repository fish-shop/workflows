# workflows

Reusable GitHub Actions workflows for [fish-shop](https://github.com/fish-shop) projects.

## Calling Reusable Workflows

Call reusable workflows with the `uses` keyword directly within a job, using the syntax `fish-shop/workflows/.github/workflows/{filename}@{ref}`. For example:

```yaml
jobs:
  release-tags:
    uses: fish-shop/workflows/.github/workflows/release-tags.yml@v1
```
## Available workflows

| Name             | Purpose                                                                            |
|------------------|------------------------------------------------------------------------------------|
| `release-tags`   | Create major and major-minor release tags after new semantic version tag is added. |
| `markdown-links` | Check for broken hyperlinks in Markdown files.                                     |

## Available Workflows

| Name                    | Description                                                                          |
|-------------------------|--------------------------------------------------------------------------------------|
| [release-tags.yml](.github/workflows/release-tags.yml)      | Create major and major-minor release tags (i.e. `vX` and `vX.Y`) for tags matching the format `vX.Y.Z`.     |

## Workflow Versions

Use one of the following patterns when specifying the version reference for workflows (i.e. the `{ref}` value in `uses: fish-shop/workflows/.github/workflows/{filename}@{ref}`):

| Pattern  | Example   | Description                                                            |
|----------|-----------|------------------------------------------------------------------------|
| `vX`     | `v1`      | the latest `v1.*` release including non-breaking changes and bug fixes |
| `vX.Y`   | `v1.1`    | the latest `v1.1.*` release including bug fixes                        |
| `vX.Y.Z` | `v1.1.0`  | the `v1.1.0` release only                                              |                

The recommended pattern is `vX` (e.g. `v1`). This will ensure that the version of the workflow used includes the latest non-breaking changes and bug fixes, and guarantees compatibility with previous versions of that major release number.

Using a `main` branch reference is _not_ recommended as this branch may include breaking changes intended for the next major release.

## License

This project is provided under the terms of the [MIT License](https://opensource.org/licenses/mit-license.php).

## Contact

Email me at [marc.ransome@fidgetbox.co.uk](mailto:marc.ransome@fidgetbox.co.uk) or [create an issue](https://github.com/fish-shop/workflows/issues). Alternatively, refer to the official [discussions board](https://github.com/orgs/fish-shop/discussions).
