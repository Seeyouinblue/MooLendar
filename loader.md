# ISE 328

# Technology and Applications of Electronic Business Systems

Instructor: Dr. YM Tang

Room: FJ 410

Contact: mfymtang@polyu.edu.hk
---

# About this Course

1. To learn what is e-business.
2. To introduce different kind of e-business technologies.
3. How to analyze business process.
4. How to apply e-business for improvement.
---
# Syllabus

1. Concept of e-Business.
2. Concept of e-Commerce.
3. Strategic of Implementing e-Business.
4. Various e-Business Technologies.
5. Concept of m-Commerce.
6. Concept of RFID.
7. Supply Chain Network.
8. Work Flow Analysis.

# Advanced Techniques for Business Intelligence – Data Mining ISE328

# Technology and Applications of Electronic Business Systems

Dr Paul Y.P. TSANG

Email: yungpo.tsang@polyu.edu.hk
---
# About this Lecture

- Background of Data Mining
- Clustering: K-means clustering
- Mechanism
- Example of the membership club
- In-class assignment
- Advanced concepts of the k-means clustering
---
# Generic Process for Data Mining

# Data description

Statistical data are summarized

# Model construction

The projected data are used to build a predictive model

# Model testing

The chosen model is needed to be tested

# Model verification

The predicted model is needed to be verified by applying it to the samples

---
# Data Mining (DM) Techniques

# Today’s Focus - Clustering

- To cluster the data into a number of groups
- E-business applications:
- Customer segmentation: To segment their customers based on various features like purchasing behavior, demographics, and past interactions.
- Product categorisation: To group similar products together based on their attributes for product recommendation.
- Anomaly Detection: To detect fraudulent transactions
- Inventory Management: To categorize inventory based on sales activity

# Data Mining Techniques

- Classification
- Clustering
- Regression
- Outer
- Sequential Patterns
- Prediction
- Association Rules

---
# Data Mining Technique:

# k-Means Clustering

# DM – Clustering

• Clustering is a division of data into groups of similar objects.

• Each group, called cluster, consists of objects that are similar between themselves and dissimilar objects of other groups. It represents many data objects by few clusters to achieve simplicity.

• Difference between clustering and classification:

- Clustering corresponds to hidden patterns, it does not show how to define the clusters but need to be discovered by the analyst.
- Unsupervised learning and the resulting system represents a data concept

---
# Partitional Clustering

- Partitional clustering classifies data into k groups while each group must carry at least one data object and each object should belong to only one group.
- Data set are partitioned into k clusters based on the mean value of the objects in the cluster.
- One of the most popular algorithms for partitional clustering is the k-means clustering algorithm.
---
# Proximity Measures

- Clustering can be done by determining Similarity or Dissimilarity of the data
- Due to the different features of the data variables, the distance between two data objects 𝑑(𝑖, 𝑗) needs to be determined in different ways (e.g. Manhattan distance)

# Different types of variables

- Categorical variables: E.g. Sex, Blood Type. Things that belong to these variables contain two or more categories but without intrinsic ordering to the categories
- Numerical variables: E.g. Weight, Height and Temperature. They are characterized by their Euclidean Distance equally difference among their nearest neighbors

# Similarity and Dissimilarity

• Example: Use customers and income as a comparison

# Example: Membership Club

Marco Polo Club is the loyalty program of Cathay Pacific that is designed to reward our most valuable customers with benefits and services that enhance their travel experience.

There are four tiers in the club – Green, Silver, Gold, and Diamond – and each offers its members a range of privileges and benefits that make every journey something to look forward to.
---
# K-Means Clustering

Suppose Marco Polo Club has picked up a sample of nine customers to study their habits of flying with Cathay Pacific.

The table shows how much they fly with Cathay Pacific within a year.

|Member ID|Number of flights with Cathay Pacific per year|
|---|---|
|001|2|
|002|4|
|003|10|
|004|12|
|005|3|
|006|20|
|007|30|
|008|11|
|009|25|

To organize these numbers into two clusters (k=2), e.g. VIP and non-VIP.
---
# Steps 1 and 2

1. Two clusters named K1 and K2, respectively, are established and randomly assigned two means as m1 = 3 (ID: 005), m2 = 4 (ID: 002)
d(004,m1)=9
004
2. Find out the 1-dimensional distance between the objects and the mean values. Take Member 004 as an example:
d(004,m1) =
12-3
=9;
d(004,m2) =
12-4
=8;
Assign each object to the cluster with the mean closest to that object
|Member ID|Number of flights per year|d(i,m1)|d(i,m2)|Cluster|
|---|---|---|---|---|
|004|12|9|8|K2|
---
# Step 3

Repeat step 2 to find out the distance between the objects and the mean values for the rest of the members.

|Member ID|Number of flights per year|d(i,m1)|d(i,m2)|Cluster|
|---|---|---|---|---|
|001| | | |K1|
|002| | | |K2|
|003|10| | |K2|
|004|12| | |K2|
|005| | | |K1|
|006|20|17|16|K2|
|007|30|27|26|K2|
|008|11| | |K2|
|009|25|22|21|K2|

K1={001, 005}

K2={002, 003, 004, 006, 007, 008, 009}

14
---
# Steps 4 and 5

1. By using the value in K1 & K2, update the cluster means (m1 and m2)
|Member ID|Number of flights per year|d(i,m1)|d(i,m2)|Cluster|
|---|---|---|---|---|
|001|2|0.5|14|K1|
|002| |1.5|12|K1|
|003|10|7.5| |K2|
|004|12|9.5| |K2|
|005|3|0.5|13|K1|
|006|20|17.5| |K2|
|007|30|27.5|14|K2|
|008|11|8.5|5|K2|
|009|25|22.5| |K2|
2. Repeat step 2 after the means are renewed, result is shown in the table
- K1 = {001, 002, 005}
- K2 = {003, 004, 006, 007, 008, 009}
---
# Steps 6 and 7

1. Repeat steps 2-4, Stop when the means of the cluster no longer change anymore
2. The changes of the content of the clusters and means are:

The final result has identified 2 distinctive segments of people which fly with Cathay Pacific more than the other segment:

- Fly less with Cathay Pacific (K1): Member 001, 002, 003, 004, 005, 008
- Fly more with Cathay Pacific (K2): Member 006, 007, 009

---
# Problems in K-Means Clustering

- Sensitive to the initialization of cluster centroids
- → Increase the number of iterations, or → Obtain another clustering result

# Start

# Steps 1 and 2

Number of cluster K

1. Two clusters named K1 and K2, respectively, are established and randomly assigned two means as m1 = 3 (ID: 005), m2 = 4 (ID: 002)
2. Find out the I-dimensional distance between the objects and the mean values. Take Member 004 as an example:

d(004,m1) = /12-31-9;

d(004,m2) = /12-41-8;

# Centroid

|Member|Number|Distance objects to centroids|move group?|
|---|---|---|---|
|004| |K1|No object|

Grouping based on minimum distance

---
# K-Means++

• Initialization of cluster centroids:

- Select the first centroid (C1) randomly, and the rest of the centroids based on the maximum squared distance.
- Calculate the distance between C1 and the rest of the data points (𝑥 ∈ 𝑋), namely 𝐷(𝑥), while each data point is assigned with the probability of 𝐷(𝑥′)² / σ𝑥∈𝑋 𝐷(𝑥)².
- Select the rest of the cluster centroid with the above probabilities.
- Proceed the standard k-means clustering algorithm.

---
# Distance Measure

Apart from the sum of the absolute distance (i.e. cityblock), other distance measures are available as follows:

|Distance Metric|Description|Formula|
|---|---|---|
|sqeuclidean|Squared Euclidean distance (default). Each centroid is the mean of the points in that cluster:|d(x, c) = (x - c)²|
|cityblock|Sum of absolute differences; i.e. the L1 distance. Each centroid is the component-wise median of the points in that cluster.|d(x, c) = |x - c||
|cosine|One minus the cosine of the included angle between points (treated as vectors). Each centroid is the mean of the points in that cluster; after normalizing those points to unit Euclidean length.|d(x, c) = 1 - (x · c) / (||x|| ||c||)|
|correlation|One minus the sample correlation between points (treated as sequences of values). Each centroid is the component-wise mean of the points in that cluster; after centering and normalizing those points to zero mean and unit standard deviation.|d(x, c) = 1 - (cov(x, c) / (std(x) * std(c)))|
|hamming|This metric is only suitable for binary data. It is the proportion of bits that differ: Each centroid is the component-wise median of points in that cluster.|d(x, y) = (1/n) * Σ (x_i ≠ y_i)|
---
# Evaluation of K-Means Clustering

The simplest method: Elbow Method – Examine the appropriateness of the k values in the k-means clustering process/no prior knowledge on the number of clusters

Sum of the squared distance within the cluster over K

|Iteration|6|K=2| |M1: 7|
|---|---|---|---|---|
|Member ID|Number of flights per year|d(x,M1)|d(x,M2)|K1/K2|
|1|2|5|23|K1|
|2|4|3|21|K1|
|3|10|3|15|K1|
|4|12|5|13|K1|
|5|3|4|22|K1|
|6|20|13|5|K2|
|7|30|23|5|K2|
|8|11|4|14|K1|
|9|25|18|0|K2|
|SumD|24|10| | |
|SumsqD|576|100|676|21|
---
# Evaluation of K-Means Clustering

# Elbow Method

| |6000| | | | | |
|---|---|---|---|---|---|---|
| |4|5184| | | | |
| |1|5000| | | | |
| |4000| | | | | |
| |1|3000| | | | |
| |2000| | | | | |
| |8|1000| | | | |
| | |6| | | | |
|K-1| |K-2|K-3| | | |
| | |676|108|105| | |
|Number of K| | | | | |22|
---
# Data Mining

# Technique:

# Association Rule Mining

---
# DM – Association Rule Mining

- An association rule tries to discover links among the huge databases in different application areas particularly for business related activities such as selective marketing, decision analysis, and business management.
- Finds out items that are frequently purchased together in order to analyze the buying habits of customers, certain items are often bought in pairs.
- Discount can be given or put the items together in pairs to increase the income.

---
# Example: Duty-Free Shopping

• Duty-free refers to exempting all taxes such as liquor tax, tobacco tax, customs duty, in addition to consumption tax.

• The duty-free shop at the airport handles the duty-free item, so if you are a user of international flight, foreigners and residents of that country can use it.
---
# Association Rule Mining (ARM)

• Association rules mining is to describe the relationship between different items that will appear at the same time.

• The rule is composed of two parts: Antecedent and Consequence

A (Antecedent) → B (Consequence)

• Example: Red Wine → Chocolate

• It implies that the customer will buy red wine together with chocolate.

---
# Types of Association Rules

- If the co-occurrences often appear, these will be regarded as a rule. The rules are not always useful.

# Useful rules (E.g. Neck Cushion and Sensitive Skin Moisturizing Milk):

- Muji to GO has found that neck cushion is the item that is most frequently bought together with moisturizing milk (i.e. the rule sensitive skin moisturizing milk → neck cushion).
- Market research has found that wives often remind their husbands to buy moisturizing milk when they are on their way home.
- 40% of husbands buy neck cushions for themselves together with moisturizing milk requested by their wives.
- As a result, the store has placed shelves for neck cushion near to the shelves for moisturizing milk so that the sales of both items recorded a 30% growth.
---
# Types of Association Rules

- Trivial rules (e.g. Notebook and Mouse):
- Results that are already known through common sense or by anyone at all familiar with the business.
- For instance, customers who purchase notebooks are very likely to purchase mouses: a trivial rule (notebook → mouse).
- Inexplicable rules (e.g. Computer store and toilet bowl):
- Some results are not satisfactorily explained by the rules.
- It was found when a new computer store opened, that one of the most commonly items sold was toilet bowl cleaner.
- “New computer store opens → toilet bowl cleaner sold”, this only tells a fact but cannot provide any insight into consumer behavior or any suggestion for marketing strategies.
---
# Types of Association Rules

• Only “useful” association rules, which contain high-quality and actionable information, can be interpreted and explained without spending too much effort.

• After the rules are clearly identified, the company can gain more insights to take appropriate actions and establish marketing strategies.

---
# Basics of ARM

- Support (s): This is the percentage of records containing an item or a combination of items to the total number of records.
- Support (A) = P(A)
- Support (A → B) = P(A B)
- The support is the probability of the presence of both A and B within the total transaction
- Inexplicable rules Confidence (c): This can reflect how sure we can be that a result with a certain combination of items will occur under a particular condition.
- Confidence (A → B) = P(B|A) = Support (A → B)/Support(A)
- Measure the ratio of A occurs together with B
---
# Basics of ARM

- For a typical association rule to be recognized as valid, the support and confidence of an association rule has to be equal to or larger than the minimum support threshold and the minimum confidence threshold respectively.
- Improvement (t): Tell how well the association rule predicts the result as compared with a single item set
- Confidence (A → B)
- Improvement (t): Support 𝐴 ∗ Support(𝐵) = Confidence 𝐴→𝐵 Support (𝐴∪𝐵) Support(𝐵)
- When improvement is greater than 1, the resulting rule is good and suitable for prediction
- When improvement is less than 1 this means the rule is doing worse than informed guessing.
- Better predicting if the improvement is larger
---
# Simple Example of ARM

• Suppose five customers have purchased various goods in a duty-free shop before flight.

|Transaction No.|Item bought|
|---|---|
|001|Souvenir, Orange Juice, Potato Chip, Beer|
|002|Orange Juice, Potato Chip|
|003|Souvenir, Beer, Potato Chip|
|004|Beer, Potato Chips|
|005|Orange Juice, Souvenir, Potato Chips|

---
# Simple Example of ARM

Based on the above information, an association rule can be constructed:

- For example: “If a customer purchases beer, he/she will purchase souvenir as well.” (Rule: Beer → Souvenir)

Support (Beer) = 3/5 = 60%

- 3 transactions containing beer out of the total five transactions

Confidence (Beer → Souvenir) = 2/3 = 66.7%

- 2 transactions also containing souvenir out of 3 transactions containing beer

Improvement (Beer → Souvenir) = Confidence (Beer → Souvenir) / Support (Beer) = 0.667/0.6 = 1.1117

- Improvement (t) >1, the rule is useful as its ability to predict the result is stronger than guessing.

---
# Apriori Algorithm for ARM

• How can we discover associate rules from a dataset?

• Nine transactions are made in the supermarket, Apriori algorithm is used to find out any association rules based on the data recorded.

|Transaction ID|Items chosen in the transaction|
|---|---|
|001|A, B, E|
|002|B, D|
|003|B, C|
|004|A, B, D|
|005|A, C|
|006|B, C|
|007|A, C|
|008|A, B, C, E|
|009|A, B, C|

A. Beer

B. Snacks

C. Juice

D. Souvenirs

E. Soft drinks
---
# 1a. Transactional data of nine customers in the supermarket

are scanned to form such a table in order to find out the frequency of occurrence of different items in transactions (i.e. Support Counts – s.c.)

|Items|Support Counts|
|---|---|
|A|6|
|B|7|
|C|6|
|D|2|
|E|2|

# 1b. Support counts are compared with the minimum support counts threshold

(min. s.c., is set to be 2 in this case). If s.c. < min. s.c., the corresponding items will be removed.
---
# 2a. Remaining items are merged to form an itemset

# 2b. Scan for support counts of there itemset

# 2c. Compare the s.c. of itemset with min. s.c. prune off the s.c. < min.

|Itemset|Support Counts|Itemset|Support Counts|
|---|---|---|---|
|AB|4|AB|4|
|AC|4|AC|4|
|AD|1|AE|2|
|AE|2|BC|4|
|BC|4|BD|2|
|BD|2|BE|2|
|BE|2|CD|0|
|CD|0|CE|1|
|CE|1|DE|0|
|DE|0| | |

---
# 3a. Generation of itemset with 3 items (i.e. 3-itemset).

Itemsets containing pruned parent itemset(s) are being pruned too

# 3b. Scan the transactional data for s.c. of each itemset

# 3c. Compare the s.c. of itemset with min. s.c.

|Steps|Itemset|Support Counts|Itemset|Support Counts|
|---|---|---|---|---|
| |ABC (AB, AC, BC)|2|ABC|2|
| |ABE (AB, AE, BE)|2|ABE|2|
| |BCD (BC, BD, CD)| | | |
| |BCD (BC, BE, CE)| | | |
---
# Find Useful Rules in n-itemsets

Taking 3-itemsets as the example as follows.

If the minimum confidence threshold is set to be 90%, then the possible rules that can be found:

6 transactions contains item C in totally nine transactions

4 contains both item A and B in totally nine transactions

|Condition|Result|Support (Condition)|Support (Result)|Support (Condition & Result)|Confidence|Improvement|
|---|---|---|---|---|---|---|
|A and B|B and C|4/9 - 44.4%|6/9 - 66.7%|2/9 - 22.2%|50.00%|0.75|
|A and C|B and C|4/9 - 44.4%|7/9 - 77.8%|2/9 - 22.2%|50.00%|0.64|
|B and C|B and C|4/9 - 44.4%|6/9 - 66.7%|2/9 - 22.2%|50.00%|0.75|
|ABC|A and B|6/9 - 66.7%|4/9 - 44.4%|2/9 - 22.2%|33.33%|0.75|
|ABC|A and C|6/9 - 66.7%|4/9 - 44.4%|2/9 - 22.2%|28.57%|0.64|
|ABC|A and B|6/9 - 66.7%|4/9 - 44.4%|2/9 - 22.2%|33.33%|0.75|
|A and B|A and B|4/9 - 44.4%|2/9 - 22.2%|2/9 - 22.2%|50.00%|2.25|
|A and E|A and E|2/9 - 22.2%|7/9 - 77.8%|2/9 - 22.2%|100.00%|1.29|
|B and E|B and E|2/9 - 22.2%|6/9 - 66.7%|2/9 - 22.2%|100.00%|1.50|
|ABE|B and E|6/9 - 66.7%|2/9 - 22.2%|2/9 - 22.2%|33.33%|1.50|
|ABE|A and E|6/9 - 66.7%|2/9 - 22.2%|2/9 - 22.2%|28.57%|1.29|
|ABE|A and B|6/9 - 66.7%|4/9 - 44.4%|2/9 - 22.2%|100.00%|2.25|
---
# Result Interpretation of ARM

- It is found that three rules’ confidences exceed the required minimum confidence threshold (>90%)

- IF beer and soft drinks are bought, THEN snacks are bought together
- IF snacks and soft drinks are bought, THEN buy beer is bought together
- IF soft drinks are bought, THEN snacks and beer are bought together
---
# Support and Confidence Thresholds

- How to define the minimum support count?
- Lower the minimum support count, more association rules will be extracted
- Normally, support is around 25% ~ 30% (depends the size of the data)
- Confidence threshold is suggested to be more than 80%

# Advanced Techniques for Business Intelligence – Text Mining

# ISE328 - Technology and Applications of Electronic Business Systems

Dr Paul Y.P. TSANG

Email: yungpo.tsang@polyu.edu.hk
---
# About this Lecture

- Text Visualisation: Word cloud
- Text Pre-processing: Tokenisation, lemmatisation, punctuation removal, stop word removal etc.
- Term frequency inverse document frequency (TFIDF)
- Naïve Bayes Classifier

---
# Text Mining

- Textual data cannot be effectively analysed by using data mining techniques
- Text mining, also known as text data mining, is the process of transforming unstructured text into a structured format to identify meaningful patterns and new insights.
- Same objective between data mining and text mining: “To explore and discover hidden relationships within unstructured data”
---
# Motivation of Text Mining

- 80% of data in the world resides in an unstructured format (i.e. No pre-defined data format)
- Text mining tools and natural language processing (NLP) techniques are applied to transform unstructured data into a structured format for analysis and high-quality insights

→ Business decision-making & outcome achievement

Gather
Preprocess
Index
Mning
Analysis
---
# Text Visualisation: Word Cloud

• Word Cloud: A visual representation of word frequencies. Higher the word frequency, larger the word to be visualised.

• Tools (example): https://www.wordclouds.com/

• Sample news: https://www.cnbc.com/2021/08/03/jdcom-strategy-why-chinese-e-commerce-giant-is-investing-in-gaming.html

• Compatible with other languages and emoji
---
# Text Pre-Processing

Before analysing the texts, data pre-processing is important to extract useful words from raw datasets.

Similar to the extract, load, transform (ELT) process in the data pre-processing.

# Key approaches in the text pre-processing:

- a) Tokenization
- b) Stemming
- c) Lemmatization
- d) Stop-word removal
---
# Tokenization

• Tokenization is the basic step in the entire text mining process to break text into a number of pieces, called “Token”.

• In text mining, tokens refer to words. For example, a sentence of 10 words contains 10 tokens.

• Tokenization is language-specific, and each language has its own tokenization requirements. English, for example, uses white space and punctuation to denote tokens, and is relatively simple to tokenize.
---
# Stemming

