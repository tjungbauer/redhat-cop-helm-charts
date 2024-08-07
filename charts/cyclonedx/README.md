

# cyclonedx

  [![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

  ![Version: 1.0.7](https://img.shields.io/badge/Version-1.0.7-informational?style=flat-square)

 

  ## Description

  A Helm chart to deploy CycloneDX to generate SBOM

CycloneDX provides advanced, supply chain capabilities for cyber risk reduction. We are using the Software Bill of Material (SBOM) parts.
SBOM is a complete and accurate inventory of all first-party and third-party components is essential for risk identification.

This chart will install CycloneDX BOM Repo server, which enables you to store SBOM inventories on your cluster.

For detailed information check: [CycloneDX SBOM](https://cyclonedx.org/capabilities/sbom/)

For an example of how to use it during a pipeline run check: [Generating an SBOM](https://blog.stderr.at/securesupplychain/2023-06-22-securesupplychain-step7/)

## Dependencies

This chart has the following dependencies:

| Repository | Name | Version |
|------------|------|---------|
| https://redhat-cop.github.io/helm-charts | tpl | ~1.0.0 |

It is best used with a full GitOps approach such as Argo CD does. For example, https://github.com/tjungbauer/openshift-clusterconfig-gitops

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| tjungbauer | <tjungbau@redhat.com> | <https://blog.stderr.at/> |

## Sources
Source:

Source code: https://redhat-cop.github.io/helm-charts/tree/main/charts/cyclonedx

## Parameters

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| namespace.create | bool | false | Create Namespace yes or not |
| namespace.name | string | `"cyclonedx"` | Name of the Namespace |

## Example values

```yaml
---
namespace:
  create: true
  name: cyclonedx
```

## Installing the Chart

To install the chart with the release name `my-release`:

```console
helm install my-release repo/<chart-name>>
```

The command deploys the chart on the Kubernetes cluster in the default configuration.

## Uninstalling the Chart

To uninstall/delete the my-release deployment:

```console
helm delete my-release
```

The command removes all the Kubernetes components associated with the chart and deletes the release.

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.12.0](https://github.com/norwoodj/helm-docs/releases/v1.12.0)
