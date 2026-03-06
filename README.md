# cs4412-project
Project Title: "United States Federal Spending in Georgia"

Description: This project aims to explore the total amount of transactions made by the federal government to the state of Georgia in 2025. 
The goal is to explore what kind of businesses the federal government funds the most and what specific businesses recieve the majority of US tax dollars.

Dataset Source: https://www.usaspending.gov/search?hash=c2c3c2289128b5b40f0f64f62e847828

Name: Seth Brice

UPDATED PROGRESS FROM M2

M2 aims to answer the discovery question: "What combinations of awarding agencies, recipients, and funding types frequently co-occur in different regions of Georgia?"

For this milestone, the raw data was extracted from the linked website as a csv file. This data was combined into one csv file (see "All Awards Final" in data folder. You will have to download it from this repository) containing every transaction. The file was then transformed into a 2D matrix, where each row represented a collection of the relevant characteristics of each transaction. This was put through the built in methods from the "mlxtend" library in Python, which then generated a new set of data listing the most frequent sets of data with supporting values at least 0.01 (see "AprioriSets" in the Output Files folder). Another csv file was created to display association rules with at least a confidence of 0.8 (see "AprioriRules" in the Output Files folder). Both of these files were examined to discover patterns in the transactions between different sized counties.
