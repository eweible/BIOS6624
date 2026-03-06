Office Hours Notes:
	- Make a correlation matrix just among all the different inflammatory markers 
	to understand the correlation between them 
		○ Could do individual models to understand what is going on there but you 
		are relying on your inference to be the overall f test 
		○ There are approaches where you can do an overall test and then protected 
		comparisons after that (if it is significant, is there one of these that is 
		driving the f test? More descriptive). Some sort of step down testing. Or 
		informal ways to say that they are all pretty consistent or not. What could 
		you provide then to the investigator from the multiple regression to 
		understand the overall and individual contributions of these markers.
			§ P values from beta estimates, actual estimate (depending on how you 
			coded the variables, they may all have different scales, so maybe think 
			about how you could report something standardized on the same scale (e.g. 
			1 sd change). 
	- In table 3, there are 9 variables. But, we should all go back into the text 
	to make sure we understand these whether or not the 20 min delay total correct 
	if it is the total correct after or are those two separate things (think they 
	are 1). Look to see if described clearly. Right place to look to see what the 
	outcomes are, use the text to go back and understand what they are and 
	determine if there are 9 or 5. We can followup on that. 
	- For aim 1, we are hypothesizing that higher baseline levels effect memory 
	and cortisol thickness, what change was expected to see? What is an expected 
	change? We have some preliminary data that can help to give some of the 
	information on that. Quite a bit from the preliminary data. 
		○ Change is going to be important, also thinking about the model that you
		are going to do, you might not need to specify how much change there is to 
		do power. Once you think of the form of the model and test you will do, you 
		might not need to specify the change to do the correct power analysis. But 
		there is other helpful information imbedded to help with the power analysis. 
			§ This should be clear once you write out your regression model/test and 
			your power. Right now, focus really hard on understanding the outcomes and 
			the form of those outcomes, same for predictors, and then what kind of 
			model. Be clear on those parts first. 
	- Question about secondary outcome for aim 1: AD cortical thickness, in the 
	grant it says that the mean cortical thickness, but later in the potential 
	barriers section, it says that changes in different regions will be more 
	related to the inflammatory markers. But it will still be our outcome? Yes 
	that is correct. For the memory consolidation value, there were 9 variables, 
	do you think including them all and then see what is valuable? Good thought 
	process. A lot here, let's assume there are 9 for now. Try to understand these 
	measures. Given what we are thinking about, even if you are not quite sure 
	what to do with the information, what would you like to know from 
	investigator? What are the important ones? Memory consolidation has long term 
	consolidation, recall, and pattern. Is one in the past proven to be a better 
	predictor of cognifive function. For the purposes of this project, the 
	investigator says not really, it depends on the context of the study. We will 
	want to be able to talk about each of these measures. We typically don’t pick 
	just one because individual symptoms of memory decline can show up 
	differently. Individual-level differences are present here, so can't just pick 
	one (restricting to one type of cognifive decline but we want to be general)
	- There are 4 key inflammatory markers but we will be measuring a lot more. 
	Later in the grant we would like to look at more but these 4 have good 
	preliminary data. C5A listed which ones will be used in primary analyses. 
	- Aim 2 expected outcomes, there are phrases of significant and elevated. 
	Another thing that we don’t have values. We think that more deposition will be 
	worse but not an absolute threshold available. Thresholds have been proposed 
	but we don’t have one yet. 
	- Are all the possible covariates in C.4 standard procedures. Wondering about 
	a good way to tackle all of them/deciding which are more relevant. If there 
	are not things that have to be in the model, how might you approach choosing 
	covariates? What matters in terms of those variables for putting them in the 
	model? Whether they effect both the outcome and primary explanatory variables. 
	If they effect both, it has the potential to be a confounder. What if it is 
	only related to the outcome? Then it is a precision variable (esp in linear 
	regression). Almost always, if something is "significant" predictor of 
	variation in the outcome, you will increase your power of detecting other 
	effects because you have reduced your residual variation. We are interested in 
	if it is a precision or confounding variable. Do you know if a particular 
	variable happens to effect the outcome? Have you shown previously that these 
	variables are related to cognitive decline? Or other outcomes? Are these also 
	related to the inflamatory markers of interest?
		○ Potential to just draw the picture on the board. Memory on one side and 
		inflammation here. Where do the other variables fit in? As investigator, 
		anything related to inflammation has the potential to be related to 
		inflammatory markers and outcome. Sample size is not big enough to include 
		anything. Need to be able to say that the associations aren't because we 
		didn’t account for a measure of inflammation. Need to be able to describe 
		what the relationships could be. APOE is a big one (best predictor of 
		cognitive decline, whether or not it is relevant here). 
		
Can you describe what the data looks like? Will there be a need to do data 
cleaning or handling? For instance, creating or adjusting variables? 
	- Not looked at the raw data, always handed it off to someone. People running 
	the labs on inflammatory markers look for expreme outliers, but we look too. 
	Some can be distinct from the clinical population. On the cognitive outcomes, 
	they are pretty straightforward. We will need to know outliers or missing data 
	(hand entered). Will be sending output from RedCap. We typically enter 
	everything into redcap using MRN and study ID. Not typically consolidating 
	variables. 
Do you care about the longitudinal nature, or do you care more about the change 
from baseline to year 1?
	- Really want to know about the change from baseline to year 1 (want to know 
	about the change, this is what we are investigating)
Which of these two hypotheses do you care about more? Are the outcomes for each 
hypothesis equally important? 
	- Hypothesis 1a and 1b are equal. First is prediction/understanding and the 
	second one is (not cause and effect) but wondering if changes are also 
	associated with changes. One is more mechanistic. Think of 1b as a followup to 
	1a. We might not see something baseline as we would change, so we will look at 
	it regardless. Also over 1 year timeframe
What counts as a clinically significant decline for memory consolidation/
cortical thickness?
	- As the investigator, it is just highly variable so we don’t know over 1 year 
	what is clinically relevant. So no benchmark for clinical relevance at this 
	point, just looking to see if we have any ability to see what is related to 
	that decline. 
	

I assume that we are treating APOE as binary (Carrier/homozygous vs. 
noncarrier), is this accurate?
	- Yes carrier vs not for APOE. Relatively few with two copies. 
For those that are associated or correlated, if we have to choose between them, 
which would you prefer us to use? 
	- Mostly leaving it up to us to decide what to include and not include for 
	correlations/associations. Well established that they are associated with 
	cognitive decline. If they help us to understand what is going on with 
	inflammatory markers would like them to be included or otherwise saying that 
	adjusting for one or more didn’t have an impact. 
		○ Probably want to address something about highly correlated will make it 
		look like not associated, so would want to understand what the correlation 
		is among the variables and if you can adjust for them great, otherwise just 
		state they are highly correlated and use general estimates (or don't put in 
		same model because misleading). 
		○ As we are describing how to handle it, talk about (briefly) you will 
		investigate correlations among primary predictors and among all the other 
		potentially related predictors. Which will give a lot of information in 
		terms of what to put in the model. In our dataset, if we look at all these 
		variables and in 1 year of time they weren't all related, do we need to even 
		worry about putting them in the model or not. 
We could test the model with interaction against the model without interaction
but including the individual predictors, or we could test either including 
interaction or including each separately against the model with neither. 
Answering different questions, can you clarify what you are interested in? 
	- Trying to help the investigator understand. Take the main effects and 
	interaction effect present. If that were the model, how would you tell the 
	investigator what you could test in the model. 
		○ Is the effect of the cytokines going to differ by how much amyloid 
		deposition you will get? DO you think the impact of having a high IL6 will 
		also depend on a high amyloid deposition. Does the effect of one of them 
		impact the effect of the other one. 
			§ Could try to draw a picture. E.g. looking at IL6 and change in memory. 
			Hard with a Amyloid deposition because it is continuous. No threshold so 
			definitely treat it continuously. But conceptually, we could pretend that 
			there are thresholds with high and low amyloid. Do we think the 
			relationship is steeper for those with high amyloid than for those with 
			low amyloid? 
				□ 
		○ Biostats perspective, I find there are certain cases where you are working 
		with categorical variables (e.g. two by two table). Sometimes they claim 
		they are only interested in a single cell but you still have to compare it 
		with something else. Statistically, fitting both marginal effects and 
		interactions as needed is more statistically sound. Can write the contrasts 
		afterwards but can protect the type 1 error by doing a standard test. 
		Testing interaction coefficient is often more power.  
			§ Is the effect estimate for two continuous variables interaction 
			interpretable? You have to know what scale each variables are in. What 
			does the interaction term refer to? Write out the model. IF it is only
			the interaction term, we are setting the other two variables to something. 
			Usually report the values to show significance, but to have it mean 
			something you have to say something like the additional change in outcome 
			above the marginal change. Then usually give a table with the expected 
			outcome for different values of the predictors to show the interaction 
			effect. The expected outcome will not change the same with each change 
			in the predictor. 
				□ Common biologically that one is more pronounced than the other, but 
				sometimes the effect of one effects with the effect of the other and the 
				lines intersect. 
Is the 125 aMCI vs 50 HC a reasonable representation of the population? Or have 
you adjusted it to capture more diversity?
	- For this, these are not necessarily proportionally what is in the 
	population, but wanted to make sure to have people at all spectrums of decline 
	and inflammatory. What to know what is happening in population so covering
	range of little to more decline. Probably over sampled cognitive decline. 
		○ Don't need to make a big deal of those proportions. 
		○ Talk about in preliminary data where these numbers came from 
		○ Hoping will be enough, hard to increase. 
			§ Do want to answer the questions, but have to adjust if not enough
Are there specific cytokine/chemokines that you want at baseline? Or just a sum 
of all? Or presence/no presence? Or use each individually, which may not be 
feasible depending on how many are present?
	- Definitely include age, sex, and all cytokines, other things it is mostly 
	for convinging that there is an understanding of the relationships. 
		○ Right now, there is not a good way to combine cytokines. But we could 
		explore that if we needed to. Hopefully including them individually is the
		way to go. 
