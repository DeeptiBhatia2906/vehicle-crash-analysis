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

