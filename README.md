# NLP Analysis of Yahoo Questions for Tagging Application





## EDA Analysis
The dataset can be downloaded from this link:
https://course.fast.ai/datasets





![](img/Classes_2.png)





![](img/most_common_words3.png)


## Data Insights

![](img/sentiment_polarity.png)

![](img/subj_vs_polar.png)



## Modeling



## ML Model

| Model Name  |  Accuracy Score |
| -- | -- |
|  Logistic Classification  |  0.72  |
|  Gradient Boost  |  0.68  |
|  Random Forest  |  0.66  |
|  Naive Bayes  |  0.65  |



![](img/ROC_Curve.png)




<img src="img/Confusion_3.png" width="550" height="550">

|      Sports        |       Politics        |
|       --           |         --            |
|![](img/Sports.png) | ![](img/Politics.png) | 
|       --           |         --            |
|      Health        |       Business        |
|![](img/Health.png) |  ![](img/Business.png)| 




## Model Review
In this section, I looked at my model in more details to figure out why it has misclassified some questions, especially "Business & Finance" and "Education" categories. After detailed analysis, I found two main reasons for misclassification: 1) mislabeling the tags by Yahoo 2) complicated sentence structure. The following section explains about these items in more details:

### Mislabeling by Yahoo!



The following part shows some questions that Yahoo tagged as "Business and Finance" but apparently they are not related to that category. I also shows how our model is picking up the word and predicts the probability of each category.

* **Question 1**: For 6 months, I have received this error,"a required DLL file, YIMAGE", was not found. Can you help me please
* **Answer 1**: delete yahoo messenger completly and make sure there nothing left in the and redownload it.
![](img/Flaged_as_buisiness.png)


* **Question 2**: why do i feel left out? all the time?
* **Answer 2**: Probably the same reason I do. I have a hard time being out 
going. But you can work on it. Just asert yourself, people WANT 
to be around you trust me I know.
![](img/Health_Predicted_7.png)


* **Question 3**: which is the largest palace in the world?
* **Answer 3**: Largest residential palace is the Istana Nurul Iman. This is where the Sultan of Brunei lives. 2,152,782 square feet.The Forbidden City in Beijing is the biggest Palace Complex and used to be the home of the Chinese Emperors before the revolution and is 7,750,000 squre feet in size.'
![](img/Palace_predicted_7.png)


### Complicated Sentence Structure

* **Question 1**: how could you distunguish a plant cell from an animal cell when looking in a microscope?4 my bio lab final...help! thanks!
* **Answer 1**: animal cells don't have a cell wall
![](img/Predicted_2_True_4.png)


* **Question 2**: what is the difference between coca-cola classic and coca-cola?
* **Answer 2**: Coca-Cola is the default name for the beverage. Coca-Cola Classic is a more recent name used in comparison with New Coke, which failed miserably.
![](img/coca_predicted_7.png)


## Towards a Better Model
In the future, I plan to continue on this project as mentioned below:

* Build a Long Short Term Memory (LSTM) deep learning model and try feature engineering by transforming
the corpus into a list of sequences using Word2Vec model

* Apply transfer learning model to the corpus using Google's BERT module (Bidirectional Encoder Representations from Transformers)



## Acknowledgments
I greatly appreciate Galvanize instructors, Juliana Duncan and Dan Rupp, for their valuable comments during this project.