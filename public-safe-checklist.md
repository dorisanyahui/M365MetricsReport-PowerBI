# Microsoft 365 Reporting and Cloud Metrics Automation Public-Safe Checklist

Use this before publishing any version of the original solution to GitHub.

## Do not publish directly

Do not upload the original `M365_1_0_0_2.zip` file to a public repository.

The package contains private organization details, including:

- Power BI workspace identifiers
- Power BI report and dataset identifiers
- SharePoint site and folder paths
- Excel workbook and table identifiers
- internal reporting metrics and environment references

## Minimum cleanup actions

Before publishing anything derived from this project:

1. Remove the raw export package from the public repo.
2. Replace real workspace IDs, dataset IDs, report IDs, workbook IDs, and SharePoint paths with placeholders.
3. Blur screenshots that show real tenant data, report contents, or internal metrics.
4. Describe the reporting workflow without exposing production configuration.
5. Sanitize any sample CSV or PDF content before sharing it publicly.

## Safe replacement examples

Use replacements like these in docs and diagrams:

- `workspace-id-placeholder`
- `dataset-id-placeholder`
- `report-id-placeholder`
- `https://tenant.sharepoint.com/sites/M365Reporting`
- `excel-workbook-id-placeholder`

## Safe portfolio materials

These are usually appropriate to publish:

- rewritten README content
- architecture diagrams
- redacted screenshots
- sanitized CSV examples
- explanations of the reporting workflow and collected metrics

## Best public framing

Instead of exposing the original configuration, describe the project like this:

> Built a Power Automate reporting solution that exports a Power BI Microsoft 365 report to PDF, extracts licensing data to CSV, stores outputs in SharePoint, and appends weekly cloud metrics into an Excel table for historical tracking.
