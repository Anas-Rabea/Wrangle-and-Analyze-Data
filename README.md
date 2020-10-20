# Wrangle-and-Analyze-Data
Gathering 3 different source (URL, API -tweepy-, CSV), Assessing, Cleaning and Reporting using Python. 

Gathering
........................
upload the intiative file of twitter_enhance
using request library for download the image_prediction table
After getting tha app Accept from twitter. used tweepy module to get the archive content. put into txt file to extract inforamtion later
using the json for convert the str to dictionary, re library to extract Id , retweet_counts , fav_counts from each line. I used a list to add in order to get a datatset.

Assessing
........................
visual
...
I used visual first to get a general idea about each column and it's value.
Knowing datatypes of each column and keep in mind the cleaning of the wrong datatypes

program
...
I used each available methode to get into each column in each table
using describe() for statistics description , value_counts() for value counts and knowing different values
seraching for missing values in each columns and duplicated
searching for duplicated columns name
using filtering or query() for specific seraching some purpuse
typing
I typed each tidness and quality issues that need to be cleaned later

Cleaning
.........................
For each quality and tidness issue , I write the code and test step
starting with copying my original sources if needed in case of fail
rename columns to match names for tables will be merged later
merging the tables tweet_df and twitter_archive
I used melt function to split multiple variable p1,p2,p3 , then melted p1_conf,p2_conf,p3_con and so on for the rest
with dropping some unuseful columns in combined one tw_clean , I satisfied for tidness
used replace function for replacing "None" values to np.nan
for the source column there's trivial letters that I prefered to remove
converting tha "a" values to Nan values in name column as it's hard to extract name from the text(I tried but no difference)
as the rate based on fixed value for the denomenator , I put 10 to each row
same for numerator, some values under 10 should be converted (it could be wrong)
changed the timestamp type to datetime type
at really tried hard for getting one value for each row in one columns-kind- with the variable
puppo,pupper,floofer,...
 
. I prefered to convert each value to revelent value in float type. Then I used a function to gather each row. And, based on the gathering result I can guess the original value.
with the previous method I noticed that, there are two values in one row so the result was = 5. I decided to remove this rows for get cleaned column
stored the final datasets with desired names
removing the False value for the dog_prediction column.

visualization & insights
.........................
I got value_counts for Most kind of dogs that retweeted by people , then Most kind of dogs that are favorite to people
as the the rate of numerator is unmodified as mention before , the result isn't not expexted
best 20 kind of dog/animal can be predicted by p1 and , I can change p1 to p2 or p3
I uesed group function to get the easiest and hardes kind of dogs/ animal could be predicted for any Algorithm and get a bar plot distingush between the worst and best kind of dog/animal.