- Stemming is the process of producing a root/base word by removing prefixed and suffixes.
- For example,
- “plays”, “played”, “playing” to the root form “play”
- “walks”, “walked”, “walking” to the root form “walk”
- Stemming is the process of producing a root/base word by removing prefixed and suffixes.
---
# Lemmatization

Lemmatization is also the process of producing morphological variants of a root/base by considering the morphological meaning.

Tend to generate the words (listed in the dictionary)

For example,

- “plays”, “played”, “playing” to the root form “play”
- “better” to the root form “good”

---
# Stop-Word Removal

- Stop words: the most common words in any language, e.g. articles, prepositions, pronouns, conjunctions, etc. ➔ low-level information
- Stop-word removal: reduce the textual dataset size and training time for the text analytics
- For example,
- “I love ISE328 teaching and materials” ➔ “love, ISE328, teaching, materials”
- Example: NLTK stopword list in the Python environment

---
# Bag-of-Words (BoW) Model

- BoW is a simple step to extract features from textual datasets for text analytics models
- A bag-of-words is a representation of text that describes the occurrence of words within a document. It involves two things:
- A vocabulary of known words.
- A measure of the presence of known words.

# Using a histogram to present the BoW

|Today is a great day:|Today:|2|
|---|---|---|
| |great:|1|
|Today is sunny day:|day:|2|
| |Sunny:|1|

Histogram

| |Today|Great|Day|Sunny|
|---|---|---|---|---|
| |1|1|2|1|
---
# Example of the BoW

# Corpus (a collection of documents):

1. I like studying ISE328
2. It is good to study data and text mining in ISE328
3. We like the materials of ISE328

# After tokenization, stemming, lemmatization, and stop-word removal

| |Like|Study|ISE328|Good|Data|Text|Mine|Material|
|---|---|---|---|---|---|---|---|---|
|1|1|1|1|0|0|0|0|0|
|2|0|0|1|1|1|1|1|0|
|3|1|0|1|0|0|0|0|1|
|Count|2|1|3|1|1|1|1|1|
---
# N-Gram Language Model

- N-gram is a sequence of N tokens (or words)
- 1-gram: “I”, “like”, “studying”, “ISE328”
- 2-gram: “I like”, “like studying”, “studying ISE328”
- N-gram language model: learn the probability of word occurrence based on examples of text or the training data
- For example, P(ISE328 | I like) = Count(“I like ISE328”)/Count(“I like”)
- Bigram model: approximate the probability of a word given the previous word (with Markovian properties)
𝑃 𝑤𝑛|𝑤1:𝑛−1 ≈ 𝑃 𝑤𝑛|𝑤𝑛−1
- N-gram model to look previous (N-1) words:
𝑃 𝑤𝑛|𝑤1:𝑛−1 ≈ 𝑃 𝑤𝑛|𝑤𝑛−𝑁+1:𝑛−1
---
# Example of the Bigram Language Model

Corpus: 
- I like studying ISE328
- I like studying at school
- I am happy

# Some bigram probabilities:

- P(like | I) = 2/3 = 0.67
- P(studying | like) = 2/2 = 1
- P(ISE328 | studying) = ½ = 0.5
- Etc.

• N-gram model to look previous (N-1) words:

• The prediction accuracy can be improved by including more training sample
---
# Applications of N-Gram Language Model

- Example: “Can you please come here?”
- “Can you please come”: History
- “here”: Word being predicted

---
# It’s also a first step towards Large Language Model…

- The basic encoder-decoder transformer architecture for building LLMs.

|Pre-processing|Input: Hi. How are you?|Output: Hello. How can I assist you today?|

# Example of LLMs:

- ChatGPT
- Bing
- Llama
- Etc.

---
# Term Frequency-Inverse Document Frequency (TF-IDF)

- Term frequency (TF): The number of times each word occurs in the text
- Inverse document frequency (IDF): An inverse weighting to scale down the words that occur too frequently
- By deploying the TF-IDF → Reflect the importance of a word in a document in a collection or corpus

TF-IDF (Term x within document y): 𝑤𝑥,𝑦 = 𝑡𝑓𝑥,𝑦 × ln( 𝑁𝑑𝑓𝑥), where,

- 𝑡𝑓𝑥,𝑦 = Frequency of 𝑥 in 𝑦
- 𝑁 = Total number of documents
- 𝑑𝑓𝑥 = Number of documents containing 𝑥

18
---
# Example of TF-IDF

# Corpus:

|D|Comments|
|---|---|
|1|I like studying ISE328|
|2|It is good to study data and text mining in ISE328|
|3|We like the materials of ISE328|

# Pre-processed Tokens

- Like study ISE328
- Good study data text mine ISE328
- Like material ISE328

# Calculation of TF and IDF separately:

|tfxy|Like|Study|ISE328|Good|Data|Text|Mining|Material|
|---|---|---|---|---|---|---|---|---|
|1|1|1|1|0|0|0|0|0|
|2|0|1|1|1|1|1|1|0|
|3|1|0|1|0|0|0|0|1|

# IDF

|IDF|Value|
|---|---|
|Like|ln(3/2) = 0.4055|
|Study|ln(3/2) = 0.4055|
|ISE328|ln(3/3) = 0|
|Good|ln(3/1) = 1.0986|
|Data|ln(3/1) = 1.0986|
|Text|ln(3/1) = 1.0986|
|Mining|ln(3/1) = 1.0986|
|Material|ln(3/1) = 1.0986|
---
# Example of TF-IDF

# Calculation of the TF and IDF scores:

| |Like|Study|ISE328|Good|Data|Text|Mining|Material|
|---|---|---|---|---|---|---|---|---|
|1|1|1|1|0|0|0|0|0|
|2|0|1|1|1|1|1|1|0|
|3|1|0|1|0|0|0|0|1|
|IDF|ln(3/2)|ln(3/2)|ln(3/3)|ln(3/1)|ln(3/1)|ln(3/1)|ln(3/1)|ln(3/1)|
| |= 0.4055|= 0.4055|= 0|= 1.0986|= 1.0986|= 1.0986|= 1.0986|= 1.0986|
|TF-IDF (1)|0.4055|0.4055|0|0|0|0|0|0|
|TF-IDF (2)|0|0.4055|0|1.0986|1.0986|1.0986|1.0986|0|
|TF-IDF (3)|0.4055|0|0|0|0|0|0|1.0986|

‘Like’ in TFIDF(1): 0.4055*1 = 0.4055

---
# Example of TF-IDF

- Keyword extraction for each document (Importance):
- Document 1: “like” = “study”
- Document 2: “Good”, “data”, “text”, “mine” > “study”
- Document 3: “like” < “material”
- Selection of a representative sentence as the summarisation
- score the sentences (averaging the TF-IDF values as the weight)
- Set the threshold (i.e. the average score in this example)
- Obtain the representative sentences (> the threshold)

|Like|Study|ISE328|Good|Data|Text|Mining|Material|Score|
|---|---|---|---|---|---|---|---|---|
|TF-IDF (1)|0.4055|0.4055|0|0|0|0|0|0.8109|
|TF-IDF (2)|0|0.4055|0|1.0986|1.0986|1.0986|1.0986|4.7999|
|TF-IDF (3)|0.4055|0|0|0|0|0|1.0986|1.5041|
|Sum|0.8109|0.8109|0|1.0986|1.0986|1.0986|1.0986| |
Average: 2.3716

---
# Other IDF Weight Approaches (MATLAB)

- Normal – For each term, set the IDF factor to ln(N/NT) [Used in the example]
- TextRank – Use TextRank IDF weighting. For each term, set the IDF factor to
- ln((N-NT+0.5)/(NT+0.5)) if the term occurs in more than half of the documents
- IDFCorrection*avgIDF if the term occurs in half of the documents or f, where avgIDF is the average IDF of all tokens.
- BM25 – For each term, set the IDF factor to ln((N-NT+0.5)/(NT+0.5)).
- Etc.

*where N is the number of documents in the input data and NT is the number of documents in the input data containing each term.
---
# Naïve Bayes Classifier

- A Naive Bayes classifier is a probabilistic machine learning model that’s used for classification task, particular for the sentiment analysis (to determine whether the statement is positive, neutral, or negative).
- The crux of the classifier is based on the Bayes theorem:

𝑃(𝐴|𝐵) = 𝑃(𝐴|𝐵)𝑃(𝐴) / 𝑃(𝐵)

- In the Bayes theorem, the conditional probability P(A|B) can be expressed in the above formula as the backbone in the Naïve Bayes Classifier.

23
---
# Mechanism

- In the sentiment analysis, we aim to classify whether the new statement is positive or negative (class variables)

Based on the Bayes theorem, the probability of the class variable (y) given that a set of parameters/features (X) are provided:

P(y | X) = P(X | y) P(y) / P(X)

P(y | x1, … , xn) = P(x1 | y) P(x2 | y) … P(xn | y) P(y) / P(x1) P(x2) … P(xn)

There are n parameters/features

X = (x1, x2, x3, … , xn)

Since the denominator is static

P(y | x1, … , xn) ∝ P(y) ∏i=1nP(xi | y)

# Key Result (max. probability of the class variable):

# y = argmaxyP(y) ∏i=1nP(xi | y)
- y = Class: positive/negative
- P(y) = Prior probability
- ∏i=1nP(xi | y) = Likelihood Probability

---
# Mechanism

- Prior probability: The percentage of the documents in each class
- Likelihood probability: To find the fraction of times of the specific parameters/features appears among all words in all documents of class y
- However, the probability for positive features in the negative class cannot be measured
- Laplace Smoothing Coefficient (e.g. a = 1) is considered when a specific word is not in the training dataset (V is the no. of dimensions/features in the data):

𝑃(𝑥𝑖|𝑦) = (count(𝑥i, 𝑦) + 𝑎) / (σ 𝑥𝑖∈𝑉count(𝑥𝑖,𝑦)+𝑎) = (count(𝑥𝑖,𝑦) + 𝑎) / (σx∈𝑉 count(𝑥𝑖,𝑦) + 𝑎𝑉)

---
# Example of the Naïve Bayes Classifier

# Training dataset:

|D|Comments|Class|
|---|---|---|
|1|Very interesting and amazing product|Positive (+ve)|
|2|Boring and predictable|Negative (-ve)|
|3|Excellent product|Positive (+ve)|
|4|Unsatisfactory services with poor quality|Negative (-ve)|
|5|Great service|Positive (+ve)|

# New comments to be classified:

- Comment 6: “Great product”
- Comment 7: “Unsatisfactory service quality”
---
# Remember: Stop-word Removal etc.

# Training dataset:

|D|Comments|Class|
|---|---|---|
|1|interesting amazing product|Positive (+ve)|
|2|Boring predictable|Negative (-ve)|
|3|Excellent product|Positive (+ve)|
|4|Unsatisfactory service poor quality|Negative (-ve)|
|5|Great service|Positive (+ve)|

# New comments to be classified:

- Comment 6: “Great product”
- Comment 7: “Unsatisfactory service quality”
---
# Remember: Stop-word Removal etc.

# Training dataset:

|Comments|Positive|Negative|
|---|---|---|
|Interesting|1|0|
|Amazing|1|0|
|Very interesting and amazing product|2|0|
|Boring and predictable|0|1|
|Excellent product|1|0|
|Unsatisfactory services with poor quality|0|1|
|Great service|1|1|
|Service|1|1|
|Poor|0|1|
|Quality|0|1|
|Great|1|0|
|Total:|7|6|
---
# Example of the Naïve Bayes Classifier

For the Comment 6: “Great product” → P(+ve|”Great Product”) & P(-ve|”Great Product”)

- Prior Probability:
- P(y = “Positive”) = 3/5 = 0.6
- P(y = “Negative”) = 2/5 = 0.4
- Likelihood Probability:
- P(“Great” | y = “Positive”) = (1 + 1)/(7 + 2*1) = 2/9
- P(“Product” | y = “Positive”) = (2 + 1)/(7 + 2*1) = 1/3
- P(“Great” | y = “Negative”) = (0 + 1)/(6 + 2*1) = 1/8
- P(“Product” | y = “Negative”) = (0 +1)/(6 + 2*1) = 1/8
- P(+ve|”Great Product”): P(y = “Positive”)* P(“Great” | y = “Positive”) * P(“Product” | y = “Positive”) = 0.6*2/9*1/3 = 0.0444
- P(-ve|”Great Product”): P(y = “Negative”)* P(“Great” | y = “Negative”) * P(“Product” | y = “Negative”) = 0.4*1/8*1/8 = 0.00625
- Therefore, argmax[P(y|”Great Product”)] = Positive (+ve)
---
# Example of the Naïve Bayes Classifier

For the Comment 7: “Unsatisfactory service quality”

- Prior Probability:
- P(y = “Positive”) = 3/5 = 0.6
- P(y = “Negative”) = 2/5 = 0.4
- Likelihood Probability:
- P(“Unsatisfactory” | y = “Positive”) = (0 + 1)/(7 + 2*1) = 1/9
- P(“Service” | y = “Positive”) = (1 + 1)/(7 + 2*1) = 2/9
- P(“Quality” | y = “Positive”) = (0 + 1)/(7 + 2*1) = 1/9
- P(“Unsatisfactory” | y = “Negative”) = (1 + 1)/(6 + 2*1) = 1/4
- P(“Service” | y = “Negative”) = (1 + 1)/(6 + 2*1) = 1/4
- P(“Quality” | y = “Negative”) = (1 + 1)/(6 + 2*1) = 1/4
- P(+ve|“Unsatisfactory service quality”): 0.6*1/9*2*9*1/9 = 0.00165
- P(-ve|“Unsatisfactory service quality”): 0.4*1/4*1/4*1/4 = 0.00625

Therefore, argmax[P(y|“Unsatisfactory service quality”)] = Negative (-ve)
---

# Cross-border E-Commerce

# Presented by

Vince Leung

---

# Content

- What is the most important?
- Why Cross-Border e-Commerce?
- Traditional Offline VS Online
- How to start an online business?
- How can AI help?
- How does CB eCom operate?
- Concerns and Challenges of CB eCom
---
# Business Sense

Everything is about business

# The Four Key Industries

- Trading and logistics
- Financial services
- Professional services and other producer services
- Tourism

---
# What are popular?

- Electronics

---
# Where to sell?

# Major Export Markets for Goods

# % share of total merchandise exports in 2023: 
- Mainland China: 55.5
- ASEAN: 7.9
- EU: 6.5
- USA: 6.6
- India: 4
- Taiwan: 3.3
- Japan: 2
- Rest of world: 14.1

---

# Regional Comprehensive Economic Partnership (RCEP)

# Agreement
- The Agreement is to broaden and deepen ASEAN's engagement with Australia, China, Japan, Korea and New Zealand.
- These countries contribute about 30% of the global GDP and 30% of the world population.
---
# Market Entry

# ASEAN Population 2021

|Country|2021 (in thousand)|ECONOMIC GROWTH 2023|
|---|---|---|
|Brunei Darussalam|430.0| |
|Cambodia|16,592.1| |
|Indonesia|272,248.4| |
|Lao PDR|7,337.8| |
|Malaysia|32,576.3| |
|Myanmar|55,295.0| |
|Philippines|110,198.0| |
|Singapore|5,453.6| |
|Thailand|65,213.0| |
|Viet Nam|98,506.2| |
|Total|663,850.3| |

# ECONOMIC GROWTH 2023

|VIETNAM|6.5 %|
|---|---|
|PHILIPPINES|5.7%|
|INDONESIA| |
|MALAYSIA|4.3%|
|THAILAND|3.9%|
|SINGAPORE|2.6%|
---


# Consuming Power

- Economic Strength
- Standard of Living
- Market Potential
- Re  Demand

# GDP per capita (USS) by ASEAN Member States, 2005-2022
- Cambodia: 1,758.0
- Indonesia: 4,777.5
- Malaysia: 12,448.0
- Lao PDR: 2,022.0
- Philippines: 3,623.5
- Singapore: 82,793.6
- Thailand: 7,494.4
- Viet Nam: 4,109.1

---
# Technology Adoption

# High Smartphone User Penetration

|Region|Smartphone User Penetration Worldwide, 2023|
|---|---|
|Southeast Asia|88.9%|
|Western Europe|86.6%|
|North America|86.3%|
|Asia-Pacific|84.5%|
|Latin America|76.9%|
|Central & Eastern Europe|79.2%|
|Middle East & Africa|50.6%|
|Worldwide|79.5%|

# Upper-middle Class Grow Rapidly
# Number of upper-middle class households in Southeast Asia
- 2023: 76.6 Million 
- Growth rate: 41%
- 2024: 118 Million

---
# Why Cross-Border e-Commerce

# Benefits of Cross-Border E-Commerce
- Increased Sales and Revenue
- Brand Awareness and Visibility
- Competitive Advantage
- Market Diversification
- Access to New Opportunities
- Reduced Demand Fluctuations

---
# Traditional Offline Business vs Online Business

# Commonalities

- Quality of Products/Services: The quality of products or services is always a key to succeed
- Customer Satisfaction: Both need to provide excellent customer service to build loyalty and trust.
- Branding: Strong branding is crucial to stand out among competitors.
- Legal and Regulatory Compliance: Local laws and regulations must be complied, such as licenses and taxes.
- Financial Management: Budgeting, accounting and financial planning are all necessary to sustain a business.

---
# Own Online Store VS Marketplace

---
# Build Own Official Store via eCommerce Platforms
Example: 
- shopify
- WOOcOMMERCE
- volusion
- PrestaShop
- WiX
- ShIFTOSHOP
- Ecwid
- Magento
- BIGCOMMERCEMnemailvendorsel ecuoncon

---
# Pros of Building Own Official Store

- Global Reach: You can sell to customers anywhere in the world.
- 24/7 Availability: Your store is always open, which is convenient and can boost sales.
- Lower Overheads: Running an online store costs less than a physical one.
- Data Insights: You get valuable information on what customers like and buy.
- Scalability: It’s easier to grow your online store by adding products or reaching new areas.
- Marketing Opportunities: Use online marketing to attract more visitors and increase sales.
---
# Cons of Building Own Official Store

- Technical Challenges:

Setting up and running an online store needs technical skills, especially for customized sites.

- Competition:

The online market is very competitive, making it hard to stand out and attract customers.

- Security Concerns:

Protecting customer data and ensuring secure transactions are crucial and can be complex.

- Shipping and Logistics:

Managing shipping, returns, and logistics can be tricky and expensive, especially for international orders.

- Customer Trust:

Building trust with customers is harder online since they can’t see or touch products before buying.

- Ongoing Maintenance:

Regular updates, security patches, and content management need continuous effort and re s.
---
# Run Business via Online Marketplace

# Top marketplaces in the world

|Taobao.com|Etsy|OZON|
|channelengine|amazon|ebay|
|Shopee|Rokuten|Rakuten|
|Walmart|fteccado|AliExpress|
|WILDBERRIES| | |
---
# Pros of using Marketplace

- Large Customer Base: Marketplaces like Amazon, eBay, and Shopee have millions of users, giving you access to a big audience.
- Trust and Credibility: These marketplaces are trusted by customers, helping new businesses gain credibility quickly.
- Ease of Setup: Setting up a store on a marketplace is easy and requires less technical knowledge than building your own site.
- Marketing and Traffic: Marketplaces heavily invest in marketing and SEO, driving traffic to their site and your products.
- Payment and Security: They handle payment processing and security, so you don’t have to worry about it.
---
# Cons of using Marketplace

- Fees and Commissions: Marketplaces charge fees on sales, which can reduce your profits.
- Limited Branding: You have less control over how your brand looks and feels compared to your own store.
- Competition: You compete directly with other sellers on the same platform, including the marketplace itself.
- Dependence on Marketplace Policies: You must follow the marketplace’s rules, which can change and affect your business.
- Data Access: You have limited access to customer data, making it harder to build direct relationships and customize marketing.
---
# Both are important

- Diversified Revenue Streams: By selling on both platforms, you reduce the risk of relying on a single   of income.
- Broader Reach: You can reach different segments of customers—those who prefer shopping on marketplaces and those who prefer direct purchases.
- Brand Building: Your own store helps build your brand identity, while the marketplace can drive initial sales and visibility.
- Data and Insights: Combining data from both  s can provide a more comprehensive understanding of your customers and market trends.
- Flexibility and Resilience: If one platform faces issues (e.g., policy changes, technical problems), you still have another channel to continue sales.

Running both an online store and a marketplace presence lets you use the strengths of each and reduce their weaknesses. This can help you build a stronger and more resilient business.
---
# How to start an online business
- Identify Your Niche and Target Audience
- Create a Business Plan
- Register Your Business for licenses and permits
- How to start an online business
- Select an E-commerce Platform
- Design Your Online Store
- Set Up Payment and Shipping Options
- SEO/SEM
- Market Your Store via Social Media
---

# How can AI help?
- Generated Ecommerce Product Photos
- Write Product Descriptions With AI

---
# E-commerce Gateway

# How Payment Gateway Works

# Online Store

1. Customers Submit Order
2. Online Store Contact Gateway
3. Payment Gateway Confirm Payment
4. Payment Processor Sattle Payment
5. Bank Transfer Payment to Merchant

