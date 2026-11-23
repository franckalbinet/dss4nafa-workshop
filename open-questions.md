# Open questions

These questions come from ongoing research. Nothing here is decided. Tell us what you think, or what you would do differently, by [opening an issue](../../issues/new).

## Sampling and restriction decisions

Source: the `scoring-experiments` branch of trufl, in [scoring-design.md](https://github.com/franckalbinet/trufl/blob/scoring-experiments/scoring-design.md) and [scoring-plan.md](https://github.com/franckalbinet/trufl/blob/scoring-experiments/scoring-plan.md). The results come from simulations on synthetic plumes and on windows of the 2011 Fukushima data.

The DSS4NAFA restriction dashboard restricts a unit when the share of its samples above the permissible level is more than an accepted proportion, given a minimum number of samples. trufl takes this rule as an input and allocates samples where they most lower the expected number of wrong decisions.

1. With this rule, one more sample can make a decision less reliable. With 10% accepted, a unit whose true share is 12% is decided wrongly 32% of the time with 9 samples and 66% of the time with 10. Should the rule change?
2. The rule counts exceedances and ignores how far a value is above the level. Should decisions target what the share stands for, such as the dose to consumers?
3. Should restriction decisions use prior information, such as an airborne survey or a dispersion model, as well as samples?
4. A needless restriction and a missed restriction do not cost the same. Would decision makers set the ratio between the two costs openly, as a dashboard setting next to the permissible level?
5. In simulations, costs used to allocate samples weakened health protection where crops are valuable. One proposal treats health as a limit: every unit is sampled until its probability of a missed restriction is below a bound. What bound is acceptable, and should it be the same for every unit?
6. Where samples go inside a unit matters. A systematic layout did better than random placement when contamination is spatially correlated, and samples clustered near roads or a single farm gave many missed restrictions. How do field teams place samples today?
7. A unit crossed by the edge of the plume is the clearest case for "partially restrict". How fine should restriction units be, compared with administrative units?
8. Some dilemmas need new parts in trufl: deadlines for perishable food such as milk and leafy vegetables, the dose received by sampling teams, a minimum coverage for fairness and trust, countermeasures other than restriction, and the choice of crop to sample. Which matter most in practice?

## Remediation

Source: Abrams (2023), see the [references](README.md#references).

Floris Abrams' PhD thesis builds a proof-of-concept spatial decision support system for the remediation of farmland contaminated with caesium-137 after a nuclear accident. The system answers where to remediate, how and when, with the farm parcel as the unit of decision. The research questions come from four dimensions: spatial, temporal, the type of criteria (on-site or off-site) and uncertainty. The case studies are the Maarkebeek catchment in Belgium (1,380 parcels) and the Niida catchment near Fukushima.

### What the thesis answered

Multi-criteria decision approaches in use (Chapter 2). Which multi-criteria decision-making approaches optimise the remediation of polluted soils today? Multi-criteria decision analysis (MCDA) works for choosing a technology at one site and for choosing which sites to treat across a region. The review found four gaps: few social criteria, little early involvement of stakeholders, weighting and aggregation methods that do not match each other, and little sensitivity analysis.

Uncertainty (Chapter 3). How do uncertain criteria weights, uncertain criteria scores and disagreement between decision makers affect the ranking of remediation technologies, separately and together? The thesis turns linguistic scales into triangular fuzzy numbers and combines them with Monte Carlo simulation. Uncertainty clearly blurs the ranking. A deterministic analysis gives stakeholders false confidence.

Spatial clustering (Chapter 4). How can contaminated parcels be grouped into clusters to make remediation more efficient, with and without an annual budget? A spatio-temporal clustering algorithm gives one compromise action to each cluster of similar neighbouring parcels. Larger clusters cost less but move further from the best plan for each parcel. Decision makers must choose the trade-off.

Temporal sequencing (Chapter 5). How can sequences of remediation actions over several years be designed under on-site criteria and an annual budget? The thesis introduces remedial trajectories, solved with integer programming and column generation. In the Maarkebeek case study, column generation lowered the accumulated priority score by 19.7%. Without remediation, the catchment would need about 90 years to return to full production.

Off-site effects (Chapter 6). Can off-site criteria be included, and can the cellular automata heuristic CAMF capture sediment loss and flow after decontamination? It can. In the Niida catchment, afforestation on the best 3.4% of candidate cells would have cut sediment export by 15.4%, against 0.8% for cells chosen at random.

Integration (Chapter 7). How can on-site criteria, off-site criteria and a budget be combined into spatio-temporal plans that account for re-contamination through sediment flow? In the Maarkebeek case, removing topsoil everywhere would raise sediment output at the catchment outlet by 111%. In the first year, a plan based on off-site criteria lowered the Cs-137 flux at the outlet by 36.6%, against 14.7% for a plan based on on-site criteria only.

The thesis concludes that the effect of an intervention depends strongly on its location, and that its methods apply to other soil contamination, such as PFAS.

### Follow-up questions

9. From restriction to remediation. DSS4NAFA decides restrictions for administrative units, and the thesis plans remediation for parcels. When does a restricted unit become a candidate for remediation, and how do the two scales connect?
10. Uncertain contamination maps. The thesis plans from a map of contamination per parcel. In a response, that map comes from samples collected with DSS4NAFA and carries uncertainty. How does that uncertainty change remediation plans, and where should extra samples go to improve the plan rather than the restriction decision?
11. Replanning. Remedial trajectories cover several years. How should a plan be updated each year as new samples, budgets and policies arrive?
12. Social criteria and stakeholders. The review found few social criteria and late involvement of stakeholders. Which social criteria matter most, such as farmers' livelihoods, acceptance and trust, and how can stakeholders set them before an emergency?
13. Showing uncertainty. Uncertainty blurs the ranking of remediation options. How do we show that to decision makers so that they can still act, and which source of uncertainty is worth reducing first?
14. Cluster size. Who should choose the trade-off between the cost of large clusters and the quality of parcel-level plans, and do clusters match how farms and cooperatives work?
15. Downstream effects. Removing topsoil can raise the sediment and Cs-137 flux downstream, often into other administrative units. How do we weigh a benefit on site against harm downstream, and who decides?
16. Data before an emergency. The methods need parcel maps, land use, soil and erosion data. Which of these can a Member State prepare in advance, and could DSS4NAFA store them?
17. Other contaminants and contexts. Which other radionuclides, such as strontium-90, other farming systems and other contaminants, such as PFAS, would test whether the methods transfer?
18. Validation. The system is a proof of concept. Which records of real remediation, for example from Fukushima, could validate its plans?
