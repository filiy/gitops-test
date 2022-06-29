# Introduction
Cluster GitOps Configuration

# Standards
## Namespaces naming conventions
- Every namespace created by us should start with the prefix `ircc-`. This is to ensure that in the future when we deployed on SSC cluster, that we allowed cluster administrator to easily see what belongs to IRCC
- The `ircc-` prefix should be followed by the team, tenant or function (in that order).  For example: `integration`, `journeylab`.
- The team, tenant, or function is to be followed by the application this relates to. Example, `cumulus`, `prdi`

Example:
`ircc-integration-cumulus` - Would run application deployed by the `integration` team for the `cumulus` application
`ircc-journeylab-prdi` - Would run application deployed by the `journeylab` team for the `prdi` application
`ircc-eso-sandbox-joe-smith` - Would run application deployed by the `eso` team to allow Joe Smith to have a sandbox.
`ircc-integration-amq-broker` - Would run application deployed by the `integr
