	- Codebook is from parent study, so includes variables that are not relevant to this project. Dataset is cut down and includes all that are relevant
	- smoking, only interested in hard drugs at baseline (year 0)
	- For the outcomes, are we interested at viral load, CD4, and quality of life? 
	- What are you interested in adjusting for? 
		○ The main variable we are interested in is the hard drug use variable.
		○ Normally in HIV studies, we adjust for age, BMI, smoking status, education (tied to income, just do education), race/ethnicity, adherence
			§ A question that the investigator has is that obviously hard drug use could influence someone's adherence to the medication, so curious if any differences in the outcomes between hard drug users and non hard drug users could be explained by adherence? 
			§ Adherence to the HAART treatment. There is an adherence variable (adh)
				□ Difference in CD4 or viral load can be explained by differences in adherence? (Mediator)
				□ Can other outcomes be explained by differences in adherence between the two drug use groups
		○ Only looking at baseline hard drugs, not concerned about y1 or y2 drug use. Problematic because it is a thing that changes over time, but we will stick with just baseline
			§ Do not care at all about outcome at year 1 (looking at treatment response at year 2 and hard drug use at year 0)
		○ No assay limitations/weird stuff expected for viral load or CD4 expectation. Ranges in data dictionary, bring up outliers if specific, but shouldn’t be anything crazy
		○ For refuse to answer for hard drugs, how do we include them? Yes/no/refuse to answer? Then they are missing, we don't know what the values are (don't want to make any inferences) 
	- How to envision treatment response? 
		○ Interested in all 4 outcomes (biological markers that are meaningful to clinicians (getting better) but also want to make sure that people are feeling better as well. Antiretroviral treatments have a lot of side effects, so even if immunological values are improving, they may not feel better due to side effects). 
	- Bayesian analysis seems cool and interested in using it, but no priority ideas about how it will be implemented
		○ Run analysis both ways and see if you find anything different
		○ Use STAN
	- CD4 and VLOAD have ranges in the value 
		○ CD4 t cell counts depend on if someone is treated or not, a lot of times treated value is around 300-500, viral load is probably going to be really really high (number of viral copies in blood, can be in the millions when untreated and can be undetectable when treated). Quality of life scores should be 0-100
	- Would you recommend a difference in outcome from y2 and baseline or just y2? Do we care about baseline/do we need baseline? Yes as this is an observational study (not randomized, may be differences in baseline for hard drug user groups). Baseline seems important to include. However you want to handle it is up to you. 
		○ For the other covariates that we are looking at, use baseline (expect race, etc. not to change, but education could potentially change)
			§ Use baseline values with the idea looking to see what factors that exist at baseline that are related to the treatment response. 
	- 4 different outcomes looking at, all important (not one primary outcome). Viral load going down would mean treatment is working as intended. CD4 counts recovering is also a good immunological sign that the treatment is working. But side effects are strong so also want to look at the quality of life scores 
		○ Is there a preference of inflating type 1 error rate or combine quality of life scores to go to 3 primary outcomes? 
			§ Outcomes are hopefully strongly associated with one another, so viral load going down would be inversely associated with CD4 counts going up. Hoping improvements in those would also translate to improvements in quality of life
				□ Not independent outcomes, expect to change together in predictable ways. (Changes the number of tests you may want to perform)
	- Can we merge some levels of race/ethnicity? Or not include all of them in the model? Look at data then return with suggestions.  
	- Adherence is self-reported categorical groupings 
Important point in discussion (study results and how they might be influenced by missing data or dropout. Be mindful of missing data but not much you can do. Could discuss dropout in relation to hard drug