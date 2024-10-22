Introduction:
The widespread use of the internet has facilitated the easy sharing of information but also the spread of fake news, posing a significant challenge. The low barrier to entry accelerates the spread of misinformation, undermining social discourse and institutional credibility. Hence, the development of tools capable of automatically detecting fake news is crucial. Such tools can help fight misinformation and enhance media literacy, leading to a more trustworthy information landscape.

Summary work of Our Project:
Our analysis involves combining two datasets—one for fake news and one for real news—comprising four variables: date, title, text, and subject. We add a 'truthfulness' attribute to each article and discover that 'subject' and 'date' aren't reliable indicators of veracity. Thus, we convert 'date' into the day of the week and merge 'title' and 'text' into a single variable. This combined text is then categorized by word count intervals of 100 words. We then focus on the mean-word-length, the top 25 single words, two-word phrases, and three-word phrases based on tf-idf values, ignoring others. Then we use those variables for logistic regression analysis. Using the R language, we assess variable relevance, multicollinearity, outliers, and high leverage points. Finally, we test this model with some current news from Reddit. We find that as time passes, the accuracy of predicting current news with past news decreases.

Introduction of Our Dataset:
For our study, we leverage the "Fake and Real News" dataset from Kaggle, which is openly available for download in the "Fake News Detection Datasets" section on the Kaggle website below.
Fake News Detection Datasets (kaggle.com)
This dataset is divided into two parts: "True.csv" and "Fake.csv". The "True.csv" file contains legitimate news articles collected from Reuters.com, while the "Fake.csv" file consists of articles classified as fake, gathered from sites flagged by Politifact and Wikipedia for their unreliability. Each record within the dataset encompasses information such as the article's title, text, genre, and date of publication from 2016 to 2017.

Research Questions:
RQ1: What features classify fake news and real news?  (By Ziang Li)
RQ2: Can we use logistic regression to build a model using those features and what is the performance? (By Zhikai Li)
RQ3: Are there any relationship between those features and how do they influence the model under the 5% significant level? (By Tao Zhang)
RQ4: How does the model perform on the news nowadays? (By ChenYang Yuan)
