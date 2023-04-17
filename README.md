# Fake-News-Detection
An NLP program to identify whether the news article is real or fake.

# Our dataset has the following attributes:
1.	id: unique id for a news article
2.	title: the title of a news article
3.	author: author of the news article
4.	text: the text of the article; could be incomplete
5.	label: a label that marks the article as potentially unreliable
    •	1: unreliable
    •	0: reliable
    
We have ‘train.csv’ file which is our dataset. 
It contains 2007 record almost 50% 1’s and 0’s.
We will check whether is there any null values. If there are any, we will fill it with empty strings.

# We will need following libraries:
1.	Pandas
2.	Stopwords
3.	PorterStemmer
4.	Regular Expressions
5.	TF IDF Vectorizer
6.	Decision Tree Classifier
7.	Pickle

# Flow of project:
1. We just load the dataset. Check the top five rows and information about the dataset.
2. We don’t want any NULL values so we checked if there are any NULL values and we got many NULL, so we filled the null values with empty string.
3. After that we remove the ID, title and author column because we don’t need it in our project.
4. I imported the library that were needed. And created a object of PortStemmer class.
5. And test with a sample sentence.
6. I created a function name stemming which will remove all the regular expressions, convert upper case letter into lower case, remove stopwords and also removes blank space.  
7. We split the data into training and testing in 80 , 20 ratio. 80 for training and 20 for testing.
8. We used the decision tree as our algorithm in this project. 
9. It gives us the accuracy of almost 83%. 
10. We imported pickle library to store the data. 
11. We created the fake news function which will detect the news is fake or not.

# Output
Unreliable in our dataset:
![image](https://user-images.githubusercontent.com/43111400/232422910-6f1cd4c6-d35d-498f-b346-d1c84efefa75.png)

Reliable in our dataset:
![image](https://user-images.githubusercontent.com/43111400/232423033-60501cad-daab-46d4-bd2f-5d2938cfa5fe.png)

If we want to check the live news. We will have to put the live news in the dataset first. 

Because if we don’t put the live news into the dataset and directly feed to the program it won’t work.

Because the live news didn’t go through any process of stopwords removal, converting the upper-case letter into lower case, neither it goes through the process of porter Stemmer nor the decision tree classifier. 

So, it will not give the accurate result.

Once we put the news into the dataset. It will go through all the process and the result will be accurate.
