	- Risk factors are listed, hypothesis lists risk profile. What is that defined 
	as?
		○ A lot of risk factors in the data. Some variables that known interest/want 
		included in analysis: age, diabetes, blood pressure
			§ Interested in baseline values only
			§ Systolic blood pressure
	- Several risk factors that not sure about inclusion. Questioning: presence of
	coronary heart disease, blood pressure medications (y/n), smoking status 
	(current smoker or not), total cholesterol, bmi
		○ What is correlation of bp and bp medication? Might limit ability to 
		include in model
	- Outcome: survival from stroke
	- Stroke == 1 at baseline => stroke in the past
		○ Not interested in these people, only want those who have a stroke during 
		the study
	- No other exclusion criteria besides normal things like missing values or 
	values that look weird for any covariates
	- Don't take into account competing risks (e.g. death, MI, etc.). Can comment 
	on limitations of that, but not interested in the other events for analysis. 
		○ Event happened beside stroke can be treated as censored (ignore other 
		competing events, if they died it will be marked as censored. Also if 
		anything happened after 10 years, want it to be censored for this analysis)
	- Treat data as though you stopped at 10 years, as follow-through was better 
	here
	- For this analysis, only interested in the fit, not including any time
	covarying pieces. Use covariates measured at baseline. But interested in if 
	that would be good for the future if the values would improve. Nothing formal, 
	just descriptives of if the variables are changing over time of if a time 
	varying model would be good and implications of not doing time covaring model.
		○ Mainly just interested in the variables diabetes and blood pressure if 
		those change over time
	- Assume average 2-3 leap years in the 10 year period, use 365.25 to account 
	for that
	- Only variables mentioned are ones of interested, no need to do further 
	exploratory analysis on other variables
	- Stratify by sex: interested in risk factors separately for both sexes. 
	Imagine it being separate. One model for males and one model for females,
	stratify to two different datasets.
		○ Really interested in what risk factors are predicting stroke for both of 
		the sexes separately, so whatever model will get you to that is preferred. 
		No need to restrict to them being the same set of covariates if the modeling 
		doesn't land that way
			§ If there are different risk factors by sex, that is ok for final models
	- 3 different periods, all there together. File outlines how it is all 
	organized within the three different time periods. 
	
