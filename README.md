# Urban Insect Biodiversity: Effects of Drought-Tolerant Plants

## Project Overview

This project statisticaly examines how drought-tolerant landscaping affects insect diversity in urban Los Angeles, using data from 30 sites sampled monthly across 2014.

## Scientific Hypothesis

**Research Question:**

1.  Do drought-tolerant plants increase insect species richness in urban Los Angeles? 

```
Drought-Tolerant Plants 
H₀: β₁ = 0 

Hᴀ: β₁ \> 0

```
2.  Do drought-tolerant plants and local temperature interact to affect insect species richness in urban Los Angeles?


```
Temperature  
H₀: β₂ = 0 
Hᴀ: β₂  0 

```
**Hypothesis:**

Sites with drought-tolerant plants have higher insect species richness than sites without drought-tolerant plants, after accounting for temperature and Urban Type.

**Justification:**

Drought-tolerant plants are better adapted to Los Angeles's naturally arid climate and may provide more suitable habitat for local insect species compared to non-native ornamental plants that require frequent watering.

## Statistical Model

**Response Variable:**

-   `CorRichne` = Insect species richness (count per site type)

**Model Family:**

-   Negative Binomial (handles overdispersion in count data)

**Model Structure:**

$$
\begin{align} 
Richness \sim \text{Negative Binomial}\,(\mu, \sigma) \\
log(\mu) 
= \beta_{0} + \beta_{1}\, \text{Drought-Tolerant Plants} + \beta_{2}\, \text{Mean Temperature} + \beta_{3} \, \text{Urban Type}
\end{align}
$$

**Link Function:**

log link (because we're modeling counts)

## Statistical Hypotheses

**Primary Hypothesis (Drought-Tolerant Plants Effect):**

H₀: β₁ = 0 (Drought-tolerant plants have no effect on species richness)

Hᴀ: β₁ \> 0 (Drought-tolerant plants increase species richness)

H₀: β₂ = 0 (Temperature has no effect on richness) Hᴀ: β₂ ≠ 0 (Temperature affects richness )

## Data Description

-   **Source:** Adams et al. (2020) - Los Angeles urban biodiversity study
-   **Samples:** 360 observations (30 sites × 12 months)
-   **Response:** Species richness per trap day
-   **Key predictors:** Drought-tolerant plants, urbanization, temperature

## Repository Structure

```         
```

## References

Adams, B. J., et al. (2020). Local- and landscape-scale variables shape insect diversity in an urban biodiversity hot spot. Ecological Applications, 30(4), e02089.
