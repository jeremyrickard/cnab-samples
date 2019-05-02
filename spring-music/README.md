# Spring Music Demo App with Azure Cosmos DB

## Prerequistes

- Azure Kubernetes Service  (AKS) is already installed

## Install this bundle

```bash
duffle build .

duffle credentials generate foo -f bundle.json --insecure
duffle credential generate azure spring-music
# enter values for clientid, pwd, sub, tenant

duffle install --credentials=azure3 spring-music spring-music:0.1.0
```


## Considerations for future iterations of this bundle
