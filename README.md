# UNSC For Us: An Interactive Exploration of UNSC Data
Collected, cleaned, and processed United Nations Security Council resolution data to be used in an interactive data portal as a winter break project!

### Overview

My intention with this project is to eventually use United Nations meeting data as a lens to view global conflict. For instance, there might be trends with certain countries voting the same way together over time or topics that are more difficult to get resolutions passed on.

The first portion of my website looks into what the UNSC really does. Using meeting outcome data from 2000-2019, I found that there were no topics where there is only disagreement, but also no topics where there is only agreement. In other words, there is disagreement and agreement over resolution topics. My first interactive tool explores UNSC actions by meeting and by topic, showcasing when resolutions get passed with respect to discussions with more intangible results.

My second interactive tool focuses exclusively on draft resolutions that failed to be adopted between 1948 and 2022. This is either due to a lack of majority support or a veto by a permanent member of the UNSC. Searching by year, topic, and resolution, this tool allows users to visualize voting results to see which countries voted in favor, abstained, or against. To give context to this information, I also had chatgpt generate meeting names and summaries.

From these two datasets, I created two interactive data pages for users to analyze the data.

#### Inspiration

Inspiration for this project came from being a Model UN kid in high school, and continuing to participate in Model UN through MUNUC at UChicago. I’ve looked through the United Nations Digital Library while researching before and I thought it would be interesting to look for all the Security Council draft resolutions that failed to pass. Then the project grew from there and I included meeting data for all meetings between 2000-2019 as well.

#### Challenges

Putting my data analysis into a website may have been the most challenging part, as this was my first time writing code in html and css.

#### Data collection + cleaning

__Getting the Data__
Starting with the meeting transcripts for the failed resolutions, I downloaded 35 pdfs from the UN digital library. I noticed a common format when votes were taken on draft resolutions, so I first attempted to write some code to read in the text using pdfminer and find the relevant parts using regex, but some documents failed to be read in properly. Eventually I just manually entered the data into google sheets, read it in using pandas, and did some data cleaning of standardizing names using another list of membership by year. This data went into an interactive map page that shows how each country voted: in favor, abstain, against for each draft resolution that failed to pass. I created this using folium and ipywidgets, and added meeting names and topic descriptions created using chatgpt, which did an impressive job after being fed the raw meeting records, which sometimes consisted of half french and half english.

__Cleaning the Data__
The data cleaning also took a bit of work; for instance, I needed to standardize country names, such as Union of Soviet Socialist Republics vs. Soviet Union vs. the Russian Federation vs. Russian Federation

### Next Steps!

I have a lot of ideas for what I can do when I revisit this project in the future. I started working on finding most common n-pairs that voted together on resolutions over time for the failed resolutions, and I think this could go somewhere with looking at the topics more depeply. I plan to work on adding this under the voting maps page. I think other types of visualizations like a network graph could also provide interesting insights into the data.
# unsc_for_us
