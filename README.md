# CustomerSegmentation_UsingKMeansClustering
Customer Segmentation using K-Means Clustering

This project performs customer segmentation on a marketing campaign dataset using the K-Means unsupervised learning algorithm. The goal is to group customers into distinct clusters based on their purchasing behavior and demographics to enable more effective and targeted marketing strategies.

Objective

The primary objective is to identify distinct customer segments within the dataset. By understanding the unique characteristics of each segment, a business can:
1) Tailor marketing messages to specific groups.
2) Develop new products that cater to the needs of different segments.
3) Optimize pricing and promotional strategies.
4) Improve customer retention by understanding group-specific behaviors.

Dataset

The project uses the marketing_campaign.csv dataset, which contains information about customers, including:
1) Demographics: Year_Birth, Education, Marital_Status, Income
2) Household Composition: Kidhome, Teenhome
3) Purchasing Behavior: Spending on various product categories (MntWines, MntFruits, etc.) and purchasing channels (NumWebPurchases, NumCatalogPurchases, etc.)
4) Campaign Responses: Acceptance of previous marketing campaigns.

Methodology

The customer segmentation was achieved through the following steps:
1) Data Preprocessing:
- Handled missing Income values by imputing the mean.
- Encoded categorical features (Education, Marital_Status) using one-hot encoding.
-Scaled all numerical features using StandardScaler to ensure all variables contribute equally to the model.

2) Optimal Cluster Selection:
-Used the Elbow Method to determine the optimal number of clusters (k). The "elbow" point on the inertia plot suggests the most appropriate value for k.

3) K-Means Clustering:
- Applied the K-Means algorithm with the optimal k=4 to group the customers into four distinct segments.

4) Visualization:
- Utilized Principal Component Analysis (PCA) to reduce the dimensionality of the data to two components, allowing for the visualization of the clusters in a 2D scatter plot.

5) Results & Customer Segments
- The analysis revealed four distinct customer segments with unique characteristics:

6) Segment Profiles:
- Cluster 0: The Cautious Spenders
Income: Moderate income.
Spending: Low to moderate spending. They are bargain hunters who respond well to deals.
Campaign Response: Low engagement with marketing campaigns.

- Cluster 1: The Affluent Wine & Meat Lovers
Income: High income.
Spending: High spending, especially on wine and meat. They make frequent catalog and in-store purchases.
Campaign Response: Good engagement with campaigns.

- Cluster 2: The Thrifty Families
Income: Lowest income group.
Spending: Very low spending across all categories.
Household: Tend to have more children at home.
Campaign Response: Very low engagement.

- Cluster 3: The High-Responding Elite
Income: The highest income earners.
Spending: The highest spenders across all categories.
Campaign Response: Extremely high response rate to all marketing campaigns, making them a prime target for new offers.