---
# Why is payment gateway important?

- Security:
Sensitive information is encrypted, such as credit card details.

- Efficiency:
Quick and easy payment lead to high conversion rates and customer satisfaction.|

- Global Reach: 
Multiple currencies and payment methods are supported to cater global audiences.

- Integration: 
Various e-commerce platforms can be integrated.

- Analytics:
Detailed reports and analytics can help businesses track sales, manage finances, and make decisions.

- Compliance: 
Regulations and standards are complied, such as PCI DSS to accept credit card.

---
# Online Marketplace

# Example of Cross-Border e-Commerce Logistics Flow

- Order Placement: 
The customer places an order on the marketplace platform

- Order Processing: 
Seller processes the order and pack the parcel

- Transshipment Warehouse: 
The packaged product is delivered to marketplace’s warehouse for consolidation

- International Freight: 
The product is shipped via air, sea, or land to the destination country

- Customs clearance: 
Upon arrival, the shipment goes through customs clearance in the destination country

- Distribution Centre: 
The product is transported to a local distribution center for sorting to different routes

- Last-mile Delivery: 
The product is delivered to the customer’s address

Transshipment Warehouse, International Freight, Customs clearance, Distribution Centre, Last-mile Delivery: Handled by the platform
---
# Which platform to pick

# Southeast Asia's e-commerce market share by operators

|Operator|Market Share (in billions)|
|---|---|
|Tokopedia|18.4|
|Lazada|20.1|
|Bukalapak|5.3|
|Shopee|47.9|
|TikTok|4.4|
|Others|1.2|

Total: 99.5 billion

---
# TikTok Shop has become the 2nd largest platform in Southeast Asia

# Adapt to Local Culture and Trend

- Language Diversity

- Cultural Sensitivity

- Religious Practices

- Payment Preferences

- Shopping habits

---

# Collaborate with affiliate partners

- KOL & Influencers: Share product review or upcoming promotion with their extensive followers via SNS
- Price Comparison: Compare offers from different sites to let shoppers select the best deal
- Coupon & Cashback: Feature brand’s deal or offer monetary reward to shopper for incentive impulse purchase
- Content Publishers: Create content like articles to introduce top recommendations

# Enhance your brand awareness via search engine and SNS
---
# Concerns and Challenges of Cross-Border E-Commerce

- Regulatory Compliance:

• Navigating different regulations, taxes, and import/export laws can be complex. It’s crucial to understand and comply with the legal requirements of each target market.

- Logistics and Shipping:

• Managing international shipping and logistics can be challenging. Businesses need to balance cost and speed while ensuring reliable delivery to maintain customer satisfaction.

- Cultural Differences:

• Understanding and adapting to cultural differences is essential for successful market entry. This includes localizing marketing strategies, product offerings, and customer service.

- Payment Processing:

• Offering multiple payment options and ensuring secure transactions are vital for building trust with international customers. Different regions may prefer different payment methods.

- Customer Support:

• Providing effective customer support across different time zones and languages can be demanding. Businesses need to ensure they can address customer inquiries and issues promptly.

---
# Uncertain Marketplace Policies

# CNN

Tm really desperate now': Temu sellers revolt against fines and withheld pay

They were protesting what they called "unjust" fines levied by the company or withheld payment on goods already sold, among other complaints:

Aug 2024

# Reutets

China's Temu vendors protest over penalty policy

Hundreds of Chinese sellers on Temu have protested against what they call unbearably high penalties imposed by the firm; one of the:

31 Jul 2024

# TechNode

Temu's Chinese suppliers protest in Guangzhou over penalty policy

Hundreds of Chinese suppliers gathered outside Temus Guangzhou office building for a few days at the end of July to protest; as merchants

Aug 2024

# Nikkei Aia

PDD shares plummet as Temu protests in China continue

Shares of Chinese commerce giant PDD Holdings sank nearly 30% during Monday morning trading in New York after quarterly sales came in below expectations a month ago

---
# Fraud Case / Return & Refund

- iPhone Delivery Fraud by amazonin
ORDERED: iPhone
RECEIVED: Razor

---


# E-Business Design and Technologies
---
# The considerations during applying e-Business
---
# Considerations of implementing e-Business

# To convert “Traditional Business” into “e-Business”

# Basic questions:

1. Which Parts/Departments?
2. What is the motivation for the changes?
3. What are the advantages and disadvantages?
4. What should convert?
5. How to do it?
6. When to implement?
---
# Small and Medium-Sized Enterprises (SMES)

# Can Small and Medium-Sized Enterprises (SMES) convert to e-Business?

- Excellent opportunity especially for SMEs.
- SMEs do not have to concern with fixing their old systems before adopting e-business like the large companies.
- SMEs are relatively more flexible, without too many departments/functional groups clearly separated.
---
# Business Transplantation Vs. Business Transformation

e-Business is NOT about complete replacement of conventional ways of doing business

# Transplantation

- to make the current ways of conducting business more efficient and reliable.
- transplanting existing business practices from conventional media to new media.

# Transformation

- Opening up completely new ways of conducting business.
---
# Business Transplantation Vs. Business Transformation

# For example: Operating a book store

# Transplantation

- Applying POS system, central database
- Some parts of workflow are changed

# Transformation

- Become an online bookstore like Amazon.com
- Whole of the business model is changed

---
# Designing e-Business

# 3 Levels in e-business direction:

1. Functions and features
2. e-Business Infra-Structure
3. e-Business Info-Structure
---
# Step 1. Functions and features

# First-level strategy

In designing your e-business, you have to take care of:

- Value Proposition (what you want to show?)

e.g. provide quality service, to be the pioneer, ……
- Customer Segments (who your customers are?)

e.g. teenagers, adults, ……
- Customer Priorities (what your customers want?)

e.g. convenient, fast, cheap, ………
---
# Step 1. Functions and features

To create an innovative e-business design….

# Q1. What business design can make your customer’s shopping and service experience unique and memorable?

- how you can impress your customers.
- how to use new technologies to surprise them.
- how to provide better services.
- how to meet your customer’s demand not only today but also in future.
---
# Step 1. Functions and features

To create an innovative e-business design….

# Q2. What capabilities and competencies can create rich customer experiences?

- What features required to meet your customer’s need, after you understand/realize what they want.
- These decisions determine what your customer will see and encounter when interacting your e-business design.
- So, what techniques should be involved?

Case A - Counter
Case B - ATM
---
# Step 2. e-Business Infra-structure

# Second-level strategy

How do you structure your organization for efficiency?

- How to reduce the time of business process by using electronic equipment?
- How to improve the communication efficiency between departments?
- How to increase the data exchange efficiency between companies.

---
# Step 2. e-Business Infra-structure

For example: Apply RFID in Japanese restaurant
RFID tag
Payment with IC card
Scan the dishes
---
# Step 2. e-Business Infra-structure

You have to analyze your company’s structure.

- How many departments there, and their relationship.
- What functions each department want to have.
- Based on the software functionality/applications required to design your e-business.

- CRM
- ERP
- e-Procurement
- Financial Control
- Supply Chain Management

---
# Step 3. e-Business Info-structure

# Third-level strategy

- This is regarded as the structural foundation supporting the application layer.
- Web Servers, Database, ASP, etc.
- Ensure the applications are working, accessible and available.
- Reliability, security, etc.
---
Electronic Business Technology

---
# What is business technology

Business technology is a strategy for organizing and coordinating technology management across the entire enterprise. 
It is a set of management practices, tools, organizational structures and technology governance. 
It is designed to optimize across the enterprise
Aim of satisfying customer needs and expectations

---
# Three dimensions

- TRANSFORM BUSINESS CAPABILITIES: innovation and data leadership
- BUILD DIGITAL FRONTLINE: Customer experience and loyalty leadership
- MODERNISE TECHNOLOGY BACKBONE: Cost, quality and performance leadership

---
# Three dimensions-1

# Business capabilities and transformation

Emerging technologies are accelerating digital transformation, requiring business and process development and a forward-looking governance.

Business capabilities are the sum of all processes and assets (systems and data), including any supporting functions within the organisation.

Business capabilities are the key for developing the business and for utilising technology in the best possible way.

Transformation comprises of the parts and processes of an organisation that are engaged in improving business capabilities.

---
# Three dimensions-2

# Digital frontline

Digitalisation provides new business opportunities and requires consistent design thinking on how to face customers, partners and employees in a networked multi-channel world.

The digital frontline can be defined as any digital means that connects the company to the user and is visible to the user, whether the user is a customer or a partner, or whether the customer is internal or external.

Customer experience is at the heart of all digital frontline activities. Digital frontline is a crucial area as it is the key area where the emerging business focus and growth possibilities reside and where digital transformation happens through speed and agility.

Digital apps and web, as well as digital enterprises, enable the creation of new business possibilities around customer experience, digital business and internet of things (IoT) services.

---
# Three dimensions-3

# Technology backbone

Traditional information technology management function (or IT) needs to become the technology backbone that is responsible for development, and management of digital and administrative solutions in a professional way.

The technology backbone consists of all information technology systems and processes that support the running of the businesses operations, through the management of end-user services, plus enterprise and business applications.

It is where the essential business asset of a company resides, and the purpose is to provide operational efficiency to the company through reliability, security and scalability.

---
# The future of business is technology

- IoT
- ERP System
- Network Security
- Digital Money
- Virtual Collaboration

---
# What is IoT?

- from WIKIPEDIA

The Internet of things (IoT) describes the network of physical objects—“things”—that are embedded with sensors, software, and other technologies for the purpose of connecting and exchanging data with other devices and systems over the internet.

- from IOT Agenda

The internet of things, or IoT, is a system of interrelated computing devices, mechanical and digital machines, objects, animals or people that are provided with unique identifiers and the ability to transfer data over a network without requiring human-to-human or human-to-computer interaction. 

- Anytime, Anything, Anywhere


# Top 10 IoT Application areas 2020
- Global share of Enterprise IoT projects
|Manufacturing|22%|
|---|---|
|Transportation|15%|
|Energy|14%|
|Retail|12%|
|Cities|12%|
|Healthcare|9%|
|Supply Chain|7%|
|Agriculture|4%|
|Buildings|3%|
|Other|3%|

N = 1,414 projects

---
# Example
# Industrial Automation

- Creates Digital Factories

- Improves Line-of-Command in work units

- Monitors in near real-time throughout the supply chain

- Smart tracking for products in-transit

- Notifies users on deviations in delivery plans

- Provides cross channel visibility into inventories

- Product Quality testing in various stages of Manufacturing cycle

- Packaging Optimization

---
# Challenges and Issues of IoT

- Ethical Issues
- Data Security
- Data Privacy
- Standardization
- Interoperability
- IPv6: Unique Addressing

---

# ERP system

- Definition: 
Enterprise resource planning (ERP) is business process management software. 
Allows an organization to use a system of integrated applications to manage the business. 
Automate many back-office functions related to technology, services and human resources.

- CSM: Controlling vendors; contracts and logistic operation

- EAM: Planning maintenance and repair

- CRM: Controlling sells; contracts and prices

- WMS: Monitoring and planning inventory and warehouse resources

- FA: Operating over enterprise finances, bank accounts, loans and debts

- HR: Governing the database and employees

- BI: Marketing reports and models for different business processes and actions 

- ECM: Enterprise knowledge base and documents content management

---
# Benefits of ERP

- SECURITY

- PRODUCTIVITY

- Mobility & FLEXIBILITY

- Collaboration

- STREAMLINE: PROCESSES & EFFICIENCY

- SAVE MONEY

- Forecasting & Report

-  CUSTOMER SERVICE

- INTEGRATED INFORMATION

---
# Four tiers of ERP

Tier 1: Enterprise
Tier 2: Upper mid-market
Tier 3: Lower mid-market
Tier 4: Entry-Level

---
# Top 10 ERP Software Vendors

JD Edwards
SAP Business
Sage Business
SYSPRO
Microsoft Dynamics
SyteLine
IQMS
NetSuite OneWorld
Epicor ERP
IFS Applications

---
# ERP System Selection

1. Form a project team and conduct the business process re-engineering (BPR).
2. Collect all possible information about ERP vendors and systems. Filter out unqualified vendors.
3. Establish the attribute hierarchy and assign weights to the attributes.
4. Interview vendors and collect detailed information.
5. Analyze the data obtained from the external professional reports to obtain the objective ERP suitability.
6. Assign subjective ratings to the ERP projects on the basis of data acquired in interviews to calculate the subjective ERP suitability.

---
# ERP System Selection

1. Combine the evaluations of both data  s and aggregate the decision-making assessments to determine the final fuzzy ERP suitability.
2. Utilize the fuzzy integral value ranking method to obtain the rank of each ERP project.
3. Analyze the results. Observe the change in the final ERP suitability and the final ranking value.
4. Select the ERP project with the maximum ranking value.
5. Implement the selected ERP project.


---
# What is Network Security

Network security consists of the policies and practices adopted to prevent and monitor unauthorized access, misuse, modification, or denial of a computer network and network-accessible re s. Network security involves the authorization of access to data in a network, which is controlled by the network administrator. Users choose or are assigned an ID and password or other authenticating information that allows them access to information and programs within their authority.
---
# Network Security Coverage

Network security covers a variety of computer networks, both public and private, that are used in everyday jobs: conducting transactions and communications among businesses, government agencies and individuals. Networks can be private, such as within a company, and others which might be open to public access.

Network security is involved in organizations, enterprises, and other types of institutions. It does as its title explains: it secures the network, as well as protecting and overseeing operations being done. The most common and simple way of protecting a network re  is by assigning it a unique name and a corresponding password.
---
# Importance

In the present day world, everyone benefits from advanced cyber defense programs. Network security is extremely essential because it encompasses everything that includes protecting:

- Our sensitive data,
- Personally Identifiable Information (PII),
- Protected Health Information (PHI),
- Personal information,
- Intellectual property data

---
# Common Types of Cyber-Attacks

# Malware

Malware “Malicious Software” is developed by a cyber-attacker with the purpose of invading the target’s computer and taking some or full control.
Usually, Malware can infect the system or network with the initial unintentional and unknowing help from a human and continue to self-replicate automatically. Once security is breached and the Malware is in the system, it can do serious damage.

---

# Phishing

A cyber-attack that aims to obtain sensitive information by cheating targets into believing fake messages.
Phishing attackers disguise themselves as a trustworthy and send lures usually through email, social media, or other electronic media.

---
# Man in the Middle Attack (MITM)

MITM attempts to secretly intercept and listen to the legitimate communication between two hosts.

# Most Common Types:

- Email Hijacking
- Wireless LAN Eavesdrop
- Session Hijacking

---
# DoS and DDoS

• Denial-of-service attack (DoS attack) is a cyber-attack in which the perpetrator seeks to make a machine or network re  unavailable to its intended users by temporarily or indefinitely disrupting services of a host connected to the Internet. Denial of service is typically accomplished by flooding the targeted machine or re  with superfluous requests in an attempt to overload systems and prevent some or all legitimate requests from being fulfilled.

• In a distributed denial-of-service attack (DDoS attack), the incoming traffic flooding the victim originates from many different sources. This effectively makes it impossible to stop the attack simply by blocking a single. (HTTP Flood is the variation of DDoS)

---
# Cross Site Scripting

- This attack aims to insert malicious code into a website which targets a visitor’s browser.
- Cross Site Scripting, also known as XSS, targets trusted web applications. The attacker uses the web app to inject the code such as browser or client-side scripts that is viewed by other users of the same application.

- Process: 
1. Perpetrator discovers website having a vulnerability that enables script injection. 
2. Perpetrator injects the website with a malicious script that steals each visitors session cookies. 
3. For each visit to the website, the malicious script is activated. 
4. Visitors session cookie is sent to perpetrator.

---
# SQL Injection Attack (SQLi)

- An SQL injection attack interferes with the queries that a web application makes to the database. 
- An attacker inserts crafted SQL (Structured Query Language) code lines that allow data to be revealed.

-Process: 
1. Hacker identifies vulnerable, SQL-driven website & injects malicious SQL query via input data.
2. Malicious SQL query is validated & command is executed by database. 
3. Hcker is granted access to view and alter records or potentially act as database administrator. 

---
# Zero-day Exploits

- The term “zero-day” refers to the day when a new vulnerability is discovered by a software vendor. From that moment, of zero-day detection, the clock is ticking for the software vendor to produce a patch as quickly as possible. Once a patch is produced, the software’s end users must install and verify the patch and security vendors must update their attack detection signatures and push those updates to their tools.

- Process: 
1. VULNERABILITY INTRODUCED: EXPLOIT RELEASED
2. ZERO-DAY VULNERABILITY DISCOVERED
3. VULNERABILITY DISCLOSED
4. VENDOR DEVELOPS FIX A 
5. VENDOR RELEASES A FIX / PATCH: ATTACLK SIGNATURES RELEASED
6. PATCH DEPLOYMENT COMPLETE & VERIFIED

---
# Security Monitoring Tools

- SolarWinds Log and Event Manager
- Splunk
- RSA NetWitness Suite
- ManageEngine Log360

---
# What is Digital Money

- Electronic money is money which exists only in banking computer systems and is not held in any physical form.
- Electronic money, or e-money, is the money balance recorded electronically on a stored-value card.
- It may refer to several systems which enable a buyer to pay electronically by transmitting a unique number (called digital certificate) similar to a banknote number.

• In economic terms electronic money is monetary value provided by the issuer on demand, expressed in government or private monetary units stored in electronic form on an electronic device.

• Both virtual currencies and cryptocurrencies are types of digital currencies, but the converse is incorrect.

---
# History

In 1983, the American cryptographer David Chaum conceived an anonymous cryptographic electronic money called ecash. In 1995, David Chaum implemented it through Digicash. In 1996, the National Security Agency published a paper entitled *How to Make a Mint: the Cryptography of Anonymous Electronic Cash*, describing a Cryptocurrency system. In 1998, Wei Dai published a description of "b-money", characterized as an anonymous, distributed electronic cash system.

In 2009, The first decentralized cryptocurrency, bitcoin, was created.

In April 2011, Namecoin was created as an attempt at forming a decentralized DNS, which would make internet censorship very difficult.

In October 2011, Litecoin was released. It was the first successful cryptocurrency to use scrypt as its hash function.

On 6 August 2014, the UK announced its Treasury had been commissioned a study of cryptocurrencies. 

---
# Cryptocurrencies

A cryptocurrency (or crypto currency) is a medium of exchange using cryptography to secure the transactions and to control the creation of additional units of the currency.

Cryptocurrencies are a subset of alternative currencies, or specifically of digital currencies.

There were more than 710 cryptocurrencies available for trade in online markets as of 11 July 2016, but only 9 of them had market capitalizations over $10 million. 

---
# Four different systems

- Centralized Systems
- Decentralized Systems
- Mobile sub-systems/Digital Wallets
- Offline Anonymous Systems

---
# Centralized Systems

- Many systems—such as PayPal, eCash, WebMoney, Payoneer, cashU, and Hub Culture's Ven will sell their electronic currency directly to the end user.
- Other systems only sell through third party digital currency exchangers

---
# Decentralized Systems

Decentralized e-money is stored and flows through a peer-to-peer computer network that directly links users, much like a chat room. No single user controls the network.

# Some decentralized types:

- Bitcoin
- Monero
- Litecoin
- Ripple Monetary System
- Dogecoin
- Nxt
---
# Bitcoin

- Bitcoin is a digital asset and a payment system invented by Satoshi Nakamoto, who published the invention in 2008 and released it as open-  software in 2009.
- The system is peer-to-peer; users can transact directly without needing an intermediary.
- Transactions are verified by network nodes and recorded in a public distributed ledger called the block chain.
- The ledger uses bitcoin as its unit of account. The system works without a central repository or single administrator, which has led the U.S. Treasury to categorize bitcoin as a decentralized virtual currency.
- Bitcoin is often called the first cryptocurrency.
---
# Mobile sub-systems/Digital Wallets

- A number of electronic money systems use contactless payment transfer in order to facilitate easy payment and give the payee more confidence in not letting go of their electronic wallet during the transaction.
- On September 9th, 2014 Apple Pay was announced at the iPhone 6 event. In October 2014 it was released as an update to work on iPhone 6 and Apple Watch. It is very similar to Google Wallet, but for Apple devices only.
---
# Mobile sub-systems/Digital Wallets

- GNU Taler is an anonymous, open   electronic payment system currently (September 2015) in development
- BKasH is the leading payment system in Bangladesh

# Offline Anonymous Systems

- It can be done ‘offline’.
- In this electronic money system, the merchants do not need to have interaction with banks before receiving currency from the users. Instead of that, the merchants can collect spent money by users and deposits the money later to the bank.
- The merchant can deliver his storage media in bank for exchanging the electronic money to cash.

---
# Comparison

|ADVANTAGES|DISADVANTAGES|
|---|---|
|Privacy and confidentiality|Fraud|
|Security|The double spending of digital coins|
|Environmental friendly|Complexity|
|Mobility|Security|
|Anonymity|Laws and regulations|
|Record of transaction|Mass exposure|
| |Cross transaction|
---
# GEQ Virtual Collaboration

