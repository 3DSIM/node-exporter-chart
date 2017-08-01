# node-exporter-chart
Helm chart to deploy a node exporter service which can be used for scraping Prometheus metrics from each node in a kubernetes cluster.

# Helm
We are using Helm along with Quay.io to host our Helm charts.  See https://github.com/app-registry/appr-helm-plugin and https://coreos.com/blog/quay-application-registry-for-kubernetes.html.

See https://docs.helm.sh for more about Helm.

# Prerequisites
* Kubernetes 1.4+ with Beta APIs enabled
* [Helm Registry plugin](https://github.com/app-registry/appr-helm-plugin)

# Installing this chart
To install with release name `my-release` run:
```
helm registry install quay.io/3dsim/node-exporter --name=my-release
```

# Uninstalling the Chart

To uninstall/delete the my-release deployment:
```
helm delete my-release
```
The command removes all the Kubernetes components associated with the chart and deletes the release.


# Customizing this chart
See [values.yaml](values.yaml) for configuration options.

Use `--set` syntax to set a value:
```console
helm registry install quay.io/3dsim/node-exporter --name=my-release --set resources.limits.cpu=300m
```

Alternatively, a YAML file that specifies the values for the parameters can be provided while installing the chart. For example,

```console
helm registry install quay.io/3dsim/node-exporter --name=my-release -f values.yaml
```

