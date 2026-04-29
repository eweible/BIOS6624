Project 4 will cover variable selection
	- Carter generally says don't do it, but sometimes it is warranted 
		○ E.g. for looking between MAR and MCAR 
			§ Models can get really big, so maybe want to do a variable reduction
	- Can overfit, can give you different models for different datasets (model 
	itself is a random variable)
		○ The variance of what actually got selected in the first place is missing 
		in the variances reported by the final selected model
	- Do variable selection grounded in what is scientifically important
		○ If they are all independent of each other, no need to do variable 
		selection 
	- Very different methods to do variable selection
		○ Evaluate from a simulation perspective which one will give you the best 
		result?
			§ How do we define best?
	- No need to hard code selection processes (OK to use from packages)
		○ Start building function outline with backwards selection with the mind 
		that it is easy to add to it as we continue to learn about the additional 
		variable selection methods. 
			§ Characterize methods
	- gendata function should be used from library(hdrm)
		○ How can we set the correlation? Corr and rho 
			§ Exchangeable and autoregressive (2 correlation patterns, looking at 
			correlations of parameters). Exchangeable is constant correlation between 
			all, autoregressive is a decrease based on the position (power) 
		○ How do you want to do it?
			§ Project is asking for some variables to have 0 betas. Value of 
			correlation. For now, how do we want the correlation pattern to be? 
			Exchangeable will be easier to interpret/think about, so let's go with 
			that. 
			§ Take 3 cases for rho (0 (all independent), something middle (0.35), 
			something high (0.7).)
	- For lasso, really want to understand how these different methods compare to 
	each other, so we want simpler decisions for lambda (generalized cross 
	validation). 
	- All predictors should be continuous (don't think you can change this in 
	gendata), betas already in the project (don't change those). Vary the 
	correlation and the method and the sample size. 
	- Same distribution for the error term (standard normal, don't change). Betas 
	stay the same. 
		○ Only vary sample size, correlation, and method
	- Intercept will automatically be created with lm or whatever you use, don't 
	need to make in the data. Not something you can change, don't worry about it. 
	- Assuming that for the ones that have no relationship, we are assuming there 
	is a correlation but no direct effect on the outcome
		○ Take a large sample to get an estimate of what the dataset looks like and 
		do a correlation table to verify
	- Report intended to a clinician or investigator, not biometrica (for someone 
	not stats focused)
	- Can test p-value criteria with step function from R. You need to pick k 
	(appropriate quantile from chisq dist) as qchisq(1-criterion, df=1)
		○ P = 0.05 is a 0.95 chisq criterion
	- For lasso/elastic net, take final list of estimates and reestimate it under 
	lm or whatever you are using for consistency/interpretability
		○ There are several different approaches to variable selection. The purpose 
		of this project is to compare the performance of these approaches in 
		moderate sample size cases. The lasso and elastic-net were developed for p>N 
		problems, but have been widely used in many common regression modeling 
		problems. In this project you will see what benefit (if any) the lasso and 
		elastic-net have over more standard model selection approaches taught in 
		your first regression courses in graduate school
		○ For this project, you may leave alpha at 0.5 

  # basic call to glmnet-uses a range of lambda values:
   lasso_mod <- glmnet(x[,-1]             # predictor matrix, intercepts are not 
   to be included
                      , y                  # outcome
                      , alpha = 1          # = 1 makes it lasso
                      , standardize = TRUE # default, just calling it out, make 
                      sure your vars are standardized
                      )
	- For project, you choose 2. For example, you can do: Lines are largest lambda 
	value 1 sd from min and where lambda is minimized
		○ Plot from: 
		  set.seed(463784)
		  lasso_mod_cv = cv.glmnet(x[,-1]             # predictor matrix, intercepts 
		  are not to be included
		                      , y                  # outcome
		                      , alpha = 1          # = 1 makes it lasso
		                      , standardize = TRUE # default, just calling it out
		                      )
		plot(lasso_mod_cv)
		○ E.g. can get values from: 
		  lasso_mod_cv$lambda.min
		  coef(lasso_mod_cv, s = 'lambda.min')
	- One iteration of sample size: 
	sol <- coef(lasso_mod_cv, s = 'lambda.1se') 
	nsol <- rownames(sol)
	nsol <- nsol[sol[,1] != 0]
	nsol <- setdiff(nsol, '(Intercept)')
	
	lm_fit <- lm(y ~ . , data = dat2[, nsol])
	
	summary(lm_fit)
		○ How do you choose how many to run? How many replications for each dataset? 
		Number of simulation iterations. Paper on simulation from first week 
		(Albert?) and big table of different types of ways you can measure the 
		simulation (bias, MSE, coverage). Pick the one that is important to you, use
		asymptotic simulation standard error, basically do a power analysis to get a 
		sample size estimate. Otherwise, do it 10,000 times. 
			§ Set seed at beginning of your process and run it through a loop
	- Glmnet does not give you any standard errors, so you can't do tests. For 
	type 2 error, calculate by the values (simulation values, run simulation and 
	test to see if parameter is significant. If simulation value is something not 
	0 and do a bunch of times, you get mean of if it is significant or not, which 
	gives you power. Below 0.05 is significant like normal). Glmnet can't do this 
	as it doesn't provide standard errors (not meaningful typically). Instead, 
	refit model using lm, get estimates, and then do tests and calculate your 
	errors that way. 
		○ If it doesn’t select the var into the model, then it is insignificant by 
		default
		○ Type I and type II for up to 5 variables (20 vars, 5 important, 15 are 0). 
		Type I error needs to be done in a setting where there is no relationship 
		with beta 0. So essentially, for the 5 vars that do have relationship with 
		outcome and 15 that don't, so if you calc power for 15, that gives you type
		I error (know not significant, how often do they appear significant)
		○  To be significant, it has to be selected and the test that you run post 
		selection has to also be significant. Otherwise, insignificant. 
			§ 0.157 with selection process when applicable
	- Here, correlation of 0 is representing independence
		○ 1a is independence (corr = 0)
		○ b is setting correlation (suggests more than 1 level: 0, 0.35, 0.7)
			§ We have uncorrelated case and correlation. Not a particular correlation, 
			but generally moderate correlation and looking at trajectory. This covers 
			1a
		
