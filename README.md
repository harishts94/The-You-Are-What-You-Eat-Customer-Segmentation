# The "You Are What You Eat" Customer Segmentation

### Project Overview

#### Context
The Senior Management team from our client, a supermarket chain, are disagreeing about how customers are shopping, and how lifestyle choices may affect which food areas customers are shopping into, or more interestingly, not shopping into.

They have asked us to use data, and Machine Learning to help segment up their customers based upon their engagement with each of the major food categories - aiding business understanding of the customer base, and to enhance the relevancy of targeted messaging & customer communications.

#### Actions
We firstly needed to compile the necessary data from sevaral tables in the database, namely the transactions table and the product_areas table. We joined together the relevant information using Pandas, and then aggregated the transactional data across product areas, from the most recent six month to a customer level. The final data for clustering is, for each customer, the percentage of sales allocated to each product area.

As a starting point, we test & apply k-means clustering for this task. We need to apply some data pre-processing, most importantly feature scaling to ensure all variables exist on the same scale - a very important consideration for distance based algorithms such as k-means.

As k-means is an unsupervised learning approach, in other words there are no labels - we use a process known as Within Cluster Sum of Squares (WCSS) to understand what a “good” number of clusters or segments is.

Based upon this, we apply the k-means algorithm onto the product area data, append the clusters to our customer base, and then profile the resulting customer segments to understand what the differentiating factors were!
