# SailPoint Saas Connectivity GitHub Action

This GitHub Action builds and uploads your saas connector to your Identity Security Cloud tenant
by adding a step to your workflow.

```yaml
- name: Build and Upload Connector
  uses: sailpoint-oss/upload-saas-connector@v1
  with:
    connector-alias: 'my-project'
    base-url: ${{ env.SAIL_BASE_URL }}
    client-id: ${{ env.SAIL_CLIENT_ID }}
    client-secret: ${{ env.SAIL_CLIENT_SECRET }}
```

This GitHub Action builds and uploads your saas connector to your Identity Security Cloud tenant
by adding a step to your workflow. This block uses `node-version` and `cli-version` to overwrite the defaults.

```yaml
- name: Build and Upload Connector
  uses: sailpoint-oss/upload-saas-connector@v1
  with:
    node-version: '20'
    cli-version: 2.1.4
    connector-alias: 'my-project'
    base-url: ${{ env.SAIL_BASE_URL }}
    client-id: ${{ env.SAIL_CLIENT_ID }}
    client-secret: ${{ env.SAIL_CLIENT_SECRET }}
```
