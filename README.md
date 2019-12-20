
# Combining Social media and public services to improve prevention of foodborne illnesses.

Link to our website : https://kaabachi.github.io/project-ada/data/2019/12/18/page.html

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
- Do chicago restaurants that fail city inspections have low ratings and negative reviews ?
- Does food inspection have a direct impact on Yelp reviews ? i.e are reviews more positive just after an inspection ?


# Dataset

We will use the dataset provided:  

- **Chicago Food Inspections**

    - The dataset's size is 220 MB. It has nearly 200K entries and 22 columns. They mainly consist of facility identification and localization and the inspection characteristics. This information is derived from inspections of restaurants and other food establishments in Chicago from January 1, 2010 to the present. A more detailed description can be found [here](https://data.cityofchicago.org/api/assets/BAD5301B-681A-4202-9D25-51B2CAE672FF)
    
    - To map using folium we collect the zip code boundaries GeoJson [file] (https://data.cityofchicago.org/Facilities-Geographic-Boundaries/Boundaries-ZIP-Codes/gdcf-axmw)

- **Yelp**

    - [Yelp](https://www.google.com) is a business directory service and crowd-sourced review forum, it focuses on publishing crowd-sourced reviews about businesses. 

    - To leverage useful data from the Yelp website, we use a combination of [Yelp's API - Yelp Fusion](https://www.yelp.com/fusion) and web scraping in order to get the reviews of the restaurants in Chicago that have been labeled with " food poisoning " during food inspections.
    
    - Here is a brief description in each column of the restaurants dataset :

| Name           | Type   | Description                                                              |
|----------------|--------|--------------------------------------------------------------------------|
| Address        | String | Address of the establishment according to our food inspection dataset    |
| Lincense #     | int    | License number of the establishment according to food inspection dataset |
| Name           | String | Name of the establishment                                                |
| alias          | String | Unique Yelp alias of this business.                                      |
| id             | String | Unique Yelp id of this business                                          |
| is_closed      | bool   | Wether the business has been (permanently) closed                        |
| overall_rating | float  | Rating for this business (value ranges from 1, 1.5, ... 4.5, 5).         |
| price          | string | Price level of the business. Value is one of `$` , `$$`, `$$$`,  `$$$$`  |
| review_count   | int    | Number of reviews for this business.                                     |



# Planning

First step : Meeting the TAs to validate the README changes, discuss the proposed plan forward.

Second step : Group meeting to divide the work between the two datasets.

Third step : Data collection.

Fourth step : Data cleaning, how to deal with missing values.

Fifth step : Data Munging and data visualization on each dataset per group of two.

Sixth step : Narrow the questions and propose a summary of the following steps.

Milestone 2. 

Seventh step : Data exploration and data transformation.

Eighth step : Answering the questions and thinking on the poster.

See the section Plan Forward of the notebook for more technical details to answer the research questions.

Milestone 3.

For this milestone we tried to find an answer to the concerns raised in the Milestone 2 review. 

We started by collecting data for a broader range of restaurants to generalize our claims and to get meaningful comparisons.

We also focused more on the analysis part while creating our data story. We chose the plots that are significant enough to be included in the data story then we tried to make them more interactive and easier on the eyes.

For this part we also worked on our website which can be found here :


**Contribution of each member**

Aymen Ayadi :Plotting graphs during data analysis, web crawling, NLP and text analysis, Yelp reviews, Data collection and organizing meetings.

Haithem Hammami :Prepping up visualizations, answering research questions, coming up with algorithms, working on food inspections, creating interactive plots.

Ridha Chahed: Running tests, tabulating final results, working on food inspections, prepping up visualizations, answering research questions.

Bayrem Kaabachi: Writing up the report or the data story, preparing the final presentation, creating the website, collecting/working on Yelp data.
