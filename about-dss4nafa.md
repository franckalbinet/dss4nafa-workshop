# About DSS4NAFA

DSS4NAFA is the Decision Support System for Nuclear Emergencies Affecting Food and Agriculture. This page summarises Chapter 3 and Annexes A-1 and A-3 of the DSS4NAFA book, Lee Zhi Yi, A. and Dercon, G. (2019), [Data management and visualisation in response to large-scale nuclear emergencies affecting food and agriculture](https://openknowledge.fao.org/3/ca6666en/CA6666EN.pdf), FAO/IAEA.

## The problem

After a nuclear or radiological accident, decision tools usually deal with external exposure, evacuation and logistics. Food safety often gets attention only once clean-up begins, although contaminated food exposes people internally and has large health and economic effects. The food response is hard to run. Food is perishable and must be sampled and analysed fast. Sample collectors and laboratory instruments are scarce. The data cover many radionuclides, soil types and foodstuffs, and scattered manual data handling causes delays, transcription errors and mixed-up sample IDs.

## What DSS4NAFA does

DSS4NAFA covers the food and agriculture response in one cloud-based system, from field sampling and laboratory analysis to decision support. It links emergency managers, sample collectors, laboratories and decision makers, in emergencies and in routine food safety monitoring. DSS4NAFA does not make decisions. For each administrative unit it suggests to restrict, not to restrict or to collect more samples, and officials accept or reject each suggestion. Governments set their action levels and risk tolerance before an emergency.

## Modules

The Session column gives the workshop session that presents each module.

| Module | What it does | Users | Session |
|---|---|---|---|
| ASTA (Advanced Sampling Task Assignment) | Selects high-priority sampling areas from agro-ecological zone or land use maps, crop calendars, exclusion zones and air dose data. In simple mode, the user draws a rectangle and gets random sampling points. | Decision makers | 1 |
| Nudge module | Imports data collected earlier or by hand, from a CSV or Excel template. | Decision makers | 1 |
| Mobile app | Registers samples in the field or the laboratory with their GPS position and time, and sends them to the cloud. Runs on Android. | Sample collectors, laboratory technicians | 1 |
| Hotspot map | Maps radioactivity levels by foodstuff, radionuclide and time. | Decision makers | 2 |
| Logmap | Shows the samples planned, collected and analysed over time, to find bottlenecks and move staff or laboratory capacity. | Decision makers | 2 |
| Food restriction dashboard | Suggests a decision for each administrative unit from the permissible level, the minimum number of samples and the share of samples within limits. Decision makers change these settings, forecast scenarios and save the settings to keep a record of each decision. | Decision makers | 2 |

## Design

The DSS4NAFA book describes DSS4NAFA as free, non-proprietary software with a modular design. A central database connects to modules that each country can adapt to its priorities or replace. Countries can host DSS4NAFA themselves, but the IAEA guarantees security and maintenance only for the package that the IAEA hosts. DSS4NAFA needs no GIS skills and little knowledge of food safety. The current implementation uses Ruby on Rails, PostgreSQL with PostGIS, D3.js and Backbone.js.

## History

The Joint FAO/IAEA Centre of Nuclear Techniques in Food and Agriculture led the development of DSS4NAFA through two IAEA Coordinated Research Projects: [D15015](https://www.iaea.org/fr/node/285860) (2013 to 2019) and [D15019](https://www.iaea.org/newscenter/news/new-crp-monitoring-and-predicting-radionuclide-uptake-and-dynamics-for-optimizing-remediation-of-radioactive-contamination-in-agriculture-crp-d15019).
