# Trigger STudy

An analysis team is using some specific trigger, dedicated for their analysis. The full chain of trigger work implies: first, trigger definition and implementation in the trigger system. Second, trigger validation. Third, calculating final trigger efficiencies. Finally, obtaining trigger systematics.

1. Trigger definition: need to access a series of variables at L1 and other variables at HLT
2. Need to extract them from two different data formats at a very early stage in the data flow (in ATLAS it would be ESDs for MC and BS for data)
3. Define the selection at L1 and at HLT that gives the best efficiency in MC (need to run on MC ESDs) and that has an acceptable rate (need to run on data BS)
4. Once the trigger has been tested in the trigger system, need to validate it. Will have to extract the same variables from the final data format (xAOD in the case of ATLAS) in MC, emulate the trigger and check that the obtained result is the same as the officially produced simulation sample.
5. When the trigger runs online, the same exercise has to be done comparing data to simulation to make sure that the simulation is correct.
6. To obtain trigger efficiencies, will use the variables extracted in step 4.
7. Trigger systematics need a comparison of the performance of the trigger in data and in MC. This implies extracting the same variables from data (same format as MC at this stage, xAOD) and run the trigger algorithm with some modifications.

Steps 1-3 have to be run in the experiment’s framework. Steps 4-7 can be done standalone.