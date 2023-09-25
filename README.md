# Istio Gateway and Virtual Service Configurations

This repository contains Kubernetes manifest files for configuring an Istio Gateway and Virtual Service. These configurations are used to expose applications within a Kubernetes cluster to the internet via the Istio Ingress Gateway.

### Note: This setup assumes that you have an Istio Ingress Gateway in place already for your Kubernetes cluster. To see how to setup, please refer to Istio Official Documentation.

## Table of Contents

- [Introduction](#introduction)
- [Manifest Files](#manifest-files)
- [Usage](#usage)
- [Customization](#customization)
- [Contributing](#contributing)
- [License](#license)

## Introduction

When using Istio as a service mesh, you may need to expose your services to external traffic. This repository provides pre-configured Kubernetes manifest files for creating an Istio Gateway and Virtual Service, enabling you to expose your applications securely and efficiently.

## Manifest Files

- `gateway.yaml`: Defines the Istio Gateway resource, which serves as the entry point for external traffic into the cluster.
- `virtual-service.yaml`: Configures the Istio Virtual Service resource, which defines how traffic should be routed to specific services within the cluster.

## Usage

To use these manifest files to expose your applications, follow these steps:

1. Clone this repository to your local machine.
   ```
   git clone https://github.com/radeeka/istio-ingress-setup-kubernetes.git
   ```

2. Change into the cloned directory.
   ```
   cd istio-ingress-setup-kubernetes
   ```

3. Review the `gateway.yaml` and `virtual-service.yaml` files and customize them to match your specific application and domain requirements. Modify hostnames, paths, and service references as needed.

4. Apply the configurations to your Kubernetes cluster:
   ```
   kubectl apply -f gateway.yaml
   kubectl apply -f virtual-service.yaml
   ```

5. Monitor the status of your Istio Gateway and Virtual Service to ensure they are correctly configured and serving traffic:
   ```
   kubectl get gateway
   kubectl get virtualservice
   ```

## Customization

You can customize the manifest files according to your application's requirements. Be sure to consult the [Istio documentation](https://istio.io/docs/) for detailed information on Istio Gateway and Virtual Service configuration options.

## Contributing

We welcome contributions to enhance and improve these Istio configurations. If you encounter issues or have suggestions, please open an issue or submit a pull request following our [contribution guidelines](CONTRIBUTING.md).

## License

This project is licensed under the [MIT License](LICENSE), which means you are free to use, modify, and distribute the configurations as per the terms of the license.
