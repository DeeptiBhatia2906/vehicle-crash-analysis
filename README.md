## NY Vehicle Crash Data Analysis
###### What are the leading causes of vehicle crashes?

This Project makes use of the NY Motor Vehicle Crash datasets from data.gov:

https://catalog.data.gov/dataset/motor-vehicle-crashes-case-information-beginning-2009
https://catalog.data.gov/dataset/motor-vehicle-crashes-individual-information-beginning-2009

Motor Vehicle Case Information provides a description of the vehicle as reported during the crash, 
Individual Information data provides data about the drivers and other passengers in the vehicle.
Both of the above datasets are for the cases reported in the period 2012-2014.

Joining the above datasets by Vehicle ID provides a total of 2,234,001 records.
Considering only the records which reported Primary Driver information and eliminating unknown data, there were 559,159 females and 827,220 male drivers reported in these crashes.
Contributing factors have been reduced to the top 10 factors.

It is noticeable from the graphs that, of all the female drivers reported, most females were involved in a crash due to failure to yield right-of-way.
* Females show 3 prominent factors with an (almost) equal probability of being involved in a crash: failure to yield right-of-way, driver distraction, following other cars closely.
* Whereas in case of male drivers, the single most prominent factor leading to a crash was following other cars too closely.
* Males were also more likely to end up in a crash due to unsafe driving speeds than females.
* Males and Females report almost equal levels of crashes due to distractions, keeping it at a leading cause of crash over these 3 years.

![alt text](https://github.com/DeeptiBhatia2906/vehicle-crash-analysis/blob/master/males_vs_females_contributing_factors.png)

### Examining Dependence of Contributing Factors and Gender:
If we perform the probabilistic test of independence between Contributing Factors and Gender, given the following Contingency Table (which is represented in the above chart):

| Contributing Factor |	Females	| Males |
|---------------------|---------|-------|
| Failure to Yield Right-of-Way |	0.19	| 0.16 |
| Driver Inattention/Distraction* |	0.19	| 0.19 |
| Following Too Closely	| 0.19 |	0.20 |
| Animal's Action	| 0.12	| 0.12 |
| Unsafe Speed	| 0.08 |	0.11 |
| Pavement Slippery	| 0.06 |	0.06 |
| Backing Unsafely	| 0.05	| 0.05 |
| Passing or Lane Usage Improper	| 0.04 |	0.05 |
| Traffic Control Device Disregarded	| 0.04	| 0.04 |
| Unsafe Lane Changing	| 0.04	| 0.04 |

Consider the events "Failure to Yield Right-of-Way" `(RoW)` and the event that the driver is a Female `(F)`

```
P(RoW | F) = 0.19
P(RoW) = 0.175
```

Since `P(RoW | F) != P(RoW)`, the events are dependent events.
Which also proves that Contributing Factors are dependent on the driver's Gender.

