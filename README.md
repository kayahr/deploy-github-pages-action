# Deploy Github Pages

This is a composite Github action combining the following steps into one, so the whole deployment step can be made conditional with a single if statement:

* [actions/configure-pages](https://github.com/actions/configure-pages)
* [actions/upload-pages-artifact](https://github.com/actions/upload-pages-artifact)
* [actions/deploy-pages](https://github.com/actions/deploy-pages)

## Usage

This step deploys the files in the `doc` folder, but only if branch is `main`:

```yaml
steps:
  - name: Deploy Github Pages
    if: github.ref == 'refs/heads/main'
    uses: kayahr/deploy-github-pages-action@v4
    with:
      path: doc
```
