# CNAB Bundle with Porter - Spring Music Demo App

This project is a sample CNAB bundle that is created and managed by Porter. https://porter.sh 

### Pre-requisites

This bundle uses two mixins to access your Azure subscription. These values need to be updated in the porter.yaml.

* The `exec` mixin uses an Azure Service Principal to access via the CLI.
* The `azure` mixin uses ARM and requires the subscription and tenant info. 

Create an Azure service principal: 

```bash
az ad sp create-for-rbac --name brians-unique-service-principal
```

Follow the process in the porter/duffle docs to add these credentials in your config.