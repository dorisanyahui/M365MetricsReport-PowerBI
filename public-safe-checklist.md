# Microsoft 365 Metrics Export and Reporting Automation Public-Safe Checklist

Use this before publishing any version of the original solution to GitHub.

## Do not publish directly

Do not upload the original `M365_1_0_0_3.zip` file to a public repository.

The package contains private organization details, including:

- Power BI workspace identifiers
- Power BI report and dataset identifiers
- SharePoint site and folder paths
- Excel workbook and table identifiers
- Microsoft Graph export configuration
- Azure Resource Graph export configuration
- SharePoint control-list definitions for enabled exports
- Azure Key Vault secret references
- internal reporting metrics and environment references

## Minimum cleanup actions

Before publishing anything derived from this project:

1. Remove the raw export package from the public repo.
2. Replace real workspace IDs, dataset IDs, report IDs, workbook IDs, and SharePoint paths with placeholders.
3. Replace real Graph endpoints, Azure Resource Graph queries, group IDs, and export configuration values with placeholders.
4. Blur screenshots that show real tenant data, report contents, control-list rows, or internal metrics.
5. Describe the reporting workflow without exposing production configuration.
6. Sanitize any sample CSV, JSON, or PDF content before sharing it publicly.

## Safe replacement examples

Use replacements like these in docs and diagrams:

- `workspace-id-placeholder`
- `dataset-id-placeholder`
- `report-id-placeholder`
- `https://tenant.sharepoint.com/sites/M365Reporting`
- `excel-workbook-id-placeholder`
- `https://graph.microsoft.com/v1.0/reports/<report-name>`
- `resource-graph-query-placeholder`

## Safe portfolio materials

These are usually appropriate to publish:

- rewritten README content
- architecture diagrams
- redacted screenshots
- sanitized CSV examples
- sanitized JSON examples
- explanations of the reporting workflow and collected metrics

## Best public framing

Instead of exposing the original configuration, describe the project like this:

> Built a Power Automate reporting solution that exports Microsoft 365 reporting outputs from Power BI, Microsoft Graph, and Azure Resource Graph, stores files in SharePoint, and appends weekly cloud metrics into an Excel table for historical tracking.
