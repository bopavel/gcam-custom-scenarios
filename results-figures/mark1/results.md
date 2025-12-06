# GCAM Results – Canada Decarbonization Scenarios

This folder contains the results and figures for the GCAM runs. We compare three scenarios for Canada with a focus on 2050:

- **Reference** – no additional climate policy (middle-of-the-road socioeconomic and technological assumptions).
- **Carbon Constraint (Cap)** – annual CO₂ emissions constrained via `carbon_cap.xml` (determine carbon price based on prescribed emissions pathway).
- **Carbon Tax (Tax)** – exogenous carbon price path via `carbon_tax_25_5_mod.xml` (incorporate policy perspectives).

All runs use GCAM 7.0 (`gcam-v7.0`) with updated configuration files
`configuration_ref_upd.xml`, `configuration_cap_upd.xml`, and `configuration_tax_upd.xml`.

---

## 1. CO₂ emissions by region (Canada)

The first set of figures shows CO₂ emissions for Canada in the three scenarios.

![CO₂ emissions by region: Canada – GCAM interface](figures/01_co2_canada_interface.png)

We then export the data to Excel and plot the trajectories:

![CO₂ emissions by region: Canada – Reference vs Cap vs Tax](figures/01_co2_canada_scenarios.png)

**Key insight:**  
- Reference: emissions peak around 2030 and decline only slightly by 2050.  
- Cap: emissions drop sharply after 2025 and approach near-zero levels by 2050.  
- Tax: emissions decline steadily but less aggressively than under the cap.

---

## 2. Where do CO₂ reductions come from? (Sector breakdown)

We use *CO₂ emissions by sector (no bio) (excluding resource production)* to
identify which sectors contribute most to reductions in 2050.

![CO₂ emissions by sector: Cement and Iron & Steel](figures/02_co2_canada_cement_steel.png)

By comparing `Ref – Cap` and `Ref – Tax` differences in 2050, we find that:

- **Electricity** and **Refining** show the largest absolute reductions in CO₂.
- These sectors drive the bulk of decarbonization under both policy scenarios.

Example summary chart:

![CO₂ emissions by sector: Canada – focus on Electricity and Refining](figures/02_co2_canada_by_sector_elec_refining.png)

---

## 3. How is energy supply decarbonized? (Primary energy and CCS)

We query *primary energy consumption with CCS by region (direct equivalent)* and
compare fuel types.

![Primary energy consumption with CCS – raw table](figures/03_primary_energy_table.png)

For illustration, we highlight oil and wind:

![Primary energy consumption: Oil](figures/03_primary_energy_oil.png)

![Primary energy consumption: Wind](figures/03_primary_energy_wind.png)

**Key insight:**

1. Fossil energy (oil, gas, coal) is reduced relative to Reference.  
2. Fossil energy with **CCS** grows, substituting some unabated fossil use.  
3. Low-carbon sources (e.g., wind, solar) grow substantially in policy scenarios.

---

## 4. End-use sectors: total energy demand

We use the *total final energy by aggregate sector* query (buildings, industry,
transportation) and build pivot tables from 2015 onwards.

### 4.1 Buildings – total final energy (EJ)

![Total final energy: Buildings](figures/04_final_energy_buildings_total.png)

- Reference: consistent growth over time.  
- Cap: growth slows after 2040–2050.  
- Tax: growth remains but with lower absolute levels than Reference.

### 4.2 Industry – total final energy (EJ)

![Total final energy: Industry](figures/05_final_energy_industry_total.png)

All scenarios show growth, but:

- Tax < Reference, and  
- Cap < Tax in terms of absolute energy use.

### 4.3 Transportation – total final energy (EJ)

![Total final energy: Transportation](figures/06_final_energy_transport_total.png)

- 2020 shows a clear increase vs 2015.  
- After a small dip in 2025, all scenarios follow a “parabola-like” trajectory.  
- Cap has the lowest absolute energy use among the three scenarios.

---

## 5. End-use sectors: fuel mix

We further examine fuel structure using *final energy consumption by sector and fuel*,
re-classified into the three aggregate sectors.

### 5.1 Buildings – final energy by fuel

#### Reference

![Buildings – Reference](figures/07_buildings_fuel_ref.png)

Moderate electrification; gradual decline in gas.

#### Carbon Constraint

![Buildings – Carbon Constraint](figures/07_buildings_fuel_cap.png)

Strongest shifts:

- Large increases in electricity and hydrogen.  
- Steep declines in gas, biomass, and coal.  
- Slight reduction in refined liquids.

#### Tax

![Buildings – Tax](figures/07_buildings_fuel_tax.png)

Similar trends to Reference but with:

- Slightly higher electricity share.  
- Stronger reduction in gas.

### 5.2 Industry – final energy by fuel

![Industry – Reference](figures/08_industry_fuel_ref.png)  
![Industry – Carbon Constraint](figures/08_industry_fuel_cap.png)  
![Industry – Tax](figures/08_industry_fuel_tax.png)

- Reference: growth in all fuels, especially electricity, biomass, refined liquids, and coal.  
- Cap: strongest growth in electricity and hydrogen; gas declines; biomass and refined liquids grow moderately; coal roughly stabilizes.  
- Tax: intermediate between Reference and Cap.

### 5.3 Transport – final energy by fuel

![Transport – Reference](figures/09_transport_fuel_ref.png)  
![Transport – Carbon Constraint](figures/09_transport_fuel_cap.png)  
![Transport – Tax](figures/09_transport_fuel_tax.png)

- Refined liquids remain dominant.  
- Coal is not used; gas is minimal and declining.  
- Reference already shows a shift toward electricity and hydrogen.  
- Cap has the highest adoption of electricity and hydrogen and largest reduction in refined liquids.  
- Tax is in between, with slightly lower electrification than Cap.

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

