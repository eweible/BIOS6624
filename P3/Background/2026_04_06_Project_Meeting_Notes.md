Notes on last time:
	- Separating by males and females. Do we want the same set of variables in both models? 
		○ Amend previous statement. Don't care if they are set to be the same or if they are different based on your variable selection as long as you can explain why you did it that way. 
			§ Pros and cons: same vars = way easier to compare them by sexes. Say you want to compare BP by sex but different sets of variables, you are not adjusting for the same things so not a direct comparison. Diff vars = two groups may have different correlations structures (e.g. differences in multicollinearity), differences in the effects 
				□ Initial exploratory study so either is fine, just explain why and the implications. If you do choose different models, you can’t directly compare
				□ If you choose the same, add variables that are present in either variable selection (e.g. males have cholesterol, so add to both final models). May be due to instability of variable selection
Some of the covariates are missing data at baseline. Should we do complete-case? Do all covariates need to be present?
	- In the final model, use as much data as possible, so if you exclude a variable with missing data, bring that data back in. Use complete case for any missing in the final model
Censor for stroke at date of death if not a stroke previously present 
	- Likely already appropriately censored
Want different risk profiles
	- Looking for estimates for the 10 year survival (or however it is worded) for ages 40, 50, and 60. For each of these ages: want estimates for someone who has baseline no risk factors (average profile without any risk factors) and for someone who has high blood pressure (defined as 160 for SYSBP), diabetes, high blood pressure and diabetes, and one additional profile that you think is interesting based on covariates included in the model and calculate survival for that. 
		○ Table with rows as 40/50/60 and columns as baseline/BP/diabetes/both/other
			§ 5 scenarios across 3 ages, separate table for each sex
Aim of study: compare more within or between sex?
	- More within sex. Not to compare the sexes, there is expected to be sex changes which is why there are separate models.
When testing proportional hazards assumption, look at it for everything but in practice, you can say that we felt the proportional hazards assumption was met for all the variables in our model. Start by looking at everything, categorical and continuous variables. 
	- Most important for the ones you are interpreting as that is where you can run into problems
	- Schoenfeld residuals works for continuous, for log-log survival plots might split it up
What do you consider baseline risk factors?
	- Know that I want in the final model age, diabetes, BP
	- Other vars not sure: coronary heart disease, BP medication, current smoker, total cholesterol, BMI
	- Not interested in any other variables in the dataset
For the table at baseline, average the continuous variables and for the categorical, interested in things that aren't risk factors (non-smoker, not on BP medication, etc.)
	- Survival probability for someone with each profile with final model after variable selection
		○ Single number estimates
