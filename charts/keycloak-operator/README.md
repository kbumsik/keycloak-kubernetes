# Helm Chart for Keycloak Operator

This is a Helm chart for the Keycloak Operator. This is based on the official
[Keycloak Operator](https://github.com/keycloak/keycloak-k8s-resources/tree/main/kubernetes) manifests.

We publish this chart because Keycloak maintainers decided to not publish it to the official Helm repository, as seen in [this issue](https://github.com/keycloak/keycloak/issues/16210).

This chart features:

- The latest Quarkus distribution of Keycloak only (Keycloak 20 and above), no support for the legacy Wildfly distribution.
- Strictly follows [the official k8s manifests for Keycloak Operator](https://github.com/keycloak/keycloak-k8s-resources). We try to keep the chart as close as possible to the original manifests.

## Documentation

For guides on how to use this chart, please refer to the [Keycloak official documentation](https://www.keycloak.org/guides#operator).

## Notes

- This is an operator chart. It does not deploy Keycloak itself. You need to create a `Keycloak` custom resource to deploy Keycloak.
- Currently the operator watches only the namespace where the operator is installed. This is the limitation of the original (official) Keycloak Operator manifests. See the [official documentation](https://www.keycloak.org/operator/installation) for more details.

## Usage

- Add repository

```bash
helm repo add keycloak-operator https://kbumsik.io/keycloak-kubernetes/
```

- Install chart

```bash
helm install my-keycloak-operator --namespace my-keycloak keycloak-operator/keycloak-operator
```
