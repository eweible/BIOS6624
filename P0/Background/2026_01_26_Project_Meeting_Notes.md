Notes on Project 0 from investigator and statistician:

Some samples missing cortisol and DHEA but the time is recorded. Why?
	- Supposed to put spit on filter. If not analyzable, then it would be missing even though they provided a sample
Missing MEMs sample interval decimal time and booklet sample interval decimal time
	- Assistant calculated and not sure if they are correct
	- May not want to use 
	- Not truly what it says, it is time since first measurement of that tyoe
		○ Interested in time since woke up not what this is measuring
	- Supposed to take a sample right when they wake up but might not be exactly that. Want to look at time since when they reported time waking up not the intervals between measurements
Wanted to measure new spit booklet for measurements to see if people can be relied on to write down the correct times when they took the samples
	- Have jar with cap that records being open and clsoed and records what time those occurs
	- Cap can malfunction if battery is low or for user error (e,g, not putting the cap back on) so that may cause missing data for the cap time/electronic time
What is agreement? What is the time window
	- As an investigator, what I am imagining is are the times correlated (user input vs. cap recorded time)
		○ Imagining scatterplot as cap time since wake and booklet time since wake (as x and y axis). Want to know if they have a strong correlation/association. 
			§ Interested to know if people tend to record booklet time earlier or later than cap time (is it biased) or are they on average similar>
For the cortisol variable, there are values of 999
	- This is missing
What do you specifically mean for question 3?
	- Changes of cortisol and DHEA over time?
		○ We expect cortisol and DHEA over time to change. 
			§ Cortisol is low when wake up, spike up at 30 min after waking, then gradually decrease 
			§ Want to know if we are seeing the expected trends with these filter papers
			§ What is the difference in cortisol and DHEA after 30 min (do we see significant increase) and then what is the rate of decline afterwards? Investigator will look to see if these align with known values as measured in the lab
	- I would like you to use the nmol/L measurements for DHEA and Cortisol
Was this study prospectively designed?
	- We didn’t speak with a statistician but hoping there is enough info to adrress our main questions about level of agreement. Even if the 30 min increase isn't statistically significant, I can tell if the estimate is similar to what we expect for blood tests. Care about p-values but also care about magnitude of changes over timea nd comparing them to blood tests
For RQ 1 and 2, do you want pvals or descriptive statistics
	- Great to have test of association (statistically significant/significant bias for time (1))
	- For 2, descriptive statistics is OK
		○ Table that has proportion adhering across each group and looking across a range of values (how close it was to the 30min/10 hrs). Additionally a figure with difference in time recorded vs. cap recorded. 
	- For R2, what does adhering mean? 
		○ Adherence window that investigator cares about (both 30min and 10hr):
			§ Good adherence is +/- 7.5min (15 min window centered at desired time)
			§ Adequate adherence is +/-  15 min 
Rely on statistical expertise for best way to use data across multiple days
Neither cap nor booklet is perfect/"truth"
	- Depends on them recording a wake up time in their sleep diary
	- Cap could be potentially inaccurate/implausible but should be obvious when you plot (booklet vs. cap)
