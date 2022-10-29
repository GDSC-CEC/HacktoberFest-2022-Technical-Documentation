# Kubernetics - Kubernetes for Humans Technical Documentation

## Introduction

Kubernetics is a project to make Kubernetes easier to use for humans. It is a set of tools and libraries that make it easier to use Kubernetes. It is not a replacement for Kubernetes, but rather a set of tools that make it easier to use Kubernetes.

## Installation

### Prerequisites

Kubernetics requires the following to be installed:

* [kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/)
* [helm](https://helm.sh/docs/intro/install/)

### Installing Kubernetics

Kubernetics is available as a helm chart in the [Kubernetics Helm Repository](https://kubernetics.github.io/helm-repo/). To install it, run the following command:

```bash
helm repo add kubernetics https://kubernetics.github.io/helm-repo/
helm install kubernetics kubernetics/kubernetics
```

## Usage

### Kubernetics CLI

The Kubernetics CLI is a command line interface for interacting with Kubernetes. It is a wrapper around `kubectl` and `helm` that makes it easier to use Kubernetes.

#### Commands

The following commands are available:

* `kubernetics get` - Get information about Kubernetes resources
* `kubernetics create` - Create Kubernetes resources
* `kubernetics delete` - Delete Kubernetes resources
* `kubernetics apply` - Apply Kubernetes resources
* `kubernetics exec` - Execute a command in a container
* `kubernetics logs` - Get logs from a container
* `kubernetics port-forward` - Forward a port to a container
* `kubernetics proxy` - Run a proxy to the Kubernetes API server
* `kubernetics version` - Print the version of Kubernetics
* `kubernetics help` - Print help information

#### Examples

The following are some examples of using the Kubernetics CLI:

```bash
# Get information about pods
kubernetics get pods

# Get information about pods in a specific namespace
kubernetics get pods --namespace my-namespace

# Get information about pods in a specific namespace in YAML format

kubernetics get pods --namespace my-namespace -o yaml

# Get information about pods in a specific namespace in JSON format

kubernetics get pods --namespace my-namespace -o json

# Get information about pods in a specific namespace in JSON format and pretty print it

kubernetics get pods --namespace my-namespace -o json | jq .

# Get information about pods in a specific namespace in JSON format and pretty print it and filter it

kubernetics get pods --namespace my-namespace -o json | jq '.items[] | {name: .metadata.name, namespace: .metadata.namespace}'

# Create a pod from a YAML file

kubernetics create -f my-pod.yaml

# Create a pod from a YAML file in a specific namespace

kubernetics create -f my-pod.yaml --namespace my-namespace

# Delete a pod from a YAML file

kubernetics delete -f my-pod.yaml

# Delete a pod from a YAML file in a specific namespace

kubernetics delete -f my-pod.yaml --namespace my-namespace

# Apply a pod from a YAML file

kubernetics apply -f my-pod.yaml

# Apply a pod from a YAML file in a specific namespace

kubernetics apply -f my-pod.yaml --namespace my-namespace

# Execute a command in a container

kubernetics exec my-pod --namespace my-namespace -- ls -l

# Get logs from a container

kubernetics logs my-pod --namespace my-namespace

# Forward a port to a container

kubernetics port-forward my-pod --namespace my-namespace 8080:80

# Run a proxy to the Kubernetes API server

kubernetics proxy

# Print the version of Kubernetics

kubernetics version
```

### Kubernetics UI

The Kubernetics UI is a web application for interacting with Kubernetes. It is a wrapper around the Kubernetics CLI that makes it easier to use Kubernetes.

#### Usage

To use the Kubernetics UI, run the following command:

```bash
kubernetics ui
```

This will start a web server on port 8080. You can access the web application at [http://localhost:8080](http://localhost:8080).

## Contributing

### Prerequisites

Kubernetics requires the following to be installed:

* [Node.js](https://nodejs.org/en/download/)

### Installing

To install the project, run the following commands:

```bash
git clone
cd kubernetics
npm install
```

### Building

To build the project, run the following command:

```bash
npm run build
```

### Testing

To test the project, run the following command:

```bash

npm run test

```

### Linting

To lint the project, run the following command:

```bash

npm run lint

```

### Releasing

To release the project, run the following command:

```bash

npm run release

```

## Author

[Palak](https://github.com/palak461)