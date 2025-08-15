# PyPSA Analysis of Solar Subsidy Removal on Interstate Power Dispatch

## 🔎 Overview
This project models and analyzes the impact of solar transmission subsidies on the energy dispatch between Indian states, specifically Karnataka and Maharashtra, using the [PyPSA](https://pypsa.org/) framework. It simulates generation, transmission, and total system costs under scenarios **with and without** solar transmission subsidies.

## 📌 Objectives
- Model hourly power dispatch using PyPSA.
- Incorporate a ₹0.4/kWh solar transmission tariff representing post-June 2025 policy changes.
- Analyze system costs, energy flows, and renewable utilization.
- Compare subsidy vs non-subsidy scenarios.

## 🏗️ Methodology
- **States considered**: Karnataka and Maharashtra (optionally Kerala).
- **Technologies**: Solar and coal-based generation.
- **Demand**: Fixed hourly demand per state.
- **Scenarios**:
  - With Solar Transmission Subsidy (no tariff)
  - Without Subsidy (₹400/MWh transmission tariff)
- **Simulation Period**: Hourly resolution for 1 day and 1 year.

## 📊 Key Results
| Scenario        | Total System Cost (₹) | Solar Flow (MW) | Coal Flow (MW) |
|----------------|------------------------|------------------|-----------------|
| With Subsidy   | 550,464,480            | ↑ More           | ↓ Less          |
| Without Subsidy| 590,064,000            | ↓ Less           | ↑ More          |

- **Subsidy leads to higher solar usage**, displacing costly coal generation.
- **Total system cost reduces** due to lower marginal cost of solar and avoided coal dispatch.
- **Interstate flows adjust** depending on tariff, impacting generator dispatch.

## 🧠 Insights
- Introducing a solar transmission fee discourages cross-border renewable exchange.
- Policy mechanisms significantly affect renewable energy penetration.
- Simulations offer data-driven justification for or against implementing such tariffs.

## 🛠️ Requirements
- Python 3.8+
- [`pypsa`](https://github.com/PyPSA/PyPSA)
- `pandas`, `numpy`, `matplotlib`

Install via:
```bash
pip install pypsa pandas numpy matplotlib
````

## 🚀 Run the Simulation

Run the base simulation:

```bash
jupyter nbconvert --to notebook --execute inter_state_transmission.ipynb
```



## 📁 Files

* `inter_state_transmission.ipynb` – Main simulation script.
* `README.md` – Project overview.
* `results.pdf` – PDF file explaining the results.



## 📄 License

[MIT License](LICENSE)

## 📬 Contact

For questions or feedback, feel free to reach out.

```
