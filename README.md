# API-Driven Financial Planning for Credit Union Members: Enhancing Budgets and Retirement with Fintech Tools
This project aims to create two financial analysis tools for members of a large credit union. The first tool is designed to assess monthly budgets to assist in emergency fund planning, while the second is to forecast retirement portfolio performance. The emergency fund planner will evaluate cryptocurrency holdings and stock/bond portfolios to ascertain if members possess sufficient savings. In the retirement planner, historical data and Monte Carlo simulations will be leveraged to forecast portfolio growth over a 30-year period. Furthermore, a shorter-term retirement plan with a 10-year horizon will be explored, adjusting asset allocations accordingly.

## Objectives:
- Develop a financial planner for emergencies to help credit union members assess their savings for an emergency fund.
- Create a financial planner for retirement to forecast portfolio performance over 30 years using Monte Carlo simulations.
- Evaluate a shorter-term retirement plan with a 10-year horizon by adjusting asset allocations and running new Monte Carlo simulations.
- Provide clear and actionable insights to credit union members based on the analysis conducted.

## Methodology:
#### Evaluation of Cryptocurrency Wallet:
- The average monthly household income for credit union members was established.
- The Requests library retrieved current Bitcoin (BTC) and Ethereum (ETH) prices from API endpoints.
- The value of each member's cryptocurrency wallet was calculated based on their current holdings.

#### Assessment of Stock and Bond Holdings:
- An environment file (.env) was created to securely store the Alpaca API key and secret key.
- The Alpaca SDK was used to retrieve the current closing prices of the SPDR S&P 500 ETF Trust (SPY) and the iShares Core US Aggregate Bond ETF (AGG).
- The value of the stock and bond portions of each member's portfolio was calculated based on their current holdings.

#### Evaluation of Emergency Fund Adequacy:
- A Python list containing the total value of the cryptocurrency wallet and the stock and bond portions of the portfolios was created.
- The list was used to create a Pandas DataFrame named savings_df to visualize the composition of each member's portfolio.
- A pie chart was plotted to illustrate the portfolio composition and determine whether it had sufficient funds to create an emergency fund equivalent to three times the member's monthly income.

#### Creation of Monte Carlo Simulation (30-Year Horizon):
- The Alpaca API was utilized to obtain 3 years of historical closing prices for a traditional 60/40 portfolio (stocks/bonds).
- A Monte Carlo simulation with 500 samples over 30 years was run to forecast portfolio growth.
- The results, including the probability distribution and confidence interval, were plotted, and summary statistics for the simulation were generated.

#### Analysis of Retirement Portfolio Forecasts:
- Lower and upper bounds for the expected portfolio value with a 95% confidence interval were determined.
- Forecasting Cumulative Returns in 10 Years:
  - Asset allocations were adjusted to 20% bonds and 80% stocks for a shorter-term retirement plan.
  - A new Monte Carlo simulation with 500 samples over 10 years was conducted.
  - Lower and upper bounds for the expected portfolio value with a 95% confidence interval were determined, and the feasibility of retiring after 10 years with a more heavily weighted stock portfolio was assessed.

## Further Implications & Significance 
In summary, these financial analysis tools mark a significant step forward in empowering credit union members to make informed financial decisions. By using API technology and advanced analytics, these tools provide valuable insights into emergency fund readiness and retirement planning. Beyond immediate benefits, they promote financial literacy and foster responsible financial habits, ultimately enhancing community financial well-being. As technology advances, these tools are vital in guiding individuals toward their long-term financial goals.
