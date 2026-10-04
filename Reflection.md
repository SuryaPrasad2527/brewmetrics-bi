# Reflection

Developing the BrewMetrics BI project with GitHub Copilot was different from building a normal Power BI lab as a single report file. Copilot was useful during DAX development because it could quickly suggest the structure of measures and recommend functions such as `CALCULATE`, `DATEADD`, `FILTER`, and `RANKX`. The suggestions provided a useful starting point, particularly when creating time-based calculations and ranking measures.

However, the generated DAX still needed to be reviewed rather than being accepted automatically. I had to check whether the suggested calculations matched the star schema and whether they worked correctly with the relationships between the fact and dimension tables. I also made changes where necessary so that calculations responded appropriately to report filters and used the correct dimension columns.

The version-controlled workflow changed how I approached the project. Instead of treating the Power BI report as one finished file, I had to think about each stage as a separate development step. The repository progressed from the initial setup to the star schema, then individual DAX measures, followed by the dashboard and documentation. This made each change more deliberate because the commit history provided a record of how the solution was developed.

Overall, Copilot reduced the time needed to create initial DAX solutions, while Git and GitHub made the BI development process more structured, traceable, and reviewable.
