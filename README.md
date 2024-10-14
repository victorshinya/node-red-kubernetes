# Node-RED on Kubernetes

This project demonstrates how to deploy and run Node-RED on a Kubernetes cluster. Node-RED is a powerful, open-source flow-based development tool for visual programming, and Kubernetes provides a robust platform for container orchestration.

## Table of Contents

1. [Prerequisites](#prerequisites)
2. [Installation](#installation)
3. [Usage](#usage)
## Prerequisites

Before you begin, ensure you have the following installed:

- Kubernetes cluster (local or cloud-based)
- kubectl CLI tool
- Docker (for building custom images, if needed)

## Installation

1. Clone this repository:

```bash
git clone https://github.com/yourusername/node-red-kubernetes.git
cd node-red-kubernetes
```

2. Apply the Kubernetes manifests:

```bash
kubectl apply -f deploy-node-red.yml
```

This will create the necessary deployments, services, and other resources for Node-RED.

## Usage

1. Access the Node-RED editor:

```bash
kubectl get services
```

Find the external IP or LoadBalancer address for the Node-RED service and open it in your web browser.

2. Start creating your flows in the Node-RED editor.

3. To view logs:

```bash 
kubectl logs -f deployment/node-red
```

## LICENSE

Copyright 2024 Victor Shinya

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.