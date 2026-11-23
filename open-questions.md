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

9. The thesis review found few social criteria, little early involvement of stakeholders and little sensitivity analysis in multi-criteria approaches to soil remediation. How do we involve stakeholders early enough?
10. Uncertainty in criteria weights, criteria scores and disagreement between decision makers blurs the ranking of remediation options. How do we show that uncertainty to decision makers?
11. Grouping parcels into clusters lowers the cost of remediation but moves the plan away from the best plan for each parcel. Who should choose the cluster size?
12. In the Maarkebeek case study, a plan based on off-site criteria reduced the Cs-137 flux at the outlet by 36.6% in the first year, against 14.7% for a plan based on on-site criteria only. How do on-site and off-site criteria get into one decision?
13. The thesis argues that its methods apply to other soil contamination, such as PFAS. Which contamination problems would you test them on?
