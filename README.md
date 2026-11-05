## Billboard Radio vs. Streaming: Chart Trends

By: Ananya Suthram, Brooke Martin, Samantha Oh, Vaishnavi Pavuluri

### Abstract

Our data topic is songs and artists on Billboard music charts and trends comparing radio and streaming platforms. One key finding from our analysis was that radio and streaming platforms highlight different types of songs, especially when comparing older charting hits with newer viral releases. Additionally, most artists tend to maintain higher rank stability on the radio than across streaming platforms because listeners on streaming platforms have more control over selecting, changing, and looping music. This contributes to more distinction between viral hits and less popular music, affecting artists’ rankings more. A few songs perform much better in one medium, which reflects differences in audience behavior and promotional strategies. Some songs consistently stay in the top twenty, which shows strong listener engagement across several charting weeks. Merging and cleaning the data helped reveal trends that are not obvious from the raw charts. 

### Introduction

Both datasets are about a collection of Billboard music charts, from the first publicly accessible records to the present. One is focused on radio and the other is focused on streaming services. These are compelling datasets to analyze because they offer the most recent data on songs and artists that we all listen to. They include data about previous rankings as well as current rankings, to help the viewer understand trends over time. This report aligns with the annual music recap drops. Our research questions are:
1. What song or album has the current highest number of charting weeks?
2. How does an artist’s rank consistency vary between radio and streaming platforms? 
3. What songs are ranked significantly higher in one data set over the other? (radio vs. streaming)
4. What songs have consistently placed in the top 20 over the past month?
Our analysis is important for artists because it can help them track their performance over time and develop methods to better cater to their audiences. For avid music listeners, our analysis provides trends and insight into popular music and artists they may be curious to learn about. 

### Data Source

This data came from Billboard charts. Billboard is a well-known American music magazine and their charts are one of the most popular music ranking systems. We accessed this data from Kaggle, and it was collected by a Kaggle contributor named Godefroy Lambert. Our dataset can be accessed at https://www.kaggle.com/datasets/ludmin/billboard. The data is freely accessible to everyone. The datasets represent songs that are popular on radio and streaming platforms. We chose these datasets because we care about music and trends in the music industry.

### Data

There are 91300 rows in the radio data set. The 8 columns include Song, Artist, Weeks_in_Charts, and Image URL which are all character data types, rank, last_week, peak_position are all doubles and then Date which is a date data type. The streaming data set has 33300 rows and the same columns. Each row represents a song during one week and statistics that are attached to that. Weeks_in_Charts contains - values when it should be 1 week and it is a character type when it should be numeric.

### Methods

For cleaning the data, we used the select column to take out the image URL column of both data sets because we felt that was irrelevant to our analysis (it linked a picture of the album). We used gsub to remove spaces from the column names and added underscores instead for both data sets. We used mutate to replace the - with a 1 for the Weeks_in_Charts column for both data sets. We then set the Weeks_in_Charts column to be numeric for both sets. We used the mutate function to create a Times_at_1 column to represent the # of times a song hit #1 for both sets. We created a Type column to prepare for merge and represent if the data is about streaming or radio. We merged the data sets together using all of the column names because they are all the same. Song name, weeks_in_charts, date, and type(streaming or radio) are all especially helpful to answer our research questions.

### View the Analysis

This project includes an R Markdown analysis comparing Billboard radio and streaming chart performance. 

- [View HTML Report](billboard_analysis_reconstructed.html) - Access the complete rendered analysis, including visualizations and results.

