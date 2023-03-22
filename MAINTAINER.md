# Notes for Maintainer

## Helm Charts

### How to package and publish maunually

> **NOTE:** This is only needed if you want to publish a new version of the Helm chart manually. The Helm chart is published automatically by GitHub Actions.

The Helm charts are published to GitHub Pages. To package and publish a new version of the Helm chart, run the following commands:

```bash
helm package charts/keycloak-operator
helm repo index ./
git checkout gh-pages
git add .
git commit -m "Release keycloak-operator-x.x.x"
git push
git checkout main
```
