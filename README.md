# ShardingSphere on Cloud

**Apache ShardingSphere Official Website:** [https://shardingsphere.apache.org/](https://shardingsphere.apache.org/)

[![GitHub release](https://img.shields.io/github/release/SphereEx/shardingsphere-on-cloud.svg)](https://github.com/apache/shardingsphere-on-cloud/releases)
[![License](https://img.shields.io/badge/license-Apache%202-4EB1BA.svg)](https://www.apache.org/licenses/LICENSE-2.0.html)
[![Twitter](https://img.shields.io/twitter/url/https/twitter.com/ShardingSphere.svg?style=social&label=Follow%20%40ShardingSphere)](https://twitter.com/ShardingSphere)
[![Slack](https://img.shields.io/badge/%20Slack-ShardingSphere%20Channel-blueviolet)](https://join.slack.com/t/apacheshardingsphere/shared_invite/zt-sbdde7ie-SjDqo9~I4rYcR18bq0SYTg)
[![Gitter](https://badges.gitter.im/shardingsphere/shardingsphere.svg)](https://gitter.im/shardingsphere/Lobby)

This repository collects scripts, tools, manifests and documentations, and provides a home for [Apache ShardingSphere](https://shardingsphere.apache.org/) on cloud solutions.

The solutions currently included in this project are:

* [The ShardingSphere Helm Charts](https://github.com/apache/shardingsphere-on-cloud/tree/main/charts/shardingsphere-proxy)
* [The ShardingSphere Operator](https://github.com/apache/shardingsphere-on-cloud/tree/main/shardingsphere-operator)

## Current Status

Currently, either the [ShardingSphere Helm Charts](https://github.com/apache/shardingsphere-on-cloud/tree/main/charts/shardingsphere-proxy) and the [ShardingSphere Operator](https://github.com/apache/shardingsphere-on-cloud/tree/main/shardingsphere-operator) make up the latest version as (5.2.0) of ShardingSphere Proxy. Refer and follow the Quick Start guide to get up and running. 

* [The ShardingSphere Helm Charts QuickStart](#quick-start)
* [The ShardingSphere Operator QuickStart](#quick-start-1)

## ShardingSphere Helm Charts

ShardingSphere Helm Charts uses [Helm](https://helm.sh/) to provide guidance for the installation of a ShardingSphere-Proxy instance in a Kubernetes cluster.


### Requirements

* [Kubernetes 1.18+]()
* [kubectl](https://kubernetes.io/docs/reference/kubectl/)
* [Helm 3.2.0+](https://helm.sh/)
* [StorageClass](https://kubernetes.io/docs/concepts/storage/storage-classes/) of [PV (Persistent Volumes)](https://kubernetes.io/docs/concepts/storage/persistent-volumes/) can be dynamically applied for persistent data (Optional)

### Quick Start

Please follow these [instructions](./doc/shardingsphere-helm-charts.md) to deploy a ShardingSphere cluster with version 5.2.0.

## ShardingSphere Operator

The ShardingSphere Operator uses predefined CustomResourceDefinitions for describing an Apache ShardingSphere Deployment on Kubernetes.

### Requirements

With the help of ShardingSphere-Operator you can create a ShardingSphere-Proxy cluster including the ZooKeeper cluster in minutes.

For installation of SharingSphere-Operator, you will need a Kubernetes cluster. No matter it is a managed Kubernetes service like AWS EKS or self-hosted Kubernetes, or just a mini-kube, you can easily install ShardingSphere-Operator with respective [ShardingSphere Operator Helm Charts](https://github.com/SphereEx/shardingsphere-on-cloud/tree/main/charts/shardingsphere-operator), and apply the manifests in [ShardingSphere Operator Cluster Helm Charts](https://github.com/SphereEx/shardingsphere-on-cloud/tree/main/charts/shardingsphere-operator-cluster) describing the expected Apache ShardingSphere deployment. **Kubernetes 1.18+ is recommended**. 

### Internal Architecture

![img.png](./doc/images/ss-operatorIA.png)

### Current Status

Minimum Viable Product

### Quick Start 

Please follows [instructions](./doc/shardingsphere-operator.md) to deploy a ShardingSphere cluster with version 5.2.0.

### Features

* Supports the use of proxy to configure and describe the shardingsphere-proxy cluster. For detailed configuration, see the deployment documentation.
* Support native shardingsphere proxy server.yaml configuration. For specific support items, please refer to the documentation
* Support automatic creation of HPA based on CPU metrics.
* Support automatic download of MySQL driver.

### Installation

#### Helm

* ShardingSphere-Operator chart
    * Support deploy shardingsphere operator.
* ShardingSphere-Cluster chart
    * Support deploy shardingsphere proxy cluster.
    * Support deploy Zookeeper by bitnami.
    * Support automatic configuration of the address of the governance center.
    * Use github pages to host repositories and support helm repo add to add repositories.

### Development Requirements

To build ShardingSphere Operator from scratch you will need to install the following tools:

* [Git](https://git-scm.com/)
* [Golang 1.17](https://golang.org/dl/)
* [make](https://www.gnu.org/savannah-checkouts/gnu/make/make.html)
* [Kubernetes 1.20+](https://github.com/kubernetes/kubernetes)
* [Kubebuilder 3.4.1+](https://github.com/kubernetes-sigs/kubebuilder)

## Contributing

To contribute to this project, refer to [Contributing](CONTRIBUTING.md).

## Community & Support

<hr>

:link: [Mailing List](https://shardingsphere.apache.org/community/en/contribute/subscribe/). Best for: Apache community updates, releases, changes.

:link: [GitHub Issues](https://github.com/apache/shardingsphere-on-cloud/issues). Best for: larger systemic questions/bug reports or anything development related.

:link: [GitHub Discussions](https://github.com/apache/shardingsphere-on-cloud/discussions). Best for: technical questions & support, requesting new features, proposing new features.

:link: [Slack channel](https://join.slack.com/t/apacheshardingsphere/shared_invite/zt-sbdde7ie-SjDqo9~I4rYcR18bq0SYTg). Best for: instant communications and online meetings, sharing your applications.

:link: [Twitter](https://twitter.com/ShardingSphere). Best for: keeping up to date on everything ShardingSphere.


## License

Apache License 2.0, see [LICENSE](https://github.com/SphereEx/shardingsphere-on-cloud/blob/main/LICENSE).
