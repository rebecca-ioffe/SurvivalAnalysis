# Game of Thrones Character Survival Analysis

This projects presents a parametric survival analysis of character deaths in HBO's *Game of Thrones*. The aim is to model and understand the time until character death (measured in hours of cumulative screen time) and how factors such as sex, social status, and allegiance switching impact survival. Using survival functions, hazard functions, and parametric models, we explore these relationships in-depth.

## Overview

The dataset includes data on 359 key characters from *Game of Thrones*, 212 of whom died and 147 survived (right-censored). Various demographic and narrative-related features were included, such as:

- **Social status**: Highborn or lowborn characters.
- **Sex**: Male or female.
- **Allegiance**: Final allegiance before death and an indicator for whether a character switched allegiances during the series.
- **Prominence**: A measure of character prominence calculated using the number of episodes and seasons the character survived.

### Time-to-Event Variable
The time-to-event variable represents the cumulative running time of the show (in hours) until the character's death. Characters who survived the series are right-censored at the total running time of the show.

## Description

This analysis focuses on fitting a probability distribution to the time until death for *Game of Thrones* characters, exploring the following:

1. **Initial Data Exploration**: We explored the distribution of the time until death variable, which appeared to be left-skewed. Parametric models were fit to the data using the Normal and Weibull distributions.
  
2. **Goodness-of-Fit Testing**: Using Anderson-Darling statistics and probability plots, the Weibull distribution was selected as the best-fitting distribution despite the Normal distribution being a close contender.

3. **Survival and Hazard Functions**: Survival curves and hazard plots were generated for:
   - All characters
   - By sex (Male vs. Female)
   - By social status (Highborn vs. Lowborn)
   - By allegiance switching (Switched allegiance vs. Did not switch allegiance)

The survival and hazard functions illustrate different survival patterns across these groups, revealing interesting trends such as higher survival probabilities for female characters and lower risk of death for characters who switched allegiances.

## Utilities Used

The following tools and libraries were used in this analysis:

- **R**: For statistical analysis and survival modeling.
  - `survival`: Used for survival analysis.
  - `fitdistrplus`: Used to fit probability distributions to the time-to-event data.
  - `ggplot2`: For visualizing the survival and hazard functions.
  
- **Minitab**: For parametric survival modeling, including obtaining parameters for the Weibull distribution.
  
- **Markdown**: For documenting the results.

## Conclusion

The survival analysis of *Game of Thrones* characters revealed several key findings:

1. The Weibull distribution provided the best fit for modeling the time until character death.
2. **Sex**: Female characters survived longer, with males facing a higher hazard rate early in their screen time.
3. **Social Status**: Lowborn characters had a better survival rate in early screen times, while highborn characters faced a continuously higher risk of death as the show progressed.
4. **Allegiance**: Characters who switched allegiances had a lower risk of death, especially in later screen times.

This analysis provides a detailed examination of the factors that impact survival in *Game of Thrones*, and demonstrates how survival analysis can be applied to narrative-based datasets.

## Example Minitab Plot Output

<img width="941" alt="Screenshot 2024-09-25 at 5 12 22 PM" src="https://github.com/user-attachments/assets/a5d89f7d-9d30-4607-93d8-45152c6e9f9f">
<img width="496" alt="Screenshot 2024-09-25 at 5 12 12 PM" src="https://github.com/user-attachments/assets/90389448-d0df-4cdd-90cb-709aa5a5057c">
<img width="649" alt="Screenshot 2024-09-25 at 5 12 02 PM" src="https://github.com/user-attachments/assets/68501dc6-6128-4d21-96a3-7e3477de4776">

