# Experiment Design Checklist

Use this checklist before launching a randomized experiment. Every example or placeholder is generic.

## Decision and hypothesis

- [ ] State the decision this experiment will inform.
- [ ] Write a falsifiable hypothesis with treatment, population, outcome, and direction.
- [ ] Define the primary metric, aggregation, analysis window, and expected data source.
- [ ] Define guardrail metrics and unacceptable tradeoffs.

## Design

- [ ] Choose the unit of randomization and check for interference or clustering.
- [ ] Record eligibility, exclusions, allocation ratio, and assignment procedure.
- [ ] Estimate baseline rate or variance from an appropriate prior period.
- [ ] Set minimum detectable effect (MDE) in practical and statistical terms.
- [ ] Set alpha, statistical power, and planned sample size.
- [ ] Estimate duration using eligible traffic and seasonality constraints.
- [ ] Plan for multiple testing when using multiple variants, outcomes, or repeated looks.
- [ ] Predefine segment analysis; distinguish confirmatory from exploratory slices.
- [ ] Define stopping rules before launch and avoid optional stopping.

## Data quality and operations

- [ ] Validate exposure logging, assignment stability, and metric joins.
- [ ] Monitor sample-ratio mismatch, missingness, contamination, and novelty effects.
- [ ] Confirm that guardrails and error monitoring are available during the test.

## Analysis and interpretation

- [ ] Use the analysis method specified before launch.
- [ ] Report effect size and uncertainty, not only a p-value.
- [ ] Check practical significance against the MDE and business context.
- [ ] Interpret segments cautiously and account for multiplicity.
- [ ] Document limitations, data-quality incidents, and deviations from plan.
- [ ] Apply the predefined decision rule: ship, iterate, stop, or gather more evidence.

Sample-size planning tool: https://yangmingli.com/tools/ab-test-sample-size/
