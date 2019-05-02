# CNAB Bundle with Porter - Spring Music Demo App

This project is a sample CNAB bundle that is created and managed by Porter. https://porter.sh 

This bundle uses two mixins to access your Azure subscription. These values need to be updated in the porter.yaml.

* The `exec` mixin uses an Azure Service Principal to access via the CLI.
* The `azure` mixin uses ARM and requires the subscription and tenant info. 

### Prerequisites

- Porter on local machine. http://porter.sh
- Docker on local machine (eg - Docker for Mac)
- Bash
- Azure service principal with rights to create a RG, AKS, Cosmos, etc. 

    ```bash
    az ad sp create-for-rbac --name ServicePrincipalName
    ```

    More details here: https://docs.microsoft.com/en-us/cli/azure/create-an-azure-service-principal-azure-cli?view=azure-cli-latest 

- Follow the process in the porter/duffle docs to add these credentials in your config.


### Build / Install this bundle

* Setup duffle credentials
* Porter

```bash
porter build

porter install -c test1 --insecure
```