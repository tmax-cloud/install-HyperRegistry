# install-HyperRegistry

## Prerequisites
* Kubernetes, Helm3

## Purpose
* For operating Tmax Cloud's Public image registry on HCDC

## Installation

1. Add HyperRegistry Chart Museum 
    ```bash
	  helm repo add HyperRegistry https://tmax-cloud.github.io/HyperRegistry-Chart/
	  ```

2. Install Chart
   ```bash
   helm install HyperRegistry HyperRegistry/HyperRegistry --set expose.type=ingress,expose.ingress.hosts.core=core.${ingressControllerExternalIp}.nip.io,expose.ingress.hosts.notary=notary.${ingressControllerExternalIp}.nip.io
    ```

3. Checkout HyperRegistry Dashboard
    * ```https://core.${ingressControllerExternalIp}.nip.io```