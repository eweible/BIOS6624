	- Makes sense to use the baseline covariates rather than the change for those 
	that change (e.g. age, bmi). Want to control for where they started.
	- Can differences between hard drug users and nonusers be explained by 
	differences in adherence
	- Want viral load counts to decrease and CD4 count + quality of life increase
	- BMI not exceeding 250 as I did
		○ How many of each predictor are missing (1 smoking and 57 BMI from Kayla)
	- 95% HPDIs for Bayesian - don't recall if I explicitly stated this in report
		○ Exclusion of 0 for association, pvals for frequentist
	- Make sure to investigate MNAR (looking at relationship between missing and 
	nonmissing for each outcome)
	- Frequentist: pvals and 95% Cis, Bayesian uses LOO_CV and 95% HPDI (posterior 
	medians from Maddie (?)
	- Maddie had two tables, one for outcomes of interest at each year and another 
	for the covariates at baseline both by hard drug use
	- Smoking grouping is OK

	- Reproducible research guidelines:
		○ At end of report:
			§ Make sure to include link to github
			§ Include full datapath link to local data location (not just from working 
			directory)
	- For table 1 and analysis, use complete case analysis. Say in report that 
	there were 715 people and there were 476 with complete data, shown in table 1. 
	There are some missing data in covariates.
		○ Explain how you got to final sample size that goes into models.
	- Mediation analysis 
		○ Compare models with and without adherence. Probably also want to talk 
		about if there is a difference that you can see between hard drug use in the 
		table 1
			§ Don't need to report %mediated or anything like that.
				□ Are there differences in adherence? Is there a relationship/difference 
				there?
				□ Fit adjusted and unadjusted model. Is there a change? What % change? 
					® Do for each outcome and for each type (frequentist and Bayesian)
						◊ OK if you don't write that much for frequentist analysis in 
						report, it is there for you to make sure your Bayesian analysis is 
						not weird.
						◊ Big giant table of results:
							Freq			Bayes	
						PE	CI	P	PM	HDPI	PP (might say PD) or DIC
						◊ Interpretation, can say that frequentist mostly agrees with 
						Bayesian
						◊ Clinically meaningful differences useful for posterior 
						probabilities 


	- Interested in treatment response between hard drug users and non hard drug 
	users and whether that can be explained by adherence
		○ No interactions needed
	- Different MCMC program that you would prefer is fine, just make sure to 
	writeup what method you used, correctly explain what sampler you used, 
	- Report: focus on Bayesian analysis but still report frequentist analysis
		○ Focus on interpreting Bayesian analysis. Can say, We find similar results 
		from the frequentist analysis, see the table. If different, explain 
		differences (or investigate yourself if something may have gone wrong)
	- Adherence: could be collapsed. Clinically, >95% and <95% make sense (highest 
	category is 100% but that is hard to achieve and suspicious). So collapse top 
	two and bottom two categories. 
	- QoL scores should be between 0-100. Should not be below 0. 
	- Smoking (already done): current vs non-current smoker
	- Have to show all of the models in your code. You can fit each model in a 
	separate file if you prefer. 
	- Mediation analysis: if there is no significant effect of hard drug use, 
	still do a mediation analysis for that outcome (do it regardless of 
	significance)
		○ Does it explain any differences (or not being a difference)
		○ Don't need to fit the model between Hard drug use and adherence (small 
		sample size for logistic regression models esp for Bayesian), can be 
		descriptively discussed (diff in adh between drug use groups, just fit 
		models with and without adherence) (% change)
			§ Fit in both frameworks, report adherence estimate, but we care more 
			about the change between the models for hard drug use (adherence can 
			explain, hence reporting. Covariate changes don't need to be reported)
				□ Put into table of regression results (don't need to include covariates 
				here, but def include in Table 1) 
	- Posterior probabilities: if you got a 90% posterior probability of their 
	being a clinical effect (that seems pretty high). Report the value, can state 
	if it is high
	- Clarifying questions:
		1. For each analysis, would you prefer I use the 476 subjects who have all 4 
		outcomes at baseline and 2 years (and baseline hard drug use), or would you 
		prefer that I restrict to the subset of 463 subjects who also have complete 
		baseline covariate data?
		
		463
		
		2. I excluded two implausible BMI values (515.01 and 514.25) based on a 
		cutoff of 250. Does this approach seem clinically reasonable, or would you 
		prefer a different strategy?
		
		fine
		
		3. Not a question, just a clarification that I plan to adjust for the 
		baseline value of each outcome in the corresponding models, which I did not 
		explicitly state in my plan.
		
		Make sure to write in final report
		
		4. A question for the statistician - Is a half-normal prior with mean 0 and 
		variance 1000 an appropriate choice? As I noted, I am planning to use 
		vaguely informative priors, and this would align with the prior variance for 
		the regression coefficients. 
		
		fine, look at sd of outcomes (residual se should be less). plot half normal 
		prior to make sure it will cover this)
	