# What is Virtual collaboration

Virtual collaboration is the method of collaboration between virtual team members that is carried out via technology-mediated communication.

Virtual collaboration follows the same process as collaboration, but the parties involved in virtual collaboration do not physically interact and communicate exclusively through technological channels.

Distributed teams use virtual collaboration to simulate the information transfer present in face-to-face meetings, communicating virtually through verbal, visual, written, and digital means.

---
# Three Characteristics

Sharing of information: Virtual collaboration is meant to enable the sharing of knowledge between parties who cannot exchange information due to physical separation. Virtual collaboration platforms allow the transfer of different types of information between collaborators to work towards a common goal.

Dispersed Collaborators: Collaborators within virtual collaboration are physically separated from each other and can only interact virtually. Being able to physically interact with a team member affords many benefits that virtual collaboration cannot provide, and eliminates any need for virtual meetings (sharing of context, interpersonal relationships, etc.).

Technology-mediated: Because virtual collaborators cannot interact physically they use technology to share information over several mediums. Most virtual collaboration platforms are carried out via the internet, for example email, video conferencing, and virtual workspaces.

---
# Two Types

- Synchronous collaboration occurs when team members are able to share information and ideas instantaneously.

Examples: instant messaging, chat rooms, and video or audio conferencing.

- Asynchronous collaboration occurs when team members communicate without the ability to instantly respond to messages or ideas.

Examples: e-mail, discussion boards, application-specific groupware, or shared databases.

---
# Advantages

# Pooling of expertise:

Virtual collaboration provides more opportunities for experts to join project groups where their knowledge can be best used, and be complemented with other experts whose knowledge contributes to a common goal.

Virtual collaboration allows teams to be formed based on subject and expertise, without the restriction of physical proximity of collaborators. The pool of expertise is much greater abroad than in most local team settings, meaning that virtual collaboration gives teams an opportunity to add a quality expert that fits the needs of the team.

This can be proved by the fact that dispersed teams with recruited experts tend to have higher net earnings than local teams with a local expert.

# Cost effective:

Compared to face-to-face meetings of distributed group members, virtual collaboration is much less costly. The time and costs associated with transportation to physically bring together team members from different geographic locations can be substantially higher than the cost of a virtual collaborative application.

Software used to connect distributed teams can be found for free on the internet, with more feature-loaded and specialized applications having a one-time cost or a paid subscription.

---
# Disadvantages

- Lower Group Potency: ineffective discussion
- Reduced Cohesiveness
- Poor Satisfaction
- Technological limits
- Reliance on Technology
- Asynchronous and lagged communication
- Means of exclusion: choose to receive certain information

---
# Challenges

- Technology-related challenges

The team needs to have knowledge of both the nature of their work and the virtual collaboration media they choose, and select the best suited media to deal with the most suitable situation. The team also need the skill to deal with the media to overcome issues coming from the media.

- Cultural diversity-related challenges

The team members need to have good knowledge on cultural differences between members and the knowledge of choosing the proper media to smooth these differences. The members are expected to have the skill to adjust their communication behavior and the language proficiency to achieve cultural adaption.

- Trust-related challenges

Trust between members of virtual teams affects the quality and amount of shared information. When virtual teams meet face-to-face, it creates trust and cohesion and ensures knowledge sharing. Knowledge sharing in virtual teams influences the formation of trust and contributes to the effectiveness of the team. In written communication one cannot be sure about other members’ commitment and it is difficult to recognize others’ emotions.

- Geographic dispersion-related challenges

The team member should clearly understand pros and cons of choosing synchronous and asynchronous medias to avoid issues resulted from dispersed workplaces. The skill of time and self-management of team members are also emphasized to overcome this challenge.

- Time-related challenges

If a virtual project is only a small part of the team members' job, members may not have enough time for the virtual project. Thus, for example, they have to process information fast. A particular challenge in virtual teams is following through and responding at a right time because not responding could be interpreted as a lack of competence or commitment.

---
# Virtual collaboration Tools
SharePoint
moodle
workfront
webex
ITrello
Postit
GoloMeeting
Skype for Business
Wrikel
OneNote
EVERNOTE


# Contemporary E-Business Models and Systems

# ISE328 - Technology and Applications of Electronic Business Systems

Dr Paul Y.P. TSANG

Email: yungpo.tsang@polyu.edu.hk
---
# Agenda

# Items to be discussed today:

- Business Models of E-Commerce
- Contemporary E-Commerce Types
- Strategies to Manage E-Commerce
---

# Evolution of E-Commerce
# Categories

- Beauty; Health, Personal & Household Care
- Beverages
- Electronics
- Food
- Fashion
- Furniture
- Media
- Toys, Hobby & DIY

---
# Contemporary E-Commerce

# From

- Conceptualization
- Fixed end
- Websites, network points
- Tool, digital economy

# To

- Industrialization
- Mobile end
- E-commerce ecosystem
- Intelligent economy/commerce
---
# Transaction Types in E-Commerce Businesses

- Business-to-Business (B2B)
- Business-to-Customer (B2C)
- Business-to-Business-to-Customer (B2B2C)
- Customer-to-Business (C2B)
- Customer-to-Customer (C2C)

---
# Business-to-Business (B2B)

B2B e-Commerce is defined as the sales of goods or services between businesses via online channels, instead of traditional ways, such as telephone and mail.

Transactions are carried out digitally, which helps reduce a great amount of overhead costs.

B2B transactions tend to happen in the supply chain, where one company will purchase raw materials from another to be used in the manufacturing process.

Example of the B2B business relationship: Apple → Intel, Panasonic, and semiconductor companies etc.
---
# Business-to-Customer (B2C)

• Business-to-consumer refers to the process of businesses selling products and services directly to consumers, with no middleperson.

• B2C is typically used to refer to online retailers who sell products and services to consumers through the Internet.

• Online B2C can be broken down into 5 categories:

- Direct sellers
- Online intermediaries, e.g. Expedia and Trivago
- Advertising-based B2C
- Community-based, e.g. Facebook
- Fee-based, e.g. Netflix

---
# Business-to-Business-to-Customer (B2B2C)

- B2B2C is an e-commerce model that combines business to business (B2B) and business to consumer (B2C) for a complete product or service transaction in a mutually beneficial manner.
- A business developing a product, service or solution partners with another business to use a particular service, such as an e-commerce website, portal or blog. The two business combine forces and promote mutually beneficial products, services and/or solutions.

---
# Customer-to-Business (C2B)

- C2B allows customers to provide a business with a service, from which the consumer makes a profit.
- This is the reverse of the typical business-to-consumer model (or B2C), in which a company provides a service to customers through the sale of goods and services.
- Example: programming/development work, reverse auction, affiliate marketing, advertisement etc.
---
# Customer-to-Customer (C2C)

- Customer to customer (C2C) is a business model that enables customers to trade with each other, frequently in an online environment.
- C2C businesses are a type of business model that emerged with e-commerce technology and the sharing economy.
- Online C2C company sites include Craigslist, Etsy, and eBay, which sell products or services through a classified or auction system.
- A market environment is built where one customer purchases goods from another customer using a third-party business or platform to facilitate the transaction.
---
# Omnichannel E-Commerce is on the rise

- Traditional: The good, old-fashioned bricks and mortar store
- E-Commerce: Online shopping has skyrocketed in recent years
- Multichannel: Various, disconnected channels for customers to use independently
- Omnichannel: An integrated, seamless experience across multiple devices and touchpoints

---
# Contemporary E-Commerce Types

- E-commerce Platform and Marketplace
- Social Commerce
- Livestream Commerce
- Community Group Buying
- Cross-border E-commerce
- Rental and Sharing Economy
- Grocery and Fresh Food E-commerce

---
# Top E-Commerce Development Platforms

WOOcOMMERCE
BIGCOMMERCE
Magento
shopify
SHIFTOSHOP
SQUARESPACE
zyro
Square
opencart
yolkart
salesforce commerce cloud
volusion

---
# Examples for E-Commerce Marketplaces

ebay
Etsy
Wish
Walmart
Shopee
Laz
Fordeal
AliExpress
1688
Taobao
JD.COM
Pinduoduo

---
# Social Commerce

# 10 Best Social Commerce Platforms and Apps in 2023

- Instagram
- Facebook
- Pinterest
- Snapchat
- TikTok
- Twitter
- Twitch
- Taggshop
- WeChat
- YouTube

---
# Livestream Commerce

- Apparel and fashion is by far the leading category in livestream events in 2023.

- % of livestreamers
Apparel and fashion: 35.6
Beauty: 7.6
Fresh food: 7.4
Consumer electronics: 4.6
Furnishing and home decor: 3.6
Automobile and local online-to-offline sales: 0.2

---
# Community Group Buying (CGB)

- Large game players such as Pinduoduo, Temu, Meituan, Groupon, etc.

- Online Marketplaces Want In: Lazada, Shopee, and Tokopedia have all implemented Group Buy options where individuals can either start a group or join a group purchasing an item in bulk at a lower rate. 

---
# Cross-border E-commerce

In the cross-border e-commerce industry has emerged domestic brands such as AliExpress, Temu, SHEIN, GLOBALEGROW as well as international brands such as Amazon, Ebay, Shopee, Lazada, etc. 

---
# Rental and Sharing Economy

- Bike-sharing
- Power bank-sharing
- Umbrella-sharing
- Charging pile-sharing

---
# Strategies to Manage E-Commerce

- SWOT analysis
- BCG matrix
- KANO model
- Pain point analysis
- Vendor management
- Revenue models
- Logistics models
---
# SWOT Analysis

- Strengths: 
Favourite competitive situation; 
Adequate financial resources; 
Technical force;
Product quality;
Market share;
Cost advantage;
Advertising campaign;

- Weaknesses
Equipment aging;
Chaotic management;
Lack of key technology;
Shortage of funds;
Product backlog;
Poor competitiveness;

- Opportunities
New products;
New markets;
New needs;
Removal of barriers to foreign markets;
Competitor mistakes;|Economic recession;

- Threats
New competitors;
Increased substitution of products;
Tightening market;
Industry policy changes;
Economic recession;
emergency;

---
# Boston Consulting Group Matrix (BCG Matrix)

- Stars: The product group in the high growth rate, high market share quadrant, such products may become cash flow products of enterprises, need to increase investment to support its rapid development.

- Question marks: The product group in the high growth rate, low market share quadrant. Its financial characteristics are low profit margins, insufficient funds required, and high debt ratio.

- Cash cows: The product group in the low growth rate, high market share quadrant, has entered the maturity stage. Its financial characteristics are large sales volume, high product profit margin and low debt ratio.

- Dogs: The product group in the low growth rate, low market share quadrant. Its financial characteristics are low profit preservation or loss; high debt ratio, can not bring profits to the enterprise.

---
# KANO Model

# Satisfaction

- Attractive: Unexpectedly, if this demand is not provided, user satisfaction will not be reduced, but when this demand is provided, user satisfaction will be greatly improved.

- Performance: When provided, user satisfaction will increase; when not provided, user satisfaction will decrease the necessary factors; when optimized, user satisfaction will not increase; when not provided, user satisfaction will decrease significantly.

- Indifferent: Whether this requirement is provided or not provided, there is no change in user satisfaction, and users do not care.

- Must-Be: When this requirement is optimized, user satisfaction will not increase, and when this requirement is not provided, user satisfaction will be significantly reduced.

---
# Customer Pain Point Analysis

|Pain points|Solutions|
|---|---|
||× Slow software|√ Automation features|
|Productivity| |
||× Unnecessary long processes|√ Speed optimization|
||× Lots of manual work|√ Distraction-free work|
||× Price increase|√ Lower prices than competitors|
|Finances| |
||× Unclear cost structure|√ More value than competitors|
||× Need to repurchase often| |
||× Lack of data exchange|√ Digitization|
|Process| |
||× Lack of strategies|√ Streamlined processes|
||× Lack of onboarding|√ Help center|
||× Poor customer support|√ Personal managers|
||× Lack of instructions| |

---
# Vendor Management

# Kraljic Purchasing Model

Bottleneck item: 
- ⚫ Low control of supplier
- ⚫ Innovation and product substitution and replacement
- ⚫ Production-based scarcity

Critical item: 
- ⚫ Development of long-term relationships
- ⚫ Collaboration and innovation
- ⚫ Natural scarcity

Routine item: 
- ⚫ Product standardisation
- ⚫ Process efficiency
- ⚫ Abundant supply

Leverage item: 
- ⚫ Exploitation of full purchasing power
- ⚫ Targeted pricing strategies/negotiations
- ⚫ Abundant supply

---
# E-commerce Business Revenue Models

- Direct to Consumer (D2C): In the D2C model, there is no middleman; instead, businesses sell rights to consumers, like Warby Parker and their prescription eyeglasses. This model builds customer loyalty quickly, as they are better able to customize the user experience.
- Subscription Service: Subscription services are convenient for customers, and businesses can easily use subscription services to sell additional products. Examples include membership-based e-commerce platforms, streaming services, or premium content subscriptions.
- Advertising Model: E-commerce companies can generate revenue by displaying advertisements on their platform. They can charge advertisers for ad placements, clicks, or impressions, leveraging the user base and traffic they attract.
- Value-Added Services Model: E-commerce companies can offer additional services such as fulfillment, logistics, customization, or extended warranties, charging customers for these value-added services on top of the product price.

---
# E-commerce Business Revenue Models

- Data Monetization Model: E-commerce companies can leverage the customer data they collect to generate revenue. This can involve selling anonymized data to third parties, conducting market research, or offering data-driven insights to other businesses.
- Affiliate or Referral Model: Under this model, the e-commerce company earns a commission or referral fee by promoting and facilitating sales of products or services offered by other businesses. This is commonly seen in affiliate marketing programs.
- Commission or Transaction Fee Model: Some e-commerce platforms act as intermediaries, connecting buyers and sellers. They earn revenue by charging a commission or transaction fee on each sale facilitated through their platform.
---
# A Brief Overview of Incoterms

When you offer your products to customers internationally, you may suggest the payment under specific incoterms. 

“Incoterms” is an acronym standing for international commercial terms.

A trademark of the International Chamber of Commerce, registered in several countries.

---
# Basic Structure of E-commerce System

Certification Center
Seller
Logistics Center
Buyer
Payment Center
E-Commerce Service Provider (ICP/ISP/ASP)

---
# Core Modules of E-commerce Platform

- WMS: 
Inbound/Outbound management
Real-time Inventory


- Operation CMS: 
Marketing system
Customer service
Evaluation system
Store management
Risk control

- Order: 
System service
Channel support
Trading Statement 

- Inventory: 
Physical inventory
Sales inventory

- Finance: 
User refund
Sales channel / Supplier settlement;
Other settlement

- Data: 
Products
Customers
Orders
Buried data

- Products: 
Product management
Basic data

- Memberships: 
Login registration
User data
User operation

---
# Cross Border E-commerce Business

- Consumer behavior change: As consumers become more dependent on the Internet, their purchasing behavior has also changed, with a greater focus on personalization and diversification.

- Global Market: Cross-border e-commerce has expanded from local to global, making it easy for global consumers to buy products from other countries or regions.

- Digital Transformation: Under the impact of the epidemic, the trend of traditional retail to online transformation has accelerated. Cross-border e-commerce uses advanced technologies, such as big data and artificial intelligence, to optimize sales, inventory, logistics and other aspects of management.

- Customer service: The operation of cross-border e-commerce needs to pay attention to every link of the supply chain, including procurement, warehousing, distribution, customer service, etc. Quality customer service increases customer satisfaction and loyalty.

---

# Guest Lecture

# The Role of Digital Transformation in Modernizing Business Processes

Presented by

Dr Jacky TING

Adjunct Assistant Professor

Department of Industrial and Systems Engineering

 
---

# What is Digital?

Digital is more than technology: It means connecting that technology with the right data science, putting a customer, device, organization or business process at the center of real change in how businesses do things and how customers experience them. In how we engage, invent, build and buy everything.

It means creating value by uniting the physical world — seamlessly, efficiently, meaningfully — to the virtual one we’re building.

---
# Digital Transformation Benefits for Businesses

Digital Transformation enables company to Interact and Engage both EXTERNAL and INTERNAL shareholders in an effective way to achieve business goals:

- Enhancing efficiency
- Improving customer experience
- Creating competitive edge (e.g. increasing revenue)

---

# Digital Transformation is Improving Customer Experience

Digital Transformation can help to accelerate and enrich data-driven insights for businesses, customers will not only reap the benefits but play a bigger role in how businesses evolve.

---
# Digital Transformation Framework

# Strategy

# People

# Organisation

# DIGITAL TRANSFORMATION

# Customer

# Culture

# Technology

 
---
# Popular Tools for Digital Transformation

Big Data Analtics 
5G and IoT
Robotic Process Automation
API-Based Integration
AI and Machine Learning 
Augmented Reality
Cloud Computing 

 
---
# Robotic Process Automation (RPA)

- RPA is the transformation and automation of business processes
- RPA changes the approach to the performance of repetitive tasks related to manual data entry and processing

# RPA System
Request
RPA
System

# Robotic Process Automation (RPA)

# Benefits of RPA for Business

- Increases scalability and flexibility of business processes
- RPA tools can work 24/7
- One software robot can do the work of 3-5 FTE
- RPA allows achieving 40-80% cost savings

# FACT BOX

Solution providers report that implementation of RPA yields to 40 - 80% of business process costs’ reduction. RPA has become one of the most efficient ways towards process optimization.

 
---
# Internet of Things (IoT)

- loT is usually defined as the connection between wireless technologies, microcontrollers, services and the Internet
- It collects, transforms, and transmits real-time data from any device or machine - anywhere
Any device
Any Business
Anywhere
Anytime
Anybody
Any Network


- IoT Application: 
Smart City
Smart Home
Health
Smart Monitor
Transport
Smart Retail
Smart Factories
Smart Farming
 
---
# Cloud Computing

- Delivery of on-demand computing services from applications to storage and processing power – typically over the Internet and on a pay-as-you-go basis

- Communication, CRM, ERP, Email, Games → SAAS: Software as a Service → USE
- Web, Application, Development, Database → PAAS: Platform Service → BUILD 
- Server, Storage, Network Security, System Management → IAAS: Infrastructure Service → MIGRATE
 
---
# Cloud Computing

# Examples of IaaS:

Microsoft Azure
AWS
Metacloud
Google Engine

# Examples of PaaS:

Stratosapache
App Engine
Elastic Beanstalk

# Examples of SaaS:

Office 365
Salesforce
Cisco Webex
Google Apps

 
---
# Cloud Computing Statistics in Year 2023

# Big Three Dominate the Global Cloud Market

# Worldwide market share of leading cloud infrastructure service providers in Q1 2023*

|aws|32%|
|---|---|
|Azure|23%|
|Google Cloud|10%|
|CJAlibabaCloud|4%|
|IBM Cloud|3%|
|salesforce|3%|
|Oracle|2%|
|Tencent Cloud|2%|

# Most Used Cloud Storage Services

# Usage of Personal Cloud Storage Survey

|Google Drive|94,44%|
|Dropbox|66.20%|
|OneDrive|39.35%|
|iCloud|38.89%|
|amazon drive|9.72%|
|MEGA|5.09%|
|bOX|4.17%|
|IDrive|1.85%|
|pCloud|1.39%|

---
# Augmented Reality (AR) and Virtual Reality (VR)

# Augmented Reality

- Overlays computer generated 3D content on the real world
- User is able to interact with real world and virtual world
- User can clearly distinguish between both the worlds
- It is achieved by smartphones, tablets or AR wearables

# Virtual Reality

- Visually immerse the user with simulated objects and environment
- Completely shut down the real world and make user think that they are really in the virtual world
- User finds it hard to differentiate between virtual and real world
- It is achieved by VR headsets

---
# Augmented Reality (AR)

# AR in Manufacturing: 

- Stock & Inventory Management
AR route guiding
Gamify picking process
Barcode scanner in smart glasses
Logistics/warehouse info overlay

- Security & Safety
Emergency info overlay
Safety instructions overlay
Hazard inspections
Security info injection
Remote Health, Safety, Environment (HSE) inspections

- Prototyping
Increase speed of approval
Fast feature adjustment
AR in Manufacturing
Real-time display & adjust prototype in 3D

- Real-Time Analysis & Digital Production Display Boards
AR issue diagnosis with Artificial Intelligence or remote expert
Remote diagnosis
Equipment condition info overlay
Intuitive condition monitoring 
Real-Time analysis of production

- Work and Assembly Instructions
Improve efficiency of quality control
Real-time warning for mistakes
Replace complex manuals
Smart glasses show intuitive instruction overlay

- Training
Real-time training instruction overlay
Reduce needs for training supervision
Supplement/reduce training manuals
Additional production insights
Real-time correction for production situations
Simulate production situations

---
# Virtual Reality (VR)

