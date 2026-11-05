# Project Risk Simulator

A Monte Carlo simulation that estimates how likely a project is to go over budget or over time, based on its risks.

**Try it:** https://AishahAbdulHakeem.github.io/Monte-Carlo-Simulation/nontechnical_report.html

## What it does

You enter a project budget, a timeline, and a list of risks. The simulator plays the project out 10,000 times. In each run, every risk either happens or doesn't, and if it does, its cost and delay are drawn between your low, most likely and high values. The results show:

- the chance of going over budget, over the deadline, or over either
- how likely the project is to stay under each cost and each delay
- which risks add the most expected cost

## How to use the web version

1. Open the link above.
2. Set your budget and timeline.
3. Edit the risk table, or upload a filled-in `Risk_Register_Template.xlsx`.
4. Click **Run simulation**.

For each risk, enter:

| Field | Meaning |
|---|---|
| Chance (%) | How likely the risk is (per year or per project, your choice) |
| Cost low / most likely / high | Dollar impact if it happens |
| Delay low / most likely / high | Days of delay if it happens |

Values like `310000`, `310K` and `2.1M` all work.

## Python and Colab version

`Monte_Carlo_Simulation.ipynb` is the same simulation in Python for Google Colab. Upload your risk register, set the budget and timeline in the first cell, and click **Runtime > Run all**.

## Files

| File | Purpose |
|---|---|
| `nontechnical_report.html` | The web simulator (no installation needed) |
| `Monte_Carlo_Simulation.ipynb` | Python version for Google Colab |
| `Risk_Register_Template.xlsx` | Blank risk register template |

## Example

The page loads with a sample scenario based on the 2026 Canvas data breach: a $1,000,000 budget, a 3-month (90-day) timeline, and seven cyber risks.

## Notes

- The web version runs entirely in your browser. Nothing you enter is sent anywhere.
- Delays are added one after another, which is a cautious assumption.
- Yearly chances are scaled to the project length. For example, 32% per year becomes about 9% over 90 days.
- Results are only as good as the risk estimates you enter.

## Credits

Built for a project management course at Morgan State University.
