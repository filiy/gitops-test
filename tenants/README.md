# Introduction
Cluster level tenant specific artifacts required by different teams using the cluster. 

# Structure of a tenant
Most tenant will follow the same structure
/base/
    00-gitops - Contains their own ArgoCD installation to sync up their application information
    01-namespaces - All the namespaces they need
    02-operators - Operators they might want
    03-argocd/apps - All the application they will have in their own ArgoCD repo.  Usually one per namespace.

/xxx/ (where xxx is an environment that extends the base)
    01-namespaces - Any additional namespaces required on a specific environment
    03-argocd/app - Add new ArgoCD apps required for environment specific namespaces
    kustomization.yaml (will patch the ArgoCD apps in the base to point them to the right env)

# Usuage of a tenant
To add a tenant to an environment, you would create the folder:
`environment/xxx/tenants`
where xxx is the environment (dev) for example.  That folder would contain one application per tenant to be added.

