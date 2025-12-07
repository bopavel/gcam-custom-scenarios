# GCAM Results – Canada Decarbonization Scenarios

This folder contains the results and figures for the GCAM runs. We compare three scenarios for Canada with a focus on 2050:

- **Reference** – no additional climate policy (middle-of-the-road socioeconomic and technological assumptions).
- **Carbon Constraint (Cap)** – annual CO₂ emissions constrained via `carbon_cap.xml` (determine carbon price based on prescribed emissions pathway).
- **Carbon Tax (Tax)** – exogenous carbon price path via `carbon_tax_25_5_mod.xml` (another way to incorporate policy perspectives).

All runs use GCAM 7.0 (`gcam-v7.0`) with updated configuration files
`configuration_ref_upd.xml`, `configuration_cap_upd.xml`, and `configuration_tax_upd.xml`.

![](https://github.com/bopavel/gcam-custom-scenarios/blob/25d4bf6367d3822f7c6e1f691b67a4a751c8c8be/results-figures/figures/fig_mk1_01.png)

---

## 1. CO₂ emissions by region (Canada)

The first set of figures shows CO₂ emissions for Canada in the three scenarios.

![CO₂ emissions by region: Canada – GCAM interface](https://github.com/bopavel/gcam-custom-scenarios/blob/e7e9130dd9b52b1c37680d0abb494fecc627de0f/results-figures/figures/fig_mk1_02.png)

We then export the data to Excel and plot the trajectories:

![CO₂ emissions by region: Canada – Reference vs Cap vs Tax](https://github.com/bopavel/gcam-custom-scenarios/blob/e7e9130dd9b52b1c37680d0abb494fecc627de0f/results-figures/figures/fig_mk1_03.png)

**Key insight:**  
- Reference: emissions peak around 2030 and barely decline by 2050.
- Cap: emissions drop sharply after 2025 and approach near-zero levels by 2050.
- Tax: emissions decline steadily but less aggressively than under the cap.

---

## 2. Where do CO₂ reductions come from? (Sector breakdown)

We use *CO₂ emissions by sector (no bio) (excluding resource production)* to
identify which sectors contribute most to reductions in 2050.

First, using “Cement” and “Iron and Steel” as examples, we observe emission reductions from 2025 onward in both carbon constraint and carbon tax scenarios.

![CO₂ emissions by sector: Cement and Iron & Steel](https://github.com/bopavel/gcam-custom-scenarios/blob/ff2ba570e7210bdea7efe3a8f0ed47d3669f27ed/results-figures/figures/fig_mk1_04.png)

Next, by comparing `Ref – Cap` and `Ref – Tax` differences in 2050, we find that:

- **Electricity** and **Refining** show the largest absolute reductions in CO₂.
- These sectors drive the bulk of decarbonization under both policy scenarios.

![](https://github.com/bopavel/gcam-custom-scenarios/blob/ff2ba570e7210bdea7efe3a8f0ed47d3669f27ed/results-figures/figures/fig_mk1_05.png)

Example summary chart:

![CO₂ emissions by sector: Canada – focus on Electricity and Refining](https://github.com/bopavel/gcam-custom-scenarios/blob/ff2ba570e7210bdea7efe3a8f0ed47d3669f27ed/results-figures/figures/fig_mk1_06.png)

---

## 3. How is energy supply decarbonized? (Primary energy and CCS)

We query *primary energy consumption with CCS by region (direct equivalent)* and
compare fuel types.

![Primary energy consumption with CCS – raw table](https://github.com/bopavel/gcam-custom-scenarios/blob/c601cde7499d18326fee8f192eadab9d1381da44/results-figures/figures/fig_mk1_07.png)

For illustration, we highlight oil and wind, with energy units (EJ) expressed in exajoules (10^18 joules).

![Primary energy consumption: Oil](https://github.com/bopavel/gcam-custom-scenarios/blob/c601cde7499d18326fee8f192eadab9d1381da44/results-figures/figures/fig_mk1_08.png)

![Primary energy consumption: Wind](https://github.com/bopavel/gcam-custom-scenarios/blob/c601cde7499d18326fee8f192eadab9d1381da44/results-figures/figures/fig_mk1_09.png)

**Key insight:**

- Fossil energy (oil, natural gas, coal) is reduced relative to Reference (decreased reliance on carbon-intensive energy sources).
- Fossil energy with **CCS** grows, substituting some unabated fossil use (Carbon Capture and Storage technology).
- Low-carbon sources (e.g., wind, solar) grow substantially in policy scenarios (expanded utilization).

---

## 4. End-use sectors: total energy demand

End-use sector decarbonization is examined through changes in total energy consumption and fuel structure.

We use the *total final energy by aggregate sector* query (buildings, industry,
transportation) and build pivot tables from 2015 onwards.

![](https://github.com/bopavel/gcam-custom-scenarios/blob/3f768036d990afb48eae50c7497dd6d890961e43/results-figures/figures/fig_mk1_10.png)

### 4.1 Buildings – total final energy (EJ)

![Total final energy: Buildings](https://github.com/bopavel/gcam-custom-scenarios/blob/3f768036d990afb48eae50c7497dd6d890961e43/results-figures/figures/fig_mk1_11.png)

- Reference: consistent growth over time.  
- Cap: growth slows after 2040–2050.  
- Tax: growth remains but with lower absolute levels than Reference.

### 4.2 Industry – total final energy (EJ)

![Total final energy: Industry](https://github.com/bopavel/gcam-custom-scenarios/blob/3f768036d990afb48eae50c7497dd6d890961e43/results-figures/figures/fig_mk1_12.png)

All scenarios show consistent growth, but:

- Tax < Reference, and  
- Cap < Tax in terms of absolute energy use.

### 4.3 Transportation – total final energy (EJ)

![Total final energy: Transportation](https://github.com/bopavel/gcam-custom-scenarios/blob/3f768036d990afb48eae50c7497dd6d890961e43/results-figures/figures/fig_mk1_13.png)

- 2020 shows a clear increase vs 2015 (initial increase).  
- After a small dip in 2025, all scenarios follow a “parabola-like” trajectory.  
- Cap has the lowest absolute energy use among the three scenarios.

---

## 5. End-use sectors: fuel mix

We further examine fuel structure using *final energy consumption by sector and fuel*,
re-classified into the three aggregate sectors (buildings, industry, and transportation).

This analysis is cross-referenced with *building final energy by fuel* and *industry final energy by fuel* data for accuracy.

![](https://github.com/bopavel/gcam-custom-scenarios/blob/30c147f201aea827923e71fa022fcf23bbd169ae/results-figures/figures/fig_mk1_14.png)

### 5.1 Buildings – final energy by fuel

![](https://github.com/bopavel/gcam-custom-scenarios/blob/30c147f201aea827923e71fa022fcf23bbd169ae/results-figures/figures/fig_mk1_15.png)

#### Reference

![Buildings – Reference](https://github.com/bopavel/gcam-custom-scenarios/blob/30c147f201aea827923e71fa022fcf23bbd169ae/results-figures/figures/fig_mk1_16.png)

Moderate transition towards electrification; gradual decline in gas consumption.

#### Carbon Constraint

![Buildings – Carbon Constraint](https://github.com/bopavel/gcam-custom-scenarios/blob/30c147f201aea827923e71fa022fcf23bbd169ae/results-figures/figures/fig_mk1_17.png)

Strongest shifts:

- Large increases in electricity and hydrogen.  
- Steep declines in gas, biomass, and coal.  
- Slight reduction in refined liquids.

#### Tax

![Buildings – Tax](https://github.com/bopavel/gcam-custom-scenarios/blob/30c147f201aea827923e71fa022fcf23bbd169ae/results-figures/figures/fig_mk1_18.png)

Similar trends to Reference but with:

- Slightly higher electricity share.  
- Stronger reduction in gas.

### 5.2 Industry – final energy by fuel

![](https://github.com/bopavel/gcam-custom-scenarios/blob/11c816e2cd38d5eb56bfea16dd97b2f6738a181c/results-figures/figures/fig_mk1_19.png)

![Industry – Reference](https://github.com/bopavel/gcam-custom-scenarios/blob/11c816e2cd38d5eb56bfea16dd97b2f6738a181c/results-figures/figures/fig_mk1_20.png)  
![Industry – Carbon Constraint](https://github.com/bopavel/gcam-custom-scenarios/blob/11c816e2cd38d5eb56bfea16dd97b2f6738a181c/results-figures/figures/fig_mk1_21.png)  
![Industry – Tax](https://github.com/bopavel/gcam-custom-scenarios/blob/11c816e2cd38d5eb56bfea16dd97b2f6738a181c/results-figures/figures/fig_mk1_22.png)

- Reference: growth in all fuels, especially electricity, biomass, refined liquids, and coal.  
- Cap: the most dramatic shifts, with the strongest growth in electricity and hydrogen; gas declines; biomass and refined liquids grow moderately; relatively stable coal use.  
- Tax: intermediate between Reference and Cap.

### 5.3 Transport – final energy by fuel

![](https://github.com/bopavel/gcam-custom-scenarios/blob/b2e387d7a4d35c461f148ae5051313951db9a05e/results-figures/figures/fig_mk1_23.png)

![Transport – Reference](https://github.com/bopavel/gcam-custom-scenarios/blob/b2e387d7a4d35c461f148ae5051313951db9a05e/results-figures/figures/fig_mk1_24.png)  
![Transport – Carbon Constraint](https://github.com/bopavel/gcam-custom-scenarios/blob/b2e387d7a4d35c461f148ae5051313951db9a05e/results-figures/figures/fig_mk1_25.png)  
![Transport – Tax](https://github.com/bopavel/gcam-custom-scenarios/blob/b2e387d7a4d35c461f148ae5051313951db9a05e/results-figures/figures/fig_mk1_26.png)

- Refined liquids remain the dominant fuel source in transportation, unlike other sectors.  
- Coal is not used; gas is minimal and declining (contrast with its importance in buildings and industry sectors).  
- Reference already shows a shift toward electricity and hydrogen.  
- Cap has the highest adoption of electricity and hydrogen and largest reduction in refined liquids.  
- Tax is in between, with slightly lower electrification than Cap and marginally higher reduction in refined liquids use compared to Reference.

---

## 6. Regional comparison: Canada vs Russia

We keep the same scenarios but compare Canada with Russia across the three
aggregate sectors.

### 6.1 Carbon Constraint (Cap)

![Cap – Buildings: Canada vs Russia](figures/10_cap_building_can_rus.png)  
![Cap – Industry: Canada vs Russia](figures/10_cap_industry_can_rus.png)  
![Cap – Transport: Canada vs Russia](figures/10_cap_transport_can_rus.png)

**Cap strategy:**

- More effective than Tax in both countries and sectors.  
- In some sectors (e.g., Russian buildings, transportation in both countries), it leads to **absolute reductions** vs Reference.  
- Particularly impactful in Russia’s building sector: Russia achieves a reduction, while Canada mainly slows growth.

### 6.2 Tax

![Tax – Buildings: Canada vs Russia](figures/11_tax_building_can_rus.png)  
![Tax – Industry: Canada vs Russia](figures/11_tax_industry_can_rus.png)  
![Tax – Transport: Canada vs Russia](figures/11_tax_transport_can_rus.png)

**Tax strategy:**

- Less effective than Cap but still reduces growth compared to Reference.  
- Appears relatively more effective in Russia’s industry sector than in Canada’s.

---

## 7. Summary

- **Cap vs Tax:** Carbon caps deliver stronger and earlier emissions reductions than
  carbon taxes in this setup, especially in electricity, refining, and transport.
- **Sector patterns:**  
  - Buildings and industry see strong electrification and some hydrogen uptake.  
  - Transport remains refined-liquid-heavy but gradually shifts to electricity
    (and some hydrogen), particularly under the Cap scenario.
- **Regional differences:**  
  - Russia’s buildings appear more responsive to the Cap strategy than Canada’s.  
  - Both strategies struggle to fully curb industrial energy growth in both regions.  
  - Transport decarbonization is effective under Cap in both countries.

Note: these comparisons are indicative and depend on differences in
economic structure and baseline energy efficiency between Canada and Russia.

