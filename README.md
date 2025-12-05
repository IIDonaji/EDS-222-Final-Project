# Urban Insect Biodiversity: Effects of Drought-Tolerant Plants

## Project Overview

This project examines how drought-tolerant landscaping affects insect diversity in urban Los Angeles, using data from 30 sites sampled monthly across 2014.

## Scientific Hypothesis

**Research Question:**
Do drought-tolerant plants increase insect species richness in urban Los Angeles?

or 

Do drought-tolerant plants and local temperature interact to affect insect species richness in urban Los Angeles?

**Hypothesis:**

Sites with drought-tolerant plants have higher insect species richness than sites without drought-tolerant plants, after accounting for temperature and season.

**Justification:**

Drought-tolerant plants are better adapted to Los Angeles's naturally arid climate and may provide more suitable habitat for local insect species compared to non-native ornamental plants that require frequent watering.

## Statistical Model

**Response Variable:**

-   `CorRichne` = Insect species richness (count)

**Model Family:**

-   Negative Binomial (handles overdispersion in count data)

**Model Structure:**

```         
$$
\begin{align}
\text{Richness} &\sim Negative Binomial(mue, sigma) \\
log(mu) = Beta_0 + Beta_1(Drought Plant) + Beta_2(Season) + Beta_3(Temperture)}
\end{align}
$$

```

**Link Function:**

log link (because we're modeling counts)

## Statistical Hypotheses

**Primary Hypothesis (Drought-Tolerant Plants Effect):**

H₀: β₁ = 0 (Drought-tolerant plants have no effect on species richness)

Hᴀ: β₁ > 0 (Drought-tolerant plants increase species richness)

H₀: β₂ = 0 (Temperature has no effect on richness)
Hᴀ: β₂ ≠ 0 (Temperature affects richness )


## Data Description

-   **Source:** Adams et al. (2020) - Los Angeles urban biodiversity study
-   **Samples:** 360 observations (30 sites × 12 months)
-   **Response:** Species richness per trap day
-   **Key predictors:** Drought-tolerant plants, urbanization, season

## Repository Structure

```         
```

## References

Adams, B. J., et al. (2020). Local- and landscape-scale variables shape insect diversity in an urban biodiversity hot spot. Ecological Applications, 30(4), e02089.
