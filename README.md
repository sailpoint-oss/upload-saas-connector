# SailPoint Saas Connectivity GitHub Action

This GitHub Action builds and uploads your saas connector to your Identity Security Cloud tenant
by adding a step to your workflow.

## Usage

### Basic Usage

```yaml
- name: Build and Upload Connector
  uses: sailpoint-oss/upload-saas-connector@v1
  with:
    connector-alias: 'my-project'
    base-url: ${{ env.SAIL_BASE_URL }}
    client-id: ${{ env.SAIL_CLIENT_ID }}
    client-secret: ${{ env.SAIL_CLIENT_SECRET }}
```
### Advanced Usage

This GitHub Action builds and uploads your saas connector to your Identity Security Cloud tenant
by adding a step to your workflow. This block uses `node-version` and `cli-version` to overwrite the defaults.

```yaml
- name: Build and Upload Connector
  uses: sailpoint-oss/upload-saas-connector@v1
  with:
    node-version: '20'
    python-version: '3.10'
    cli-version: 2.1.4
    connector-alias: 'my-project'
    base-url: ${{ env.SAIL_BASE_URL }}
    client-id: ${{ env.SAIL_CLIENT_ID }}
    client-secret: ${{ env.SAIL_CLIENT_SECRET }}
```
## Inputs

- node-version: Node.js version (default: '18')
- python-version: Python version (default: '3.10')
- cli-version: The version of the SailPoint CLI to use (default: 2.1.5)
- connector-alias: The alias of the connector to upload (required)
- base-url: The base URL of the Identity Security Cloud Tenant (required)
- client-id: The client ID of the Identity Security Cloud Tenant (required)
- client-secret: The client secret of the Identity Security Cloud Tenant (required)