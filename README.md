German Electricity Consumption Analysis (Python, SQL & Power BI)
End-to-end data analytics project examining hourly German electricity consumption, grid load, residual load, and pumped hydro demand across the German power grid (Jan–Oct 2026, 6,575 hourly records).

![Power BI Dashboard](dashboard%20preview.png)

Business Questions Answered:
What are the monthly trends and peaks in total German grid load and residual load?

How does pumped-storage hydro demand scale alongside regular industrial and residential electricity consumption?

Technical Workflow
Data Scrubbing (Python / Pandas): Corrected Windows-1252 encoding, stripped semicolon/comma numeric separators, cleaned and standardized column headers into snake_case, parsed timestamps into datetime64, and cast consumption metrics into clean floating-point numbers (float64).

Data Querying & Auditing (SQLite): Loaded scrubbed records into a local in-memory sqlite3 database, cutting timestamps with strftime() and running monthly aggregations (SUM, AVG, GROUP BY, ORDER BY) to verify data integrity prior to visualization.

Visualization (Power BI Desktop): Built an executive 1-page dashboard featuring KPI cards for headline demand metrics, a clustered bar chart for load breakdown, and chronological monthly line charts.

Key Insights
Grid Demand Volatility: Total monthly grid load hovers between 35M and 46M MWh through the first three quarters of 2026, driven by industrial and seasonal baseloads.

Pumped-Storage Role: Pumped-storage hydro accurately captures peak charging cycles, maintaining stable base adjustments relative to overall residual demand curves.
