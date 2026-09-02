# coral-reef-pollution-analysis-caribbean

**Overview:** This project examines whether pollution levels (sewage, industrial pollution, siltation, and trash) are associated with coral bleaching and disease incidence across over 1,000 coral reef sites in the Caribbean. It also tests whether distance to nearest human population center predicts coral bleaching or disease.

**Findings:** Coral reefs in the Caribbean that suffer from pollution frequently have greater levels of bleaching and disease, which are key indicators of coral health. In particular, sewage, industrial pollution, and siltation were all significantly associated with coral bleaching and/or disease incidence, with siltation showing the strongest and most consistent effect across pollution levels. Distance to nearest population center was not a significant predictor of either outcome. 

**Data:** The data set included >2,000 reef-level observations throughout the Caribbean. The data can be accessed upon request from the Reef Check Foundation but is not included here due to data-use restrictions.

**Acknowledgement:** Thank you to the Reef Check Foundation, its chapters, and its volunteers, who have spent countless hours collecting this data. This project would not have been possible without their contribution. 

**View formatted analysis:** [https://htmlpreview.github.io/ama7738/coral-reef-pollution-analysis-caribbean/blob/main/Coral_Reef_Analysis.html](https://htmlpreview.github.io/?https://github.com/ama7738/coral-reef-pollution-analysis-caribbean/blob/main/Coral_Reef_Analysis.html)

**Methods:** 
- ANOVA and Tukey HSD post-hoc testing to compare mean bleaching and disease levels across pollution categories
- Shapiro-Wilk normality testing to check ANOVA assumptions. Where ANOVA was not applicable due to small sample size, Kruskal-Wallis rank sum tests and pairwise Wilcoxon tests were used in place of ANOVA and Tukey
- Linear regression and Pearson correlation to test relationship between distance to population and coral bleaching / disease
- All analysis and figures created in R using tidyverse, ggpubr, and cowplot

**Key Results: Coral Bleaching**

Analysis of variance revealed a statistically significant difference in coral bleaching by level of sewage pollution (F(3, 2837) = 3.43, p = 0.016) and siltation (F(3, 2856) = 7.34, p < 0.001). Tukey’s post hoc tests revealed that coral reefs with medium sewage pollution had significantly more coral bleaching than reefs with low sewage pollution (p = 0.036). Reefs that always experienced siltation had significantly greater bleaching than reefs that experienced siltation often (p = 0.047), occasionally (p < 0.001), or never (p = 0.021). Error bars indicate standard error.  * indicates statistical significance at p < 0.05 and ** at p < 0.01.

**Key Results: Coral Disease Incidence**

Analysis of variance showed a significant difference in coral disease incidence by level of sewage (F(3, 781) = 4.64, p = 0.0032) and siltation (F(3, 802) = 19.96, p < 0.0001). Tukey’s post hoc tests showed that reefs with no sewage pollution had significantly less disease incidence than reefs with medium sewage (p = 0.0085) and high sewage (p = 0.044). Reefs with constant siltation had significantly higher levels of disease incidence than reefs that often had siltation (p = 0.0057), occasionally (p < 0.0001), and never (p < 0.0001). Error bars indicate standard error. * indicates statistical significance at p < 0.05 , ** at p < 0.01, and *** at p < 0.001.

**Key Results: Distance to Population**

Linear regression revealed no statistically significant relationship between distance to nearest population and coral bleaching (p = 0.717) or disease (p = 0.909).

See coral_reef_analysis.html for full annotated code, output, and figures.

Author: Annabelle Mauri

