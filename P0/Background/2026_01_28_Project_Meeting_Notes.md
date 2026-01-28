	- RQ1: mixed effects model
		○ Random intercept for subjects and nested random intercept for days to account for repeated measurements by subject and repeated measurements within each day. Google says format is (1 | subject / day) in lme4/lmer
		○ Pearsons correlation bad because repeated measures
		○ Fit linear mixed model to data
			§ Expect intercept and slope to be 0/1 if perfect agreement. You will get estimates for intercept and slope that are not perfectly 0/1, so explain what that means to the investigator. If the slope is close to 1, then 1 min change in cap is associated with 1 min change in booklet (strong "association"), if the intercept is getting shifted up or down it could give evidence for some level of bias (on average earlier or later) 
		○ Keep it simple, random intercept for subject (done). If you think you need a random intercept nested within day, see if the model converges/singularity/if anything changes
			§ Often models can explode so ok to take things off/back up
			§ Minimum is random intercept for subject to account for that aspect 
				□ Could argue that the days are more replicates than repeats 
				□ Or could go super fancy, but most improvement is with the random intercept and minimal improvements beyond that that may challenge model convergence 
	- RQ2: Visualization is OK
	- RQ3: Spaghetti plot for all days all participants

Class notes:
	- RQ1: 
		○ Investigator showed scatterplot of cap min from wake (x) and booklet min from wake (y) with a line through it and some type of correlation. Won't work with correlation.
			§ LMM (outcome is book min from wake, predictor is cap time from wake with random intercept for subject)
				□ Does the cap time predict the book time? 
				□ Will get from this model an intercept and a slope (need to interpret and explain how they answer the RQ about agreement)
					® Expect if perfect agreement to be 0 and 1. Fit your model and get some values and they will likely not be 0 or 1 (what does that mean to the investigator?). 
			§ If for some reason there is a compelling reason to control for there being multiple days (1-3), you could see if that matters. We would hope that people's observations across the day would be correlated. 
			§ We do want minutes from sleep diary reported waking time
			§ In table 1, might want to present descriptive stats for the difference between book and cap times
	- RQ2:
		○ Meant to be simple
		○ Descriptive statistics (figure out if observations fall in window, summarize them)
			§ Don’t need any tests for it, if you want you can offer the CI or something but really just cares about the proportion within the regions
	- RQ3:
		○ Investigator thinks in first 30 min, the hormones should go up and then slowly decrease over time 
			§ Is there a significant increase from 0-30 and what's the rate of decline over the rest
		○ Piecewise regression with knot at 30min
			§ LMM still because repeated measures
			§ Likely booklet time is better because there is less missing, don't include those with missing time or missing cortisol/DHEA unless you want to impute from other time option, but may cause issues if they do not agree
Report and presentation due 5min before class on Wednesday
	- Assigned to 2 different classrooms for presentations
Presentations downloaded from canvas onto the desktop (pdf/ppt doesn't matter)