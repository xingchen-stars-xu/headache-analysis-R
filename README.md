# Hangover Treatment Effectiveness: A Factorial ANOVA Case Study in R

This project investigates how alcohol consumption levels and treatment types affect the severity of hangover headaches. Using R and a publicly available dataset, I modeled both main and interaction effects using **factorial ANOVA** and visualized the results to identify significant patterns.

## Research Questions

1. Does the amount of alcohol consumed influence headache intensity?
2. Do treatments (Charcoal, B12, Placebo) reduce headache intensity?
3. Does treatment effectiveness vary by level of alcohol consumption?

## Dataset

- **Source:** [Headache-3f.csv](https://github.com/psyc111/datasets/blob/main/Headache-3f.csv)
- **Design:** 3×3 factorial (Alcohol: Low/Medium/High × Treatment: Charcoal/B12/Placebo)
- **Outcome:** Headache intensity rated from 0 (none) to 100 (worst ever)

## Analysis Overview

| Model Type           | Predictor(s)             | R²     | Key Findings |
|----------------------|--------------------------|--------|--------------|
| **Model 1:** Consumption Only | Alcohol Consumption         | 0.82   | Higher consumption → more intense headaches |
| **Model 2:** Treatment Only   | Treatment                  | 0.03   | Treatment effect weak overall |
| **Model 3:** Additive         | Treatment + Consumption     | 0.86   | Both predictors matter |
| **Model 4:** Interaction      | Treatment × Consumption     | 0.90   | Treatment only effective at high consumption |

**Statistical Tools Used:**
- `lm()`, `anova()`
- Post-hoc: `TukeyHSD()`
- Visualization: `ggplot2`

## Key Visualizations

| Consumption Effect | Treatment Effect | Interaction Effect |
|--------------------|------------------|--------------------|
| ![Consumption](figures/main_effects_consumption.png) | ![Treatment](figures/main_effects_treatment.png) | ![Interaction](figures/interaction_plot.png) |

## Tools & Libraries

- `R`, `tidyverse`, `ggplot2`, `broom`, `supernova`, `mosaic`, `TukeyHSD`

## Why This Matters for Quant UX / Data Science (Analytics)

This project demonstrates:
- Designing and interpreting **factorial experiments**
- Modeling **main effects** and **interactions**
- Translating complex statistical output into actionable insight
- Capability of running analysis in **R**

This is the kind of analysis useful in A/B testing, feature rollout evaluation, or assessing UX outcomes across user contexts.

## Project Structure

