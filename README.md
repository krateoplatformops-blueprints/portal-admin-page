# _Admin Page_ Blueprint
The Admin Page Blueprint provides a ready-to-use page to monitor Krateo and its resources. This Blueprint includes a Helm chart to help you bootstrap your own Krateo Composable Portal experience.

## What It Does
This blueprint deploys a new menu option that offers control over Krateo functionalities, allowing you to avoid the terminal. The pages include:
- Krateo's status page;
- Blueprints available in the cluster;
- Installed blueprints;
- Local users and permissions;
- FinOps notebooks.

## Install the Helm Chart

Install the Blueprint:

```sh
helm install <name> portal-admin-page \
  --repo https://marketplace.krateo.io \
  --namespace <krateo-namespace> \
  --set portalBlueprintPage.installCompositionDefinition=<true|false> \
  --version 1.0.2
  --wait
```

The admin-page **must** be installed in the Krateo Namespace. If you install using Helm, then you must set `.Values.global.krateoNamespace` to the Krateo namespace.
