# Project Title: Opinion Mining 
![word_cloud_pic](https://user-images.githubusercontent.com/54416525/89357425-6f589d80-d68e-11ea-9000-592687563645.PNG)


## Objective: 
Our objective is to determine how the people in United State are reacting towards the Pandemic, for example, people tweets praises for doctors and nurses on how helpful they are, how the stay at home have helped in controlling the spread on Virus, etc. In the similar way there are negative tweets as well which we are trying to find. Hence, we are looking for the change in Sentiments of Public based on COVID-19, and the measures implemented for it.
## Goal: 
Our goal is to check the awareness the mass has about the Corona Pandemic and how people are accepting the changes that took place. And therefore, this sentiment of the people will be one of the factors which will help government officials and the general public in making decisions in controlling the situation.
## Details:
•	 The twitter API provided with the last 7 days tweets only. So, we had to extract the data every few days to see the trend. Also the data fetched included the multi-language data but in English script hence during labelling the data as positive and negative some of the data actually does not make any sense so we had to clean the data using various majors. <br />
•	The huge dataset could not be computed using the normal machines. Thus, we had to sample the dataset into parts to execute the models. But even though the model tends to overfit very fast and the information learning rate was less in sample set. 
## Conclusion & Insights
•	Using the Recurrent Neural Network - Long short term model, the Sentiments from the United States Tweets were analysed. As the data we extracted have an overview of the covid-19 situation in USA along with the thoughts of the measures taken by the governments and medical officials, we could see the POSITIVITY among the masses. <br />
•	The people show good reaction due to factors like Staying at home, Environment healing, Family Bonding, Praises for Medical facilities, etc.<br />
•	Similarly, there are negative reaction for the Corona Pandemic as - huge human loss, travel banned, etc.<br />
 ![pic1](https://user-images.githubusercontent.com/54416525/89357996-1b4eb880-d690-11ea-9312-23dd17da4bc9.jpg)
 
Sentiment Statistics over Past Month <br />
•	Looking at the above graph we could conclude that the most of the negative tweets are seen at the time of 22nd April to 30th April when US was facing a huge peek of deaths and Lockdown in most of the States.<br />
NOTE- Due to the computational limitations we could not execute the model with large dataset. Therefore we tried using a sample data to build the model. Although due to small dataset the model does not work as expected <br />
Data Preprocessing<br />
•	Initially, we extracted the data of 50,000 tweets from the twitter API. The cleaning of the data left us with approximately 23,000 data entries. <br />
•	The Sentiments were assigned using the SentimentAnalysis Libarary as Positive and Negative. <br />
•	There was a biase in the dataset for which we had to balance the data in equal number of positive and negative entries. hence we were left with ~12,000 data entries. <br />
Text to Tensors <br />
•	The dataset is then converted into set of tokens which were then vectorized to form tensors. These tensors acts as an input to the Neural Network.
Model<br />
Embedding Layer Dense Model - The first model we build we the layer embedding of input tensors of 10,000 performed very poorly with low accuracy and high loss.<br />
RNN Model - Later to improve the model we used the Recurrent neural network and the accuracy improved slightly. But due to very small sampel set the model tends to overfit at the earliest.<br />
LSTM Model - We tried the same RNN model using the layer LSTM and could see the accuracy and losses are performing better.<br />
Hypertuning<br />
•	Droupouts <br />
•	L2 regularization<br />

PLots of Accuracy and Losses for the Models <br />

Accuracy<br />
 ![pic2](https://user-images.githubusercontent.com/54416525/89357998-1d187c00-d690-11ea-9ffe-c4b15d3ae524.jpg)

Loss<br />
![pic3](https://user-images.githubusercontent.com/54416525/89358036-3a4d4a80-d690-11ea-895b-649800b585c2.png)

![pic3](https://user-images.githubusercontent.com/54416525/89358003-20136c80-d690-11ea-8cd0-734bc6a08572.JPG)

## Note:
Data  <br />
[Data](https://github.com/Harikapenjerla/Opining-Mining/blob/master/TwitterCovidData.zip)   <br />
Using available resources, we sampled the data and proceeded for the analysis and modeling. For more details: <br />

[SampleData-RCode](https://github.com/Harikapenjerla/Opining-Mining/blob/master/SampleDataFile.Rmd)  <br />
[SampleData-html](https://github.com/Harikapenjerla/Opining-Mining/blob/master/SampleDataFile.html)   <br />

For complete data analysis and modeling, we also provide the details of our planning/ approach  <br />
[CompleteData-RCode](https://github.com/Harikapenjerla/Opining-Mining/blob/master/OpinionMining_COVIDTweets.Rmd)   <br />
[CompleteData-html](https://github.com/Harikapenjerla/Opining-Mining/blob/master/OpinionMining_COVIDTweets.html)   <br />

Presentation  <br />
[Presentation](https://github.com/Harikapenjerla/Opining-Mining/blob/master/Opinion_Mining_Presentation.pdf)    <br />

Word Cloud details <br />
[WordCloud](https://github.com/Harikapenjerla/Opining-Mining/blob/master/WordCount.Rmd)  <br />



