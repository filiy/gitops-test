# Introduction
Cluster level tenant specific artifacts required by different teams using the cluster. 
For example, a team will likely need a set of namespaces, there own gitops-operator installation, etc. 
in order to deploy their work.

Usually you will see in the environment/xxx/tenants folder a kustomization that will grab which tenants is on which environment.
