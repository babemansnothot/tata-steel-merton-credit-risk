TATA STEEL — STRUCTURAL CREDIT RISK ANALYSIS

A Merton model implementation in Python, with credit risk stress scenarios visualised in Tableau.


PROJECT OBJECTIVE

Estimate Tata Steel’s asset value, asset volatility and one-year risk-neutral default probability, and examine how these change under equity-market stress.


METHODOLOGY

• Calculated annualised equity volatility from historical daily log returns.
• Calculated equity market value using the closing share price and historical shares outstanding.
• Numerically solved the Merton equity-value and volatility equations.
• Recalibrated the model under price and volatility stress scenarios.
• Presented the results in a Tableau dashboard.


KEY FINDINGS

Base case:
• Estimated asset value: ₹319,293.78 crore
• Estimated asset volatility: 22.88%
• Risk-neutral distance to default: 5.93

Combined stress — share price falls 30% and equity volatility rises 50%:
• Risk-neutral distance to default falls to 3.49.
• One-year risk-neutral default probability rises to approximately 0.0243%.

The combined shock increases model-implied risk more than the price-only scenarios. Default probability remains low in absolute terms under the stated assumptions.


TOOLS

Python: pandas, NumPy, SciPy, Matplotlib and yfinance
Analysis environment: Jupyter Notebook
Visualisation: Tableau Public


PROJECT FILES

• tata_steel_merton.ipynb — Python model and analysis
• tata_steel_scenarios.csv — Exported scenario results
• <img width="1198" height="797" alt="image" src="https://github.com/user-attachments/assets/a056a0c7-5cc8-4cb9-b87b-69f12c27970f" />
 — Tableau dashboard preview


DATA SOURCES

Historical share prices:
Yahoo Finance via yfinance — TATASTEEL.NS

Financial statements:
Tata Steel FY2025–26 Consolidated Financial Statements
Note 19: Historical share count
Note 41: Current and non-current borrowings

https://www.tatasteel.com/investors/integrated-report-2025-26/pdf/Consolidated.pdf


ASSUMPTIONS AND LIMITATIONS

• Retrospective analysis using the 30 March 2026 closing price and 31 March 2026 financial-statement inputs.
• Financial statements were published after the valuation date.
• Borrowings are approximated as a single payment due in one year.
• Lease liabilities are excluded.
• The risk-free rate is an illustrative 6%, continuously compounded.
• The basic Merton model assumes no asset payouts.
• Parent equity and consolidated borrowings approximate the group as a single firm; subsidiary claims are not modelled separately.
• Stress scenarios are hypothetical.
• Risk-neutral probabilities are model estimates, not forecasts of actual default.


PROJECT STATUS

Working prototype. Historical risk-free-rate validation and final documentation remain in progress. Results are provisional.


AUTHOR

Santhosh Raghavendran Rao
Model implementation, financial analysis and Tableau dashboard.
