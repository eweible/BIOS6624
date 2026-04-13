Notes on preliminary plan:

Other events in the dataset:
	- Events other than stroke that we are not interested in (e.g. 
	hospitalization)
	- When you are making your columns for stroke and time of stroke, you should 
	not need to look at the other event columns to get those values
	- If you look at the data, there is not censoring for events other than death 
	if a stroke occurs afterwards. You can ignore the other events. 
		○ For the death event, you can look at it to comment on competing risks, but 
		to get what you need for the actual analysis you shouldn’t have to look at 
		it. This is not required.

Note, people can experience more than one type of event (i.e. Angina Pectoris 
and then stroke), and you'll see that they do in the dataset. Experiencing 
non-stroke event shouldn't necessitate censoring. The only time an event 
precludes stroke is if individual dies before having a stroke, and this is 
already pre-built into the TIMESTRK variable where people who die before stroke 
have a TIMESTRK at the time of death.