# Monte-Carlo-Portfolio-Risk-Simulator
Monte Carlo Wealth Planner: Portfolio Risk & Withdrawal Simulation (Excel)
Project Overview
This project uses Monte Carlo simulation in Microsoft Excel to explore how a mixed portfolio of equities and government bonds may evolve over a 10-year planning horizon under uncertain equity returns and recurring withdrawals.
The workbook contains a single 10-year projection path and a 1,000-trial simulation table of terminal wealth outcomes. It is designed as a personal-finance and portfolio-risk learning project—not as an investment recommendation.
Project Objectives
Model a portfolio allocated between equities and government bonds.
Introduce uncertainty in annual equity returns using a normal random variable.
Estimate the distribution of wealth remaining after 10 years.
Illustrate how recurring withdrawals can affect long-term wealth.
Summarize simulated terminal outcomes using the average and standard deviation.
Model Inputs
The workbook's current example assumptions are:
Input	Value
Initial wealth	2,000,000
Expected annual government-bond return	4%
Expected annual equity return	12%
Equity return standard deviation	30%
Equity allocation	40%
Government-bond allocation	60%
Annual withdrawal	200,000
Donation input	1,000,000
Projection horizon	10 years
Simulation trials	1,000
Note: The donation amount is present as an input in the workbook but is not currently connected to the wealth calculations.
Methodology
For each year:
Beginning wealth is split between equities and government bonds according to the selected allocation.
A standard-normal random draw is generated for the equity return.
The equity return is modeled as:
`Equity return = Expected equity return + (Standard normal draw × Equity return standard deviation)`
The equity and bond holdings grow at their respective modeled returns.
The annual withdrawal is deducted from year-end wealth to determine the next year's starting wealth.
The workbook's terminal wealth output is the wealth remaining after the withdrawal in Year 10. The simulation table uses Excel's What-If Analysis Data Table mechanism to generate 1,000 terminal-wealth outcomes, with average and standard deviation summary cells.
How to Use
Download and open the `.xlsx` workbook in desktop Microsoft Excel.
Edit the input assumptions in the input section.
Allow Excel to recalculate the workbook. The random draws and simulation results can change when recalculation occurs.
Review the 10-year projection and the 1,000-trial terminal wealth results.
Compare how different return, volatility, allocation, and withdrawal assumptions change the simulated outcomes.
> The workbook uses Excel functions and a What-If Analysis Data Table. Compatibility and recalculation behavior may differ in Google Sheets, LibreOffice, or other spreadsheet applications.
Outputs
Annual wealth progression for a 10-year scenario.
Simulated terminal-wealth outcomes across 1,000 trials.
Average simulated terminal wealth.
Standard deviation of simulated terminal wealth.
Validation Notes & Limitations
The core allocation arithmetic is consistent with the stated equity allocation: the remaining portfolio is assigned to government bonds.
Equity returns are modeled with a normal distribution; bond returns are assumed fixed at the specified rate.
The withdrawal is deducted at the end of each year, including Year 10.
The donation input is not applied in the current formulas. Add a clearly defined donation timing and cash-flow treatment if it should affect the projection.
The model assumes a constant asset allocation and does not include rebalancing costs, taxes, inflation, fees, changing bond prices, or correlations between multiple risky asset classes.
A normal distribution can generate equity returns below -100%, which can produce unrealistic negative asset values in extreme simulated cases. Consider adding a return floor or adopting a different return model, while documenting the choice.
A single 1,000-trial run may be noisy. Increase the number of trials and compare results for stability before drawing conclusions.
Results are scenario-based and depend heavily on the assumptions. They are not forecasts or guarantees of future investment performance.
Tools & Concepts
Microsoft Excel · Monte Carlo Simulation · Portfolio Allocation · Equity Return Modeling · Risk Analysis · Wealth Planning · Scenario Analysis · What-If Data Tables
Disclaimer
This workbook is for educational and analytical purposes only. It is not financial advice, and simulated outcomes do not guarantee actual investment results.
