# Data Dictionary — Executive Sales & Profitability Dashboard

**Author:** Ajim Mujavar  
**Project:** Executive Sales & Profitability Dashboard  
**Visualization Tool:** Tableau Desktop

## 1. Purpose

This document explains the business measures, dimensions, KPIs, filters, and validation considerations relevant to the Executive Sales & Profitability Dashboard.

It is intended to help viewers understand the meaning of the fields used in the dashboard and how they support business analysis.

**Important:** Field names and definitions below are examples commonly used in sales analytics. Confirm them against the actual dataset and Tableau workbook. Remove any fields that are not present.

## 2. Dataset Information

| Attribute | Description |
|---|---|
| Dataset Name | Enter the actual dataset name |
| Data Source | Enter the original source or provider |
| Reporting Period | Enter the actual date range |
| Data Granularity | Specify what one row represents |
| Last Refreshed | Enter the actual refresh date |
| Visualization Tool | Tableau Desktop |
| Workbook File | Executive_Sales_Dashboard_Final.twbx |

Do not publish private source information or datasets that you are not authorized to share.

## 3. Measures

Measures are quantitative fields that can be aggregated and analyzed.

| Field | Business Meaning | Typical Calculation |
|---|---|---|
| Sales | Monetary value of sales transactions | SUM(Sales), if appropriate for the source |
| Profit | Profit value associated with transactions | SUM(Profit), if defined in the source |
| Quantity | Number of units sold | SUM(Quantity) |
| Order ID | Identifier for an order | COUNTD(Order ID) for distinct orders |
| Profit Margin | Profit as a proportion of sales | SUM(Profit) / SUM(Sales), when appropriate |

### Measure Notes

- Confirm the source definition of sales and profit.
- Specify the currency used in the dashboard.
- Confirm whether the dashboard displays raw values, thousands, or millions.
- Use distinct order counts when the goal is to count unique orders and the source provides a suitable order identifier.
- Handle zero or missing sales values when calculating profit margin.

Profit margin is commonly calculated as:

`Profit Margin = Total Profit / Total Sales`

Format the result as a percentage when appropriate. Confirm the actual Tableau calculation before using this definition.

## 4. Dimensions

Dimensions describe categories or attributes used to group, filter, and compare measures.

| Field | Business Meaning | Analytical Use |
|---|---|---|
| Order Date | Date associated with an order or transaction | Trend analysis and date filtering |
| Region | Geographic business region | Regional sales comparison |
| State / Province | Geographic subdivision | Detailed geographic analysis |
| Country | Country associated with a transaction | Geographic mapping |
| Category | Broad product classification | Category performance |
| Sub-Category | More detailed product classification | Product comparison |
| Segment | Customer or market segment | Segment performance |
| Product Name | Name or identifier of a product | Product-level analysis |
| Customer ID | Customer identifier | Customer analysis, where appropriate |
| Order ID | Order identifier | Order-level analysis |

Use only fields available in the actual data source. Check geographic roles and locations before interpreting map visualizations.

## 5. KPI Definitions

Document the exact KPIs displayed in the finished dashboard.

| KPI | Definition | Unit / Format |
|---|---|---|
| Total Sales | Total sales for the selected records | Actual currency |
| Total Profit | Total profit for the selected records | Actual currency |
| Total Quantity | Total units represented by the selected records | Units |
| Total Orders | Number of distinct orders, if implemented that way | Count |

These are example KPI definitions. Replace or remove entries to match the actual KPI cards in the dashboard.

### KPI Validation

For every KPI, confirm:

1. The field or calculated field used.
2. The aggregation method.
3. The effect of dashboard filters.
4. The number format and displayed unit.
5. Agreement between the dashboard and the source data.

## 6. Dashboard Filters

Document only the filters present in the final workbook.

| Filter | Purpose | Configuration |
|---|---|---|
| Date | Limits the reporting period | Record the actual field and default range |
| Region | Selects geographic regions | Record available values |
| Category | Selects product categories | Record available values |
| Segment | Selects customer segments | Record available values |
| Other Filters | Additional dashboard filters | Document as applicable |

Filters may affect multiple worksheets differently depending on their Tableau configuration. Verify that the intended charts respond consistently.

## 7. Geographic Analysis

Geographic visualizations may use fields such as Country, State, Province, or Region.

Before interpreting a map:

- Confirm that geographic fields are assigned the correct geographic roles.
- Check for unknown or unmatched locations.
- Verify that the map represents the intended measure.
- Ensure that filters are applied as expected.
- Avoid treating missing geographic records as zero sales.

## 8. Data Quality Considerations

The following checks are recommended before publishing:

- Identify missing values in important dimensions and measures.
- Investigate duplicate records.
- Confirm the granularity of the dataset.
- Check whether orders appear on multiple rows.
- Validate sales and profit calculations.
- Confirm date ranges and currency formats.
- Verify the behavior of dashboard filters.
- Reconcile KPI totals against the underlying dataset.

## 9. Assumptions and Limitations

The meaning of each metric depends on the original data source and business definitions.

Potential limitations include:

- Missing or incomplete records.
- Incomplete geographic coverage.
- Different levels of data granularity.
- Incorrectly configured aggregations.
- Unrefreshed data extracts.
- Differences between row-level ratios and ratios calculated from totals.

Document any limitations actually identified in the dataset. Do not state that validation has been completed unless it has been performed.

## 10. Privacy and Data Sharing

Before publishing the workbook or its data:

- Confirm permission to share the dataset.
- Check whether a packaged workbook includes an embedded data extract.
- Remove confidential business information.
- Avoid exposing customer-identifying information.
- Verify that the data source license permits redistribution.

## 11. Maintenance

Update this document whenever the dataset, calculations, filters, or KPI definitions change.

| Version | Date | Change |
|---|---|---|
| 1.0 | Enter publication date | Initial data dictionary template |

---

**Maintained by Ajim Mujavar**  
Part of the Executive Sales & Profitability Dashboard portfolio project.