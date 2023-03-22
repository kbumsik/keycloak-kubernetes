# Helm Chart for Keycloak Operator

This is a Helm chart for the Keycloak Operator. This is based on the official
[Keycloak Operator](https://github.com/keycloak/keycloak-k8s-resources/tree/main/kubernetes) manifests.

We publish this chart because Keycloak maintainers decided to not publish it to the official Helm repository, as seen in [this issue](https://github.com/keycloak/keycloak/issues/16210).

This chart features:

- The latest Quarkus distribution of Keycloak only (Keycloak 20 and above), no support for the legacy Wildfly distribution.
- Strictly follows [the official k8s manifests for Keycloak Operator](https://github.com/keycloak/keycloak-k8s-resources). We try to keep the chart as close as possible to the original manifests.

For guides on how to use this chart, please refer to the [Keycloak official documentation](https://www.keycloak.org/guides#operator).
