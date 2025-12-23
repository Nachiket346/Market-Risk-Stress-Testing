
Objective:
Quantify tail risk (99% VaR) under baseline and stressed market conditions.
Design thematic stress scenarios capturing AI bubble dynamics.
Measure incremental capital impact under each stress.


Process & Methodology
1. Portfolio Construction
Five-equity portfolio (tech-heavy exposure).
Daily log returns computed from historical prices.
Portfolio returns aggregated using fixed portfolio weights.

2. Baseline Risk Measurement
Historical 99% one-day VaR.
Serves as reference capital requirement.

3.Stress Scenario Design (AI Bubble Burst)
Each scenario is economically motivated and reflects real-world risk transmission channels:

| Scenario                         | Risk Channel              | Stress Design                                |
| -------------------------------- | ------------------------- | -------------------------------------------- |
| **Systemic Crash (AI Bubble)**   | Broad market repricing    | −2% daily shock for 5 days                   |
| **AI Leaders Collapse**          | Concentration risk        | −4% daily shock for AI-heavy stocks (5 days) |
| **Volatility Scaling (+60%)**    | Uncertainty & repricing   | Portfolio volatility scaled by 1.6×          |
| **Correlation Spike (ρ = 0.85)** | Diversification breakdown | Cross-asset correlation stress               |


4. Capital Impact Assessment
Recomputed stressed 99% VaR for each scenario.
Measured Δ Capital vs Baseline.
Compared severity and risk drivers across scenarios.


Tech Stack:
Python.
NumPy.
Pandas.
Matplotlib.
Jupyter Notebook.

Results
| Scenario                     | 99% VaR | Δ Capital vs Baseline |
| ---------------------------- | ------- | --------------------- |
| Baseline                     | 0.0466  | 0.0000                |
| Systemic Crash (AI Bubble)   | 0.0559  | +0.0093               |
| AI Leaders Collapse          | 0.0559  | +0.0093               |
| Volatility Scaling (+60%)    | 0.0746  | +0.0280               |
| Correlation Spike (ρ = 0.85) | 0.0523  | +0.0057               |


Intepretation:
Stress Scenario Impact vs Baseline VaR
The baseline portfolio exhibits a 99% one-day VaR of 4.66%, representing the expected tail loss under normal market conditions. Stress scenarios linked to an AI bubble burst materially increase tail risk, highlighting vulnerabilities to systemic shocks, concentration risk, volatility amplification, and correlation breakdown.

Baseline (Reference Case)
99% VaR: 4.66%
Reflects historical market dynamics without forward-looking stress.
Serves as the capital benchmark for incremental stress impact.

Scenario 1: Systemic Crash (AI Bubble Burst)
Stressed 99% VaR: 5.59%
Δ Capital vs Baseline: +0.93%
Impact: ~20% increase in tail risk
Interpretation:
A broad market repricing triggered by an AI bubble burst leads to a sharp increase in portfolio tail losses. the uniform stress across all equities captures systemic risk, indicating that diversification benefits materially weaken during AI-driven market sell-offs.

Scenario 2: AI Leaders Collapse (Tech Concentration Risk)
Stressed 99% VaR: 5.59%
Δ Capital vs Baseline: +0.93%
Impact: Comparable to systemic crash
Interpretation:
Despite being sector-specific, concentrated losses in AI-heavy names generate VaR levels similar to a full market crash. this highlights concentration and factor exposure risk, where losses in large-cap AI leaders propagate to the overall portfolio through correlation and weighting effects.

Scenario 3: Volatility Scaling (+60%)
Stressed 99% VaR: 7.46%
Δ Capital vs Baseline: +2.80%
Impact: ~60% increase in tail risk (largest impact)
Interpretation:
Volatility amplification is the most severe risk channel. elevated uncertainty around AI earnings, positioning, and leverage leads to significantly fatter tails. This scenario demonstrates that volatility risk dominates capital requirements, consistent with regulatory stress frameworks and crisis-period observations.

Scenario 4: Correlation Spike (ρ = 0.85)
Stressed 99% VaR: 5.23%
Δ Capital vs Baseline: +0.57%
Impact: ~12% increase in tail risk
Interpretation:
Rising cross-asset correlations reduce diversification benefits, increasing portfolio risk even without large price shocks. this scenario captures contagion and market crowding effects, commonly observed during systemic de-risking events.


Future Enhancements:
Expected Shortfall (ES) stress capital.
Rolling (time-varying) stressed VaR.
Liquidity-adjusted VaR.
FRTB risk factor mapping (Equity General / Equity Specific).
Scenario weighting & reverse stress testing.
Integration with VaR backtesting (UC / CC) under stressed forecasts.

Key Takeaways:
Volatility risk is the dominant driver of stressed capital, exceeding both systemic and concentration shocks.
Sector-specific AI concentration risk can be as severe as a broad market crash.
Correlation breakdowns materially erode diversification, increasing tail risk even in moderate price moves.
Stress results highlight the importance of forward-looking scenario analysis beyond historical VaR.