Expected range for cortisol and DHEA?
	- Cortisol: nmol/L, biologic range of data: cortisol levels over 26 are possible but not super likely (wouldn't remove them, just higher than expected). Anything over 80 is a lab error/incorrect/potentially something went wrong. 
	- DHEA: nmol/L, there is an upper limit on our assay (5.205/whatever max is in the dataset). Very high value (corresponds to 15000 pg/dl) and those are likely errors (but if an individual person who was recording a level that high repeatedly, then maybe be concerned they might have a different disease process and may want to exclude them from the dataset as they would not be representative and wouldn't be able to see the temporal change with the assay limit)
	- Assayed once (not in replicate)

BY EOD Wednesday have a plan for each RQ

Group Analysis Plan Brainstorming:
RQ1:
	- Needs to have a statistical analysis for this RQ.
	- Are we going to average the cap or the booklet? How much detail are we going to look into - daily or each sample? 
		○ For each sample where we have both time values, then we will use the difference between the two values as the primary variable. (not absolute) 
			§ Booklet and MEMs clock time not interval time
		○ Look at correlation 

Questions as a class again
	- Can treat time (min since waking up) as a continuous variable
	- There is structure to the data - there are numerous measurements per person that are clustered within days. Do we think calculating a correlation is a good idea or should we do something else?
		○ Highly correlated within each person, so how do we answer RQ1? 
			§ Pearson's correlation? Mixed model?
				□ Mixed model. Investigator does not know how to interpret that. Need to explain to them the results in terms of bias and strength of the correlation
				□ Is it a bad idea to take a subject's average? Could take the difference between the two and present descriptive statistics 
					® % of samples within 7.5 min and within 15 min
						◊ Could alternatively present hist/boxplot of differences but probably would be better to instead give them the scatterplot that they desire
				□ Only calculate for when the pair is available. Would like to know about differing levels of missingness by type of measurement
	- For RQ3, should we use booklet time or cap time?
		○ Investigator tells you to use whichever you think is best to use (hoping the two times agree really well, if they do agree then use whichever one you think is best from a statistical point of view)
			§ Also use whichever you think is best if they don't agree
	- RQ2 is OK as descriptive

Wed: lecture on baysian, wrap up worksheet 1, spend more time doing P0 questions. Based on what we talked about today, there is data management to do that you might want to get going on & look at descriptive statistics/boxplots/statistics of outcome. A week from Wednesday, report is due. Want to have some stuff done with data done so that on Wednesday you can focus on nailing down the rest of the analysis plan and it is just implementing


Points from questions for the investigator on 1/26:

- General questions and comments:
  - The investigator stated that the sample.interval variables are the times between first booklet (and first cap) recorded time and subsequent recorded samples. The investigator said she was not sure these were calculated correctly and that she was not interested in using these values in analysis.
  - Rather, she said she is interested in measuring booklet and cap time since waking, where wake time is determined from the sleep diary.
  - Missing data:
    - DHEA and cortisol measurements may be missing even if a booklet or cap time is recorded due to lab errors or insufficient sample collection/poor sample quality.
    - Cap times can be missing even if a booklet time is recorded. This could be due to cap malfunction (low battery) or due to user error (they forgot to put the booklet back in the bottle before taking the next sample).
    - The investigator is interested in knowing about the rates of missing data in your report.
- For question 1, what is meant by agreement?
  - The investigator said she imagined a scatter plot showing the correlation between time since waking measured using the booklet vs. the cap and wanted to know if the two measures were significantly associated. She said she was interested to know if there was any bias/if the booklet times tended to be recorded earlier or later or at about the same as the cap times.
- For question 2, what is meant by adherence?
  - The investigator stated that she wanted to consider adherence in two ways.
    - The percentage of samples taken within 7.5 minutes of the scheduled time.
    - The percentage of samples within 15 minutes of the scheduled time.
- For question 3:
  - Which DHEA and cortisol measurements should be used?
    - The nmol/L measures.
  - What is the expected range of cortisol and DHEA?
    - Cortisol: values over 26 are high, but biologically possible. Values over 80 are likely lab errors and should be excluded.
    - DHEA: there is an upper detection limit to the assay (5.205). This corresponds to an extremely high DHEA level and since the level is not observed, it could make it difficult to see the diurnal patterns of DHEA change over the course of the day.  These observations should be excluded.  The investigator also said that if any participants had several DHEA measures at the detection limit, they could have underlying health problems and that she would want to exclude that person from Q3 analysis. She asked that you let her know if you found any participants like this.
- What are the patterns of change over the course of the day? What is the investigator interested in knowing about changes over time?
    - The investigator stated that levels of cortisol and DHEA are expected to increase sharply from waking to 30 minutes after waking and then decline more slowly over the rest of the day.
    - She was interested in knowing if the SPIT test shows this expected pattern.
    - She wanted to know: 1) is there an increase in cortisol and/or DHEA from waking to 30 minutes post waking? And 2) what is the rate of decline in cortisol and DHEA after 30 minutes from waking?
    - She also stated that even if there are not statistically significant differences, she would like to know the estimates for the initial increase and rates of decline so she can compare them to what is known from other more standard hormone tests.
- Which time measurement should be used for this analysis (Cap or Booklet)?
  - The investigator said she thought the two time measures should agree and therefore either would be fine. She asked us to choose whichever we thought would be best for statistical reasons.
  
  