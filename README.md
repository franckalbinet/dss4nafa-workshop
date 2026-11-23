# DSS4NAFA workshop

Materials for a half-day workshop on DSS4NAFA, the Decision Support System for Nuclear Emergencies Affecting Food and Agriculture, and on the research around it.

The workshop is for everyone who responds to nuclear emergencies that affect food, agriculture and soils, or who remediates them afterwards: decision makers, sample collectors, laboratories and the institutions they work for. It is also for researchers who want to work on the open research questions, and for Member States that want to try DSS4NAFA, help improve it or adapt it to their own requirements. We present the system and our ongoing research, and we want your feedback, your ideas and partners.

## What DSS4NAFA does

After a nuclear or radiological accident, decision tools usually deal with external exposure, evacuation and logistics. Food safety often gets attention only once clean-up begins, although contaminated food exposes people internally and has large health and economic effects. The food response is hard to run. Food is perishable and must be sampled and analysed fast. Sample collectors and laboratory instruments are scarce. The data cover many radionuclides, soil types and foodstuffs, and scattered manual data handling causes delays, transcription errors and mixed-up sample IDs.

DSS4NAFA covers the food and agriculture response in one cloud-based system, from field sampling and laboratory analysis to decision support. It links emergency managers, sample collectors, laboratories and decision makers, in emergencies and in routine food safety monitoring. DSS4NAFA does not make decisions. For each administrative unit it suggests to restrict, not to restrict or to collect more samples, and officials accept or reject each suggestion. Governments set their action levels and risk tolerance before an emergency.

| Module | What it does | Users | Session |
|---|---|---|---|
| ASTA (Advanced Sampling Task Assignment) | Selects high-priority sampling areas from agro-ecological zone or land use maps, crop calendars, exclusion zones and air dose data. In simple mode, the user draws a rectangle and gets random sampling points. | Decision makers | 1 |
| Nudge module | Imports data collected earlier or by hand, from a CSV or Excel template. | Decision makers | 1 |
| Mobile app | Registers samples in the field or the laboratory with their GPS position and time, and sends them to the cloud. Runs on Android. | Sample collectors, laboratory technicians | 1 |
| Hotspot map | Maps radioactivity levels by foodstuff, radionuclide and time. | Decision makers | 2 |
| Logmap | Shows the samples planned, collected and analysed over time, to find bottlenecks and move staff or laboratory capacity. | Decision makers | 2 |
| Food restriction dashboard | Suggests a decision for each administrative unit from the permissible level, the minimum number of samples and the share of samples within limits. Decision makers change these settings, forecast scenarios and save the settings to keep a record of each decision. | Decision makers | 2 |

The DSS4NAFA book describes DSS4NAFA as free, non-proprietary software with a modular design. A central database connects to modules that each country can adapt to its priorities or replace. Countries can host DSS4NAFA themselves, but the IAEA guarantees security and maintenance only for the package that the IAEA hosts. DSS4NAFA needs no GIS skills and little knowledge of food safety. The current implementation uses Ruby on Rails, PostgreSQL with PostGIS, D3.js and Backbone.js.

The Joint FAO/IAEA Centre of Nuclear Techniques in Food and Agriculture led the development of DSS4NAFA through two IAEA Coordinated Research Projects: [D15015](https://www.iaea.org/fr/node/285860) (2013 to 2019) and [D15019](https://www.iaea.org/newscenter/news/new-crp-monitoring-and-predicting-radionuclide-uptake-and-dynamics-for-optimizing-remediation-of-radioactive-contamination-in-agriculture-crp-d15019). The DSS4NAFA book is Lee Zhi Yi, A. and Dercon, G. (2019), [Data management and visualisation in response to large-scale nuclear emergencies affecting food and agriculture](https://openknowledge.fao.org/3/ca6666en/CA6666EN.pdf), FAO/IAEA. Chapter 3 and Annexes A-1 and A-3 cover DSS4NAFA.

## Sessions

The workshop follows the steps of a response, with one session for each step:

- Sampling and data collection: DSS4NAFA plans the samples, guides the field teams and collects the laboratory results.
- Decision making: the DSS4NAFA dashboards turn the results into restriction options. [trufl](https://fr.anckalbi.net/trufl/), a Python library under development, decides where each round of samples goes, to make restriction decisions right.
- Remediation: OREFA, from the PhD research of Floris Abrams at KU Leuven and SCK CEN, plans where, how and when to clean up contaminated farmland.

## Agenda

The first half has presentations and demos. The second half has questions and practice exercises.

| # | Session | Speakers | Minutes |
|---|---|---|---|
| 1 | [DSS4NAFA added value](01-added-value/) | Lazar Adjigogov | 30 |
| 2 | [DSS4NAFA decision making](02-decision-making/) | Franck Albinet | 30 |
| 3 | [OREFA: optimizing decision making](03-orefa/) | Floris Abrams | 30 |
| 4 | Break | | 30 |
| 5 | Questions and answers | Lazar, Franck, Floris | 15 |
| 6 | [Practice exercises](04-exercises/) | Lazar, Franck, Floris | 60 |
| 7 | Wrap-up, questions and answers | Lazar, Franck, Floris | 15 |

## Before the workshop

1. Watch the [DSS4NAFA video](https://www.youtube.com/watch?v=Ut4GzjKabMc) (3.5 minutes).
2. Ask the organisers for a login to the [DSS4NAFA demo instance](https://dss4nafa.edusoft.mk:3000/). You need it for the practice exercises.
3. If you have time, read Chapter 3 of the [DSS4NAFA book](https://openknowledge.fao.org/3/ca6666en/CA6666EN.pdf).

## Take part

- Member States and institutions: try DSS4NAFA on the demo instance, and tell us what you need to use it in your country. To discuss using DSS4NAFA, contact Gerd Dercon at the Soil and Water Management and Crop Nutrition Laboratory (SWMCNL), part of the Joint FAO/IAEA Centre of Nuclear Techniques in Food and Agriculture, at the IAEA Laboratories in Seibersdorf, Austria.
- Researchers: most of the research presented here is not finished. [open-questions.md](open-questions.md) lists the questions we want to work on with partners.
- Everyone: to send a question, an idea or a proposal to work together, [open an issue](../../issues/new) in this repository.

## Repository layout

    01-added-value/        session 1: from sampling plan to laboratory results
    02-decision-making/    session 2: dashboards, restriction rule and trufl
      dashboards/          step-by-step screenshots of the hotspots, logmap and restriction dashboards (PDF)
    03-orefa/              session 3: remediation of contaminated farmland
    04-exercises/          practice exercises
    data/                  example input files for DSS4NAFA
    open-questions.md      open research questions for discussion

## References

- Abrams, F. (2023). Towards more effective spatio-temporal schemes for remediation of agricultural soils in response to large-scale contamination with radionuclides. PhD thesis, KU Leuven and SCK CEN. [Lirias](https://lirias.kuleuven.be/handle/20.500.12942/730653).
- Lee Zhi Yi, A. and Dercon, G. (2019). Data management and visualisation in response to large-scale nuclear emergencies affecting food and agriculture. Rome: FAO/IAEA. [PDF](https://openknowledge.fao.org/3/ca6666en/CA6666EN.pdf).
- [trufl documentation](https://fr.anckalbi.net/trufl/) and [source code](https://github.com/franckalbinet/trufl).
- [Joint FAO/IAEA Centre of Nuclear Techniques in Food and Agriculture](https://www.fao.org/agriculture/fao-iaea-nuclear-techniques/en).

## Contributors

Lazar Adjigogov, Franck Albinet and Floris Abrams.