- Entire digital environments
- Training simulations
- Distance work collaboration
- Product development

 
---
# Industrial VR Applications

- Product design & virtual prototyping
- Virtual factory
- Planning, simulation & training
- Assembly & service
- Training
- Quality assurance
- Fault diagnosis

---
# Industrial VR Advantages

# Visualization

- VR makes it easier to view the effects of complex data and interactions in models
- Additional views and navigation of a model not viewable with 2D and in some cases difficult to see with screen-based 3D pre-presentations are possible with VR

# Understanding

- Ability to capture and compare the virtual and physical state of objects

# Communication

- Aids in communicating changes to both internal and external organizations

 
---
# Extended Reality (XR)

Extended Reality (XR): a range of technologies, covering mixed, virtual & augmented reality environments

- It is an umbrella term used for the new set of technologies namely Augmented reality, Virtual reality, and Mixed reality that are changing the way we interact with the world and each other.
- Extended Reality includes real and virtual environments generated with the help of computer technologies and wearable devices for providing immersive experiences.

---
# Big Data

Big data is an evolving term that describes any voluminous amount of structured, semi-structured and unstructured data that has the potential to be mined for information.

# Big Data is used for

- Understanding and Targeting Customers
- Understanding and Optimizing Business Processes
- Personal Quantification and Performance Optimization
- Improving Healthcare and Public Health
- Improving Sports Performance
- Improving Science and Research
- Optimizing Machine and Device Performance
- Improving Security and Law Enforcement
- Improving and Optimizing Cities and Countries
- Financial Trading

 
---
# Big Data Characteristics

Below are the five main characteristics that differentiate data categorized as "Big" data from other forms of data.

# Five Vs:

- Volume
- Velocity
- Variety
- Veracity
- Value

# Volume

This refers to the sheer volume of data being generated.

# Velocity

Having access to big data well and the speed at which data is generated and processed.

# Variety

Can use structured as well as unstructured data.

# Veracity

Data reliability and trust: Verifying and validating the data.

# Value

Only into value; understanding the importance of the data.

 
---
# Big Data Characteristics

- Data variety refers to the multiple formats and types of data that need to be supported by Big Data solutions, such as structured, semi-structured and unstructured data.
- Data variety brings challenges for enterprises in terms of data integration, transformation, processing and storage.
- Examples:

|Structured data|Semi-structured data|Unstructured data|
|---|---|---|
|Databases|XML|Audio|
| |Email|Video|
| |Web pages|Image data|
| | |Natural language Documents|
| | |Documents|
 
---
# 4 Types of Data Analytics

1. Descriptive: 
Based on Live Data, Tells what's happening in real time. 
Accurate & Handy for Operations management. Easy to Visualize

2. Diagnostic: 
Automated RCA - Root Cause Analysis 
Explains "why" things are happening
Helps trouble shoot issues

3. Predictive
Tells what's likely to happen? 
Based on historical data, and assumes a static business plans/models
Help business decision to be automated using algorithms


4. Prescriptive: 
Defines future actions i.e., 'What to do next?'
Based on current data analytics, predefined future plans, goals, and objectives
Advanced algorithms to test potential outcomes of each decision and recommends the best course of action

---
# Practical Big Data Benefits

- Better dialogue with consumers
- Opportunity for product re-development
- Efficient risk analysis
- High level of data safety
- New revenue streams
- Real time website customization
- Acquiring enterprise-wise insights
- Making cities smarter

---
# Artificial Intelligence and Machine Learning

Al is the simulation of human intelligence processes by machines.

This includes learning (the acquisition of information and rules for using the information), reasoning (using the rules to reach approximate or definite conclusions) and self-correction.

Machine learning is a way to make Al possible.

 
---
# AI: Past, Present and Future

- Deep learning, big data and general AI: 2011 - present 
Access to large amounts of data
Faster computers
Deep learning drives progress in image and video processing, text analysis, speech recognition
Google DeepMind defeats world champion in Go (2016): Widespread discussions around, Strong Al: superhuman intelligence

- Goals fulfilled: 1993 - 2011
Deep Blue (1997): Victory of the "neats" (2003)
DARPA Grand Challenge (2005): AI untold successes in data mining, robotics, logistics, speech recognition, search engines


- 2nd AI Winter: 1987 - 1993
Expert systems boom: 1980-1987
Rule-based, logical systems
Selection of component based on customer requirements 5th gen project (Japan) Neural networks, backprop


- 1st AI Winter: 1974-1980
Golden years: 1957-1974
Symbolic AI, search algorithms, neural nets, industrial robots, etcs

---
# The Industrial AI Stack in Reality

- Process: 
Data collection and cleaning 
Representation
“Solving the problem”
Validation
Deployment, maintenance and support


- Data collection and cleaning: Often 80% of total effort
- Representation, “Solving the problem”, Validation: Foundations of value creation (20% of effort) 
- Deployment, maintenance and support: End-user value

---
# Use Case: Text Analytics

Text analytics is the specialized analysis of text through the application of data mining, machine learning and natural language processing techniques to extract value out of unstructured text.

# Different Data  s

- Call Center
- Online Chat
- Feedback
- Email
- SMS
- Web
- Mobile
- Social Communication
- Social Media

# What actions customers are taking and where

# What customers are saying socially

# Data Preprocessing

1. Convert text to lowercase
2. Remove Numbers (if required)
3. Remove Punctuations/Special characters
4. Remove English stop words
5. Remove Own stop words (if required)
6. Strip whitespace
7. Stemming
8. Lemmatization
9. Create document term matrix

# Clustering/Topic Model

# Classification

# Sentiment Analysis

 
---
# The Most Popular GPT:

# ChatGPT

Advanced Artificial Intelligence (AI) chatbot that utilizes Natural Language Processing to simulate human-like conversations. Interact with users in a way that feels natural and intuitive.

Built on top of OpenAI’s GPT-3 language model (and GPT-4 is under review).

Most used in: Understand and respond to a wide range of queries and requests, questions to complex conversations.

---
# A New Era of Customer Engagement in the Mix Technology World

# O+O is all about Driving Customers from Online Screen Merge Offline Experiences

“The key to O+O is that it brings consumers seamless experience regarding they are shopping in either online or real-world stores. It is a combination of payment model and foot traffic generator for merchants (as well as a ‘discovery’ mechanism for consumers) that creates seamless purchases.” AS Watson Group, 2019

---
# IoT x AI for Video Analytics

- Identify Marketing Effectiveness of in-store marketing and product links with product sales.

- Identify Customer Demographics such as gender; age and ethnicity to improve, target and optimize in-store marketing:

- Manage Queues to enhance the customer experience by reducing waiting times and walk-offs.

- Count People to improve staff ratios and increase sales conversion rates.

- Identify Unattended Customers to improve customer service and increase sales conversion rates.
 
---
# IoT x AI for Video Analytics

- Identify Customer Demographic

Display appropriate products for his/her age, and gender

- Identify VIP Members

Facial Recognition to identify VIP members for Proactive and dedicated Account Executive


- Help Closing Deal

Through Big Data Analytic, Signage recommend personalized best products, discounts and assistance to members

- Identify Marketing Effectiveness

of in-store marketing and Promotion products

---
# Strategies for Successful Digital Transformation

- Agile Methodology
Adopting an agile approach allows organizations to iterate quickly, respond to feedback, and adapt to evolving customer needs

- Data-Driven Decision Making
Utilizing data analysis and understanding customer journeys enables informed decision-making and helps optimize experiences and prioritize digital transformation initiatives.

- Customer-Centric Approach
Understanding customer journeys and pain points helps optimize experiences and prioritize digital transformation efforts
 
---
# Conclusion and Key Takeaways

- Digital transformation is crucial for businesses to stay competitive and meet evolving customer expectations
- Successful digital transformation requires strategic planning, leadership buy-in, and a customer-centric approach
- Companies like Walmart, Netflix, and Nike serve as inspiring examples of digital transformation's power to drive innovation and success

---


# Technology and Applications of E-Business Systems

# Guest Lecture

# ISE328

Department of Industrial & Systems Engineering,

Hong Kong Polytechnic University

Dr Hing Kai Chan

---
# Outline

# Case Study 1: An Authentication Platform based on the Patented 3D Printing Digital Watermarking Technology and Blockchain Technology

# Case Study 2: Supply Chain Integration and Optimisation for intermodal transportation
---
# Case Study 1 Outline

# An Authentication Platform based on the Patented 3D Printing Digital Watermarking Technology and Blockchain Technology

# 1. Introduction

# 2. Phase 1 Study: Industrial Needs

# 3. Phase 2 Study: Digital Watermarking

# 4. Phase 3 Study: Blockchain-based Authentication Platform

# 5. Conclusions
---
# Introduction

The rapid development of 3D printing industry:

- in terms of the increased industry size, further segmented Industrial market, the focus shifting towards the more profitable mid- and downstream service sectors


# The difficulties in intellectual property rights (IPRs) protection
- Time consumed to authorising the rights
- Difficulties to realising the profit
- Low efficiency of protecting the rights

- The digital data, like the 3D printing design, characterised as large amount of data, real-time, rely heavily on the electronic devices, easy to tamper and lose etc., making it more difficult to store as evidence for intellectual property rights.

---

# Phase 1 Study: Industrial Needs

# Semi-structured Interviews

- Interviews with 3D Printing related companies
- Local governmental IP department
- 3D cloud computing content sharing platform
- Industrial 3DP manufacturer
- 3D printing service company
- 3DP product platform

# In industry cities

- Ningbo
- Shanghai
- Hangzhou
- Beijing
- Guangzhou
- Shenzhen

---
# Phase 1 Study: Industrial Needs

# Insights from the interviews

- R&D and design
- Manufacturing and supply chain
- Data management
---
# Phase 1 Study: Industrial Needs

# Insights from the interviews

- Potential issues from current IP Law – illegal usage activities of IP:
Easy access to obtain digital content and print
Serious brand dilution
Hard to detect infringement
Difficult for company to track for counterfeiting and tracing the origins of source materials

- Lack of IP standards and regulation in the industry
- High workload, time consuming, and costly to gain IP
- Conflicts between innovation and business opportunity
- Collision when old laws meet new ecosystem
- Complicated IP law on 3DP

- There was no real support for a sui generis (new 3DP) style right
- Some companies are completely ignorant of IPR (50-50 I would say on our interviews)
- Others are interested, but mainly in patents
- Around 10-20% were already interested in watermarking technologies
- Those involved in medical devices are most knowledgeable of the law

# Areas for Improvement

To tackle the above issues, several areas have been identified that could be improved further: licensing platforms particularly; the legal circumstances concerning 3D printed content could be overcome.

---

# Phase 2 Study: Digital Watermarking

# 1) Pre-processing

# 2) Watermark pattern generation

# 3) Watermark embedding

# Process flow of 3D printing (3D打印工艺流程)
1. CAD
2. STL convert
3. File transfer to machine
4. Machine setup
5. Build
6. Remove
7. Post-process
8. Application

# Our Patented Approach

- Watermark information is added into the original 3D digital model, which is kept by the designer and not distributed
- Making small, imperceptible changes to the model
- Objects are printed with “watermark” (i.e., changes)
- Will not affect the overall feature and functionality of the design

- These changes are recorded as a key by the designers
- Designers can have different keys corresponding to different customers
- Data can be traced (i.e., become big data)

- The coordinates of pre-determined key points from both the original and watermarked 3D models are extracted
- Their differences are calculated by a specific algorithm and then plotted as a variance graph
- The variance graph is unique for the specific pair of original and watermarked digital model
- When the design is printed, the watermark stays with the printed physical objects

---
# Phase 2 Study: Digital Watermarking

# Our Patented Approach

- The globe coordinates of all the key points of the original 3D model, x, y, zi are exported and recorded
- Then a matrix representing the original model is obtained
- Slightly change some non-functional positions or non-critical regions
- Export data points along with all coordinates and individually save in the database

- Calculate the coefficients of each modified model and the original model and save in another database recording file name and the corresponding coefficient (roMi)
- Note that all coefficients should be within a certain threshold R
- Calculate the deviation of every point of original model corresponding to each point of the modified model
- Graph the relation between position deviation and serial number of each key point, note as pi

---
# Phase 3 Study: Blockchain-based Authentication Platform

# Research on demand for 3D printing digital model authentication

- Conduct several field visits to relevant enterprises to fully understand user needs for 3DP digital model authentication in the context of digital manufacturing
- Collect target users’ profiling and identify their pain points in actual operations
- Determine user pain points regarding 3DP digital model authentication and provide a strong requirements document to support the subsequent platform construction

# Phase 3 Study: Blockchain-based Authentication Platform

# 3DP authentication platform design based on patented watermarking and blockchain

# Research on the key techniques

- Blockchain and cloud storage technology
- 3D Printing digital model
- Computer visual recognition technology
- Document compilation technology
- Authentication technology based on the patented 3D printing watermarking technology

---
# Phase 3 Study: Blockchain-based Authentication Platform

# Blockchain – is it also copyrightable?

Blockchain “may enable unprecedented levels of accessibility to information about copyright ownership, transparency and traceability of its subsequent changes”

# Specialty and Competitive advantage

1. Develop the watermarking technologies
2. Develop a means to enable the licensing of the content online

---
# Phase 3 Study: Blockchain-based Authentication Platform

# Specialty and Competitive advantage

- Blockchain can help and had been helping in restoring the evidences of intellectual property rights
- The judicial interpretation facilitated by blockchain deposition services has been recognized by The Supreme Court.

# Blockchain is no silver bullet!

The application of blockchain technology for intellectual property protection is still limited.

---
# Phase 3 Study: Blockchain-based Authentication Platform

# Specialty and Competitive advantage

# Current 3D printing Service platform
Limited to Printing-related Service

# Our 3D printing service platform
The authentication service supported by patented technology
Authentication, trading and storage Integrated for IPRs
A platform for multiple digital products
Data storage using blockchain and cloud storage technology

---
# Phase 3 Study: Blockchain-based Authentication Platform

# Key bottlenecks to be addressed

- Lack an integrated 3D printing authentication service platform with digital model property rights authentication, trading and storage service
- The commercialisation of the 3D print authentication encryption algorithm still need further development of additional extensions, such as 3D digital model compilation techniques and 3D printed entity computational visual recognition techniques.
- While blockchain technology is becoming increasingly mature for IP protection mechanisms, there is a need to build a cloud blockchain storage solution for 3D printed digital models encryption

---
# Phase 3 Study: Blockchain-based Authentication Platform

# Research objectives

- This project intends to use blockchain technology to build a 3D printing authentication platform and industry ecosystem with the patented 3D printing watermarking technology as the core:

Provides a 3D printing authentication service platform to protect the IPRs of 3D printing products in ways that easy to use, accurate and worry-free

Fills the gap in the industrial market with a platform that covering multiple product authentication services based on the 3D printing authentication

Helps promoting the standardized development of the 3 D printing industry and the process of national digital asset intellectual property protection

---
# Phase 3 Study: Blockchain-based Authentication Platform

# Research objectives

- Complete the development of core technologies around patented 3D printing watermarking technology:
3D printing digital model encryption algorithm compilation technology
3D printing entity computing visual recognition technology
Blockchain cloud storage technology

- Complete 3D printing authentication platform construction and maintenance

- Promote the protection of intellectual property rights of 3D printing enterprises and the industry

# Conclusions

- A 3DP authentication platform based on the patented 3DP watermarking and blockchain technology including three major systems: 

3 DP digital model encryption service system
3 DP authentication (validation) system
3 D digital model trading business system

---
# Case Study 2 Outline

# Supply Chain Integration and Optimisation for intermodal transportation

 1. Introduction

 2. One-stop sea and land logistics reservation and tracking system

 3. Analysis of hinterland competitiveness and prediction of port throughput

 4. Container transportation route selection based on multi-modal transportation

---
# Introduction

- Maritime Economy: National strategic plan
- Ports: an important pillar of marine economic development
- Intermodal transportation: the main form of international multimodal transport, which has the characteristics of low price, convenient, flexible and stable transportation

- A hub city linked by sea and land
- Strategic focus city for innovative development of marine economy in the 13th five year plan
- The merge of the Ningbo-Zhoushan Port
  An international shipping service platform integrating port shipping, logistics, shipping agency, finance, insurance and other functions
---
# Introduction

The intelligent and information service industry of Ningbo-Zhoushan port is still in its infancy:

- Port operation: the independent and decentralised information system leads to "information silos”
- Business management system: inconsistent database standards lead to inconsistent information resource  base
- Information platform: limited to a single industry, shipping and land transportation are relatively independent, and two-way connection has not been achieved
- The establishment of sea and land logistics booking and tracking system cannot be separated from the support of electronic logistics information system
- But there are still problems such as slow development process, inconsistent logistics standards among different logistics enterprises, and limited flexibility of suppliers
- The relatively independent sea and land logistics standards lead to differences in the evaluation criteria of the information system of the sea and land logistics enterprises
- There is a lack of an information system evaluation system suitable for both sea and land transportation
- It is very important to build an evaluation system of logistics information system suitable for sea land combined transportation to assist the system design and meet market expectations

---
# One-stop sea and land logistics reservation and tracking system

# Objectives:

- Understand the current booking process of sea and land transportation
- Explore the factors that affect the adoption of electronic reservation and tracking systems by different enterprises in the industry
- Based on the above, to develop an electronic reservation and tracking system
---
# One-stop sea and land logistics reservation and tracking system

# CLASSIC MODE OF CONTAINER BOOKING PROCESS

# THE MODE OF INTERORGANIZATION IS FOR BOOKING


# I. Organizational context

- 7. Top management support
- 8. Firm size
- 9. Ownership structure

# Technological context

- 1. Ease of use
- 2. Usefulness
- 3. Relative advantage
- 4. Cost
- 5. Information confidentiality
- 6. Service quality

# III. Environmental context

- 10. Industrial characteristics
- 11. Power: authority, supply chain partners
- 12. Industrial environment

---
# One-stop sea and land logistics reservation and tracking system

# Insights:

- Some shipping companies have developed and launched one-stop booking and tracking platforms
- But such platforms are only used in the field of shipping
- Sea and land transportation belong to different fields, and the shipping space and means of transportation (ship, train, automobile) are operated by different enterprises
- It is still difficult to realise the booking and tracking activities of through one platform
- Requires multi-party coordination of the industry
- Such platforms need a lot of data to support

# Objectives:

- Comparison of time series methods for container throughput prediction
- Develop a hybrid time series prediction model based on SARIMA and SVR
- Explore the applications of new technology in marine supply chain

# Comparison of time series methods for container throughput prediction:

- Ningbo port as the research object
- The accuracy of different prediction models on the port throughput data is compared
- Data: Historical data of Ningbo port container throughput from the Ningbo statistical yearbook
- Training set to validation set: 80:20 (Deo et al., 2016; Al-Musaylh et al., 2018)
- The validation set is used to verify the prediction model obtained from the training set

- Six time series prediction models are used to mine and verify the same container throughput time series data:
- Moving Average (MA)
- Multivariate Adaptive Regression Spline (MARS)
- Auto-Regressive Integrated Moving Average (ARIMA)
- Grey Model GM(1,1)
- Support Vector Regression (SVR)
- Artificial Neural Network (ANN)
- Take the throughput of the previous years as the input variable to predict the throughput of the next year

# Comparison of time series methods for container throughput prediction:

|Models|ME|RMSE|MAE|MPE|MAPE|
|---|---|---|---|---|---|
|MA|346.17|377.90|346.17|17.96|17.96|
|MARS|107.38|120.03|107.38|5.55|5.55|
|ARIMA|49.06|74.43|61.71|2.39|3.14|
|GM(1,1)|-257.89|266.88|257.89|-13.58|13.58|
|SVR|14.91|44.30|44.25|0.63|2.38|
|ANN|108.44|162.14|133.40|5.29|6.78|

---
# Analysis of hinterland competitiveness and prediction of port throughput

# Comparison of time series methods for container throughput prediction:

- Insights:
 - The prediction accuracy of MARS and ARIMA, two traditional regression methods, are significantly better than that of MA and GM (1,1)
 - In addition, the prediction performance of ARIMA is better than MARS
 - ANN performs worse than SVR, ARIMA and MARS
 - Obviously , SVR has advantages in dealing with nonlinear problems such as container throughput prediction, especially the data scale of this study is relatively small

# Hybrid time series prediction model based on SARIMA and SVR: 

# Insights:

- The prediction accuracy can be improved by adding Gaussian white noise to the learning model
- Gauss white noise and SARIMA's results together cannot improve the results
- Incorporating the results of SARIMA into the prediction model does not improve the accuracy

# Container transportation route selection based on multi modal transportation

# Introduction:

- The first step to find the optimal path is to determine the optimisation objectives
- There are three optional optimisation objectives, namely, the optimal cost, the shortest time, and the pareto optimisation considering both time and cost
- The optimisation goal here can be provided to end users to choose the optimisation goal they want

---
# Container transportation route selection based on multi-modal transportation

# Total transportation cost objective function：

