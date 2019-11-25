
# Combining Social media and public services to improve prevention of foodborne illnesses.

# Abstract

Food safety is a sensitive subject that is taken very seriously by the public authority. Indeed, each year  roughly 1 among 6 Americans (48 million people) gets food poisoning, resulting in 128’000 hospitalizations and 3’000 deaths ([CDC](https://www.cdc.gov/foodborneburden/2011-foodborne-estimates.html?fbclid=IwAR3BqyBvIe03qtiJKLqrh7wnprI_5oiUdwbVFyEe4s2_N4Tq9ulsjysQT20)). This phenomenon is even worse in urban areas, and one of those affected is the city of Chicago.  

To prevent the deterioration of this situation, the Chicago Department of Public Health’s Food Protection Program uses a standardized procedure to ensure that food preparation in every food establishment across the city meets the health code criteria. This work is summed up in a dataset made publicly available and updated on a daily basis by the city of Chicago. 

As mentionned in the [Chicago Tribune](https://www.chicagotribune.com/opinion/editorials/ct-inspect-food-safety-edit-20161209-story.html?fbclid=IwAR3csHYii5Zx0DWaztytqWG2RCZgXvwntuXKV1bmhECrz1r_G2oZRUJdqEQ) :
- "The Chicago Department of Public Health requires "high risk" food establishments, such as restaurants, school and hospital kitchens and day care centers to be inspected twice a year. In 2015, fewer than half of them got two inspections, city Inspector General Joseph Ferguson recently reported. Grocery stores are supposed to get an annual inspection, but nearly 1 in 5 were not visited by sanitarians last year. Bars and convenience stores are supposed to be inspected once every two years, but fewer than 1 in 4 got a visit from inspectors in 2014 and 2015."

However as highlighted in the same article and due to the sheer number of food based establishments compared to the food inspection staff, the city's department of public health struggles to detect and deal with establishments that don't respect certain hygiene standards. 

Social sources such as Yelp provide a new view of what’s happening that would not have been detected through official channels. Indeed, when you get food borne illness you usually don't go through the hassle of filing a formal claim but you share it on social networks. 

Recently the Chicago Department of Public Health (CDPH) identified a Salmonella outbreak in Best Barbecue Ribs restaurant and another one in Sun View Produce, [as mentioned in the news](http://outbreaknewstoday.com/chicago-officials-investigate-salmonella-infections-linked-to-sun-view-produce-store-deli-28775/) . Basing ourselves on Yelp review data would it have been possible to contain this kind of epidemia and was it an isolated case ?

Through the inspection of the data and its analysis, we would like to introduce a new metric based on food inspection data and Yelp reviews, in order to establish a new ranking and a better recommendation for the consumers. In addition, we aim to introduce a new criterion allowing food inspectors to judge if an establishment should be inspected or not. 

Strengthened by this knowledge and motivated by improving food inspections we will ultimately propose a higher resolution model for detecting health issues that enhances the general customers health.

# Research questions

- Are food chains in different areas more prone to food inspections failure than the same food chains in other areas ?
- Can we assess how real Chicago Tribune's critics are ? 
- Is it possible to predict the results of food inspections by analyzing the yelp reviews of said establishments ?
- Do chicago restaurants that fail city inspections have lower ratings?
- Does food inspection have a direct impact on Yelp reviews ? i.e are reviews more positive just after an inspection?
- Can foodborne illness be detected in Yelp reviews ?

# Dataset

We will use the dataset provided:  

- **Chicago Food Inspections**

    - The dataset's size is 220 MB. It has nearly 200K entries and 22 columns. They mainly consist of facility identification and localization and the inspection characteristics. This information is derived from inspections of restaurants and other food establishments in Chicago from January 1, 2010 to the present. A more detailed description can be found [here](https://data.cityofchicago.org/api/assets/BAD5301B-681A-4202-9D25-51B2CAE672FF)
    -To map using folium we collect the zip code boundaries GeoJson file at https://data.cityofchicago.org/Facilities-Geographic-Boundaries/Boundaries-ZIP-Codes/gdcf-axmw

- **Yelp**

    - This dataset is a subset of Yelp's businesses, reviews, and user data. It was originally put together for the Yelp Dataset Challenge which is a chance for students to conduct research or analysis on Yelp's data and share their discoveries. In the dataset there is information about businesses across 11 metropolitan areas in four countries.  A more detailed description can be found [here](https://www.kaggle.com/yelp-dataset/yelp-dataset/data#)

    - The datasets size is 8 GB. 5,200,000 user reviews. Information on 174,000 businesses. The data spans 11 metropolitan areas.

    - Webscraping


# Planning

First step : Meeting the TAs to validate the README changes, discuss the proposed plan forward.

Second step : Group meeting to divide the work between the two datasets.

Third step : Data collection.

Fourth step : Data cleaning, how to deal with missing values.

Fifth step : Data Munging and data visualization on each dataset per group of two.

Sixth step : Narrow the questions and propose a summary of the following steps.

Mileestone 2. 

Seventh step : Data exploration and data transformation.

Eighth step : Answering the questions and thinking on the poster.


- Yelp dataset :

Leverage natural language processing tools to model the reviews to get a clear view for further use of the data.

Explore the possibility of applying sentiment analysis on review content.

Explore the relationship between words in review, for example see that "poisoning" mostly comes with other words in order to construct a dictionary that describes food poisoning.

Is it possible to match the outbreak cases with the reviews and explore the possibility of discovering new restaurants affected by the epidemia ? Study the feasability of such approach.

Try to detect unreported outbreaks.

- Food poisoning dataset : 

High level analysis of all information we have about restaurants and other food facilities in the database: 

Explore facility types, and get their distribution over state/city/ward features. 

Inspect the features community types and census tracts, and it's influence on facility types.

How dates are distributed ? how an inspection date is set up: periodically or depending on factors related to the                 facility ?

Explore the results of inspections, and related violations if there is.

# Questions for TAa

Add here some questions you have for us, in general or project-specific.
