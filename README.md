# Title

# Abstract
In 2000, Enron was one of the largest companies in the United States. Its stock kept soaring higher and higher day by day. By 2002, it had collapsed into bankruptcy due to widespread corporate fraud. In the resulting Federal investigation, a significant amount of typically confidential information entered into the public record, including around 500.000 emails and detailed financial data for top executives.

Getting access to an email database without violating user privacy is close to impossible. The fall of Enron gave us the opportunity to dive into the detailed analysis of emails and how people use them.

During this project, we'll try to investigate this dataset and try to answer the research questions we came up with below.

# Research questions
- Social Bias : Can we find a correlation between higher income areas and failure to comply to food inspections ?
- Is there a common trend in violations depending on the areas in Chicago, IL ?
-  Are food chains in poor areas more prone to food inspections failure than the same food chains in higher income areas ?

# Dataset
We will use the dataset provided:  

- **Chicago Food Inspections**
The dataset's size is 220 MB. It has nearly 200K entries and 22 columns. They mainly consist of facility identification and localization and the inspection characteristics. This information is derived from inspections of restaurants and other food establishments in Chicago from January 1, 2010 to the present. A more detailed description can be found here: https://data.cityofchicago.org/api/assets/BAD5301B-681A-4202-9D25-51B2CAE672FF

For further exploration, we will be looking at other datasets from the same source which is https://data.cityofchicago.org. These datasets are :

- **311 - Service Requests - Sanitation Code Complaints:**

o Description: All open sanitation code complaints made to 311 and all requests completed since January 1, 2011. The Department of Streets and Sanitation investigates and remedies reported violations of ChicagoÕs sanitation code. Residents may request service for violations such as overflowing dumpsters and garbage in the alley.

o The dataset's size is 35 MB. It has nearly 150K entries and 21 columns. We will be using it to relate the general sanitation situation to the facilitiesÕ level of hygiene.

o Link to the DB: https://data.cityofchicago.org/Service-Requests/311-Service-Requests-Sanitation-Code-Complaints-No/rccf-5427

- **Business Licenses**

o Description: Business licenses issued by the Department of Business Affairs and Consumer Protection in the City of Chicago from 2002 to the present.

o The datasetÕs size is 328 MB. It has nearly 1M entries and 34 columns. We aim to join this DB to the main DB to have a more detailed understanding about each facility characteristics.

o Link to DB: https://data.cityofchicago.org/Community-Economic-Development/Business-Licenses/r5kz-chrr/data

- **Crimes: 2001 to present**

 Description: This dataset reflects reported incidents of crime (with the exception of murders where data exists for each victim) that occurred in the City of Chicago from 2001 to present, minus the most recent seven days. Data is extracted from the Chicago Police Department's CLEAR (Citizen Law Enforcement Analysis and Reporting) system.
 
o The datasets size is 1.7GB. It has nearly 7M entries and 30 columns. First, we will focus on the subset starting from year 2010, which has 4M entries to study its evolution in correlation with the food inspections to see whether locations with a high rate of crime tend to have more code violating facilities. Then we will do further exploration by linking these records to the main DB to see what kind of other crimes are happening in these facilities for example.

o Link to DB: https://data.cityofchicago.org/Public-Safety/Crimes-2001-to-present/ijzp-q8t2/data



# Planning

- Data Exploration:
	- High level analysis of all information we have about restaurants 	and other food facilities in the database: 
	- Explore facility types, and get their distribution over 	state/city/ward features. 
	- Inspect the features community types and census tracts, and 	it's influence on facility types.
	- Explore data related to inspections: 
		- how dates are distributed ? how an inspection date is set 			up: periodically or depending on factors related to the 				facility ?
		- explore the results of inspections, and related violations 			if there is.
	- Analyze the feature Risk, and inspect potential correlations with 	other features => trying to understand what's behind such a Risk. 

	- Make visualization describing the data and plotting relative 	insights to our problematic.
	
=> The goal is to draw out insights to understand the data and links between its features, in order to make assumptions explaining the factors leading to a high-risk facility status.

- This exploration and data analysis will allow us to discuss some preventing solutions: 
	- Mainly how social situation is influencing food inspections/risk/violations.
	- What might be done to prevent facilities from being at risk.

- Once all the above steps are processed, we will put in place a descriptive notebook that illustrates our work in a narrative data story way.


# Questions for TAa
Add here some questions you have for us, in general or project-specific.

