McDonald's Customer Segmentation and Profiling

Overview

This project performs customer segmentation using clustering techniques such as K-Means and Gaussian Mixture Models (GMM) on the McDonald's customer perception data. The segmentation is followed by an analysis of customer profiles using PCA (Principal Component Analysis) and a decision tree model for understanding the factors affecting customer satisfaction. Finally, the project provides insights for selecting target segments and customizing the marketing mix for those segments.

Project Steps

Step 1: Load Data
- The dataset is loaded from a CSV file into a pandas DataFrame. The dataset contains customer perceptions of McDonald's, including responses to multiple questions about their experience and satisfaction.

Step 2: Explore Data
- We explore the dataset by printing the columns, shape, and first few rows to understand the data structure.

Step 3: Convert YES/NO to Binary
- The first 11 columns of the dataset, which contain "Yes" or "No" responses, are converted to binary values (1 for Yes, 0 for No). This is used for segmentation.

Step 4: PCA (Principal Component Analysis)
- PCA is applied to reduce the dimensionality of the segmentation variables and to visualize customer perceptions in two dimensions. This helps in understanding how the different customer segments are distributed.

Step 5: K-Means Clustering
- We use K-Means clustering to segment customers into 4 distinct groups based on their responses. The results are visualized using a scatter plot of the first two principal components.

Step 5.2: Gaussian Mixture Model (GMM) Clustering
- GMM is applied as an alternative clustering method, and a cross-tabulation of the K-Means and GMM clusters is performed to compare the results.

Step 6: Profiling Segments with Decision Tree Regressor
- A decision tree model is built to profile the customer segments based on their satisfaction level (the "Like" column). The "Like" column is converted to numeric values for this analysis.
- The decision tree helps in understanding the key factors that drive customer satisfaction.

Step 7: Describing Segments
- A descriptive analysis of the customer segments is performed. We calculate the mean of the numeric columns (e.g., Age, Like, VisitFrequency) for each segment to profile them based on different characteristics.

Step 8: Selecting the Target Segment(s)
- The target segment is selected based on the highest satisfaction scores (highest "Like" values) among the clusters. This helps in identifying which group of customers should be prioritized for marketing efforts.

Step 9: Customizing the Marketing Mix
- The marketing mix (Product, Price, Place, and Promotion) is customized for the selected target segment, based on their preferences and profile.

Step 10: Evaluation and Monitoring
- Key Performance Indicators (KPIs) are defined to evaluate the success of the marketing efforts. These include tracking sales, satisfaction scores, and return on marketing investment (ROMI).

 Requirements

- Python 3.7+
- Required libraries:
  - `pandas`
  - `numpy`
  - `sklearn`
  - `matplotlib`

 Installation

To install the required dependencies, use the following command:

```
pip install pandas numpy scikit-learn matplotlib
```
Usage

1. Prepare the dataset: Place your McDonald's CSV dataset in the appropriate location and update the file path in the code (`data = pd.read_csv(r'C:\path\to\mcdonalds.csv')`).

2. Run the code: Execute the script in your Python environment. The script will:
   - Perform PCA for visualizing customer perceptions.
   - Perform clustering (K-Means and GMM) to segment customers.
   - Profile customer segments using a decision tree.
   - Provide insights for targeting and customizing marketing efforts.

3. Visualizations: The code will generate multiple plots:
   - PCA scatter plot of customer perceptions.
   - K-Means clustering result plot.
   - Decision tree for segment profiling.

4. Outputs:
   - Descriptive statistics of customer segments.
   - Cross-tabulation of K-Means and GMM clusters.
   - Custom marketing mix suggestions for the target segment.

 Example Outputs

- Cluster Visualization: PCA plots showing customer segmentation.
- Segment Description: Summary of each segment's demographic and satisfaction statistics.
- Target Segment: Identification of the customer group with the highest satisfaction for focused marketing.
- Marketing Mix: Custom recommendations for Product, Price, Place, and Promotion.

 Evaluation and Monitoring

The effectiveness of the segmentation and marketing strategies can be evaluated using:
- Sales tracking: Monitor changes in sales among the targeted customer segment.
- Customer satisfaction: Track changes in satisfaction scores (from the "Like" column) post-campaign.
- Return on Marketing Investment (ROMI): Measure the financial impact of the marketing campaign relative to its cost.
