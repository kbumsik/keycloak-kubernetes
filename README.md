# Page for Helm Charts Repository

This GitHub Page is only for hosting the Helm Charts Repositories for [kbumsik/keycloak-kubernetes](https://github.com/kbumsik/keycloak-kubernetes).

- [keycloak-operator](./charts/keycloak-operator/): Helm chart for the Keycloak Operator.

Go to the original GitHub Link: [kbumsik/keycloak-kubernetes](https://github.com/kbumsik/keycloak-kubernetes).

## Usage

References:

- https://helm.sh/docs/topics/chart_repository/#github-pages-example
- https://helm.sh/docs/howto/chart_releaser_action/#helm
- https://github.com/marketplace/actions/helm-chart-releaser

[Helm](https://helm.sh) must be installed to use the charts.  Please refer to
Helm's [documentation](https://helm.sh/docs) to get started.

Once Helm has been set up correctly, add the repo as follows:

  helm repo add <alias> https://kbumsik.io/keycloak-kubernetes

If you had already added this repo earlier, run `helm repo update` to retrieve
the latest versions of the packages.  You can then run `helm search repo
<alias>` to see the charts.

To install the <chart-name> chart:

    helm install my-<chart-name> <alias>/<chart-name>

To uninstall the chart:

    helm delete my-<chart-name>
