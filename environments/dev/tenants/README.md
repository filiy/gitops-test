# Introduction
Contains an application for each tenant you want to on-board in this environment 

# Promotion thru the environment
In the dev environment, each application will likely be pointing to HEAD. In all other environment, we recommend that you point the application to a specific tag of the repository that you create before promote a tenant to any higher environment than DEV.

Worth nothing that deployment informat
# Usuage of a tenant
To add a tenant to an environment, you would create the folder:
`environment/xxx/tenants`
where xxx is the environment (dev) for example.  That folder would contain one application per tenant to be added.
Each application would point to the kustomization at the root of the specific tenant folder.

