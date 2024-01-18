# helm-charts

## Usage

1. Add or update a Helm chart: push your source code of Helm chart under `charts/<your chart>`
1. New release will be created by [GitHub Actions](https://github.com/hyperter96/helm-charts/blob/main/.github/workflows/release.yaml) (e.g. https://github.com/hyperter96/helm-charts/releases/tag/vnp-0.1.0)
1. Add this helm chart repo to your helm client configuration
    ```
    helm repo add hyperter96 https://hyperter96.github.io/helm-charts
    helm repo update
    ```
1. Update repo and search
    ```
    helm search repo hyperter96
    NAME                     	CHART VERSION	APP VERSION	DESCRIPTION
    hyperter96/atwan/vnp    	0.1.0        	v1.16.0     A Helm chart for Kubernetes
    ```
1. Install
    ```
    helm install vnp hyperter96/atwan/vnp
    ```
1. Upgrade (optional)
    ```
    helm upgrade vnp hyperter96/atwan/vnp --set xxx=aaa
    ```
1. Uninstall
    ```
    helm uninstall vnp
    ```

## Setup

follow [chart-releaser Action](https://github.com/marketplace/actions/helm-chart-releaser#pre-requisites)