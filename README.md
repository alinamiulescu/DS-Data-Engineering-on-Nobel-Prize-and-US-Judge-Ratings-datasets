## EDA on Nobel Prize dataset

The first part of this exercise consists of finding and eliminating dirty data in the Nobel Prize dataset. The final aim is to have a cleaned dataset that is ready to be explored by EDA. The following points are considered:

a) the first Nobel was awarded in 1901

b) replace empty strings, i.e. '', with NaN

c) some names are marked with an asterisk, denoting that these winners are recorded by country of birth, not country at the time of winning the prize. Clean up those names by removing the asterisks and strip any remaining whitespace. Generate a flag variable that equals 1 if the country is the country of birth

d) some names are duplicated. This could indicate that some people have won the Nobel Prize more than once. However, it could also be that a winner is "claimed" by more than one country. Remove all real duplicates. For instance, Marie Curie is contained 4 times: twice for Poland and twice for France: remove 2 of them e) consider the missing values in the field category. Are they really missing or just entry mistakes? f) is there an explanation of the missing values of the field gender? Remove all rows without gender

g) what about missing values for date_of_birth?

h) convert the date_of_birth into a Numpy datetime64 object. You may replace incorrect dates, e.g. 'None', by NaN. Determine the winners' ages by subtracting the prize year from date_of_birth


## Apply PCS on US Judge Ratings dataset

In the file JudgeRatings.csv, you can find the information about Lawyers' ratings of state judges in the US Superior Court. The file contains 43 observations on 12 numeric variables.
- CONT Number of contacts of lawyer with judge.
- INTG Judicial integrity.
- DMNR Demeanor.
- DILG Diligence.
- CFMG Case flow managing.
- DECI Prompt decisions.
- PREP Preparation for trial.
- FAMI Familiarity with law.
- ORAL Sound oral rulings.
- WRIT Sound written rulings.
- PHYS Physical ability.
- RTEN Worthy of retention.

Apply PCA to the 12 components after standardizing. Determine how many components to use based on:
- Eigenvalue Criterion
- Proportion of Variance Explained Criterion (with a minimum of 90% variability)
- Scree Plot Criterion Communality
