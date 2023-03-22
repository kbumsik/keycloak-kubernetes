# Notes for Maintainer

## Helm Charts

### How to package and publish maunually

> **NOTE:** This is only needed if you want to publish a new version of the Helm chart manually. The Helm chart is published automatically by GitHub Actions.

The Helm charts are published to GitHub Pages. To package and publish a new version of the Helm chart, run the following commands:

```bash
helm package --sign --key 'Bumsik Kim' --keyring ~/.gnupg/secring.gpg charts/keycloak-operator
git checkout gh-pages
helm repo index ./
git add .
git commit -m "Release keycloak-operator-x.x.x"
git push
git checkout main
```

References:

- https://helm.sh/docs/topics/provenance/
