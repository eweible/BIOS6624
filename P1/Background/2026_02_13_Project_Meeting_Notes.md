Notes from investigator on presentation: 

Slide 1:
--------

Clinician talks about VLOAD in terms of log10 anyways rather than natural log. 
Don’t need to back transform, log10 would be understandable for interpretation. 

Look at the marginal distributions after covariates. Obviously VLOAD needs a 
transformation, very clear. Look at residual plots to see if a transformation is 
necessary after the covariates. CLT 

Main question is the difference in year 2 between the groups (this is fine). We 
assume that the treatment is working/doing something. But, it has been 2 years, 
so maybe staying stable is a good treatment response since they are not getting 
worse, as this shows stability. So, we don’t care if there is a statistically 
significant change across years, focusing more on the difference between the 
hard drug users and others.

Clinically meaningful differences (two-sided): 
QoL: 2 point change
CD4: change of 50 cells per ___ mL^3
VLOAD: 0.5 log10 change 

Slide 2:
--------

Collapse education to be completing college and above or not college (combine 
lower two groups together)

Race, combine other and black_nonhisp together to just get other and white 
nonHisp 

Add smoke to slides and make sure you don’t need to collapse

Reduce baseline groups to only those with Y2 data to aid with collapsing 
decisions

Slide 3:
--------
Outcome and baseline as predictor has more power than using a difference as 
outcome. Difference as outcome and adjusting for baseline in the model has the 
same outcomes if you control for baseline (mathematical relationship, gives you 
the same result). Just make sure to control for baseline.
Don’t need causal relationship framework. Know rules for identifying mediation/
confounding, has to be associated with predictor/outcome, stick in model to see 
if the results change is OK plan. Model with and without and see what happens 
even if there is not a difference between HD use (could mask effects) 
Frequentist helps with validating for Bayesian. Think about centering intercept 
or not but for 1000 not super important. In report, make sure to talk about how 
you decided on the priors (chose coefficients because big variance and no big 
influence due to lack of prior information, centered at zero which may not make 
sense for intercept but variance mitigates the issues with this). Want to get to 
place to understand how many subjects have both baseline and y2 data for each 
outcome (different patterns in missingness across outcomes). How different is 
the set of individuals for each model and then ask the investigator to aid in 
decision of who to choose for each model (same across all models or different 
since there are very different groups of individuals/bigger sample sizes by 
choices – can send Canvas messages or ask questions in report/presentation)  

BMI: -1 (improbable, exclude), 999 (insufficient, exclude). 515/514 values 
should be dropped (error and excluded)

Fitting the same model but in two different frameworks and shared methods across 
the four outcomes (nearly the same model). Frequentist (regular linear 
regression), Bayesian using these priors and STAN software. Hopefully not too 
onerous for writeup (don’t get any extra length). 

When people are missing QOL, they are missing both outcomes. So those are 
aligned together. Lab values are typically aligned, but some are just missing 
onr or the other, but usually they are missing both of the labs. Not a huge 
number. Would suggest that we keep to a consistent set of subjects that have all 
4 outcomes, preliminary outcome of 476. Write up how we got to 476 (think 
flowchart but not actually as a figure, why did people end up kicked out).

Missing data and dropout are important, can’t analyze y2 outcomes for those that 
have them. Look at proportion of people who started study how many made it to 
y2? Did that differ between HD use or not? Are you worried about biased results?  

Can buy that there is strong correlation between two sets of lab and QoL. We 
have 4 outcomes, here is unadjusted pval and adjusted pval (e.g. Bonferroni). 
Definitely need to report the unadjusted pvalue. Just fine to report unadjusted, 
especially as you can’t adjust for Bayesian since there are not pvalues there. 
