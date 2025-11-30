# gcam-custom-scenarios
This repository documents the configuration and results of GCAM runs using custom carbon policy and power sector technology assumptions. The underlying GCAM code is maintained in our fork of "gcam-core" (see link below); this repo focuses on:

- Input & Config XML files for carbon caps and carbon taxes
- Modified power sector technology cost and lifetime assumptions
- Run configuration files used to execute the model
- Extracting and visualizing results

## 1. Related repositories

- GCAM core fork (with custom Input XML files): <LINK-TO-OUR-GCAM-CORE-FORK>
- Upstream GCAM: <LINK-TO-OFFICIAL-GCAM-REPO>

## 2. GCAM version and environment

- GCAM version: `v7.0`
- OS: Windows 10
- Recommended computer specs: 16GB RAM, Core i5 or higher
- Pre-reqs: Java JDK 64, R, XML Maker

## 3. Configuration files

All custom Config XML files are stored in `config/`.

## 4. How to run the scenarios

1. Clone and build `gcam-core` from our fork:
2. Enter MainGCAMFolder/exe/ and place any custom Config XML file there
3. Rename this custom Config XML file to `configuration.xml`
4. Alternatively, to run this scenario (e.g., `configuration_ref.xml`) open `run-gcam.bat` in notepad and change “gcam.exe -C configuration.xml” to the new name (e.g., “gcam.exe -C configuration_ref.xml”)
5. Enter your MainGCAMFolder/exe/ and run run-gcam.bat
6. Outputs will be written to MainGCAMFolder/output/database_basexdb
7. Can visualize data from MainGCAMFolder/ModelInterface/run-model-interface.bat (see our Results in `results-figures/`)

## 4. About Global Change Analysis Model

- GCAM is a global hierarchical equilibrium integrated assessment model
- GCAM links Economic, Energy, Land-use, Water, and Climate systems in a technology-rich model
- Runs to 2100 in 5-year time-steps
- Emissions of 16 greenhouse gases (GHG) and air pollutants are tracked
- GCAM is natively coupled to a simple climate model HECTOR, but can also be coupled to Energy Exascale Earth System Model (E3SM)
- GCAM is a community model, instructions on the GCAM tutorial and documentation available at: https://jgcri.github.io/gcam_training/gcam.html
- GCAM is primarily developed with support from Office of Science, but has wide reaching applications in policy, science, and philanthropies

