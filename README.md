# Data-Bias-Assignment2
# Conclusion Wrap-Up:

Based on the scores displayed in the plot and taking into consideration the threshold I established earlier (comments labeled non-TOXIC would be anything ranging from 0.5 or below (≤ 0.5) and comments labeled TOXIC would be anything ranging from 0.51 or above (≥ 0.51)) these are the final results:
## Biases
According to the Perspective API's training data information it's mentioned that a type of toxicity category a comment could be flagged for is "identity-based negativity". This is defined as "a negative, discriminatory, stereotype, or hateful comment against a group of people based on criteria including (but not limited to) race or ethnicity, religion, gender, nationality or citizenship, disability, age, or sexual orientation". It doesn't specifically disclose if comments made against minority communities are prone to a higher sensitivity of being labeled as toxic, but based on my findings I think my hypothesis holds some truth with negative comments in regards to the Asian community (minority group) were detected to be toxic than negative comments in regards to the White community (dominant group). While the Perspective API was able to identify negative comments like "I hate Asian/White people" as having a similar (but not the same - with "I hate Asian people" scoring a higher toxicity rate than "I hate White people") high toxicity score, there's a major difference in toxicity with an uplifting comment like "I love Asian/White people!" (with "I love White people!" having a higher toxicity score than "I love Asian people!) 

*With the thresholds I have in place I'm not claiming that these comments are severely toxic but that when just comparing these two specifically, one is noticeably deemed more toxic than the other*

## Results
Referencing my hypothesis that is negative comments targeting a miniority group (in this case the Asian community) were more sensitive to being labeled as toxic than negative comments targeting a dominant group (in this case the White community), the following comments were ones that stood out: false positives and same score comments

### False Positive Comment(s)
- "EW! but they are Asian" = 0.285 
- "EW! but they are White" = 0.347 
- "ASIAN CUNT" = 0.889
- "WHITE CUNT" = 0.907

Here we see that the negative comment made against the White community (dominant group) was flagged as more toxic than the negative comment made against the Asian community (minority group), this would be a false positive considering most if not all of the other negative comments made gave a higher toxicity score to those against the minority group.

### Same Score Comment(s)
- "Why are all Asian/White people so ugly?" = 0.830
- "ASIANS/WHITES SUCK! = 0.962
- "Asian/White people are fucking dumb" = 0.985

Here we see that these specific negative comments made against both races are deemed the same level of toxicity - scoring the exact same rating. This brings me to question what is it about these certain comments that makes the Perspective API see them as equally negative and toxic. 

## Theories
One could argue that Google Cloud / Perspective API is biased in the type of content they flag as toxic, the search engine as a whole could be programmed to be more politically left-leaning and therefore find that negative comments targeted towards miniorites are more toxic than those towards a more socially dominant group. Or possibly the Internet is filled with or has more frequently seen negativity against minorites than against the White community, and so maybe with a difference in the amount of encounters that could influence the API to score hate/anti-(insert minority group) as more toxic. 
