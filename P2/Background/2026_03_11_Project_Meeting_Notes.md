	- Aim 1:
		○ For both 1a and 1b, the outcome of interest is the change over one year
		○ For aim 1a, the baseline value for cytokines and for 1b, looking at the 
		change of cytokines
	- For the power calculations, there is not enough information. 
		○ In background of grant, there are some regression models (t-statistic or 
		parameter estimate, is this helpful for the power? Here, we are doing 
		correlation)
			§ Do we have reasonable estimates of what the correlation is expected to 
			be? No. 
			§ Since there are figures in the preliminary data, can we have the 
			preliminary data? Yes, that data can be made available to you for some of 
			the variables (~30 people, some memory outcomes and inflammatory outcomes).
				□ Will give you a sense of the range of correlations that we might expect
	- Dichotomizing amyloid deposition could be feasible. Want to know in general 
	if they are related. Would be interested to also explore if this other cutoff 
	is meaningful (does this have a stronger association than just the continuous 
	variable?)
		○ Think about the fact that you have a potential cutoff when trying to 
		figure out the power for that. To do something that is a little simpler
	- The aims both specify the population as being aMCI but there are also HC 
	subjects recruited. How should we approach the analysis then? As noted in the 
	grant, the HC allows us to have a broad range in memory decline, as we do see 
	this in people who are not diagnosed. Hoping to get a broader range of memory 
	decline variables and possibly inflammatory variables. Not interested in 
	comparing the aMCI and HC individuals. I know there are differences in 
	inflammatory markers and I think they are related to the memory decline. HC 
	may have lower levels of inflammatory markers and less decline, so if we 
	adjust for if you are a control, it will remove the effect that we are trying 
	to identify (might be a mediator). Good to consider/investigate. For this, 
	analyze them together as a diverse population. 
	- Minimum possible power would be 80% for a reasonable number of things we 
	are looking at. Don’t need to power for secondary, but if you told me you were 
	going to do a range of correlations and it wasn’t 80% for all of them, that is 
	ok, but don't want just one that is 80%. 
	- Modeling each predictor separately has a bunch of different models, so that 
	may not be ideal. But if they are correlated, then a joint model would also 
	cause issues. The tradeoff to think about is that it is a lot of models but it 
	is not impossible to run all of them (and you are not doing them here). The 
	preliminary data is not enough to determine if the inflammatory markers are 
	highly correlated or not. 
		○ You could describe what you would have done with the preliminary data and 
		explain if you would do a joint or individual models based on what the data 
		looks like. For each case, you would have a different test (group or 
		individual or maybe not, up to you). If you did it x way, here is how I 
		would test and here is my power. Or, you could pick one and have the others 
		be sensitivity analysis. 
			§ If you look at what is required for the power calculation, you wont' 
			have different ones for the different models (regarding what parameters 
			you need to specify). A range of correlations but that can apply to 
			multiple outcomes. 
			§ If you do all the models, you have to have a plan of how you would 
			summarize them/make sense of all of the models. 
		○ In this case, we don't have enough information to specify the overall 
		test with all 4 predictors in the models at once. The problem is we don’t
		know how correlated they are, which could inflate the variance/reduce the 
		power. For this purpose, it is hard to do a power test for the omnibus test 
		(need to be able to specify all the correlations among all the variables and 
		each with the outcome, but we don't have that information). Powertools could
		do explained and unexplained variance, which would be reasonable, but may 
		still run into the same problem, would need to look into the documentation. 
		○ A lot of the explanation will rely on what the actual correlations will be
		(might be under or over powered). Is there a case to be made for a much
		bigger sample size or not? Here, we are stuck with this sample size for this 
		grant. 
			§ Need to propose analysis that has reasonable sample size for some of the 
			questions given the range of correlations from preliminary data
	- Simulated data will allow you to see some correlations, just not for all 
	outcomes/predictors (just 2 of each).
		○ You will give a low score if you give power of 20% because you choose 
		bonferroni correction as then the grant is not competitive. How will you 
		organize the description of it. Including a discussion about p-value 
		adjustment (there should be some adjustment), but especially for Bonferroni,
		note why it might be highly conservative (correlated variables and many 
		tests).
			§ Bonferroni is too conservative, so could choose something different
			(explain why it is reasonable to choose something different).
	- Can reference tables and figures already in the grant (e.g. Table 3)
	- When doing the sample size correlation with correlations from preliminary 
	data, do we want to test a few options that are greater or less than the 
	range. If it helps to make the case then you can include this. 
	- For aim 2, there is a question about interaction. You can use another 
	package than powertools if you want to, but there is a relatively simple way 
	to use something in powertools with correlation.
		○ Thinking about the interaction, can that test still be within the 
		correlation sphere given the other information from the investigator on 
		correlations for amyloid deposition. 
	- Feel free to write and respond to email. Feedback should be by Friday on 
	your initial plan. 
			
