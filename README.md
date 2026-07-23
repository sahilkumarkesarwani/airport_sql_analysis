# Airport Flights SQL Analysis Project

A SQL-driven analysis of a U.S. domestic flights dataset, translating raw flight records into actionable business insights on route performance, capacity utilization, seasonal trends, and year-over-year growth.

## Overview

Airlines and airport authorities need more than raw flight logs — they need answers to concrete operational questions: which routes are underperforming, when does demand peak, and where is capacity being wasted? This project uses MySQL to work through **13 business problem statements** on a real flights dataset, then translates the query results into specific, actionable recommendations.

![Query results screenshot](./Screenshot%202026-06-21%20002755.png)

## Dataset

**Table:** `airports`

| Column | Description |
|---|---|
| `Origin_airport` | Code of the departure airport |
| `Destination_airport` | Code of the arrival airport |
| `Origin_city` | City of departure |
| `Destination_city` | City of arrival |
| `Passengers` | Number of passengers on the route |
| `Seats` | Number of seats available |
| `Flights` | Number of flights operated |
| `Distance` | Distance flown (miles) |
| `Fly_date` | Date of the flight record |
| `Origin_population` | Population of the origin city |
| `Destination_population` | Population of the destination city |
| `Org_airport_lat` / `Org_airport_long` | Origin airport coordinates |
| `Dest_airport_lat` / `Dest_airport_long` | Destination airport coordinates |

## Tools & Techniques

- **MySQL** — querying, aggregation, and analysis
- **SQL techniques applied:** `GROUP BY`, `HAVING`, window functions (`ROW_NUMBER`, `LAG`), CTEs (`WITH`), `CASE` statements, date functions (`YEAR`, `MONTH`)

## Business Problems Solved

The analysis is organized into 13 business problem statements, each addressing a specific operational question:

| # | Problem Statement | Business Purpose |
|---|---|---|
| 1 | Total passengers per origin–destination pair | Identify most frequented routes |
| 2 | Average seat utilization per route | Measure occupancy efficiency |
| 3 | Top 5 routes by passenger volume | Spot highest-demand routes |
| 4 | Total flights & passengers per origin city | Evaluate city-level travel activity |
| 5 | Total distance flown per origin airport | Forecast fuel demand and operational reach |
| 6 | Monthly/yearly flight, passenger & distance trends | Detect seasonal patterns |
| 7 | Routes with passenger-to-seat ratio ≤ 0.5 | Flag underutilized capacity |
| 8 | Top 10 busiest origin airports by flight frequency | Identify high-traffic hubs |
| 9 | Top contributing cities to Bend, OR traffic | Understand feeder-city demand |
| 10 | Longest flight routes by distance | Assess long-haul service opportunities |
| 11 | Busiest and least busy months across years | Reveal peak vs. lean travel seasons |
| 12 | YoY passenger growth % per route | Track route-level demand trends |
| 13 | YoY growth % in total flights & passengers | Assess overall annual industry growth |

Full SQL code for all 13 queries is in [`airport_sql_project.sql`](./airport_sql_project.sql).

## Key Insights & Recommendations

**1. Route Optimization and Realignment**
- Reduce flight frequency or capacity on underperforming routes with declining passenger trends.
- Invest in expanding capacity on routes showing consistent year-over-year growth.

**2. Enhance Seat Utilization**
- Realign aircraft sizes to better match passenger demand on low-utilization routes.
- Implement dynamic pricing and targeted promotions to fill more seats, particularly on off-peak flights.

**3. Leverage Seasonal Demand**
- Use historical peak-month data to increase flight frequency or deploy larger aircraft during high-demand periods.
- Tailor marketing campaigns to attract passengers during peak seasons to maximize capacity use.

**4. Maximize Long-Distance Route Efficiency**
- Prioritize routes with the longest average distance and significant passenger volume for efficient resource allocation.
- Explore opportunities to introduce additional services on high-demand, long-haul routes.

## How to Run

1. Set up a MySQL instance and create the `airport_db` database.
2. Load the flights dataset into the `airports` table (ensure column names match those listed above).
3. Run the queries in `airport_sql_project.sql` sequentially, problem by problem.
4. Review the output of each query against its corresponding business question for insights.

## Future Improvements

- Add sample output rows/screenshots next to each query so insights are visible without running the SQL locally
- Build a lightweight dashboard (Power BI/Tableau/Excel) on top of key query outputs to visualize trends
- Add an ERD or schema diagram for the `airport_db` database
- Parameterize a few queries (e.g., top-N routes by city) so they're reusable beyond the specific examples given

## Conclusion

This project demonstrates how SQL can be used end-to-end — from raw transactional flight data to strategic business recommendations — covering aggregation, ratio analysis, time-series trends, and year-over-year growth calculations using window functions and CTEs.

## Author

**Sahil Kumar Kesarwani**
[GitHub](https://github.com/sahilkumarkesarwani)
