# Introduction
Cluster level tenant specific artifacts required by different teams using the cluster. 

# Structure of a tenant
Most tenant will follow the same structure
00-gitops - Contains their own ArgoCD installation to sync up their application information
01-namespaces - All the namespaces they need
02-operators - Operators they might want
03-argocd/apps - All the application they will have in their own ArgoCD repo.  Usually one per namespace.

# Usuage of a tenant
To add a tenant to an environment, you would create the folder:
`environment/xxx/tenants`
where xxx is the environment (dev) for example.  That folder would contain one application per tenant to be added.
Each application would point to the kustomization at the root of the specific tenant folder.

