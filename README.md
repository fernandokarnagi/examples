# Helm Example Repository

Ahoy world! I'm a Helm repository for example charts.

## Get started

### Prepare the HELM Chart in the Repo

![image](https://github.com/fernandokarnagi/examples/assets/15156095/97dfa4ca-f84e-41d6-b332-d57c51641463)

Important files:
* Chart.yaml
* Values.yaml
* templates/*.yaml

### Prepare the GitHub page to store the Helm

Create gh-pages branch for this page

![image](https://github.com/fernandokarnagi/examples/assets/15156095/2017c17f-80d6-4f36-86a5-9d204249545d)

Configure the GitHub page

![image](https://github.com/fernandokarnagi/examples/assets/15156095/f2808081-adf6-4b08-8bb6-b58a5a74964d)

### Prepare GitHub Action for the Helm Chart update

![image](https://github.com/fernandokarnagi/examples/assets/15156095/4aa978ed-d65d-40e9-81a3-ce802c9906f9)

The following screenshot shows an example of the Action execution.

![image](https://github.com/fernandokarnagi/examples/assets/15156095/8e40b3e7-5469-44d8-97e0-b0a04899a724)

### Add Helm Chart into Repo

Add the Helm Chart into the local Repo in K8S

```
helm repo add fernandohello https://fernandokarnagi.github.io/examples
```

### Release this Helm

```
helm install fernandohello fernandohello/hello-world --debug
```

### Upgrade Helm Chart

If there is any upgrade to the Helm Chart, run this command

```
helm repo update
```

### Update Helm Release Configuration

If you need to update the Helm values / configurations, run this command

```
helm upgrade fernandohello fernandohello/hello-world --set image.tag=1.25.4 --set replicaCount=4
```
