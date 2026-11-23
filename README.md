# DSS4NAFA workshop

Materials for a half-day workshop on DSS4NAFA, the Decision Support System for Nuclear Emergencies Affecting Food and Agriculture, and on the research around it. We present the system and our ongoing research, and we want your feedback, your ideas and partners.

The workshop is for:

- **Responders**: decision makers, sample collectors, laboratories and the institutions they work for, in nuclear emergencies that affect food, agriculture and soils, and in remediation afterwards.
- **Researchers** who want to work on the open research questions.
- **Member States** that want to try DSS4NAFA, help improve it or adapt it to their own requirements.

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

- **Member States and institutions**: try DSS4NAFA on the demo instance, and tell us what you need to use it in your country. To discuss using DSS4NAFA, contact Gerd Dercon at the Soil and Water Management and Crop Nutrition Laboratory (SWMCNL), part of the Joint FAO/IAEA Centre of Nuclear Techniques in Food and Agriculture, at the IAEA Laboratories in Seibersdorf, Austria.
- **Researchers**: most of the research presented here is not finished. [open-questions.md](open-questions.md) lists the questions we want to work on with partners, and [dilemmas.md](dilemmas.md) the trade-offs behind them.
- **Everyone**: to send a question, an idea or a proposal to work together, [open an issue](../../issues/new) in this repository.

## DSS4NAFA in brief

DSS4NAFA covers the food and agriculture response to a nuclear or radiological accident in one cloud-based system, from field sampling and laboratory analysis to decision support. It links emergency managers, sample collectors, laboratories and decision makers.

DSS4NAFA does not make decisions. For each administrative unit it suggests to restrict, not to restrict or to collect more samples, and officials accept or reject each suggestion.

[about-dss4nafa.md](about-dss4nafa.md) describes the problem it solves, its modules, its design and its history.

## The three steps of a response

The workshop follows the steps of a response, with one session for each step:

- **Sampling and data collection** (session 1): DSS4NAFA plans the samples, guides the field teams and collects the laboratory results.
- **Decision making** (session 2): the DSS4NAFA dashboards turn the results into restriction options. [trufl](https://fr.anckalbi.net/trufl/), a Python library under development, decides where each round of samples goes, to make restriction decisions right.
- **Remediation** (session 3): OREFA, from the PhD research of Floris Abrams at KU Leuven and SCK CEN, plans where, how and when to clean up contaminated farmland.

[dilemmas.md](dilemmas.md) lists the trade-offs that each step involves.

## Repository layout

    about-dss4nafa.md      the problem DSS4NAFA solves, its modules, design and history
    01-added-value/        session 1: from sampling plan to laboratory results
    02-decision-making/    session 2: dashboards, restriction rule and trufl
      dashboards/          step-by-step screenshots of the hotspots, logmap and restriction dashboards (PDF)
    03-orefa/              session 3: remediation of contaminated farmland
    04-exercises/          practice exercises
    data/                  example input files for DSS4NAFA
    dilemmas.md            trade-offs in sampling, restriction and remediation
    open-questions.md      open research questions for discussion

## References

- Abrams, F. (2023). Towards more effective spatio-temporal schemes for remediation of agricultural soils in response to large-scale contamination with radionuclides. PhD thesis, KU Leuven and SCK CEN. [Lirias](https://lirias.kuleuven.be/handle/20.500.12942/730653).
- Lee Zhi Yi, A. and Dercon, G. (2019). Data management and visualisation in response to large-scale nuclear emergencies affecting food and agriculture. Rome: FAO/IAEA. [PDF](https://openknowledge.fao.org/3/ca6666en/CA6666EN.pdf).
- [trufl documentation](https://fr.anckalbi.net/trufl/) and [source code](https://github.com/franckalbinet/trufl).
- [Joint FAO/IAEA Centre of Nuclear Techniques in Food and Agriculture](https://www.fao.org/agriculture/fao-iaea-nuclear-techniques/en).

## Contributors

Lazar Adjigogov, Franck Albinet and Floris Abrams.

## Licence

The materials in this repository are licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). See [LICENSE](LICENSE).