𝑍1 = min(
∑∑ 𝑄𝑐𝑖𝑗𝑚𝑑𝑖𝑗𝑚𝑥𝑖𝑗𝑚 + ∑∑ 𝑄𝑐𝑖𝑚ℎ𝑦𝑖𝑚ℎ + 𝑃𝑇)

𝑖,𝑗∈𝑁𝑚∈𝑀
𝑖∈𝑁𝑚,ℎ∈𝑀

Transportation cost
Transshipment cost
Penalty cost

# Total transportation time objective function：

𝑍2 = min(
∑∑ 𝑡𝑖𝑗𝑚𝑥𝑖𝑗𝑚 + ∑∑ (𝑄𝑡𝑖𝑚ℎ𝑦𝑖𝑚ℎ + 𝑡))𝑖

𝑖,𝑗∈𝑁𝑚∈𝑀
𝑖∈𝑁𝑚,ℎ∈𝑀

Transportation time
Transshipment time
Penalty cost

# Risk index objective function：

Z3 = min( 1 / 𝑇𝐶𝐼𝑙)

---
# Container transportation route selection based on multi-modal transportation

# Penalty function 𝑃𝑇 :

\[
P_T = 
\begin{cases} 
(a(u - T)Q & T < u \\ 
0 & 0 \leq T \leq u \\ 
b(T - V) & T > v 
\end{cases}
\]
# Node Confidence and Route Information

\[
TC_I = \sum_{i \in N} \sum_{m \in M} W_i C^m_i + \sum_{i,j \in N} \sum_{m \in M} W_{ij} C_{ij}^m
\]

where \( n_1 \) is the number of nodes, and \( n_1 - 1 \) is the constraint.

# Constraints

\[
\sum_{m \in M} x_{ij}^m = 1 \quad \forall i,j \in N
\]
\[
\sum_{m \in M} y_{ij}^m = 1 \quad \forall i,j \in N
\]
\[
x_{ij}^m \in \{0,1\} \quad \forall i,j \in N, \forall m \in M
\]
\[
\sum_{m \in M} x_{ij}^m - \sum_{m \in M} y_{ij}^m = 0 \quad \forall i,j \in N
\]

---


# Introduction to eBusiness and Application

# Electronic Business Applications

# In this Lecture

# Summary

1. What is e-business?
2. Examples of e-business.

# Idea of e-business

“e” stands for “Electronic”

By Louis Gerstner, CEO of IBM in its advertising campaign in the 1990s.

At that time 
e-Business was defined as “the transformation of key business process through the use of Internet Technologies”. 

---
# Idea of e-business

- use Electronic Means to conduct business / any business processes.

- Business means a company, a corporation, partnership, or have any such formal organization.

# Business is:
- the activity of making money
- producing or buying and selling products (goods and services)
- Shipping
- procurement
- Manufacturing
- ERP or management

---
# Idea of e-Business

- Transforming from book shop into e-Commerce and e-Business

# Business Categories
- RETAIL
- TELECOMMUNICATIONS
- BANKING
- TOURISM
- PUBLIC TRANSPORT
- ENTERTAINMENT

---
# Examples of e-business

Examples can be found easily in everywhere:

- e-Banking (HSBC, Hang Seng Bank)
- Online Auction (e-Bay)
- Online Book Seller (Amazon)
- Online Game Providers
- e-Government
- e-Public Services
- e-Health
- e-Learning


# Steps in analyzing the applications of e-business:

1. Analyze the existing process.
- Flow Chart.
2. Identify the advantages and disadvantages of the existing processes.
3. Determine what processes can be (to) improve.
- Outcome, will be system.
4. Identify how e-business is applied for the new approach.
- Apply electronic means to replace existing process.
5. Identify the advantages of new approach.
- What processes have improved?
6. Identify the disadvantages of new approach.
- Any drawback?

---
# Example of e-business Bank

- HANG SENG BANK

---
# Example of e-business Bank

# Functions of Bank

1. Banking
- Deposit money
- Withdraw Cash
- Money Transfer
- Bill Payment

2. Investment
- Securities
- Foreign currency exchange
- IPO
- Investment Deposits
- Gold Margin

3. Insurance
- Travelsure
- Home Care
- Personal Accident
- Term Life

4. Personal Credit
- Loan
- Tax Comforter
- Overdraft Facility

5. Mortgage

- Valuation
- Mortgage Loan

6. Credit Card

- Credit Card Application
- Card Security Service

# Example of e-business Bank

# Tradition approach:

- Deposit Money

# Example of e-business: e-Banking

# Step 1: Analyze the existing process.

|Process|Person|Time (s)|
|---|---|---|
|Request Deposit & Amount|Customer|5|
|Report A/C no.|-|5|
|Fill in Deposit Form|Staff|5|
|Count the Amount|-|20|
|Input A/C no. into System|-|10|
|Print the Data on Deposit Slip|-|15|
|Return slip to customer|-|2|
|Total|Total|62|


# Step 2: Identify the advantages and disadvantages of the existing processes.

# Disadvantages for the company:

- Staffing cost
  Types of staffs: Counter service officer, shop manager, security guards, etc.

- Rent.
  Depends on the size of the shop.

- Facilities cost.
  Decoration, electricity, etc

- Maintenance cost.
  Repair/replacement, etc.

- Various insurance costs.

- Limited office hours.

- Non-environmental friendly.
  Wasting paper: various of documentation work, receipt, etc.

- Risks of Human Error.
  Miscalculation of money, input incorrect data, etc.

- Time consuming.
  Counting money, input data, etc.

---
# Example of e-business: e-Banking

# Cost Analysis

|Initial cost:|Decoration & Furniture|$500,000|
|---|---|---|
|Staffing cost:|Counter officer|$12,000|
| |Supervisor|$15,000|
| |Branch manager|$30,000|
| |Security guard|$10,000|
|Rental cost:|Tsim Sha Tsui ~ 7400 ft.|$27,000|
|Facilities cost:|Electricity|$10,000|
|Maintenance cost:|Repair/Replace|$1,000|
|Total|Total|$605,000|

---
# Example of e-business: e-Banking

# Disadvantages for the customers:

- Wasting time.
  Go to the shop, Queuing, etc.
- Inconvenience.
  Office hours, etc.

---
# Example of e-business: e-Banking

# Step 3: Determine what processes can be (to) improve.

- Save Cost, Reduce processing time

# Improved approach: (Quick Deposit Machine)

# Step 4: Identify how e-business is applied for the new approach.

# Step 5: Identify the advantages of new approach.

# Advantages of new approach:

- Shop size smaller.
- Decoration much lesser.
- Staff number reduced.
- Manual process reduced.
- Risk of human error reduced.
- Lead time of the process reduced.
- No office hour limitation.

---
# Old process

|Process|Person|Time (s)|
|---|---|---|
|Request Deposit & Amount|Customer|5|
|Report A/C no.|-|5|
|Fill in Deposit Form|Staff|5|
|Count the Amount|-|20|
|Input A/C no. into System|-|10|
|Print the Data on Deposit Slip|-|15|
|Return slip to customer|-|2|
|Total|Total|62|

# New process

|Process|Person|Time (s)|
|---|---|---|
|Input A/C no.|Customer|10|
|Feed in the money|-|20|
|Print Receipt|-|5|
|Total|Total|35|

---
# Example of e-business: e-Banking

# Cost Analysis

- Old process
| | |$|
|Initial cost:|Decoration & Furniture|500,000|
|Staffing cost:|Counter officer|12,000|
| |Supervisor|15,000|
| |Branch manager|30,000|
| |Security guard|10,000|
|Rental cost:|Tsim Sha Tsui ~ 7400 ft.|27,000|
|Facilities cost: |Electricity|10,000|
|Maintenance cost: |Repair/Replace|1,000|
|Total| |605,000|

- New Process
| | |$|
|Initial cost|Machine|70,000|
| |Decoration & Installation|50,000|
|Rental cost:|Tsim Sha Tsui|1,500|
|Facilities cost:|Electricity|500|
|Maintenance cost:|Repair/Replace|500|
|Total| |122,500|

---
# Example of e-business: e-Banking

# Step 6: Identify the disadvantages of new approach.

# Disadvantages:

- Machine costs.
- Installation fee.
- Maintenance costs.
- Security.
- Inconvenience to elders

# Summary:

- Analyze the existing process.
- Identify the advantages and disadvantages.
- Apply electronic means to replace existing process.
 - Quick Deposit Machine
- Identify the advantages and disadvantages of the new approach.
 - Reduced the Cost, and Processing Time.

---
# Example of e-business: e-Banking

# Tradition approach:
- Securities

# Example of e-business: e-Banking

# Step 1: Analyze the existing process.

|Process|Person|Time (s)|
|---|---|---|
|Reach an Agent|Customer|120|
|Identify yourself|-|10|
|Verify the identity|Staff|10|
|Make order|Customer|20|
|Input Data|Staff|10|
|Confirmation|-|5|
|Total|Total|175|

# Step 2: Identify the advantages and disadvantages of the existing processes.

# Disadvantages for the company:

- Human mistakes.
- Listening to others spoken language.
 - “command”, “stock code”, “quantity”.
- Incorrect in Input data.

# Mistakes lead to:
- Financial lost.
- Lost of customers.
- Damage in company reputation.

---
# Example of e-business: e-Banking

# Disadvantages for the company:
- Staff.
- required many staff to receive calls.
- High cost in making records.
- voice recording.

---
# Example of e-business: e-Banking

# Disadvantages for the customers:

- Hard for Real time transaction.
- Stock Prices changes every sec.
- Transaction must be quick.
- Can’t wasting time in queuing.
- Long lead time for customer identification/verification.
- Can’t wasting time in contacting servicing staff on call.


# Step 3: Determine what processes can be (to) improve.

- Save Cost
- Reduce processing time.

# Improved approach: (Internet)

# Step 4: Identify how e-business is applied for the new approach.

Stay Home/Office - Get online - Bank (website)

# Step 5: Identify the advantages of new approach.

 # Advantages of company:

 - Avoid human error made by staff.
 - Customers become self servicing.

 # Advantages of customer:

 - Transaction faster.
 - Response to the market faster.
 - Wider Accessibility.
 - More command support.

---
# Example of e-business: e-Banking

|Command|Description|
|---|---|
|Market Order|Client does not set a limit price. Such order will be executed at prevailing market at time of execution.|
|At Auction Limit Order|A limit order with a specified price for single price auction during pre-open session.|
|At Auction Market Order|This is a market order which can only be inputted for single price auction during the pre-open session.|
|Limit Order|This order type allows the buyer to define the maximum price to pay and the seller the minimum price to accept.|
|Stop Loss Order|A sell instruction to preset the selling price range.|
|All-In-One Order|A limit buy order followed by either a limit sell order with selling price higher than the purchase price or a stop loss order.|
|Win-Win Order|This order type allows to sell the shares through a pair of limit sell and stop loss orders.|

---

# Old process

|process|Person|Time (s)|
|---|---|---|
|Process|Customer|120|
|Identify yourself|-|10|
|Verify the identity|Staff|10|
|Make order|Customer|20|
|Input Data|Staff|10|
|Confirmation|-|5|
| |Total|175|

# New process

|Time (s)|Process|Person
|---|---|---|
|10|Login|Customer|
|10|Select function|-|
|15|Input A/C no. and Amount|-|
|10|Receipt & Confirmation|-|
|45|Total Time|

---
# Example of e-business: e-Banking

# Cost Analysis (Securities)

| |Old process|$| |New process|$| |
|---|---|---|---|---|---|---|
|Initial cost:|Decoration & Furniture|500,000|Initial cost:|Web Design|50,000| |
|Staffing cost:|Counter officer|12,000| |Office computer|20,000| |
| |Supervisor|15,000|Staffing cost:|Programmer|15,000| |
| |Branch manager|30,000| |Supervisor|20,000| |
| |Security guard|10,000| |Rental cost:|Web server|1,600|
|Rental cost:|Tsim Sha Tsui|27,000| |Facilities cost:|Electricity|300|
|Facilities cost:|Electricity|10,000| |Maintenance cost:|Repair/Replace|1,000|
|Total|605,000| |Total| |106,900| |

---
# Example of e-business: e-Banking

# Step 6: Identify the disadvantages of new approach.

- Disadvantages of customer:

- Risk of inaccessible.

---
# Traditional bookstores VS amazon.com e-Bookstores

# Example of e-business: e-Bookstores

# In Tradition: (Book Store)

# Disadvantages for the company:

- High Fixed cost.
 - Wide space,
 - High level decoration to provide a leisure reading environment.
- Risk of stock keeping.
 - Stocks are “books”.
 - Damage by customers.

- High inventory holding cost.
 - Keep humidity of the room temperature.
- High/Distributed inventory level.
 - Each shop keeps certain inventory.

# Advantages of company:

- Avoid high fixed cost.
- Reduce the risk of book damaging.
- Keeping low inventory cost.
- Centralized warehouse.

# Inventory Level

|Shop|Book A|Book B|
|---|---|---|
|1|20|30|
|2|20|30|
|3|20|30|
|.|.|.|
|8|20|30|

# Inventory Replenishment

- Inventory Level

|Shop|Book A|Book B|
|---|---|---|
|1|20|30|
|2|20|30|
|3|20|30|
|.|.|.|
|8|20|30|

- Demand

|Shop|Book A|Book B|
|---|---|---|
|1|25|5|
|2|10|20|
|3|0|10|
|.|.|.|
|8|5|50|

- Safety Stock

|Shop|Book A|Book B|
|---|---|---|
|1|10|15|
|2|10|15|
|3|10|15|
|.|.|.|
|8|10|15|

- Back Order/Surplus

|Shop|Book A|Book B|
|---|---|---|
|1|-5|25|
|2|10|10|
|3|20|20|
|.|.|.|
|8|15|-20|

# Back Order/Surplus Replenish to Safety Stock

- Inventory level

|Shop|Book A|Book B|
|---|---|---|
|1|20|30|
|2|20|30|
|3|20|30|
|.|.|.|
|8|20|30|
|Total|160|240|

- Demand 

|Shop|Book A|Book B|
|---|---|---|
|1|25|5|
|2|10|20|
|3|0|10|
|.|.|.|
|8|5|50|


# Inventory level

|Centralized Warehouse|Book A|Book B|
|---|---|---|
|1|80|150|

# Disadvantages of company:

- Relatively higher transportation cost.

# Advantages of customer:

- Accessible 24 hrs.
- Easier to search for specify books.

# Summary:

- Apply electronic means to replace existing process.
 - Internet.
- Advantages.
 - Create a Centralized Warehouse.
 - Minimize the Safety Stock level.

---

# Technologies for Inventory Optimization

1. Recognize trends and optimization
2. Understand how specific SKUs impact sales
3. Faster decision making at all levels
4. Streamline product allocation

# New business opportunities

- e-Publication

# In tradition: (Publication)

- Printing out the manual script
- Submit manual script to publisher
- Editing
- Send to the printer
- Doing the printing and binding
- Deliver to different book stores
- Display

---
# Example of e-business: e-Bookstores

# Advantages to company

- More unique books.
- Increase the diversity of collections.

# Advantages to authors

- Reduce the publication lead time.
- Readers can come from world wide.

---
# Traditional music stores VS Online music stores

# Examples of e-business: Online music stores

# In Tradition: (Music Store)

# Disadvantages for the company: 

- High Fixed cost.
- Wide space,
- Leisure environment,
- Numerous of high quality music players / displayers.
- Risk of stock keeping.
- Distributed inventory.

# Advantages and Disadvantages for the Company
- Avoid High Fixed cost.
- Search function.
- Sample music / video.
- Keeping low inventory cost.
- Centralized warehouse.
- Availability of electronic version.

# Disadvantages of company:
- Relatively higher transportation cost

---
# Steps in analyzing a process for improvement

1. Analyze the existing process.
- Flow Chart.
2. Identify the advantages and disadvantages of the existing processes.
3. Determine what processes can be (to) improve.
- Weakness of existing process.
4. Identify how e-business is applied for the new approach.
- Apply electronic means to replace existing process.
5. Identify the advantages of new approach.
- What processes have improved?
6. Identify the disadvantages of new approach.
- Limitations

# Reasons of driving e-Business

Many people say in the business world already transition from physical reality based on atoms to a digital one. Many business processes become digitalization.

- Mail
- Form
- e-mail
- e-form

# Reasons of driving companies go e-business:

1. # Customer-Oriented Trends

- Service availability
- Servicing time
- Self-service
- More product choices
- Integrated solutions


2. # Service

- Integrated sales and service
- Seamless support
- Flexible fulfillment
- Convenient service delivery


3. # Organizational

- Outsourcing
- Contract manufacturing
- Virtual distribution


4. # Enterprise technology

- Integrated enterprise applications.


5. # General technology

- Wireless Web applications
- Portable computing and information appliances
- Infrastructure convergence
- Application service providers.

---
# Reasons of driving e-Business

# 1. Customer-Oriented Trends:

- Service Availability (Ability to provide immediate service)
 - first step to attract consumers to use your service.
 - most customers count the speed of service as a key reason
 - they like to get the service as fast as possible
 - they hate waiting for service

- Servicing Time
 - important factor to retain consumer.
 - customers look for companies that provide faster service.
 - to customers, time is money.
 - companies are forced to reduce the number of steps it takes to serve customers
 - enhance the efficiency by technology

---
# Reasons of driving e-Business

e.g. Deposit money

How to reduce the number of processes, and time required for each process.

Reducing the processing time of counting, form filling, and data entry.

# Case A: Counter Service

|Fill forms|+ 15 Sec|
|---|---|
|Manually count money|+ 20 Sec|
|Input command|+ 15 Sec|
|Receipt / Confirmation|+ 10 Sec|
|Total|= 60 Sec|

# Case B: Quick Deposit Machine

|Input A/C no.|+ 10 Sec|
|---|---|
|Manually Feed in Cash|+ 10 Sec|
|Automatic counting|+ 5 Sec|
|Receipt / Confirmation|+ 10 Sec|
|Total|= 35 Sec|

---
# Reasons of driving e-Business

# 1. Customer-Oriented Trends:

- Self-service
 - customers are looking for self-service solutions that not only save them time but also empower them.
 - they can finish their transaction (buying what they want) without the help of sales personnel.
 - they are able to shop at anytime, and if possible should be in anywhere.

# Example: Online Shopping

Consumers are changing their buying habit from traditional face-to-face model to purchase online.

In the survey, 67% of the respondents said they had searched for the company name, product or service names, or advertising slogan that they saw in offline marketing or ads. And of those online searchers who started with an offline marketing message, 39% eventually made a purchase.

---
# Reasons of driving e-Business

# 1. Customer-Oriented Trends:

- More product choices
 - customers love one stop locations that offer them everything under one roof.
 - however, impossible in traditional retailer
 - because of the limited shelf space and inventory constraints, especially in Hong Kong
 - online companies can offer more different merchandise than a physical company does.


- Integrated solutions

 - Consumers don’t like to go to many places to look for different services they want.
 - They want integrated-service business that provide them one-stop shopping needs.
 - In today’s business, customers usually have too many choices, products, and stores.
 - To solve the “choice” problem, customers increasingly looking for integrated solutions that can make their decision process easier.

---

# 2. Service:

# Integrated sales and service:

- Its idea is to narrow the gap between sales and services.
- Provide better customer relationship.
- Customers usually like to have some access about the information of product and the services they will have before they purchase the product.

# What is Sales?

In economics, it is an exchange process between two parties. 
It involved in selling products or services in return for money or other compensation.

# What is Service?

It is a form of product that consist of activities, benefits, or satisfactions offered for sale that are essentially intangible and do not result in the ownership of anything.
---
# Reasons of driving e-Business

# Seamless support

- Provide user friendly and easy-to-use customer service processes with single point of contact.
- Named “customer service easy” and “solution oriented” are the most important trends in today’s business.

# Flexible fulfillment and convenient service delivery

- Home delivery and other unique fulfillment services continue to gain importance.
- In old model, companies waiting for customer to come.
- In new model, companies bring their services to customers.

---
# Reasons of driving e-Business

# 2. Service:

- Increased process visibility
---
# Reasons of driving e-Business

# 3. Organizational:

# Outsourcing Management

- Today’s business climate demands companies to be flexible in order to survive.
- It forces companies to out  specific business processes in order to improve the overall business performance, called Business process outsourcing (BPO).
- Traditionally, outsourcing is a cost-control technique.
- Today, outsourcing is for quality improvement.
- Outsourcing always takes about some parts that you are not strong/specialize on.
- Then you out  it in order to improve the product quality.

# Contract manufacturing
- Usually used by those companies, if their capital is very tight, or if they don’t want to spend much money in install the machines, building a factory, order too urgent, etc.
- Companies only focus on the designing the core/key component and subcontract other to suppliers.
- This can help them to increase their flexibility.
- To move them from capital/asset-intensive focus to knowledge-intensive one.

e.g. Limit capacity

If a shoes manufacturer has to produce 1000 pair of shoes, but its production capacity can produce only 600 unit, then it can contract out to other manufacturers.

# Virtual distribution
- A new intermediary , like a virtual company
- These companies aggregate buyers and sellers by using Web technology.
- They aggregate the marketing and product information content and establish efficient marketplaces.

e.g. e-Chemical
A neutral online marketplace that allows registered buyers and sellers to select a product, get a price, and order or track small chemical shipments online through its web site.

---
# Reasons of driving e-Business

# 4. Enterprise technology:

- Integrated enterprise applications
- Traditionally, most companies separated their business application, creating specialized functional areas
- Such as Accounting, Finance, Manufacturing, Distribution, and Customer service.

---
# Reasons of driving e-Business

# 4. Enterprise technology:

- Integrated enterprise applications
- Each of them work as an Individual Unit, totally Independent, lacking or with little communication with others.
- Recently, companies recognize that if a chain of processes is to perform at a high level.
- The individual business functions (departments) and their applications, which supporting them must be tightly linked with each other.

# 4. Enterprise technology:

Because of the popularity and maturity of ERP system…

- Companies who interested in implementing such application can save lot of constructing time and unpredictable cost expenditure.
- Most importantly, companies can then focus on their core business processes.
- It can increase the speed with which decisions are made and communicated.
- Companies and customers have become accustomed to having information in real-time at their fingertips.

# Example: Systems Applications and Product (SAP)

- SAP is the world’s leading provider of e-business software solutions.
- Through the mySAP.com e-business platform, businesses are improving relationships with customers and partners, streamlining operations, and achieving efficiencies throughout their supply chains.

# SAP System
It is an integrated ERP software including different functions such as Finance, Materials, Production, Quality, Maintenance & HR. 

---
# Reasons of driving e-Business

# 5. General technology:

# Wireless Web applications
- with the widespread rollout of wireless infrastructure, a new wave of consumer and business applications will begin.
- Wireless applications increase the efficiency of performing everyday tasks, such as organizing business, personal affairs, sending e-mail, making phone calls, etc.

# Portable computing and information appliances

- The reduction in device size and cost, and the improvements in the functionality, storage and reliability stimulate the usage of portable appliances.
- Consumers are more demanding to have same productivity and communications capability everywhere as they are working on their desks.

---


# Introduction to e-Commerce
---
# Difference between e-commerce and e-business

# Argument

There is no Exact definition in defining the meaning and limitations of both e-commerce and e-business.

Researchers and ICTs experts are arguing on this topic.

Rayport and Jaworksi (2003): “e-commerce includes the entire world of electronically based organizational activities that support a firm’s market exchanges – including a firm’s entire Information System’s infrastructure”.

Kalakota and Robinson (2003) “e-business encompasses the entire world of internal and external electronically based activities, including e-commerce”.

---
# Difference between e-commerce and e-business

We adopt this idea: 
Laudon and Traver (2007): 
They proposed that “it is important to make a working distinction between e-commerce and e-business because they refer to different phenomena”.

# e-business (1)

It refers primarily to the digital enablement of activities and processes within a company. 
e.g. Information systems under the control of the company.

---
# Difference between e-commerce and e-business

# e-business (2)

It does not include commercial transactions across the company’s boundaries. 
It will not directly generate revenue for the company from outside the company’s boundaries. 
e.g. a company’s online inventory control system is a component of e-business, you will not generate revenue from it.

# e-commerce

Includes commercial transactions across the company’s boundaries. 
It will directly generate revenue for the company from outside the company’s boundaries.

---
# What is transaction?

Transactions are exchanges that occur when one economic entity sells a product or service to another entity. In e-commerce, a transaction should involve money. Can generate revenue.
---

# Difference between e-commerce and e-business

# Which services are regarded as e-commerce?

Providing Information

- Simply providing information to customer alone is NOT e-commerce.

e.g. Checking balance, request e-statement, etc.


e-Commerce

- Generate revenue for company.

e.g. Buying stock, money transfer (with service charges), etc.
---

# Seven unique features of e-business technology

1. Ubiquity
2. Global reach
3. Universal standards
4. Information Richness
5. Interactivity
6. Information Density
7. Personalization/Customization
---

# Seven unique features of e-business technology

# 1. Ubiquity

It means just available everywhere, at all times. e-Business technology moves the marketplace from traditional physical space to your desktop / mobile / etc. Ubiquity reduces the transaction costs, mainly in the cost of participating in a market.

e.g. Think about the ways of checking the balance of your bank account.


# 2. Global reach

e-Business technology permits commercial transactions to cross cultural and national boundaries far more conveniently and cost effectively. The potential market size for e-commerce merchants is roughly equal to the size of the world’s online population.

e.g. As we mentioned before, whoever has a computer and can access Internet can be your customer. In contrast, most traditional commerce is local or regional.


# 3. Universal standards (common platform)

It refers to the technical standards of the Internet. The universal technical standards of Internet and e-commerce greatly lower market entry cost, meaning the cost just to bring their goods to market. It also reduces the search costs that the effort required to find the suitable products.


# 4. Information Richness

Information Richness refers to the complexity and content of a message. It refers to the personal, face-to-face service provided when making a sale. Traditional markets make good use of them to increase their selling power.

e.g. Buying a digital camera

- When you go to buy a digital camera in some shop in person, the salesperson in the shop will usually “nicely” explain the features and functions of the product, letting you play around with different camera models. You can ask questions and their opinions about the camera.

However, since the larger the audience reached, the less rich the message. A trade-off between richness and reach should be made.

e.g. Buying digital camera

- If you buy it online, no salesperson will come to service you.
- This is one of the disadvantages in doing e-commerce.
- When you do business, you have to realize that whether your customers can purchase the product online or not. If your products can also be purchased online, then you have to provide much better customer services to attract them to shop.


# 5. Interactivity

e-Commerce technology allows for two-way communication between merchant and consumer.

Television, for example, cannot ask viewers any questions or enter into conversations with them.

In contrast, all of these activities are possible on an e-commerce Web site.

Interactivity allows an online merchant to engage a consumer in ways similar to face-to-face experience.

e.g.

- Internet conferencing, internet phone, e-mail, etc.
- However, this information richness still may not be as good as traditional approach.


# 6. Information Density

e-business technologies reduce cost in information collection, storage, processing, and communication. In the mean time it also increases the currency, accuracy and timeliness of information.

e.g. The old way to share information……
Paper, Mail, Voice


# 6. Information Density

making information more useful and important than ever. In e-commerce market, therefore, prices and costs become more transparent.

e.g. Comparing Prices

- Strictly speaking, this fast spreading of information feature is because of the advantage of the Internet.
- Getting the idea of the price of a iPod Nano.


# 7. Personalization/Customization

e-Business technologies permit personalization. Merchants can target their marketing messages to specific individuals by adjusting the message to a person’s name, interests, and past purchases record.

e.g. Nike enables consumers to design their own pair of personalized shoes by allowing consumers to specify the colors for the various shoe parts.

e.g. More example:

For customers:

You can set your preference to include the things or news that you are interested in.


For companies:

They can categorize their customers according to their buying habits, age groups, academic background, etc. and deliver some special or tailor-made promotion to them.

For customization, user’s preferences or behavior can be changed as desired.
---

# Seven unique features of e-business technology

# 7. Personalization/Customization

# Advantages:

1. Save time & money on repetitive searches
- e.g. find movies by the same director
2. Better information
- e.g. filter out the advertisements that we don’t want
3. Tailor a product to a customer’s taste
- e.g. able to offer unique combination
4. Create a feeling of “ownership” of one’s web experience


# Disadvantages:

1. Anonymity preferred
- e.g. some people may not want to be identified
2. Lack of relevance
- e.g. I don’t want customized earrings
3. Impossible
- e.g. I can’t watch American TV shows on Hulu.com, if I am out of the country.
---

# Introduction to m-commerce

# Basic Introduction to m-commerce

“m” refers to Mobile

Idea of m-commerce is to conduct commerce using mobile device. e.g. mobile phone, PDA, etc.

# Other definitions:

- “next generation e-commerce” (Rana Tassabehji, 2003)
- “a subset of e-commerce” (C. Coursaris & K. Hassanein, 2002)
- “at least one side uses mobile communication techniques.” (N Kreyer, K Pousttchi, K Turowski, 2002)
- “any transaction with monetary value that is conducted via a mobile network” (I. Clarke III, 2001)

# Survey In 2005:

- There are many people using mobile phone than there are in using Internet.
- An estimated 1 billion people having a mobile phone.
- Mobile phone usage is much higher especially in Asia and Europe.
- Because of the huge number of mobile phone subscribers, it induces more new business opportunities.
- In the last 10 years, many consumers becoming increasingly comfortable with online purchasing.
- It is believed that in the next phase for those consumers who are looking for even more convenient methods of doing purchasing will be “mobile purchase”.

This is the reason why m-commerce becomes more popular and important.
---

# Applications of m-commerce technologies

---
# Applications of m-commerce technologies

# Commonly used in Six areas:

1. Mobile Ticketing.
2. Mobile Coupon.
3. Information Services.
4. Mobile Banking.
5. Mobile Marketing.
6. Mobile Payment.


# 1. Mobile Ticketing

The idea is to make use of the mobile phone to buy and obtain the tickets from any location and at any time.

e.g.

- It can be used in buying mass transit tickets, sports tickets, and cinema tickets.


# Advantages and Disadvantages of m-Ticketing

# Advantages:

- Reduce cost of ticket printing and mailing.
- Reduce staffing costs.
- Improve customer convenience.
- Increase the accessibility to tickets.

Indeed, this feature is even more convenient than using Internet because all you need is just a mobile phone.

# Disadvantage:

- No battery !!
---

# Applications of m-commerce technologies

# 2. Mobile Coupons

- Mobile ticketing technology can be used for the distribution of coupons to the mobile phone users.
- Then the customers can present the coupons in their mobile phones to shop when they use them.

# Advantages of m-Coupons:

- Its cost effective, again companies can save money in doing the printing, and distributions.
- The coupons are stored in the mobile phone, so that customers can have the coupons with them all the time whenever they have their mobile phone with them.
- Quick and easy to deliver.
- Compatible with the needs of target customers.
---

# Applications of m-commerce technologies

# Paper Coupon vs. Mobile Coupon

|Feature|Paper Coupon|Mobile Coupon|
|---|---|---|
|Logo Support|Yes|Yes|
|Preparation and Distribution|7 to 14 days|Less than 24 hours|
|Controlled time distribution (e.g. distribution at 13:00)|No|Yes|
|Ability to modify after published|No|Yes|
|Real time tracking|No|Yes|
|Automatic expiration|No|Yes|
|Distribution based on customer's interest|No|Yes|
|Environment friendly|No|Yes|
---

# Applications of m-commerce technologies

# 3. Provide Information Services

A wide variety of information services can be delivered to mobile phone users in much the same way as it is delivered to PCs.

e.g.
- Map/Locations
- News services
- Stock Information
- Sports results
- Financial records
- Traffic data

# Advantages:

- Increase music, animation, video and reading experiences
- Tell the specific location of the user’s mobile
- Search for internet content in search engine conveniently
- Get real-time information in everywhere at anytime

# So that, you can …...

- Prevent traffic jam with real-time traffic data
- Identify your location, destination and route in a map
- Make a quick decision in stock market
- Receive latest news in the world
---

# Applications of m-commerce technologies

# 4. Mobile Banking

Many banks and some financial institutions enable their customers not only to access their account’s information, but also to make transactions.

e.g.

- Purchasing stocks
- Money transfer

# Hang Seng Mobile Trading Demo
1. Login
2. Main Menu
3. Transaction


# Advantages of m-Banking:

- increase customer satisfaction and loyalty by providing anywhere, anytime banking
- lower administrative costs / handling charges
- lesser number of branches
- inform customers better, e.g. reminder of repayment
- save papers, e.g. receipts & forms


# Technologies Behind m-Banking:

1. IVR (Interactive Voice Response)
2. SMS (Short Messaging Service)
3. WAP (Wireless Access Protocol)
4. Standalone Mobile Application
---
# Applications of m-commerce technologies

# Technologies Behind m-Banking:

1. IVR (Interactive Voice Response)
- Customer makes a call at the IVR number and chooses options by pressing the corresponding number in their keypads.
- The corresponding information will be read out.
- Major limitation: only provides Enquiry-based service


2. SMS (Short Messaging Service)
- Customer requests for information by sending an SMS containing a service command to pre-specified number.
- The bank responds with a reply SMS containing the specific information.
- Main advantage: almost all mobile phones are SMS enabled.


3. WAP (Wireless Access Protocol)
- Similar to internet banking.
- Customers use WAP compatible browser on their mobile phones and access the bank’s site.
- They can access all enquiry and transaction based services and also more complex transaction like trade in securities through their phone.


# 4. Standalone Mobile Application Clients

- Customers are required to download the mobile applications clients into their mobile phones.
- Users’ mobile phones must support one of the many development environments like J2ME.
- Major limitation: the applications needs to be customized to each mobile phone on which it might finally run.


# 5. Mobile Marketing

Many companies are now using m-commerce to do marketing and advertisement.

e.g.

- Some company using the automatic dial-up program to make a call to you, and play the voice message that introduces their companies, products, and services.
- Another way is done by sending you some messages.
---

# Applications of m-commerce technologies

# Advantages of m-Marketing:

Mobiles are attractive medium for marketers because:

- People are always reachable
- Phones give the user’s location
- Relatively high response rate
- Cost-effective
- High-speed message delivery
- Targeted
- Interactivity
---

# Applications of m-commerce technologies

# 6. Mobile Payment

- This is often referring to m-Payment
- At least one part of the transaction is conducted using a mobile device through a mobile telecommunication network, or via various wireless technologies.


# Advantages of m-Payment:

- Queue avoidance
- Enhanced payment instrument availability
- Complement to cash
- Digital content and services, e.g. ticketing
- Small value purchases at point of sale, e.g. vending
- Being used for sudden need for payments

---

# Case Study: Container Terminals

# Functions of Terminals

- Provide parking place for vessels.
- Helping the vessels to unload / upload containers.

# Locations

TSING YiISIANM

Rambler channel

# Terminals

- HIT terminals
- terminal 6 & 7
- terminal (East)
- Kwai Chung terminal

# Additional Features

- Traffic view cam
- Virtual tour
---
# Case Study: Container Terminals

# A Simple Operation flow of the Terminal (1):

- Once a vessel (full of containers) arrives the Terminal.
- First, it will be assigned to park in one of the berths.
- Then the terminal will use the Quay cranes to lift the containers and load it to the Internal Tractors.

Quay Cranes are designed to provide fast loading and discharging container to/from large ocean vessels. They are built to handle panamax and post-panamax size vessels.

These vehicles pull trailers, which in turn transport the containers.

---

# Case Study: Container Terminals

The Mainframe computer will then determine where the container should be placed in the yard according to the heuristics rules that they defined.

- Then the Internal tractor will carry the container to the particular place
- Container will be unloaded by Rubber-tyred gantry crane (Rubber crane) or Rail-mounted gantry crane (Rail crane).

- The RTGCs run on rubber tyre wheels. The speed and the operating efficiency are relatively lower than the RMGCs because they are manually operated. However, RTGCs are more flexible to use because they can move from block to block.
- The container will then be stacked.

The RMGCs are highly automated with stacking capability by adopting the laser guidance technology. They move automatically over the rail with high speed and thus achieve better operating efficiency.


When this container is about to leave the Terminal:

- An External tractor will enter the Terminal.
- Passing the gates and wait in the yard for further instructions.

---
# Case Study: Container Terminals

- When the container is ready for pick-up, then the driver will be acknowledged by a mobile message sent by the Terminal.
- The voicemail is in three different languages, such as Chinese, English, and Mandarin.
- This service called “Mobile Container Movement Slip” (CMS).
- HIT teams up with Orange (mobile phone service provider) to offer the system.


# Advantages

- Reduces the time in acknowledging the driver about location.
- Drivers do not need to go to collect the notification from the HIT’s Despatch Office.
- Shorten the processing time of the whole container pickup process.
- So that, the number of tractors inside the yard reduced.


# Comparing with traditional approach:

- Drivers have to park their tractors in the yard.
- Then go to the HIT’s Dispatch Office to see when and where they should go inside the yard to pickup the container.

---
# Case Study: Container Terminals

# Traditional approach: (Time Comparison)

Drivers need to go to the Dispatch Office

|Lead time:|From tractor to Office – 10 min.|
|---|---|
| |Waiting for document – 10 min.|
| |Back to tractor – 10 min.|
|Total:|30 min.|

Assuming: 500 parking places

Theoretically: Max. number of tractors can be handled = 1,000 tractors (per hour) (60 min/30 min*500 tractor)


# New approach: (Time Comparison)

Drivers just wait in tractor for message

|Lead time:|Time to listen the message: 2 min.|
|---|---|
|Assuming:|500 parking places|
|Theoretically:|Max. number of tractors can be handled = 15,000 tractors (per hour). (60 min/2 min*500 tractor)|

- Mathematically, more tractors can be handled with the same parking capacity.


# Other Advantages of using Mobile technologies:

- Especially when there is typhoons, the tractor drivers can also receive some special information about the operational arrangement before they arrive the Terminal.


# ISE 328

# Technology and Applications of Electronic Business Systems

Instructor: Dr. YM Tang

Room: FJ 410

Contact: mfymtang@polyu.edu.hk

# About this Course

1. To learn what is e-business.
2. To introduce different kind of e-business technologies.
3. How to analyze business process.
4. How to apply e-business for improvement.

# Syllabus

1. Concept of e-Business.
2. Concept of e-Commerce.
3. Strategic of Implementing e-Business.
4. Various e-Business Technologies.
5. Concept of m-Commerce.
6. Concept of RFID.
7. Supply Chain Network.
8. Work Flow Analysis.

---
# LEARNING TO LEARN

‘Learning to learn’ is the ability to pursue and persist in learning, to organise one's own learning, including through effective management of time and information, both individually and in groups.

- This competence includes awareness of one's learning process and needs, identifying available opportunities, and the ability to overcome obstacles in order to learn successfully.
- This competence means gaining, processing and assimilating new knowledge and skills as well as seeking and making use of guidance.
- Learning to learn engages learners to build on prior learning and life experiences in order to use and apply knowledge and skills in a variety of contexts: at home, at work, in education and training. Motivation and confidence are crucial to an individual's competence.


# Approaches for learning to learn

1. Diffused and Focused Mode
2. Chunking
3. Over-Learning
4. Recalling
5. Bite-Sized Testing
6. Interleaving
7. Know thyself

---
# 1. Diffused and Focused Mode

- Focused mode: learners concentrate on the material
- Diffused mode: a neural resting state in which consolidation occurs — connections between bits of information, and unexpected insights, can occur.

# Pomodoro Technique

- An effective learning session is to take regular breaks by applying the Pomodoro technique. In this technique, we work for 25 minutes, then take a break for 5 minutes.
- The lengths of work and break time can be adjusted depending upon what works best for the learner. But, the most important aspect is to take a regular break.
---

# 2. Chunking

- What we want to learn should be broken into solid chunks of smaller concepts
- The main objective is to learn in mental chunks and all the mental chunks serve as notable puzzle pieces.

# Chunking Technique

For instance, to master a Social Sciences concept, we must also know how to break the concept into mental chunks and how does this concept fit into the larger picture.

- Firstly, survey and priming, which involves scanning the syllabus or book to get an idea of the larger picture.
- Then observe an example.
- Do it yourself and repeat the process in different contexts.
---
# 3. Over-Learning

- We must not spend extra time learning the same material in one sitting.
- Spreading out the learning in different modes and many sessions. It is better to learn a new concept for 30 to 60 minutes each day and gradually increase the depth of learning and skill levels.
- This spaced repetition of concepts will not only lead to successful learning but would also shift the learning to our long-term memory. 6
---
# 4. Recalling

- Spending a few minutes to recall or summarise the topic we are trying to learn.
- It is an effective way to transfer something from short-term learning into long-term memory.
- Also, deliberate practice of recalling concepts in the different physical surroundings can improve learning outcomes and help us understand the concept independent of any physical cues our mind may have.


---
# 5. Bite-Sized Testing

# Illusions

One common obstacle: illusions of Competence

As the material becomes familiar, we gain fluency. Sometimes we feel as if we have “understood” a concept, but we don’t. For instance:

- We may look at an answer and feel that we already know how to come to that solution.
- Underlining or highlighting the most important parts may also result in an illusion of learning. Instead, it is more beneficial to write brief notes summarising the key concepts.

Overcome the illusions of Competence by Bite-Sized Testing:

- Using Bite-Sized Testing as mental tools to assess ourselves.
- Mini-tests are amongst the most useful learning mechanisms that can be accomplished through recalling any concept. Even if we fail to pass this bite-sized testing, we must correct all the mistakes and solidify the learning.
---
# 6. Interleaving

After gaining basic knowledge of the concepts, interleaving can help in mastering the concepts.

- Do not keep working on the same kind of problems for too long
- By practising problems using different practical techniques, we may solidify our knowledge of the concepts and we may learn how to apply these in different situations.
- Knowing how to use a particular concept is an active process, which is as important as knowing when to use it in a learning experience.
---
# 7. Know thyself

- People learn in different ways.
- Those who have “racecar brains” snap up information;
- Those with “hiker brains” take longer to assimilate information but, like a hiker, perceive more details along the way.
- Recognizing the advantages and disadvantages is the first step in learning how to approach unfamiliar material.


# Objectives

This subject will provide students with

1. the opportunity to understand and evaluate the basic design and architecture of electronic business systems;
2. awareness of the latest electronic business system applications in the manufacturing and service industry;
3. opportunity to evaluate the contemporary application of electronic business systems;
4. concepts and applications related to business intelligence for electronic businesses.

# Intended Learning Outcomes

Upon completion of the subject, students will be able to

1. apply the design techniques to the development of architecture of electronic business systems;
2. identify, examine, and evaluate the application of electronic business systems in the manufacturing and service industry;
3. analyze and evaluate the contemporary application of electronic business systems in the context of the manufacturing and service industry;
4. select an appropriate type of electronic business system and apply it to the relevant work context of the manufacturing and service industry;
5. apply the business intelligence software and techniques to enhance electronic businesses.

# Subject Synopsis/Indicative Syllabus

The syllabus consists of the following topics:

1. Design and Architecture of Electronic Business Systems

System development and analysis; Web-based technology, mobile technology, database technology, network and web security; Data visualization and analysis of business intelligence in the support of electronic business.

2. Application of Electronic Business Systems in the Manufacturing and Service Sector

Applications in workflow management, production planning and inventory control, electronic procurement and trading, and others.

# Teaching/Learning Methodology

A combination of lectures, case studies, and projects with the support of laboratory work is used to deliver the various topics in this subject. Students carry out the practical work in the Microsoft Enterprise Systems Center. Some topics are covered in a case-based format to enhance learning experience, whereas others are covered through directed study to cultivate self-learning. Case studies are used to demonstrate how the various techniques are interrelated and how they are deployed in an actual environment.


Assignments are designed to assess students’ knowledge in identifying and testing the contemporary application of electronic business systems in real situations, and the understanding of the business intelligence techniques.

Projects are designed using some case studies to assess students’ understanding and presentation skills of different concepts, including how to identify, select, and apply e-business technology, and to develop and evaluate an e-business system.

Laboratory exercise is designed to explore a business intelligence software in the context of electronic business, and assess students’ knowledge in data visualization and analysis.

Examinations are designed to test students’ understanding of the topics and whether they can present the concepts clearly.
---

# Laboratory (Session 1) – Business Intelligence (Qlik)

# ISE328 – Technology and Applications of Electronic Business Systems

Dr Paul Y.P. TSANG

Email: yungpo.tsang@polyu.edu.hk
---
# Agenda of Our Laboratory

- Registration on Qlik Sense
- Lecturing on the Background of Business Intelligence
- Practice with Qlik Sense Together
---
# Account Registration

- Register our own account on Qlik Sense at https://www.qlik.com/us/products/qlik-sense
- Remember and save the login configurations for coming laboratory sessions

---
# Business Intelligence (BI)

• Business intelligence (BI): the procedural and technical infrastructure that collects, stores, and analyzes the data produced by a company’s activities (Investopedia, 2022).

# Aim:

- Easy-to-digest reports
- Performance measures
- Business trends to support management decisions.
---

# The Use of Data Analytics to Power BI

# Descriptive analytics (what happened?)

- Data aggregation, summary statistics, KPI

# Predictive analytics (What might/would happen?)

- Econometrics, statistics/data mining, qualitative analytics

# Prescriptive analytics (What should we do?)

- Optimization, data modelling
---

# How the BI Process Works

|STEP 1|STEP 2|STEP 3|STEP 4|STEP 5|
|---|---|---|---|---|
|Data from   systems is integrated and loaded into a data warehouse or other analytics repository.|Data sets are organized into analytics data models to prepare them for analysis.|BI analysts, other analytics professionals and business users run analytical queries against the data.|The query results are built into data visualizations, dashboards, reports and online portals.|Business executives and workers use the information for decision-making and strategic planning.|
---

# Business Intelligence (BI) Tool

- Qlik Sense: A data visualization and discovery product that allows you to create flexible, interactive visualizations that lead to meaningful decisions.
- Instead of deploying and managing huge business applications, you can create your own Qlik Sense apps that you can reuse, modify and share with others.
---


Laboratory (Session 2) – Business Intelligence (Qlik)

# ISE328 – Technology and Applications of Electronic Business Systems

Dr Paul Y.P. TSANG

Email: yungpo.tsang@polyu.edu.hk
---
# Background of the Exercise

• Imagine that you are going to launch your own retail business in Hong Kong, but you have no idea about the current situation of the retail market. Thus, you are going to analyse the data published on the public sector information portal (DATA.GOV.HK) for getting some insights and business directions.

• The collected data are managed on Qlik Sense, and you have to build your own dashboard for effective data visualization. Subsequently, you can have a clear picture on the current retail market in Hong Kong, and select the suitable type of retail business.
---

# Digital Policy Office

# Data.gov.hk

A Public Sector Information Portal to consolidate 19 categories of data (developed and supported by Digital Policy Office)

- City Dashboard (Traffic & Transport): https://data.gov.hk/en/city-dashboard
- Applications by using Data.gov.hk: https://data.gov.hk/en/application
---


# Introduction & Radio Frequency Identification (RFID) Technologies
---
# About this lecture

- Development of Internet of Things (IoT)
- Obtain fundamental Components and Development of RFID System
- Identify Standard and Cases of using RFID nowadays
- Recognize Characteristics and Physical Property of RFID
---

# Internet of Things (IoT)

# Industry 4.0

It encompasses a whole series of innovative processes and developments that are combining new technologies with industry standards in the manufacturing sector in order to serve increasingly fast-moving markets.

|First Industrial Revolution|Second Industrial Revolution|Third Industrial Revolution|Fourth Industrial Revolution|Degree of complexity|
|---|---|---|---|---|
|through the introduction of mechanical production facilities with the help of water and steam power|through the introduction of a division of labor and mass production with the help of electrical energy|through the use of electronic and MT systems that further automate production|through the use of cyber-physical systems| |
---

# Internet of Things (IoT)

# Definitions

- The term "Internet of Things" has come to describe a number of technologies and research disciplines that enable the Internet to reach out into the real world of physical objects (IoT 2008)
- Things having identities and virtual personalities operating in smart spaces using intelligent interfaces to connect and communicate within social, environmental, and user contexts (IoT in 2020)

Internet of Things (IoT) is the general term for the technology behind Industry 4.0.

Radio Frequency Identification (RFID) is one kind of enabling technology.
---

# IoT Applications

- Smart Health

- Industrial Automation

- Smart Home

- Smart City

---

# RFID System - Fundamental Components

# RFID History and Development

# World War II

|1939|1980|1990|2000|Future|
|---|---|---|---|---|
|Scientific and Battlefield Applications|Public Operated Proprietary Applications|Private Applications|Public Open-end Applications|Applications in Different Industries with United Standard|
|E.g.: Identify friendly parties in battlefield|E.g.: Autotoll System, Animal Tagging, Octopus System (Public Transport Only)|E.g.: Door Entry System|E.g.: Octopus System (Other Use), STRIDE (HK Jockey Club)|E.g.: EPCglobal Applications in Global Supply Chain Management, Chipless Tag|
---

# Introduction

- RFID is a kind of technology that use radio waves to automatically identify individual items without a direct line-of-sight automatically.
- Individual item is stored in term of a serial number as identifier in an RFID tag.
- It aims to reduce data entry errors, save manpower, and increase efficiency.
- Essential Components:
- Reader /Writer
- Antenna
- Tag
---

# Working Principle

- Reader Antenna emits radio signals to activate the tag and R/W data to it
- Tag Antenna and Reader Antenna are the conduits between the Tag and the Reader / Programmer
- Antennas allow Reader / Programmer R/W towards the Tag

# Process: 
1. "Smart" Labels are placed on pallets, cartons or individual items.
2. Radio waves transfer data between a reader and a movable item. 
3. An antenna captures the item’s ID number. 
4. A reader converts the radio waves into digital information. 
5. A host computer provides control over and access to logistical data.
---

# Working Principle (Video)

# RFID-Technology

# Chip for data
- Barcode number
- Product code
- Manufacturer
---

# Comparison between Barcode and RFID

|Feature|Barcode|RFID|
|---|---|---|
|Reading Method|Requires line-of-sight|No line-of sight required|
|Speed|Simple label per scan|Multiple tags in a single pass|
|Cost|Less than US$0.01 per label|Around US$0.25 to $0.5 per tag|
|Storage of Information|1D barcode: 20 chars 2D barcode: 2000 chars|Several thousand chars / Several kilobytes|
|Update Information|Replace another new barcode label|Wireless update the information in the tag|
|Durability|Easy to be damaged Not subject to many variables|More durable than barcode Limited to proximity of metals and liquids, and environmental conditions like snow and humidity|
|Implementation Limitation|Being physically visible|Limited to proximity of metals and liquids, and environmental conditions like snow and humidity|

---

# Using RFID in the Supply Chain

- RFID tags labels embedded with silicon chips.
- Stock items of all sizes, such as products, boxes, and pallets can be attached with RFID tags.
- As they travel through the supply chain network, they can easily be tracked throughout the wireless network environment of the RFID system.
- Any distribution centers and retail stores around the world can act as a check-point to locate the item and synchronize the information to the global central database.

---

# Supply Chain Visibility

RFID enables automatic ID of inventory out of line of sight

- at Dock doors
- Rack and Shelving
- in transit
---

# RFID Readers

An RFID reader is a device that can read from and write data to compatible RFID tags.

A reader has the following main components:

- Transmitter
- Receiver
- Microprocessor
- Memory
- Input/output channels for external sensors, actuators, and annunciators
- Controller
- Communication interface
- Power

---
# RFID Antennas

- A reader communicates to a tag through the antenna, a separate device that is physically attached to a reader, at one of its antenna ports, by means of a cable.
- A single reader can support up to four antennas (that is, have four physical antenna ports).
- An antenna broadcasts the reader transmitter’s RF signal into its surroundings and receives tag responses on the reader’s behalf. Therefore, proper positioning of the antennas, not the readers, is essential for good read accuracy.
---
# RFID Readers and Antennas
- Scanner
- Mobile reader
- Reader-embedded glove

---

# RFID Tags

- Inlet is a tag contains IC and antenna
- IC (integrated circuit) provides the memory and stores data
- Antenna harvests power & communicates with the reader
- Inlay is a inlet tag with adhesive layer and acts as label for application

---
# RFID Tag Read and Write

- Additional steps, including initial verification, data erasing, writing new data, and final verification, are required for write operation comparing with read only.
- In addition, the data is written on the tag in blocks in multiple steps.

|Read|Write|
|---|---|
|Requires less energy|Requires more energy|
|Simple step for read operation|Multiple steps for write operation|
|Multiple tags can be read at the same time|Only one tag can be written each time|
|Read range is longer|Write range is shorter|
---

# Types of RFID Tag

# Passive Tag

- Powered by electromagnetic waves energy from reader (no internal battery)
- Smaller, lighter, less expensive
- Almost unlimited life
- Requires higher power from reader

# Active Tag (battery-assisted and true active)

- On-board battery power  
- Greater range but higher cost
- Requires less power from reader
- Finite Life
- Periodically broadcast signals

# Semi-Active Tag (also called a “Semi-Passive Tag”)

- A “hybrid” tag that uses both beam and battery power.
- The battery power enables the tag to perform functions such as monitoring time and taking periodic temperature readings when it is not in a reader’s RF field.
- Battery power also greatly enhances the tag’s read/write range.


| |Passive|Active|Semi-Passive|
|---|---|---|---|
|Battery|Yes|No|Mainly For Communication|
|Distance|3 - 5m|~ 100m|< 50m|
---

# Cost Structure of RFID System

|Hardware subcomponent|Cost in US Dollars|
|---|---|
|Active tag (limited functionality)|$1.50 – $10|
|Passive tag|$0.1 - $0.2*|
|EPCGlobal™-compliant fixed reader|$2,000.00|
|Antenna|$200.00|

• Software costs are highly variable

• Licenses for middleware solutions $20K – 200K

• Implementation costs high because it still has emerging technology problems

• Change management costs can be substantial

• Training, installation, re-engineering processes

*Recent cost of RFID tag drop to US 10 cents by vendors who want to gain market share even if it is below manufacturing costs (for large volume > 100K pcs)
---

# Cost and Performance Comparison of Various RF Selection

|Frequency|Reader Cost|Antenna Cost|Tag Cost|Read Range|Effect of Interference and Reflection|
|---|---|---|---|---|---|
|Low Frequency (125 KHz)|$US50 - $US300|$US75 - $US500|US$5|<0.5m|Low|
|High Frequency (13.56 MHz)|$US50 - $US300|$US50 - $US5,000|US$2|<1m|Fair|
|Ultra High Frequency (915 MHz)|US$200 - US$2,000|US$5,000|US$0.10|~3m|High|

Almost 90% of RFID applications are HF and UHF.
---

# Framework of RFID System

- Reader antenna

- Sensor (optional)

- Tag

- Reader

- Actuator / Annunciator (optional)

- Controller

- Host and software system

- Communication infrastructure

---

# RFID Standard / Protocol

|Organization|ISO 18000|EPCglobal|
|---|---|---|
|Purpose|Air-interface standard. Compactable to any RFID license-free spectrum application|Data labeling standard on supply chain management application|
|Application|Mainly on HF and UHF|Mainly on HF and UHF|
|Characteristic|High adoptability and compatibility, No Standard Data, High cost of tags, Larger memory of tags|Applied by different vendors such as Wal-Mart, Relatively low cost of tags (comparing with ISO tags)|

---

# Electronic Product Code™ (EPC™)

- The Electronic Product Code™ (EPC™) is a numbering scheme designed to uniquely identify all objects.

- An EPC contains
 - a manufacturer identifier
 - a product identifier
 - an item serial number (extra information)

- It was created to enable the electronic connection between physical objects and computer networks – to serve as an efficient information reference.

- It can be applied with RFID or current Bar-code system.

---

# Example of EPC

# ELECTRONIC PRODUCT CODE TYPE I
01.0000A89.0016F.000169DC0

|01|0000A89|0016F|000169DC0|
|---|---|---|---|
|Header|EPC Manager|Object Class|Serial Number|
|8 bits|28 bits|24 bits|36 bits|
|Purpose Field: Trade Product|Corporation unit: Apple Inc.|Object Class: iPod, iPhone, iPad|Serial Number: Unique unit code|

268 million companies can each categorize 16 million different products and each product category may contain over 687 billion individual items !!
*Barcode could only perform functions to object class, but not serial number.
---

# RFID System

# Case Studies

# 1. Animal Tagging System

- RF tags are injected into dogs’ body in RSPCA council
- The Agriculture, Fisheries and Conservation Department uses tag ID to retrieve dog information from adopted animal database
- Label individual wild animal to track and record their living style
- Label individual livestock for livestock management purpose

# Example: 
Animal tag
Read RF tag
---

# (2) HK Autotoll System

# Autotoll is widely adopted in HK Harbor Tunnels

- Utilization of the 4 autotoll lanes in 2002 was
37,111 vehicles per day
- Representing 50.6% of the daily throughput

# Mechanism

- Stick active RF tag on vehicle wind screen
- Active tag emits signals that carries the car ID and time data
- RF reader receives signals and update the data in database of transaction server
- Bills are issued to tag owner monthly according to those transactions data


# (3) Wal-Mart

- Wal-Mart is going to push its suppliers to start using RFID to track inventory by 2005
- Wal-Mart wants to begin tracking items using a 96-bit EPC™ with a Global Trade Identification Number (GTIN)
- Wal-Mart is already tracking pallets and cases from suppliers coming into distribution center


# (4) HK International Airport

- Tune $50 million Auto-ID project to improve baggage handling and security
- Expect RFID system would reduce a failure rate to 5%, which would greatly improve customer satisfaction and efficiency
- If 1% of the bags went missing, rectifying the problem would cost $17 million a year


# (5) HK Jockey Club - STRIDE

- STRIDE - Sectional Timing Racing Information Dynamic Entertainment

- Transponder tags are placed in each jockey's skull cap, and 31 radio frequency (RF) transceivers are placed around the racecourse.
- The transceivers send RF signals about 12 times per second for Location process server [LPS] to calculate the tag's location.
- Max. 30 targets can be tracked with accuracy range: ±10cm.

---

# Practical Uses of RFID in Public Utilities

- Electricity, Natural Gas and Water Companies
- Smart Grid and Meter
- Telecommunication Companies
- Mobile Payment and Loyalty Program
- Transportation Companies
- Ticketing
---

# Electricity, Natural Gas and Water Companies

# Smart Meter

- Contactless RF reader and microcontroller technology
- Collect accurate information on the amount of electricity and gas being used
- New, fast and convenient way payment services for customer
- Reducing the risk of non-payment

# Smart Grid

- Total interactive system
- Exchange the information in real time

---

# Telecommunication Companies

# Mobile Payment and Loyalty Program

# Dallas, Texas-based Device Fidelity with two credit card companies
- Passive tag and RFID reader (inserted into mobile phone)
- Linked to bank accounts for mobile payment

# Dairy Queen and Vivotech
- New loyalty and rewards program
- Receive promotions and coupons

# 7-Eleven and MasterCard
- New touch-free payment system (for Nokia 3220, 6212 cell phone)
- RFID-capable MasterCard credit card
- Store card information

---

# Transportation – Ticketing

- Shenzhen Metro, Mainland China

- Shanghai Metro, Mainland China

- The Sentosa Express, Singapore

- Hong Kong International Airport, Hong Kong

---

# RFID System

# Physical Property

# Antenna Footprint

- The footprints of the reader’s antennas determine the read zone (also called the read window) of a reader.
- In general, an antenna footprint, also called an antenna pattern, is a three-dimensional region shaped somewhat like an ellipsoid or a balloon projecting out of the front of the antenna.
- In this region, the antenna’s energy is most effective; therefore, a reader can read a tag placed inside this region with the least difficulty.

# Antenna Polarization

- As discussed previously, an antenna emits electromagnetic waves into its surroundings. The direction of oscillation of these electromagnetic waves is called the polarization of the antenna.

- The main antenna types in UHF, based on polarization, are:

 - Linear polarized
 - Circular polarized

Linear pattern
Circular pattern
---

# Linear vs Circular

- A linear polarized antenna has a narrower radiation beam with a longer read range compared to a circular polarized antenna.
- However, a linear polarized antenna is sensitive to tag orientation with respect to its p
olarization direction.
- A circular polarized antenna has a wider radiation beam and hence reads tags in a wider area compared to a linear polarized antenna.
- Because of the nature of polarization, a circular polarized antenna is largely unaffected by tag orientation.

---

# Tag Orientation (Linear)

# Plane on Which a Tag Can Be Read Properly (Tag Orientation Restricted)

- Legend:
 True: Proper tag alignment and placement resulting in good readability
 ?: Proper tag alignment but indirect placement that may not result in good readability: This can be affected if the tagged object is made (or contains items made of) AF-opaque RF-absorbent materials
 False: Either improper tag alignment or indirect placement = both leading to poor readability,
---

# RF Properties of Different Materials

- Radio waves can be affected by the material through which they propagate.
- A material is called RF-lucent or RF-friendly for a certain frequency if it lets radio waves at this frequency pass through it without any substantial loss of energy.
- A material is called RF-opaque if it blocks, reflects, and scatters RF waves.
- A material can allow the radio waves to propagate through it but with substantial loss of energy. These types of materials are referred to as RF-absorbent.
- The RF-absorbent or RF-opaque property of a material is relative, because it depends on the frequency. That is, a material that is RF-opaque at a certain frequency could be RF-lucent at a different frequency.
---

# RF Properties of Different Materials (Cont’)

|Material|LF|HF|UHF|Microwave|
|---|---|---|---|---|
|Clothing|RF-lucent|RF-lucent|RF-lucent|RF-lucent|
|Dry wood|RF-lucent|RF-lucent|RF-lucent|RF-absorbent|
|Graphite|RF-lucent|RF-lucent|RF-opaque|RF-opaque|
|Liquids (some types)|RF-lucent|RF-lucent|RF-absorbent|RF-absorbent|
|Metals|RF-lucent|RF-lucent|RF-opaque|RF-opaque|
|Motor oil|RF-lucent|RF-lucent|RF-lucent|RF-lucent|
|Paper products|RF-lucent|RF-lucent|RF-lucent|RF-lucent|
|Plastics (some types)|RF-lucent|RF-lucent|RF-lucent|RF-lucent|
|Shampoo|RF-lucent|RF-lucent|RF-absorbent|RF-absorbent|
|Water|RF-lucent|RF-lucent|RF-absorbent|RF-absorbent|
|Wet wood|RF-lucent|RF-lucent|RF-absorbent|RF-absorbent|

