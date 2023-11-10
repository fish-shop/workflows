# workflows

Reusable GitHub Actions workflows for [fish-shop](https://github.com/fish-shop) projects.

## Calling Reusable Workflows

Call reusable workflows with the `uses` keyword directly within a job, using the syntax `fish-shop/workflows/.github/workflows/{filename}@{ref}`. For example:

```yaml
jobs:
  dependency-review:
    uses: fish-shop/workflows/.github/workflows/dependency-review.yml@v1
```

## Available Workflows

| Name                    | Description                                                                          |
|-------------------------|--------------------------------------------------------------------------------------|
| `release-tags.yml`      | Create major and major-minor release tags (i.e. `vX` and `vX.Y`) for tags matching the format `vX.Y.Z`.     |

## License

This project is provided under the terms of the [MIT License](https://opensource.org/licenses/mit-license.php).

## Contact

Email me at [marc.ransome@fidgetbox.co.uk](mailto:marc.ransome@fidgetbox.co.uk) or [create an issue](https://github.com/fish-shop/workflows/issues). Alternatively, refer to the official [discussions board](https://github.com/orgs/fish-shop/discussions).
