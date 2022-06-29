# Introduction
Cluster GitOps Configuration

# Standards

## Namespaces naming conventions
- Every namespace deployed by the OpenShift software should, as much as possible, keep the OpenShift prefix to the namespace. Example: `openshift-dns`, `openshift-infra`
- Every namespace created by us should start with the prefix `ircc-`. This is to ensure that in the future when we deployed on SSC cluster, that we allowed cluster administrator to easily see what belongs to IRCC
- The `ircc-` prefix should be followed by the team, tenant or function (in that order of preference).  For example: `integration`, `journeylab`. If there is no team, or tenant, in some case this can be omitted.
- The team, tenant, or function is to be followed by the application this relates to. Example, `cumulus`, `prdi`

Example:
- `ircc-integration-cumulus` - Would run application deployed by the `integration` team for the `cumulus` application
- `ircc-journeylab-prdi` - Would run application deployed by the `journeylab` team for the `prdi` application
- `ircc-eso-sandbox-joe-smith` - Would run application deployed by the `eso` team to allow Joe Smith to have a sandbox.
- `ircc-integration-amq-broker` - Would run the AMQ Broker application deployed by the `integration` team for their need
- `ircc-monitoring` - Would run `monitoring` software for all tenants and team
- `openshift-dns` - DNS software installed by openshift

## Tenants
A Tenant is a team, a group, a group of groups, or a Line of Business, working on one or more related application.

## Tagging and reference
When working in a dev environment, try to point everything to the Main branch as much as possible on HEAD.  When promoting to higher environment, use meaningful tag to point to specific point in time in the repository. The tagging is on top of any possible environment overlays which will be applied to the base, which may vary in the main branch.
