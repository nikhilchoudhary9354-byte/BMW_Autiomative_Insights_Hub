# BMW Automotive Insights Hub

A project where I built a small MCP (Model Context Protocol) server that lets an LLM query BMW sales data by region and car model, and get back a summary report.

## What it does

- Generates simulated BMW sales data (order id, date, car model, region, price, units sold) for about a year
- Sets up an MCP server (`BMW Sales Assistant`) with one tool: `get_bmw_sales_summary`
- The tool can filter sales by region and/or car model, then returns:
  - Top performing region (most cars sold)
  - Lowest performing region
  - A detailed region-wise breakdown (total cars sold, total revenue)
- Tests the tool with a few different filters (region, no filter, invalid region) to check it works
- Plots revenue by region and revenue by car model as bar charts

## How to run

1. Clone this repo
2. Install the libraries:
   ```
   pip install pandas numpy matplotlib seaborn "mcp<2.0.0"
   ```
3. Run `BMW_Automotive_Insights_Hub.ipynb` in Jupyter or Google Colab

## Sample Output

```
Top Performing Region: Asia-Pacific (311 cars sold, Revenue: $27,544,288.63)
Lowest Performing Region: Middle East (236 cars sold, Revenue: $20,438,120.94)
```

## Notes

- The sales data used here is randomly generated (simulated), not real BMW sales data. This project is meant to show how an MCP tool/server can be built and connected to a dataset, not to make real business claims.
- MCP is the protocol some AI tools (like Claude) use to let an LLM call functions/tools with structured inputs, so this project is basically me learning how to expose a dataset as a callable tool for an LLM.

## Tech Used

Python, Pandas, NumPy, Matplotlib, Seaborn, MCP (Model Context Protocol)

## Author

Nikhil Choudhary
[LinkedIn](https://linkedin.com/in/nikhilchoudhary) | [GitHub](https://github.com/nikhilchoudhary9354-byte)
