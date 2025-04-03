# Analysis of Aircraft Accidents in the NTSB Aviation Accident Dataset
## The company is interested in becoming involved in the aviation industry. Specifically with owning and operating aircraft in a commercial endeavor, which would indicate an interest in airplanes or helicopters.
## Overview of the Dataset
The NTSB aviation accident database that I used in this presentation contains data about civil aviation accidents that occurred from 1948 through 2022. The aircraft categories for these accidents include every conceivable kind of aircraft from airplanes and helicopters to hot-air balloons and powered parachutes.
There are 31 fields of data for each of the 88,889 accidents in the database. These fields are Event Id, Investigation Type, Accident Number, Event Date, Location, Country, Latitude, Longitude, Airport Code, Airport Name, Injury Severity, Aircraft damage, Aircraft Category, Registration Number, Make, Model, Amateur Built, Number of Engines, Engine Type, FAR Description, Schedule, Purpose of flight, Air carrier, Total Fatal Injuries, Total Serious Injuries, Total Minor Injuries, Total Uninjured, Weather Condition, Broad phase of flight, Report Status, and Publication Date.
## Methodology and Cleaning the Dataset
Since a large part of this analysis concerns the type of aircraft, it was imperative that the Aircraft Category field be as complete as possible. After removing some duplicate records, I was left with 87,951 accident records. The category field contained about 32,000 values. This is only 37% complete. The Make field (which represents the manufacturer of the aircraft) was 99.9% complete, and I found it to be useful in helping to complete the Category field, since for makes such as Cessna, the resulting category was either airplane or empty (NaN). Therefore, I could fill in all the empty fields for Cessna with “airplane”. The make Sikorsky was exclusively helicopter, so its empty category fields were filled in as well.
After cleaning the Make field for misspellings or alternative versions of makes, and filling in the category fields for all the particular makes that could reasonably be filled in with one category, I was left with a category field that was 94% complete (82,608 records), with only about 5300 “Unknown” aircraft types. 
The fields that yielded the most useful information for this analysis are:
Event Date: the date of the incident
Aircraft Damage: the level of damage sustained, from destroyed to minor damage
Aircraft Category: the type of aircraft involved in the incidents
The 3 injuries fields (Fatal, Serious, Minor) and Total Uninjured: number of the injured and uninjured
Broad phase of flight: from taxiing and takeoff to landing
Report Status: the conclusion drawn from the investigation regarding the main cause of the incident
## The Analysis
The frequency of airplane accidents over the 40-year period from 1982 through 2022 dramatically decreased, whereas the frequency of helicopter incidents remained quite steady. It would be reasonable to chalk this up to advances in technology and safety infrastructure in the airplane travel industry. Therefore, airplane travel is more reliable and safer than it was in 1982, whereas travel by helicopter is relatively just as safe as it was 40 years ago.
Regarding the safety of the humans on board aircraft, it is evident that the likelihood of injury or death in an airplane accident is much lower than in a helicopter accident.
For destructive accidents in both airplanes and helicopters, the injury level is likely to be fatal.
Helicopter accidents resulting in damage are more dangerous for the passengers than in the equivalent damage in an airplane accident.
The importance of training, proper maintenance, and strict adherence to safety protocols cannot be stressed enough. Of the over 18,000 investigations that yielded an informative cause of the accidents, more than half were attributed to pilot error and about a third to equipment failure. These were accidents that most likely could have been avoided if not for human error in the operation and/or maintenance of the aircraft.
The safety of air travel has significantly improved over the past half-century, but if an accident does occur during the operation of an aircraft, the likely result is going to be substantial damage or destruction. There’s rarely such a thing as “just a fender bender” in the airplane and helicopter industries.
## Suggestions for further study
It would be informative to aggregate some data concerning the overall number of aircraft in use in the industries over the same period as the accident dataset. This would give us the opportunity to evaluate the safety record of different makes and models of aircraft as we would have figures related to their overall representation in the industry. Then, recommendations could be made regarding what makes and models would be the best investment for the company from a reliability and safety standpoint.
Completing the Report Status column of the dataset would be extremely helpful in providing more insights as to the safety protocols, training, and maintenance of the aircraft industries.
## Repo Structure
Phase_1_project-aviation.ipynb is the aggregation of the analysis code
working-df holds the dataset (AviationData.csv)
## Links to external project files
<a href="https://public.tableau.com/views/Aviation_17434275679900/phaseanddamage?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link" target="_blank">Tableau Worksheets and Dashboard</a>
