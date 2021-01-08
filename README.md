Executes a workflow on a Cloudify deployment.

# Environment Variables

This Action uses the Cloudify Profile environment variables described in the official
Cloudify documentation (see [More Information](#more-information) below).

# Inputs

(Certain commonly-used inputs are documented in our official website; see [More Information](#more-information) below)

| Name | Description
|------|------------
| `workflow` | The ID of the workflow to execute
| `parameters-file` | Path to YAML/JSON containing workflow parameters
# Example

```yaml
jobs:
  test_job:
    steps:
      - name: Execute installation workflow
        uses: cloudify-cosmo/execute-workflow-action@v1.1
        with:
          environment-name: "my-environment"
          workflow: "install"
          parameters-file: "install-params.json"
```

# More Information

Refer to [Cloudify CI/CD Integration](https://docs.cloudify.co/latest/working_with/integration/) for additional information about
Cloudify's integration with CI/CD tools.
