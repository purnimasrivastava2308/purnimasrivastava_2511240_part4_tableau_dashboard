# Part 4: Tableau Dashboard

## Business Problem Summary

Retail leadership needs an executive dashboard to monitor sales performance, profitability, customer segments, category performance, shipping performance, discount impact, and return patterns. The goal is to identify business opportunities and risks using a clear decision-focused dashboard.

## Dataset Description

- Source file: `data/dashboard_sales_data.xlsx`
- Main sheet: `dashboard_sales_data`
- Rows: 4,200
- Date range: 2024-01-01 to 2025-12-31
- Key fields: `order_id`, `order_date`, `ship_date`, `customer_segment`, `region`, `state`, `city`, `category`, `sub_category`, `ship_mode`, `sales`, `quantity`, `discount`, `profit`, `return_flag`, `delivery_days`, `customer_rating`, and `campaign_channel`

## Tableau Workbook Description

The packaged Tableau workbook is saved as `tableau/executive_dashboard.twbx`. It is intended to include an executive dashboard and supporting sheets for sales trends, regional performance, category profitability, customer segment performance, shipping performance, discount impact, and return analysis.

## Calculated Fields Created

- Profit Margin: `SUM([Profit]) / SUM([Sales])`
- Cost: `[Sales] - [Profit]`
- Average Order Value: `SUM([Sales]) / COUNTD([Order ID])`
- Return Rate: `SUM([Return Flag]) / COUNTD([Order ID])`
- Shipping Delay Bucket: groups delivery days into meaningful delivery-speed buckets such as fast, moderate, and delayed

## Dashboard Components

- Sales trend view
- Regional performance view
- Category profitability view
- Customer segment view
- Shipping performance view
- Discount vs profit view
- Return analysis view
- KPI cards for total sales, total profit, profit margin, order count, and return rate

## Filters And Interactions Used

Suggested dashboard filters include Region, Category, Customer Segment, Order Date, Ship Mode, and Campaign Channel. The dashboard should also include at least one action/filter interaction so leadership can click a chart element and filter related views.

## Key Business Insights

- Total sales are 217,017,651.92 and total profit is 33,306,312.84.
- Overall profit margin is 15.35%.
- South is the highest-sales and highest-profit region.
- Technology is the strongest profit category.
- Home Office is the highest-value customer segment.
- Heavy discounts above 30% are associated with negative profit.
- Standard Class carries the largest sales volume but has the slowest average delivery time.
- Furniture has the highest return rate at 7.67%.

## Dashboard Story Summary

The dashboard story shows that the business has strong sales and profit scale, but leadership should balance growth with margin discipline. The main opportunities are Technology products, South-region practices, Home Office customers, and organic demand. The main risks are heavy discounting, Furniture returns, and slower Standard Class delivery.

## Assumptions And Limitations

- The dashboard is based on historical order data and does not automatically prove causation.
- Return analysis uses `return_flag` as the return indicator.
- Delivery performance uses `delivery_days`.
- Campaign performance is summarized by `campaign_channel`, but full marketing cost is not available.
- Screenshots should be captured from Tableau after final dashboard review.

## Screenshots Included

- `screenshots/full_dashboard.png`
- `screenshots/sales_trend_view.png`
- `screenshots/regional_performance_view.png`
- `screenshots/category_profitability_view.png`
- `screenshots/filter_interaction_view.png`
