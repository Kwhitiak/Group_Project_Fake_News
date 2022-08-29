# Group_Project_Fake_News

### Group
 - Amanda Goguen
 - Salih Ayhan
 - Anthony Marquez
 - Kevin Whitiak

With the advent of the internet, and more importantly social media, fake news and missinformation has been on the rise and has been plaguing our society.  Some is so well hidden and advertised, it may be dfficult to spot if a source is fake news or not.  The purpose of this project is to create a Machine Learning model to detect fake news and missinformation.  We will be using Natural Language processing and Bianary Classification Evaluators on our dataset to help with training and testing of the Model.

# Technologies Used
## Data Cleaning and Analysis
Pandas will be used to clean the data and perform an exploratory analysis. Further analysis will be completed using Python and Machine Learning algorithms.

## Database Storage
SQL is the database we intend to use, and we will integrate Flask to display the data.

## Machine Learning
In the end we swtiched from SciKitLearn to Spark-NLP which is a library created by John Snow Labs for preforming efficient natural language processing tasking using Spark. We decided to use this because it it was something we learned brefly in a preveous moduel and learning it can improve our skills. but also it is made for decifering words and so far it does it well with a 94 %. It also has a whole pipe line which include removing stop words which helps alot. It also is used for huge data which means this data set could be scaled and still produce results. Its not by all means perfect. Transformation code is a little clunky and manipulation is not as easy as pandas(could be a personal oppinon). You need to use it on google colab (good and bad thing). 

# Description of preliminary data preprocessing
* Data went through many transformations when trying to make it work with pyspark nlp pipeline. One being having it actually reading it correctly because the many tabs, enters and commas in it that are miss read as escape and delimiter value. After which we finally go into the pipeline which includes: 
   * tokenizing the data : which splits the strings into a list of words
   * removing SW: Removing stop words that really dont have any meaning to the thext it self 
   * Hashing : turns the code into a matrix that holds the occurrence counts
   * IDF: idf is a vector that fix a huge underlying problem of non meaningfull words that appear many times within our text 
   * vectorAssember
 * after which we split the data in training and testing data using pysparks code : randomSplit([0.7, 0.3], 21)
 * train the data and fit it 
 * and test it to see our accuracy
* So far we have a 94% accuracy
#  Description of preliminary feature
 * befor i orginaly i had 93 befor i had the mashine learning also look at thet text as well
 * 94 % is good but not perfect. Word Bias would be important to look at fallowing through. with out research ive created my own code that would make a confusion matrix given a word. doing so showws if the word were wrong guessing it was fake news when it reality it should have been real and vise versa. seeing this can give us a better understanding of each value
# Conclussion
 * there is still much to do. starting this week i wanto try removing data with words that may confuse the matrix. I also want to try replacing None( our word we used to replace N/A) with another word that might not pop up as much cause this could create bias as well. 
 
 # Problems with code
 * The only bugs that can really effect the code is the data it self. It needs to be cleaned. 
  * Tabs and enters have to be removed in pandas. 
  * Nan and empy cells need to be replaced. 
 * Well trying my own way of checking bias it was found that removing the word complelty only made the percentage lower. 
=======
# Group Project Fake News
