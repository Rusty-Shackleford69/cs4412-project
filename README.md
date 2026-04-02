# cs4412-project
Project Title: "United States Federal Spending in Georgia"

Description: This project aims to explore the total amount of transactions made by the federal government to the state of Georgia in 2025. 
The goal is to explore what kind of businesses the federal government funds the most and what specific businesses recieve the majority of US tax dollars.

Dataset Source: https://www.usaspending.gov/search?hash=c2c3c2289128b5b40f0f64f62e847828

Name: Seth Brice

UPDATED PROGRESS FROM M2:

M2 aims to answer the discovery question: "What combinations of awarding agencies, recipients, and funding types frequently co-occur in different regions of Georgia?"

For this milestone, the raw data was extracted from the linked website as a csv file. This data was combined into one csv file (see "All Awards Final" in data folder. You will have to download it from this repository) containing every transaction. The file was then transformed into a 2D matrix, where each row represented a collection of the relevant characteristics of each transaction. This was put through the built in methods from the "mlxtend" library in Python, which then generated a new set of data listing the most frequent sets of data with supporting values at least 0.01 (see "AprioriSets" in the Output Files folder). Another csv file was created to display association rules with at least a confidence of 0.8 (see "AprioriRules" in the Output Files folder). Both of these files were examined to discover patterns in the transactions between different sized counties.

UPDATED PROGRESS M3:

M3 aims to run a deeper approach to the apriori method from M2 by using multiple sets of variables. Each run's results will be compared to each other to see how surprising the different results are.

The other goal is to answer the discovery question: "What natural groupings of recipients appear based on their total obligations and number of awards?" For this, k-means was implemented using the sklearn Python package. 

First, I ran three more runs of apriori using the same code from the precious milestone. The first run examined agency and business type relations based on county (see "AgencyBusinessTypeSets" in the Output folder). The second broke down each transaction's description into a set of words, then output a file of the most frequent set of words (see "FrequentWordsSets" in the Output folder). The third run examined agency and recipient relations (see "AgencyRecipientSets" in the Output folder). All of these results, along with the patterns from M2, were analyzed and compared to each other to determine what results were more surprising.

Next, the preprocessed data was put through the k-means method. A matrix of each recipient, their obligations, and award amounts was created, and clustered into five different clusters (see "KMeansClusters" in the Output folder). These clusters were each analyzed and examined to determine natural characteristics of the recipients in each cluster.
